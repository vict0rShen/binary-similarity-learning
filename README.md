# binary-similarity-learning

二进制代码相似度分析（Binary Code Similarity Analysis）学习笔记

`[paper]`：论文发布页；`[note]`：论文笔记 ；`[github]`：github源码；`[dataset]`：数据集

方法名前的`*`表示该方法使用了动态分析

## 基本概念解析

已整理于[基本概念解析文档](./concept.md)，学习笔记中涉及相关概念位置均已设置超链接。

## 综述 (review)

- A Survey of Binary Code Similarity (*WOS-Q1; 中科院-1区；2021*) [[paper]](https://dl.acm.org/doi/abs/10.1145/3446371) [[note]](./notes/A_Survey_of_Binary_Code_Similarity.md)
  - HAQ I U, CABALLERO J. A Survey of Binary Code Similarity [J]. ACM Comput Surv, 2021, 54(3): Article 51. 
  - 领域内常用方法的分类与概述，适合入门
  - 仅包含2019年及以前的文献

## Binary Diffing

- Bindiff (*DIMVA2004*) [[paper]](https://www.researchgate.net/profile/Thomas-Dullien-3/publication/28356113_Structural_Comparison_of_Executable_Objects/links/568c0fb108ae197e426895bc/Structural-Comparison-of-Executable-Objects.pdf)
  - FLAKE H. Structural comparison of executable objects[C]//Proc. of the International GI Workshop on Detection of Intrusions and Malware & Vulnerability Assessment, number P-46 in Lecture Notes in Informatics.2004:161-174. 
- Graph-based comparison of executable objects (*SSTIC2005*) [[paper]](http://195.154.171.95/SSTIC05/Analyse_differentielle_de_binaires/SSTIC05-article-Flake-Graph_based_comparison_of_Executable_Objects.pdf) [[note]](./notes/Graph-based_comparison_of_executable_objects.md)
  - DULLIEN T, ROLLES R. Graph-based comparison of executable objects (english version) [J]. Sstic, 2005, 5(1): 3.
- BinHunt (*CCF-C；ICICS2008*) [[paper]](https://link.springer.com/chapter/10.1007/978-3-540-88625-9_16) [[note]](./notes/BinHunt.md)
  - GAO D, REITER M K, SONG D. BinHunt: Automatically Finding Semantic Differences in Binary Programs[C]//International Conference on Information and Communications Security. Berlin, Heidelberg:Springer Berlin Heidelberg,2008:238-255. 


## Binary Similarity (one-to-one)

- *BLEX *(CCF-A; USENIX2014)* [[paper]](https://www.usenix.org/conference/usenixsecurity14/technical-sessions/presentation/egele) [[note]](./notes/BLEX.md)
  - EGELE M, WOO M, CHAPMAN P, et al. Blanket execution: Dynamic similarity testing for program binaries and components[C]//23rd USENIX Security Symposium (USENIX Security 14).2014:303-317. 

## Binary Search (one-to-many)

- TEDEM (*CCF-B; ACSAC2014*)  [[paper]](https://dl.acm.org/doi/abs/10.1145/2664243.2664269) [[note]](./notes/TEDEM.md)
  - PEWNY J, SCHUSTER F, BERNHARD L, et al. Leveraging semantic signatures for bug search in binary programs[C]//Proceedings of the 30th Annual Computer Security Applications Conference.2014:406-415. 
- Tracy (*CCF-A；PLDI2014*) [[paper]](https://dl.acm.org/doi/abs/10.1145/2666356.2594343) [[github]](https://github.com/Yanivmd/TRACY) [[note]](./notes/Tracy.md)
  - DAVID Y, YAHAV E. Tracelet-based code search in executables[C]//Proceedings of the 35th ACM SIGPLAN Conference on Programming Language Design and Implementation. Edinburgh, United Kingdom:Association for Computing Machinery,2014:349–360. 10.1145/2594291.2594343.
- Multi-MH (*CCF-A；S&P2015*) [[paper]](https://ieeexplore.ieee.org/abstract/document/7163056) [[note]](./notes/Multi-MH.md)
  - PEWNY J, GARMANY B, GAWLIK R, et al. Cross-Architecture Bug Search in Binary Executables[C]//2015 IEEE Symposium on Security and Privacy.2015:709-724. 10.1109/SP.2015.49.
- BinGo (*CCF-A；FSE2016*) [[paper]](https://dl.acm.org/doi/10.1145/2950290.2950350) [[note]](./notes/BinGo.md)
  - CHANDRAMOHAN M, XUE Y, XU Z, et al. Bingo: Cross-architecture cross-os binary search[C]//Proceedings of the 2016 24th ACM SIGSOFT International Symposium on Foundations of Software Engineering.2016:678-689. 

- discovRE (*CCF-A；NDSS2016*)  [[paper]](https://www.ndss-symposium.org/wp-content/uploads/2017/09/discovre-efficient-cross-architecture-identification-bugs-binary-code.pdf) [[note]](./notes/discovRE.md)
  - ESCHWEILER S, YAKDAN K, GERHARDS-PADILLA E. discovRE: Efficient Cross-Architecture Identification of Bugs in Binary Code[C]//NDSS.2016
- Esh (*CCF-A；PLDI2016*) [[paper]](https://nlibvpn.bit.edu.cn/https/77726476706e69737468656265737421f4fb0f9d243d265f6c0f/doi/10.1145/2908080.2908126) [[github]](https://github.com/tech-srl/esh) [[note]](./notes/Esh.md)
  - DAVID Y, PARTUSH N, YAHAV E. Statistical similarity of binaries[C]//Proceedings of the 37th ACM SIGPLAN Conference on Programming Language Design and Implementation. Santa Barbara, CA, USA:Association for Computing Machinery,2016:266–280. 10.1145/2908080.2908126.
- Genius (*CCF-A；CCS2016*) [[paper]](https://dl.acm.org/doi/abs/10.1145/2976749.2978370) [[github]](https://github.com/qian-feng/Gencoding) [[note]](./notes/Genius.md)
  - FENG Q, ZHOU R, XU C, et al. Scalable Graph-based Bug Search for Firmware Images[C]//Proceedings of the 2016 ACM SIGSAC Conference on Computer and Communications Security. Vienna, Austria:Association for Computing Machinery,2016:480–491. 10.1145/2976749.2978370.
- Gemini (*CCF-A；CCS2017*) [[paper]](https://dl.acm.org/doi/abs/10.1145/3133956.3134018) [[github]](https://github.com/Yunlongs/Gemini) [[note]](./notes/Gemini.md)
  - XU X, LIU C, FENG Q, et al. Neural Network-based Graph Embedding for Cross-Platform Binary Code Similarity Detection[C]//Proceedings of the 2017 ACM SIGSAC Conference on Computer and Communications Security. Dallas, Texas, USA:Association for Computing Machinery,2017:363–376. 10.1145/3133956.3134018.

## Clone Search

- Kam1n0 *(CCF-A; KDD2016)*  [[paper]](https://dl.acm.org/doi/abs/10.1145/2939672.2939719) [[github]](https://github.com/McGill-DMaS/Kam1n0-Community)
  - DING S H H, FUNG B C M, CHARLAND P. Kam1n0: MapReduce-based Assembly Clone Search for Reverse Engineering[C]//Proceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining.2016:461-470. 
  - 侧重于新哈希算法和MapReduce方案的设计
- Asm2Vec (*CCF-A；S&P2019*) [[paper]](https://ieeexplore.ieee.org/abstract/document/8835340) [[note]](./notes/Asm2Vec.md)
  - DING S H H, FUNG B C M, CHARLAND P. Asm2Vec: Boosting Static Representation Robustness for Binary Clone Search against Code Obfuscation and Compiler Optimization[C]//2019 IEEE Symposium on Security and Privacy (SP).2019:472-489. 10.1109/SP.2019.00003.

## Measurement Study

- How machine learning is solving the binary function similarity problem *(CCF-A; USENIX2022)* [[paper]](https://www.usenix.org/conference/usenixsecurity22/presentation/marcelli) [[github]](https://github.com/Cisco-Talos/binary_function_similarity) [[note]](./notes/How_Machine_Learning_is_Solving_the_BInary_Function_Similarity_Problem.md)
  - MARCELLI A, GRAZIANO M, UGARTE-PEDRERO X, et al. How machine learning is solving the binary function similarity problem[C]//31st USENIX Security Symposium (USENIX Security 22).2022:2099-2116. 
  - 构建开源数据集，将现有方法在同一基准下进行测试
  - 阅读相关论文时可作为分析用参考，精读对应部分

## Dataset

- Esh Dataset [[dataset]](https://github.com/nimrodpar/esh-dataset-1523)
  - 包含3015个二进制函数，覆盖8类实际漏洞


## 专有名词及其缩写

| 缩写 | 名词全称                            | 中文释义           |
| ---- | ----------------------------------- | ------------------ |
| ACFG | Attributed Control Flow Graph       | 属性控制流图       |
| ALSH | Adaptive Locality Sensitive Hashing | 自适应局部敏感哈希 |
| CDF  | Cumulative Distribution Function    | （累计）分布函数   |
| CFG  | Control Flow Graph                  | 控制流图           |
| GI   | Graph Isomorphism                   | 图同构             |
| IR   | Intermediate Representation         | 中间表示           |
| IVL  | Intermediate Verification Language  | 中间验证语言       |
| LCS  | Longest Common Subsequence          | 最长公共子序列     |
| LSH  | Locality Sensitive Hashing          | 局部敏感哈希       |
| MCS  | Maximum Common Subgraph             | 最大公共子图       |
| MRR  | Mean Reciprocal Rank                | 平均倒数排名       |
| PDG  | Program Dependence Graph            | 程序依赖图         |
| TED  | Tree Edit Distance                  | 树编辑距离         |

# to-do list

- [ ] 略读文献：Graph-based Comparison of Executable Objects.
- [x] 略读文献：BinHunt
- [ ] 略读文献：Binary Function Clustering Using Semantic Hashes.
- [ ] 略读文献：Fast Location of Similar Code Fragments Using Semantic ’Juice’
- [ ] 略读文献：Discovering Potential Binary Code Re-use.
- [x] 基本概念：S-Expression
- [ ] 阅读文献：*Rendezvous
- [x] 阅读文献：BinGo: cross-architecture cross-OS binary search
- [x] 阅读文献：[Neural Machine Translation Inspired Binary Code Similarity Comparison beyond Function Pairs](https://www.semanticscholar.org/paper/fe3470a9c37e88928fbd0d84ed578357b1f07a0d)
- [x] 阅读文献：How Machine Learning Is Solving the Binary Function Similarity Problem
- [ ] 阅读文献：Order Matters: Semantic-Aware Neural Networks for Binary Code Similarity Detection
- [x] 阅读文献：Statistical similarity of binaries.
- [ ] 阅读：https://googleprojectzero.blogspot.com/2018/12/searching-statically-linked-vulnerable.html
- [ ] 阅读文献：Graph matching networks for learning the similarity of graph structured objects
- [ ] 阅读文献：Binary Similarity Detection Using Machine Learning.
- [ ] 阅读文献：*Safe: Self-attentive function embeddings for binary similarity
- [ ] 阅读文献：Investigating Graph Embedding Neural Networks with Unsupervised Features Extraction for Binary Analysis. 
- [ ] 阅读文献：Codecmr: Cross-modal retrieval for function-level binary source code matching.
- [ ] 阅读文献：Trex: Learning execution semantics from micro-traces for binary similarity
- [ ] 阅读文献：Library functions identification in binary code by using graph isomorphism testings
- [ ] 阅读文献：Semantics-based obfuscation-resilient binary code similarity comparison with applications to software plagiarism detection
- [ ] 阅读文献：Cross-Architecture Bug Search in Binary Executables
- [ ] 阅读文献：*Binary Code Clone Detection across Architectures and Compiling Configurations
- [ ] 阅读文献：BinClone: Detecting Code Clones in Malware
- [ ] 略读文献：Distributed Representations of Sentences and Documents
- [ ] 阅读文献：Compiler-agnostic function detection in binaries
- [ ] 阅读文献：*Accurate and Scalable Cross-Architecture Cross-OS Binary Code Search with Emulation
- [ ] 阅读文献：*Learning Program-Wide Code Representations for Binary Diffing
- [ ] 阅读文献：jTrans: jump-aware transformer for binary code similarity detection
- [ ] 阅读文献：[Semantic Learning and Emulation Based Cross-Platform Binary Vulnerability Seeker](https://www.semanticscholar.org/paper/4c16bf0be5ee1eff6f3749a56fea215cc812ba96)
- [ ] 阅读文献：[Revisiting Binary Code Similarity Analysis using Interpretable Feature Engineering and Lessons Learned](https://www.semanticscholar.org/paper/3121b307c1e1e893e001ac8f7742e8b3f87ea966)
- [ ] 阅读文献：BinSim: Trace-based Semantic Binary Diffing via System Call Sliced Segment Equivalence Checking
- [ ] 阅读文献：Similarity of binaries through re-optimization
- [ ] 阅读文献：*[Semantics-Based Obfuscation-Resilient Binary Code Similarity Comparison with Applications to Software and Algorithm Plagiarism Detection](https://www.semanticscholar.org/paper/d86129473ebc932af4cdcf143a196e60e24fad9b)
- [ ] 阅读文献：[Accurate and Scalable Cross-Architecture Cross-OS Binary Code Search with Emulation](https://www.semanticscholar.org/paper/842f0e0022a16cb194cfb86d153bfe37ff39bb46)
- [ ] 阅读文献：semantics-based obfuscation-resilient binary code similarity comparison with applications to software plagiarism detection.（bingo前置）
- [ ] 略读文献：value-based program characterization and its application to software plagiarism detection
- [ ] 略读文献：Finer-grained control flow integrity for stripped binaries（bingo前置）
- [ ] 略读文献：Towards automatic software lineage inference（经典文献）
- [ ] 略读文献：Binslayer: accurate comparison of binary executables
- [ ] 阅读文献：[Extracting Conditional Formulas for Cross-Platform Bug Search](https://www.semanticscholar.org/paper/c75d9f1ff9177b26b7681876d7ee810d14401a49)
- [ ] 阅读文献：Patch based vulnerability matching for binary programs
- [ ] 阅读文献：[Semantics-Based Obfuscation-Resilient Binary Code Similarity Comparison with Applications to Software and Algorithm Plagiarism Detection](https://www.semanticscholar.org/paper/d86129473ebc932af4cdcf143a196e60e24fad9b)
- [ ] 略读文献：iBinHunt

