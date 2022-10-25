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

- Multi-MH (*CCF-A；S&P2015*) [[paper]](https://ieeexplore.ieee.org/abstract/document/7163056) [[note]](./notes/Multi-MH.md)
  - PEWNY J, GARMANY B, GAWLIK R, et al. Cross-Architecture Bug Search in Binary Executables[C]//2015 IEEE Symposium on Security and Privacy.2015:709-724. 10.1109/SP.2015.49.

- Genius (*CCF-A；CCS2016*) [[paper]](https://dl.acm.org/doi/abs/10.1145/2976749.2978370) [[github]](https://github.com/qian-feng/Gencoding) [[note]](./notes/Genius.md)
  - FENG Q, ZHOU R, XU C, et al. Scalable Graph-based Bug Search for Firmware Images[C]//Proceedings of the 2016 ACM SIGSAC Conference on Computer and Communications Security. Vienna, Austria:Association for Computing Machinery,2016:480–491. 10.1145/2976749.2978370.
- discovRE (*CCF-A；NDSS2016*)  [[paper]](https://www.ndss-symposium.org/wp-content/uploads/2017/09/discovre-efficient-cross-architecture-identification-bugs-binary-code.pdf) [[note]](./notes/discovRE.md)
  - ESCHWEILER S, YAKDAN K, GERHARDS-PADILLA E. discovRE: Efficient Cross-Architecture Identification of Bugs in Binary Code[C]//NDSS.2016
- Gemini (*CCF-A；CCS2017*) [[paper]](https://dl.acm.org/doi/abs/10.1145/3133956.3134018) [[github]](https://github.com/Yunlongs/Gemini) [[note]](./notes/Gemini.md)
  - XU X, LIU C, FENG Q, et al. Neural Network-based Graph Embedding for Cross-Platform Binary Code Similarity Detection[C]//Proceedings of the 2017 ACM SIGSAC Conference on Computer and Communications Security. Dallas, Texas, USA:Association for Computing Machinery,2017:363–376. 10.1145/3133956.3134018.



## 专有名词及其缩写

| 缩写 | 名词全称                         | 中文释义         |
| ---- | -------------------------------- | ---------------- |
| ACFG | Attributed Control Flow Graph    | 属性控制流图     |
| CDF  | Cumulative Distribution Function | （累计）分布函数 |
| CFG  | Control Flow Graph               | 控制流图         |
| IR   | Intermediate Representation      | 中间表示         |
| LSH  | Locality Sensitive Hashing       | 局部敏感哈希     |
| MCS  | Maximum Common Subgraph          | 最大公共子图     |

# to-do list

- [x] 阅读文献：Gemini
- [ ] 阅读文献：ASM2VEC
- [x] 阅读文献：discovre: Efficient cross-architecture identification of bugs in binary code
- [x] 阅读文献：Cross-architecture bug search in binary executables
- [ ] 略读文献：Recognizing Functions in Binaries with Neural Networks
- [x] 基本概念：Jaccard index
- [x] 基本概念：Minhash
- [ ] 略读文献：Blanket execution:Dynamic similarity testing for program binaries and components.
- [ ] 阅读文献：Leveraging Semantic Signatures for Bug Search in Binary Programs.
- [ ] 阅读文献：Tracelet-based code search in executables.
- [ ] 略读文献：Discriminative Embeddings of LatentVariable Models for Structured Data
- [ ] 阅读文献：Finding Unknown Malice in 10 Seconds: MassVetting for New Threats at the Google-Play Scale

