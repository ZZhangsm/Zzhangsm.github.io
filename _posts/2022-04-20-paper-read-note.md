---
title: "论文阅读笔记"
date: 2022-04-21
categories:
  - Paper
tags:
  - note
---


# **Decison Tree + Neural Networks**

1. Perceptron trees
   - DOI: https://doi.org/10.1080/09540098908915648
   - Utgoff, P. E. (1989). Perceptron trees: A case study in hybrid concept representations. Connection Science, 1(4), 377-391.
   - Every leaf nodes of a binary decision tree were realized with linear threshold units (LTU);
   - The sole requirement is that the space of instance at a node be split if that space is not linearly separable;
   - W in the LTU is a special case of absolute error correction procedure described in Nilsson(1965) 
   
2. Hybrid Decision Tree
   - DOI: https://doi.org/10.1016/S0950-7051(02)00038-2
   - Zhou, Z. H., & Chen, Z. Q. (2002). Hybrid decision tree. Knowledge-based systems, 15(8), 515-528.
   - ordered attributes → quantitative analysis → neural learning approaches
    unordered attributes → qualitative analysis → decision tree
   - **The splits of HDT** are similar to C4.5 except in two aspects: 
     - only based upon only unordered attributes
     - are selected based upon attributes-value pair instead of only attribute so that a binary tree instead of a multi-nary is generated
   - **A leaf node** is generated when either of the following situations occurs.
     - All training examples falling into current node belong to a same class
     - Diversity-threshold in the instance space
   - HDT virtually embeds feedforward neural network in leaf nodes where and only where neural processing is necessary;
   - The value of ordered attributes can be normalized;
   - In order to solve the  speed and the large amounts of training examples,we use a specific feedforwad neural network named FANNC
   - Another technique may be helpful to alleviate the lack of enough training examples, Any future examples 
falling into dummy nodes are classified by the trained collective network.
   -  Incremental Learning
    
3. NeC4.5
   - DOI: https://doi.org/10.1109/TKDE.2004.11
   - Zhou, Z. H., & Jiang, Y. (2004). NeC4. 5: neural ensemble based C4. 5. IEEE Transactions on Knowledge and Data Engineering, 16(6), 770-773.
   - Bagging随机抽取数据训练神经网络
   - 用此神经网络根据训练数据生成新的标签，并根据完全随机数据及参数mu生成标签，mu标志着额外数据的比例
   - 集合以上三种数据训练C4.5