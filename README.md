# LncRNA-disease association prediction methods Review
![GitHub stars](https://img.shields.io/github/stars/sheng-n/lncRNA-disease-methods?color=red) ![GitHub forks](https://img.shields.io/github/forks/sheng-n/lncRNA-disease-methods?color=green&label=Fork) ![visitors](https://visitor-badge.glitch.me/badge?page_id=sheng-n.lncRNA-disease-methods)

## What is LncRNA?
RNA can be divided into two categories based on its coding function: (1) RNAs with coding potential, and (2) RNAs without coding potential, also known as non-coding RNA (ncRNA), which includes microRNAs (miRNA), snoRNAs, circRNAs and lncRNAs. Long non-coding RNAs (lncRNAs) are a major class of important ncRNAs with the lengths more than 200 nucleotides. An increasing number of lncRNA have been found to be abnormally expressed in human diseases, and play a critical role in tumor development.

## Table of Contents
* [Overview](#Overview) 
* [Machine learning-based methods](#Machine-learning-based-methods) 
  - [Regularized Least Square](#Regularized-Least-Square)
  - [Support Vector Machine](#Support-Vector-Machine)
  - [Random Forest](#Random-Forest)
  - [Naive Bayesian](#Naive-Bayesian)
* [Network propagation-based methods](#Network-propagation-based-methods) 
  - [Random walk](#Random-walk)
  - [Flow propagation and label propagation](#Flow-propagation-and-label-propagation)
  - [Network inference](#Network-inference)
  - [Other network propagation algorithms](#Other-network-propagation-algorithmse)
* [Matrix factorization- and completion-based methods](#Matrix-factorization-and-completion-based-methods) 
  - [Matrix factorization](#Matrix-factorizatione)
  - [Matrix completion](#Matrix-completion)
* [Deep learning-based methods](#Deep-learning-based-methods) 
  - [Full connected neural network](#Full-connected-neural-network)
  - [Convolutional neural network](#Convolutional-neural-network)
  - [Autoencoder](#Autoencoder)
  - [Generative adversarial network](#Generative-adversarial-network)
* [Graph neural network-based methods](#Graph-neural-network-based-methods) 
  - [Graph feature extraction](#Graph-feature-extraction)
  - [Graph matrix completion](#Graph-matrix-completion)
* [Cancer-related lncRNA candidates](#Cancer-related-lncRNA-candidates) 
  - [Lung cancer-related lncRNA candidates](#Lung-cancer-related-lncRNA-candidates)
  - [Prostate cancer-related lncRNA candidates](#Prostate-cancer-related-lncRNA-candidates)
  - [Breast cancer-related lncRNA candidates](#Breast-cancer-related-lncRNA-candidates)
  - [Colorectal cancer-related lncRNA candidates](#Colorectal-cancer-related-lncRNA-candidates)
  - [Colon cancer-related lncRNA candidates](#Colon-cancer-related-lncRNA-candidates)
  - [Cervical cancer-related lncRNA candidates](#Cervical-cancer-related-lncRNA-candidates)
  - [Gastric(Stomach) cancer-related lncRNA candidates](#Gastric(Stomach)-cancer-related-lncRNA-candidates)

## Overview
We present a timely and comprehensive review of existing computational methods for lncRNA-disease association prediction. Specifically, these methods are systematically classified and divided into 5 categories, including machine learning, network propagation, matrix factorization and completion, deep learning, and graph neural networks, as shown below.
![Computational lncRNA-disease association prediction methods based on various models.](https://user-images.githubusercontent.com/95516781/168040579-416a1848-be8b-4066-af50-48453d29f011.png)
Fig 1: Computational lncRNA-disease association prediction methods based on various models.

## Machine learning-based methods
### Regularized Least Square
1. **[LRLSLDA]** Chen X, Yan G-Y. Novel human lncRNA–disease association inference based on lncRNA expression profiles, Bioinformatics 2013;29(20):2617-2624.

2. **[LNCSIM]** Chen X, Clarence Yan C, Luo C et al. Constructing lncRNA functional similarity network based on lncRNA-disease associations and disease semantic similarity, Scientific Reports 2015;5(1):11338.

### Support Vector Machine
1. **[LDAP]** Lan W, Li M, Zhao K et al. LDAP: a web server for lncRNA-disease association prediction, Bioinformatics 2016;33(3):458-460.

2. **[ILDMSF]** Chen Q, Lai D, Lan W et al. ILDMSF: Inferring Associations Between Long Non-Coding RNA and Disease Based on Multi-Similarity Fusion, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(3):1106-1112.

### Random Forest
1. **[RFLDA]** Yao D, Zhan X, Zhan X et al. A random forest based computational model for predicting novel lncRNA-disease associations, BMC Bioinformatics 2020;21(1):126. [**[Code]**](https://github.com/ydkvictory/RFLDA "Click") 

2. **[IPCARF]** Zhu R, Wang Y, Liu J-X et al. IPCARF: improving lncRNA-disease association prediction using incremental principal component analysis feature selection and a random forest classifier, BMC Bioinformatics 2021;22(1):175. [**[Code]**](https://github.com/zhurong1942/IPCARF_zr1 "Click") 

### Naive Bayesian
1. **[CFNBC]** Yu J, Xuan Z, Feng X et al. A novel collaborative filtering model for LncRNA-disease association prediction based on the Naïve Bayesian classifier, BMC Bioinformatics 2019;20(1):396. [**[Code]**](https://github.com/jingwenyu18/CFNBC "Click") 

2. **[NBCLDA]** Yu J, Ping P, Wang L et al. A Novel Probability Model for LncRNA–Disease Association Prediction Based on the Naïve Bayesian Classifier, Genes 2018;9(7).

## Network propagation-based methods
### Random walk
1. **[RWRlncD]** Sun J, Shi H, Wang Z et al. Inferring novel lncRNA–disease associations based on a random walk model of a lncRNA functional similarity network, Molecular Biosystems 2014;10(8):2074-2081.

2. **[RWRHLD]** Zhou M, Wang X, Li J et al. Prioritizing candidate disease-related long non-coding RNAs by walking on the heterogeneous lncRNA and disease network, Molecular Biosystems 2015;11(3):760-769.

3. **[IRWRLDA]** Chen X, You Z-H, Yan G-Y et al. IRWRLDA: improved random walk with restart for lncRNA-disease association prediction, Oncotarget 2016;7(36):57919-57931.

4. **[GrwLDA]** Gu C, Liao B, Li X et al. Global network random walk for predicting potential human lncRNA-disease associations, Scientific Reports 2017;7(1):12442.

5. **[BRWLDA]** Yu G, Fu G, Lu C et al. BRWLDA: bi-random walks for predicting lncRNA-disease associations, Oncotarget 2017;8(36):60429-60446.

6. **[BiWalkLDA]** Hu J, Gao Y, Li J et al. A novel algorithm based on bi-random walks to identify disease-related lncRNAs, BMC Bioinformatics 2019;20(18):569. [**[Code]**](https://github.com/jhu99/BiwalkLDA "Click") 

7. **[LDA-LNSUBRW]** Xie G, Jiang J, Sun Y. LDA-LNSUBRW: lncRNA-disease association prediction based on linear neighborhood similarity and unbalanced bi-random walk, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2020:1-1. [**[Code]**](https://github.com/JIAWEI1234/LDA-LNSUBRW "Click") 

8. **[HAUBRW]** Xie G, Wu C, Gu G et al. HAUBRW: Hybrid algorithm and unbalanced bi-random walk for predicting lncRNA-disease associations, Genomics 2020;112(6):4777-4787.

9. **[LION]** Sumathipala M, Maiorino E, Weiss ST et al. Network Diffusion Approach to Predict LncRNA Disease Associations Using Multi-Type Biological Networks: LION, Frontiers in Physiology 2019;10.

10. **[MHRWR]** Zhao X, Yang Y, Yin M. MHRWR: Prediction of lncRNA-Disease Associations Based on Multiple Heterogeneous Networks, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(6):2577-2585. [**[Code]**](https://github.com/yangyq505/MHRWR "Click")

11. **[IDHI-MIRW]** Fan X-N, Zhang S-W, Zhang S-Y et al. Prediction of lncRNA-disease associations by integrating diverse heterogeneous information sources with RWR algorithm and positive pointwise mutual information, BMC Bioinformatics 2019;20(1):87. [**[Code]**](https://github.com/NWPU-903PR/IDHI-MIRW "Click") 

12.**[LRWRHLDA]** Wang L, Shang M, Dai Q et al. Prediction of lncRNA-disease association based on a Laplace normalized random walk with restart algorithm on heterogeneous networks, BMC Bioinformatics 2022;23(1):5. [**[Code]**](https://github.com/wang-124/LRWRHLDA "Click")

13. **[IIRWR]** Wang L, Xiao Y, Li J et al. IIRWR: Internal Inclined Random Walk With Restart for LncRNA-Disease Association Prediction, IEEE Access 2019;7:54034-54041.

14. **[LRWHLDA]** Li J, Zhao H, Xuan Z et al. A Novel Approach for Potential Human LncRNA-Disease Association Prediction Based on Local Random Walk, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(3):1049-1059.

### Flow propagation and label propagation
1. **[LncRDNetFlow]** Zhang J, Zhang Z, Chen Z et al. Integrating Multiple Heterogeneous Networks for Novel LncRNA-Disease Association Inference, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2019;16(2):396-406.

2. **[LLCLPLDA]** Xie G, Huang S, Luo Y et al. LLCLPLDA: a novel model for predicting lncRNA–disease associations, Molecular Genetics and Genomics 2019;294(6):1477-1486.

### Network inference
1. **[Ping et al]** Ping P, Wang L, Kuang L et al. A Novel Method for LncRNA-Disease Association Prediction Based on an lncRNA-Disease Association Network, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2019;16(2):688-693.

### Other network propagation algorithms
1. **[Yang et al]** Yang X, Gao L, Guo X et al. A Network Based Method for Analysis of lncRNA-Disease Associations and Prediction of lncRNAs Implicated in Diseases, PLOS ONE 2014;9(1):e87797.

2. **[TPGLDA]** Ding L, Wang M, Sun D et al. TPGLDA: Novel prediction of associations between lncRNAs and diseases via lncRNA-disease-gene tripartite graph, Scientific Reports 2018;8(1):1065. [**[Code]**](https://github.com/USTC-HIlab/TPGLDA "Click") 

3. **[IDLDA]** Wang Q, Yan G. IDLDA: An Improved Diffusion Model for Predicting LncRNA–Disease Associations, Frontiers in genetics 2019;10.

4. **[NCPLDA]** Li G, Luo J, Liang C et al. Prediction of LncRNA-Disease Associations Based on Network Consistency Projection, IEEE Access 2019;7:58849-58856. [**[Code]**](https://github.com/ghli16/NCPLDA "Click") 

5. **[LDAI-ISPS]** Zhang Y, Chen M, Li A et al. LDAI-ISPS: LncRNA–Disease Associations Inference Based on Integrated Space Projection Scores, International journal of molecular sciences 2020;21(4).

6. **[LDAH2V]** Deng L, Li W, Zhang J. LDAH2V: Exploring Meta-Paths Across Multiple Networks for lncRNA-Disease Association Prediction, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(4):1572-1581.

7. **[SVDNVLDA]** Li J, Li J, Kong M et al. SVDNVLDA: predicting lncRNA-disease associations by Singular Value Decomposition and node2vec, BMC Bioinformatics 2021;22(1):538.

## Matrix factorization- and completion-based methods
### Matrix factorization
1. **[MFLDA]** Fu G, Wang J, Domeniconi C et al. Matrix factorization-based data fusion for the prediction of lncRNA–disease associations, Bioinformatics 2017;34(9):1529-1537. [**[Code]**](http://www.sdu-idea.cn/codes.php?name=MFLDA "Click") 

2. **[WMFLDA]** Wang Y, Yu G, Wang J et al. Weighted matrix factorization on multi-relational data for LncRNA-disease association prediction, Methods 2020;173:32-43. [**[Code]**](http://mlda.swu.edu.cn/codes.php?name=WMFLDA "Click") 

3. **[DNILMF-LDA ]** Li Y, Li J, Bian N. DNILMF-LDA: Prediction of lncRNA-Disease Associations by Dual-Network Integrated Logistic Matrix Factorization and Bayesian Optimization, Genes 2019;10(8).

4. **[PMFILDA]** Xuan Z, Li J, Yu J et al. A Probabilistic Matrix Factorization Method for Identifying lncRNA-Disease Associations, Genes 2019;10(2).

5. **[WGRCMF]** Liu JX, Cui Z, Gao YL et al. WGRCMF: A Weighted Graph Regularized Collaborative Matrix Factorization Method for Predicting Novel LncRNA-Disease Associations, IEEE Journal of Biomedical and Health Informatics 2021;25(1):257-265.

6. **[LDGRNMF]** Wang M-N, You Z-H, Wang L et al. LDGRNMF: LncRNA-disease associations prediction based on graph regularized non-negative matrix factorization, Neurocomputing 2021;424:236-245.

### Matrix completion
1. **[SIMCLDA]** Lu C, Yang M, Luo F et al. Prediction of lncRNA–disease associations based on inductive matrix completion, Bioinformatics 2018;34(19):3357-3364. [**[Code]**](https://github.com//bioinfomaticsCSU/SIMCLDA "Click") 

2. **[GMCLDA]** Lu C, Yang M, Li M et al. Predicting Human lncRNA-Disease Associations Based on Geometric Matrix Completion, IEEE Journal of Biomedical and Health Informatics 2020;24(8):2420-2429.  [**[Code]**](https://github.com/bioinfomaticsCSU/GMCLDA "Click") 

## Deep learning-based methods
### Full connected neural network
1. **[NNLDA]** Hu J, Gao Y, Li J et al. Deep Learning Enables Accurate Prediction of Interplay Between lncRNA and Disease, Frontiers in genetics 2019;10. [**[Code]**](https://github.com/gao793583308/NNLDA "Click") 

2. **[DMFLDA]** Zeng M, Lu C, Fei Z et al. DMFLDA: A Deep Learning Framework for Predicting lncRNA–Disease Associations, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(6):2353-2363. [**[Code]**](https://github.com/CSUBioGroup/DMFLDA "Click")

3. **[SDLDA]** Zeng M, Lu C, Zhang F et al. SDLDA: lncRNA-disease association prediction based on singular value decomposition and deep learning, Methods 2020;179:73-80. [**[Code]**](https://github.com/CSUBioGroup/SDLDA "Click") 

### Convolutional neural network
1. **[CNNLDA]** Xuan P, Cao Y, Zhang T et al. Dual Convolutional Neural Networks With Attention Mechanisms Based Method for Predicting Disease-Related lncRNA Genes, Frontiers in genetics 2019;10.

2. **[LDApred]** Xuan P, Jia L, Zhang T et al. LDAPred: A Method Based on Information Flow Propagation and a Convolutional Neural Network for the Prediction of Disease-Associated lncRNAs, International journal of molecular sciences 2019;20(18).

3. **[iLncRNAdis-FB]** Wei H, Liao Q, Liu B. iLncRNAdis-FB: Identify lncRNA-Disease Associations by Fusing Biological Feature Blocks Through Deep Neural Network, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(5):1946-1957.

4. **[MCA-Net]** Zhang Y, Ye F, Gao X. MCA-Net: Multi-feature coding and attention convolutional neural network for predicting lncRNA-disease association, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021:1-1.

### Autoencoder
1. **[CNNDLP]** Xuan P, Sheng N, Zhang T et al. CNNDLP: A Method Based on Convolutional Autoencoder and Convolutional Neural Network with Adjacent Edge Attention for Predicting lncRNA–Disease Associations, International journal of molecular sciences 2019;20(17).

2. **[LDNFSGB]** Zhang Y, Ye F, Xiong D et al. LDNFSGB: prediction of long non-coding rna and disease association using network feature similarity and gradient boosting, BMC Bioinformatics 2020;21(1):377. [**[Code]**](https://github.com/MLMIP/LDNFSGB "Click") 

3. **[LDASR]** Guo Z-H, You Z-H, Wang Y-B et al. A Learning-Based Method for LncRNA-Disease Association Identification Combing Similarity Information and Rotation Forest, iScience 2019;19:786-795.

4. **[MAN]** Su X, You Z, Yi H. Prediction of LncRNA-Disease Associations Based on Network Representation Learning. In: 2020 IEEE International Conference on Bioinformatics and Biomedicine (BIBM). 2020, p.1805-1812.

5. **[VADLP]** Sheng N, Cui H, Zhang T et al. Attentional multi-level representation encoding based on convolutional and variance autoencoders for lncRNA–disease association prediction, Briefings in Bioinformatics 2020;22(3).

### Generative adversarial network
1. **[BiGAN]** Yang Q, Li X. BiGAN: LncRNA-disease association prediction based on bidirectional generative adversarial network, BMC Bioinformatics 2021;22(1):357. [**[Code]**](https://github.com/TomasYang001/BiGAN-lncRNA-disease-associations-prediction "Click")

## Graph neural network-based methods
### Graph feature extraction
1. **[GCNLDA]** Xuan P, Pan S, Zhang T et al. Graph Convolutional Network and Convolutional Neural Network Based Method for Predicting lncRNA-Disease Associations, Cells 2019;8(9).

2. **[GAERF]** Wu Q-W, Xia J-F, Ni J-C et al. GAERF: predicting lncRNA-disease associations by graph auto-encoder and random forest, Briefings in Bioinformatics 2021;22(5).


3. **[MLGCNET]** Wu QW, Cao RF, Xia J et al. Extra Trees Method for Predicting LncRNA-Disease Association Based on Multi-layer Graph Embedding Aggregation, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021:1-1. [**[Code]**](https://github.com/QingwWu/MLGCNET "Click")

4. **[MGATE]** Sheng N, Huang L, Wang Y et al. Sheng N, Huang L, Wang Y et al. Multi-channel graph attention autoencoders for disease-related lncRNAs prediction, Briefings in Bioinformatics 2022;23(2). [**[Code]**](https://github.com/sheng-n/MGATE "Click")

5. **[GANLDA]** Lan W, Wu X, Chen Q et al. GANLDA: Graph attention network for lncRNA-disease associations prediction, Neurocomputing 2022;469:384-393.

6. **[GTAN]** Xuan P, Zhan L, Cui H et al. Graph Triple-Attention Network for Disease-related LncRNA Prediction, IEEE Journal of Biomedical and Health Informatics 2021:1-1.

7. **[PANDA]** Silva ABOV, Spinosa EJ. Graph Convolutional Auto-Encoders for predicting novel lncRNA-Disease associations, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021:1-1.


### Graph matrix completion
1. **[GAMCLDA]** Wu X, Lan W, Chen Q et al. Inferring LncRNA-disease associations based on graph autoencoder matrix completion, Computational Biology and Chemistry 2020;87:107282.

2. **[GCRFLDA]** Fan Y, Chen M, Pan X. GCRFLDA: scoring lncRNA-disease associations using graph convolution matrix completion with conditional random field, Briefings in Bioinformatics 2021;23(1). [**[Code]**](https://github.com/jademyC1221/GCRFLDA "Click")

3. **[HGATLDA]** Zhao X, Zhao X, Yin M. Heterogeneous graph attention network based on meta-paths for lncRNA–disease association prediction, Briefings in Bioinformatics 2021;23(1).

4. **[VGAELDA]** Shi Z, Zhang H, Jin C et al. A representation learning model based on variational inference and graph autoencoder for predicting lncRNA-disease associations, BMC Bioinformatics 2021;22(1):136. [**[Code]**](https://github.com/zhanglabNKU/VGAELDA "Click")


## Cancer related lncRNA candidates

### Lung cancer-related lncRNA candidates
| Unverified lncRNA  | Rank  | Prediction model | Unverified lncRNA  | Rank  | Prediction model
|:------------------:|:-----:|:---------------: |:------------------:|:-----:|:---------------:|
|TCL6                | 5     | LDGRNMF          |LINC00271           |16     |ILDMSF           |
|PTCSC1              |8      |LDGRNMF           |BACE1-AS            |17     |ILDMSF           |
|LINCMD1             |8      |iLncRNAdis-FB     |DISC2               |20     |ILDMSF           |
|CCDC26              |14     |iLncRNAdis-FB     |PCA3                |2      |CNNLDA           |
|SRA1                |8,9    |LDA-LNSUBRW, DNILMF-LDA |LINC00675     |3      |CNNLDA           |

### Prostate cancer-related lncRNA candidates
| Unverified lncRNA  | Rank  | Prediction model | Unverified lncRNA  | Rank  | Prediction model
|:------------------:|:-----:|:---------------: |:------------------:|:-----:|:---------------:|
|LSINCT5             |5      | GAERF            |RN7SK               |4      |DMFLDA           |
|TDRG1               |7      |GTAN              |NPTN-IT1            |8      |DMFLDA           |
|EGOT                |10     |GANLDA            |HIF1A-AS2           |4      |LDASR            |
|PRINS               |14     |GANLDA            |CYTOR               |8      |LDASR            |
|PANDAR              |2      |DMFLDA            |CDKN2B-AS1          |2      |BiWalkLDA        |

### Breast cancer-related lncRNA candidates
| Unverified lncRNA  | Rank  | Prediction model | Unverified lncRNA  | Rank  | Prediction model
|:------------------:|:-----:|:---------------: |:------------------:|:-----:|:---------------:|
|GACAT2              |15     |GCRFLDA             |LRRC2-AS1         |7      |SVDNVLDA         |
|DNM3OS              |1,5    |LDGRNMF, DNILMF-LDA |lnc-KCTD6-3       |9      |SVDNVLDA         |
|RN7SK               |5      |LDGRNMF             |RPL34-AS1         |7      |DNILMF-LDA       |

### Colorectal cancer-related lncRNA candidates
| Unverified lncRNA  | Rank  | Prediction model | Unverified lncRNA  | Rank  | Prediction model
|:------------------:|:-----:|:---------------: |:------------------:|:-----:|:---------------:|
|TCL6                |5      |LDNFSGB           |LINC00237           |2      |DMFLDA           |
|HAR1B               |6      |LDNFSGB           |FAS-AS1             |10     |DMFLDA           |
|NBAT1               |10     |DMFLDA            |             

### Colon cancer-related lncRNA candidates
| Unverified lncRNA  | Rank  | Prediction model | Unverified lncRNA  | Rank  | Prediction model
|:------------------:|:-----:|:---------------: |:------------------:|:-----:|:---------------:|
|DNM3OS              |6      |VGAELDA           |LINC00663           |10     |iLncRNAdis-FB    |
|SPRY4-IT1           |10     |VGAELDA           |LRRC75A-AS1         |9      |LDAH2V           |
|LINC01628           |4      |iLncRNAdis-FB     |BC040587            |10     |DNILMF-LDA       |
|KIRREL3-AS3         |9      |iLncRNAdis-FB     |

### Cervical cancer-related lncRNA candidates
| Unverified lncRNA  | Rank  | Prediction model | Unverified lncRNA  | Rank  | Prediction model
|:------------------:|:-----:|:---------------: |:------------------:|:-----:|:---------------:|
|HOTTIP             |8       |GCRFLDA           |HOTAIRM1            |7      |LDNFSGB          |
|IGF2-AS            |11      |GCRFLDA           |FER1L4              |8      |IIRWR            |
|TUSC7              |15      |GCRFLDA           |FAM212B-AS1         |10     |IIRWR            |

### Gastric(Stomach) cancer-related lncRNA candidates
| Unverified lncRNA  | Rank  | Prediction model | Unverified lncRNA  | Rank  | Prediction model
|:------------------:|:-----:|:---------------: |:------------------:|:-----:|:---------------:|
|bx118339            |9      |LDGRNMF           |MEG8                |7      |GANLDA           |
|KCTD21-AS1          |17     |GANLDA            |KIRREL3-AS3         |8      |MLGCNET          |
|GATA3-AS1           |18     |GANLDA            |



## Welcome to contribute
If you would like to help contribute this list, please feel free to contact me by email:

* Email: shengnan21@mails.jlu.edu.cn
