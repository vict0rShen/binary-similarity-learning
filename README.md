# binary-similarity-learning

二进制代码相似度分析（Binary Code Similarity Analysis）学习笔记

`[paper]`：论文发布页；`[note]`：论文笔记 ；`[github]`：github源码

## 基本概念解析

已整理于[基本概念解析文档](./concept.md)，学习笔记中涉及相关概念位置均已设置超链接。

## 综述 (review)

- A Survey of Binary Code Similarity (*WOS-Q1; 中科院-1区；2021*) [[paper]](https://dl.acm.org/doi/abs/10.1145/3446371) [[note]](./notes/A_Survey_of_Binary_Code_Similarity.md)
  - HAQ I U, CABALLERO J. A Survey of Binary Code Similarity [J]. ACM Comput Surv, 2021, 54(3): Article 51. 
  - 领域内常用方法的分类与概述，适合入门
  - 仅包含2019年及以前的文献

## Binary Diffing

- Graph-based comparison of executable objects (*SSTIC2005*) [[paper]](http://195.154.171.95/SSTIC05/Analyse_differentielle_de_binaires/SSTIC05-article-Flake-Graph_based_comparison_of_Executable_Objects.pdf) [[note]](./notes/Graph-based_comparison_of_executable_objects.md)
  - DULLIEN T, ROLLES R. Graph-based comparison of executable objects (english version) [J]. Sstic, 2005, 5(1): 3.


## Binary Similarity

- BLEX *(CCF-A; USENIX2014)* [[paper]](https://www.usenix.org/conference/usenixsecurity14/technical-sessions/presentation/egele) [[note]](./notes/BLEX.md)
  - EGELE M, WOO M, CHAPMAN P, et al. Blanket execution: Dynamic similarity testing for program binaries and components[C]//23rd USENIX Security Symposium (USENIX Security 14).2014:303-317. 

## Binary Search

- TEDEM *(CCF-B; ACSAC2014)*  [[paper]](https://dl.acm.org/doi/abs/10.1145/2664243.2664269) [[note]](./notes/TEDEM.md)
  - PEWNY J, SCHUSTER F, BERNHARD L, et al. Leveraging semantic signatures for bug search in binary programs[C]//Proceedings of the 30th Annual Computer Security Applications Conference.2014:406-415. 

- Multi-MH (*CCF-A；S&P2015*) [[paper]](https://ieeexplore.ieee.org/abstract/document/7163056) [[note]](./notes/Multi-MH.md)
  - PEWNY J, GARMANY B, GAWLIK R, et al. Cross-Architecture Bug Search in Binary Executables[C]//2015 IEEE Symposium on Security and Privacy.2015:709-724. 10.1109/SP.2015.49.

- Genius (*CCF-A；CCS2016*) [[paper]](https://dl.acm.org/doi/abs/10.1145/2976749.2978370) [[github]](https://github.com/qian-feng/Gencoding) [[note]](./notes/Genius.md)
  - FENG Q, ZHOU R, XU C, et al. Scalable Graph-based Bug Search for Firmware Images[C]//Proceedings of the 2016 ACM SIGSAC Conference on Computer and Communications Security. Vienna, Austria:Association for Computing Machinery,2016:480–491. 10.1145/2976749.2978370.
- discovRE (*CCF-A；NDSS2016*)  [[paper]](https://www.ndss-symposium.org/wp-content/uploads/2017/09/discovre-efficient-cross-architecture-identification-bugs-binary-code.pdf) [[note]](./notes/discovRE.md)
  - ESCHWEILER S, YAKDAN K, GERHARDS-PADILLA E. discovRE: Efficient Cross-Architecture Identification of Bugs in Binary Code[C]//NDSS.2016
- Gemini (*CCF-A；CCS2017*) [[paper]](https://dl.acm.org/doi/abs/10.1145/3133956.3134018) [[github]](https://github.com/Yunlongs/Gemini) [[note]](./notes/Gemini.md)
  - XU X, LIU C, FENG Q, et al. Neural Network-based Graph Embedding for Cross-Platform Binary Code Similarity Detection[C]//Proceedings of the 2017 ACM SIGSAC Conference on Computer and Communications Security. Dallas, Texas, USA:Association for Computing Machinery,2017:363–376. 10.1145/3133956.3134018.


## Clone Detection

- Kam1n0 *(CCF-A; KDD2016)*  [[paper]](https://dl.acm.org/doi/abs/10.1145/2939672.2939719) [[github]](https://github.com/McGill-DMaS/Kam1n0-Community)
  - DING S H H, FUNG B C M, CHARLAND P. Kam1n0: MapReduce-based Assembly Clone Search for Reverse Engineering[C]//Proceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining.2016:461-470. 
  - 侧重于新哈希算法和MapReduce方案的设计

## Measurement Study

- a *(CCF-A; USENIX2022)* [[paper]](https://www.usenix.org/conference/usenixsecurity22/presentation/marcelli) [[github]](https://github.com/Cisco-Talos/binary_function_similarity) [[note]](./notes/How_Machine_Learning_is_Solving_the_BInary_Function_Similarity_Problem.md)
  - MARCELLI A, GRAZIANO M, UGARTE-PEDRERO X, et al. How machine learning is solving the binary function similarity problem[C]//31st USENIX Security Symposium (USENIX Security 22).2022:2099-2116. 
  - 构建开源数据集，将现有方法在同一基准下进行测试
  - 阅读相关论文时可作为分析用参考，精读对应部分


## 专有名词及其缩写

| 缩写 | 名词全称                            | 中文释义           |
| ---- | ----------------------------------- | ------------------ |
| ACFG | Attributed Control Flow Graph       | 属性控制流图       |
| ALSH | Adaptive Locality Sensitive Hashing | 自适应局部敏感哈希 |
| CDF  | Cumulative Distribution Function    | （累计）分布函数   |
| CFG  | Control Flow Graph                  | 控制流图           |
| GI   | Graph Isomorphism                   | 图同构             |
| IR   | Intermediate Representation         | 中间表示           |
| LSH  | Locality Sensitive Hashing          | 局部敏感哈希       |
| MCS  | Maximum Common Subgraph             | 最大公共子图       |
| MRR  | Mean Reciprocal Rank                | 平均倒数排名       |
| TED  | Tree Edit Distance                  | 树编辑距离         |

# to-do list

- [ ] 阅读文献：ASM2VEC
- [ ] 阅读文献：Tracelet-based code search in executables.
- [ ] 略读文献：Discriminative Embeddings of Latent Variable Models for Structured Data
- [x] 略读文献：Graph-based Comparison of Executable Objects.（bindiff）
- [ ] 略读文献：BinHunt
- [ ] 略读文献：Binary Function Clustering Using Semantic Hashes.
- [ ] 略读文献：Fast Location of Similar Code Fragments Using Semantic ’Juice’
- [ ] 略读文献：Discovering Potential Binary Code Re-use.
- [x] 基本概念：S-Expression
- [ ] 阅读文献：Rendezvous
- [ ] 阅读文献：BinGo: cross-architecture cross-OS binary search
- [ ] 阅读文献：[Neural Machine Translation Inspired Binary Code Similarity Comparison beyond Function Pairs](https://www.semanticscholar.org/paper/fe3470a9c37e88928fbd0d84ed578357b1f07a0d)
- [x] 阅读文献：How Machine Learning Is Solving the Binary Function Similarity Problem
- [ ] 阅读文献：Order Matters: Semantic-Aware Neural Networks for Binary Code Similarity Detection
- [ ] 阅读文献：Statistical similarity of binaries.
- [ ] 阅读：https://googleprojectzero.blogspot.com/2018/12/searching-statically-linked-vulnerable.html
- [ ] 阅读文献：Graph matching networks for learning the similarity of graph structured objects
- [ ] 阅读文献：Binary Similarity Detection Using Machine Learning.
- [ ] 阅读文献：Safe: Self-attentive function embeddings for binary similarity
- [ ] 阅读文献：Investigating Graph Embedding Neural Networks with Unsupervised Features Extraction for Binary Analysis. 
- [ ] 阅读文献：Codecmr: Cross-modal retrieval for function-level binary source code matching.
- [ ] 阅读文献：Trex: Learning execution semantics from micro-traces for binary similarity
- [x] 基本概念：MRR
- [ ] 略读文献：Structural Comparison of Executable Objects
- [x] 基本概念：幂集

