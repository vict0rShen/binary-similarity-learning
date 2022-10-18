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

## 高水平文献

- Genius (*CCF-A；CCS2016*) [[paper]](https://dl.acm.org/doi/abs/10.1145/2976749.2978370) [[github]](https://github.com/qian-feng/Gencoding) [[note]](./notes/Genius.md)
  - FENG Q, ZHOU R, XU C, et al. Scalable Graph-based Bug Search for Firmware Images[C]//Proceedings of the 2016 ACM SIGSAC Conference on Computer and Communications Security. Vienna, Austria:Association for Computing Machinery,2016:480–491. 10.1145/2976749.2978370.

## 专有名词及其缩写

| 缩写 | 名词全称                      | 中文释义     |
| ---- | ----------------------------- | ------------ |
| ACFG | Attributed Control Flow Graph | 属性控制流图 |
| CFG  | Control Flow Graph            | 控制流图     |
| IR   | Intermediate Representation   | 中间表示     |
| LSH  | Locality Sensitive Hashing    | 局部敏感哈希 |

# to-do list

- [x] 阅读文献：Genius
- [ ] 阅读文献：GEMINI
- [ ] 阅读文献：ASM2VEC
- [ ] 阅读文献：discovre: Efficient cross-architecture identification of bugs in binary code
- [ ] 阅读文献：Cross-architecture bug search in binary executables

