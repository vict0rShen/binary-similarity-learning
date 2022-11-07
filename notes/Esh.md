# Esh

| Target（目标）     | 已知某个二进制函数，在其他二进制文件中检索具有与之相似的函数 |
| :----------------- | :----------------------------------------------------------- |
| Input（输入）      | 待搜索二进制代码库；已知二进制函数                           |
| Process（处理）    | 1. 将二进制函数拆分为片段<br />2. 根据输入输出和中间变量判断两个代码片段是否相同<br />3. 基于代码片段的相似度综合判断二进制函数的相似度 |
| Output（输出）     | 与已知二进制函数相似的函数列表                               |
| Problem（问题）    | 解决的问题：<br />1. 算法建立在程序控制流图基本不变的前提上（对控制流图结构敏感），跨编译器分析效果不佳<br />2. 算法分析粒度较粗（函数级/程序级）相似性分析误报率高 |
| Condition（条件）  | 程序未被混淆                                                 |
| Difficulty（难点） | 1. 代码片段拆分<br />2. 不同代码片段间高效率的匹配分析       |
| Level（水平）      | PLDI2016                                                     |

## 算法原理

利用图像领域中子图匹配的思想，如果一段二进制代码能够用另一段二进制代码的片段构成，则认为两段代码相似

### 拆分为代码片段

将汇编代码转换为中间验证语言（IVL），对函数中的每一个变量做程序切片，获得代码片段

### 代码片段间比较

1. 假设两个代码片段的输入等价
2. 设置判断代码片段输出等价的断言
3. 使用程序验证器检查断言，计算等价的变量

#### 匹配程度计算

- 程序状态 $\sigma$ ：一个对 $(l,values)$ ，表示一组变量在程序第 $l$ 行的值为 $values$ 

- 程序记录 $\pi$ ：描述程序一次运行的一个程序状态序列 $\langle\sigma_0,\dots,\sigma_n\rangle$ ，程序所有可能的记录集合表示为 $[\![P]\!]$ 

- 变量关联 $\gamma$ ：如果两个程序状态之间存在变量存在相同的值，则可将变量关联

  - 例： $values_q=\{x\mapsto3,y\mapsto4\},values_t=\{a\mapsto4\}$，则变量关联为 $\{y\mapsto a\}$ 

- 程序状态/记录等价 $\equiv$ ：程序状态中的所有变脸都能匹配/程序记录中最后一个状态等价
- 程序片段等价：需满足两个条件：1）片段输入能实现关联；2）与输入相同的所有程序记录等价
- 程序状态间的VCP（variable containment proportion，VCP）：关联变量占全部变量的比例
  - $\displaystyle VCP(\sigma_q,\sigma_t)\triangleq\frac{|\gamma_{max}|}{|\sigma_q|}$
- 程序记录间的VCP：记录最后一个状态之间的VCP
- 程序片段间的VCP：所有匹配程序记录中关联的最大变量数占所有变量的比例
  - $\displaystyle VCP(s_q,s_t)\triangleq \frac{\max\{|\gamma|\big{|}\forall(\pi_q,\pi_t)\in(s_q,s_t):\pi_q\equiv\pi_t\}}{|Var(s_q)|}$
  - 注意：VCP非对称，即将两个参数交换位置结果可能不同


#### 实际实现过程

将代码转换为BoogieIVL中间语言，使用Boogie程序验证器检查断言

#### 匹配重要性计算

不同代码片段的重要程度不同（有些代码片段是通用代码，不能很好表征函数特征），代码片段匹配的重要性用局部置信度（local evidence score，LES）表示。

$$\displaystyle LES(s_q|t)=\log\frac{\max_{s_t\in t}Pr(s_q|s_t)}{Pr(s_q|H_0)}$$

论文使用sigmoid函数近似某一函数中代码片段出现的概率（sigmoid函数的中心设置至 $x=0.5$ ，$k$ 取10）

$$\displaystyle Pr(s_q|s_t)\triangleq g(VCP(s_q,s_t))=1/(1+e^{-k(VCP(s_q,s_t)-0.5)})$$

而 $Pr(s_q|H_0)$ 表示在随机函数中找到与被搜索代码片段匹配的代码片段的概率，设 $T$ 为待搜索二进制代码库：

$$\displaystyle Pr(s_q|H_0)=\frac{\sum_{s_t\in T}Pr(s_q|s_t)}{|T|}$$

### 代码片段相似度上升为函数相似度

根据LES计算全局置信度（global evidence score，GES）

$$\displaystyle GES(q|t)=\sum_{s_q\in q}LES(s_q|t)=\sum_{s_q\in q}\log\frac{\max_{s_t\in t}Pr(s_q|s_t)}{Pr(s_q|H_0)}$$

