# 🏎💨lncRNA-disease association prediction methods <a href='https:/lncRNA-disease-methods.r-lib.org'></a>
# Data resources and computational methods for lncRNA-disease association prediction
![GitHub stars](https://img.shields.io/github/stars/sheng-n/lncRNA-disease-methods?color=red) ![GitHub forks](https://img.shields.io/github/forks/sheng-n/lncRNA-disease-methods?color=green&label=Fork) ![visitors](https://visitor-badge.glitch.me/badge?page_id=sheng-n.lncRNA-disease-methods)

## What is LncRNA?
RNA can be divided into two categories based on its coding function: (1) RNAs with coding potential, and (2) RNAs without coding potential, also known as non-coding RNA (ncRNA), which includes microRNAs (miRNA), snoRNAs, circRNAs and lncRNAs. Long non-coding RNAs (lncRNAs) are a major class of important ncRNAs with the lengths more than 200 nucleotides. An increasing number of lncRNA have been found to be abnormally expressed in human diseases, and play a critical role in tumor development.

## Table of Contents
* [Overview](#Overview) 
* [Data resources](#Data-resources) 
  - [LncRNA-disease association data resources](#LncRNA-disease-association-data-resources)
  - [LncRNA-related data resourcess](#LncRNA-related-data-resources)
  - [Disease-related data resources](#Disease-related-data-resources)
* [Machine learning-based methods](#Machine-learning-based-methods) 
  - [Regularized Least Square](#Regularized-Least-Square)
  - [Support Vector Machine](#Support-Vector-Machine)
  - [Random Forest](#Random-Forest)
  - [Naive Bayesian](#Naive-Bayesian)
* [Network propagation-based methods](#Network-propagation-based-methods) 
  - [Random walk](#Random-walk)
  - [Flow propagation and label propagation](#Flow-propagation-and-label-propagation)
  - [Network inference](#Network-inference)
  - [Other network propagation algorithms](#Other-network-propagation-algorithms)
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
* LncRNA-related and disease-related data resources for LDA prediction are collected and presented, covering LDA data, lncRNA-related data (expression profiles, sequences, genes, miRNAs, proteins), and disease-related data (semantics, phenotypes, genes, miRNAs, proteins).
* We present a timely and comprehensive review of existing computational methods for lncRNA-disease association prediction. Specifically, these methods are systematically classified and divided into 5 categories, including machine learning, network propagation, matrix factorization and completion, deep learning, and graph neural networks, as shown below figure 1.
![Computational lncRNA-disease association prediction methods based on various models.](https://user-images.githubusercontent.com/95516781/168040579-416a1848-be8b-4066-af50-48453d29f011.png)
Fig 1: Computational lncRNA-disease association prediction methods based on various models.

* We collected and analyzed potential seven disease-related lncRNAs, which were predicted from LDA computational prediction methods over the last three years (2019-2021), to provide a candidate lncRNAs list for biological experimental verification.

## Data resources
### LncRNA-disease association data resources
| Database  | Description  | URL | 
|:------------------:|:-----:|:---------------: |
|LncRNADisease  | Documents 19,166 lncRNAs, 529 diseases and 10,564 association in Homo sapiens, Mus musculus, Rattus norvegicus and Gallus gallus  | http://www.rnanut.net/lncrnadisease/ |
|Lnc2Cancer     |Collects 2,659 lncRNAs, 216 cancers and 9,254 associations in human     |http://bio-bigdata.hrbmu.edu.cn/lnc2cancer/ |
|MNDR           |Records 39,880 lncRNA, over 1,600 diseases and 295,834 associations in 11 mammals |http://www.rna-society.org/mndr/  |

### LncRNA-related data resources
| Database  | Description  | URL | 
|:------------------:|:-----:|:---------------: |
|NONCODE     |Records the comprehensive knowledge database of ncRNA from 39 speciesn |http://www.noncode.org/ |
|RNAcentral  |Documents ncRNA sequences for 296 species  |https://rnacentral.org/  |
|EVLncRNAs   |Collects sequence, structure, function and phenotype information of experimentally validated lncRNAs|https://www.sdklab-biophysics-dzu.net/EVLncRNAs2/|
|starBase (ENCORI)|Records lncRNA-miRNA, miRNA-mRNA, ncRNA-RNA interactions information|  https://starbase.sysu.edu.cn/|
|NPInter     |Documents the regulatory interactions between ncRNAs and other biomolecules| http://bigdata.ibp.ac.cn/npinter4/|
|LncRNA2target| Collects experimentally supported lncRNA and target relationships|http://www.bio-annotation.cn/lncrna2target/index.jsp|
|LncACTdb| Records ceRNA interactions and comprehensive annotations | http://bio-bigdata.hrbmu.edu.cn/LncACTdb/|
|LNCipedia| A public database of lncRNA sequences and annotations | https://lncipedia.org|
|lncRNAWiki| Integrates lncRNA sequence and annotation information from three data sources, including GENCODE, NONCODE and LNCippedia | http://lncrna.big.ac.cn|
|lncRNome| Provides experimental and prediction datasets of RNA-protein interactions for lncRNAs | http://genome.igib.res.in/lncRNome|
|LncExpDB| A comprehensive database for human lncRNA expression | https://ngdc.cncb.ac.cn/lncexpdb|
|RAID| Provides RNA-associated crosstalk, including RNA-RNA and RNA-protein interactions,| https://www.rna-society.org/raid2|

### Disease-related data resources
| Database  | Description  | URL | 
|:------------------:|:-----:|:---------------: |
|Disease Ontology   | The DO semantically integrates disease and medical vocabularies  | https://disease-ontology.org/ |
|HPO     |A comprehensive logical standard for describing and computationally analyzing phenotypic abnormalities found in human diseases |https://hpo.jax.org/app/ |
|OMIM  |Describes genes with known sequence and phenotypes   |http://www.ncbi.nlm.nih.gov/omim  |
|DisGeNet   |Collects 30,170 diseases, 21,671 genes and 1124,942 associations|https://www.disgenet.org/|
|HMDD (ENCORI)|Records 893 diseases, 1,206 miRNAs and 35,547 associations in human|  http://www.cuilab.cn/hmdd|


## Machine learning-based methods
### Regularized Least Square
1. **[LRLSLDA]** Chen X, Yan G-Y. Novel human lncRNA–disease association inference based on lncRNA expression profiles, Bioinformatics 2013;29(20):2617-2624. [**[Download]**](https://academic.oup.com/bioinformatics/article/29/20/2617/276977?login=true "Click") 

2. **[LNCSIM]** Chen X, Clarence Yan C, Luo C et al. Constructing lncRNA functional similarity network based on lncRNA-disease associations and disease semantic similarity, Scientific Reports 2015;5(1):11338. [**[Download]**](https://www.nature.com/articles/srep11338 "Click") 

### Support Vector Machine
1. **[LDAP]** Lan W, Li M, Zhao K et al. LDAP: a web server for lncRNA-disease association prediction, Bioinformatics 2016;33(3):458-460. [**[Download]**](https://academic.oup.com/bioinformatics/article/33/3/458/2593899?login=true "Click")

2. **[ILDMSF]** Chen Q, Lai D, Lan W et al. ILDMSF: Inferring Associations Between Long Non-Coding RNA and Disease Based on Multi-Similarity Fusion, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(3):1106-1112. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/8807138 "Click") 

### Random Forest
1. **[RFLDA]** Yao D, Zhan X, Zhan X et al. A random forest based computational model for predicting novel lncRNA-disease associations, BMC Bioinformatics 2020;21(1):126. [**[Download]**](https://link.springer.com/article/10.1186/s12859-020-3458-1 "Click") [**[Code]**](https://github.com/ydkvictory/RFLDA "Click") 

2. **[IPCARF]** Zhu R, Wang Y, Liu J-X et al. IPCARF: improving lncRNA-disease association prediction using incremental principal component analysis feature selection and a random forest classifier, BMC Bioinformatics 2021;22(1):175. [**[Download]**](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-021-04104-9 "Click")  [**[Code]**](https://github.com/zhurong1942/IPCARF_zr1 "Click") 

### Naive Bayesian
1. **[CFNBC]** Yu J, Xuan Z, Feng X et al. A novel collaborative filtering model for LncRNA-disease association prediction based on the Naïve Bayesian classifier, BMC Bioinformatics 2019;20(1):396. [**[Download]**](https://link.springer.com/article/10.1186/s12859-019-2985-0 "Click") [**[Code]**](https://github.com/jingwenyu18/CFNBC "Click") 

2. **[NBCLDA]** Yu J, Ping P, Wang L et al. A Novel Probability Model for LncRNA–Disease Association Prediction Based on the Naïve Bayesian Classifier, Genes 2018;9(7). [**[Download]**](https://www.mdpi.com/2073-4425/9/7/345 "Click") 

## Network propagation-based methods
### Random walk
1. **[RWRlncD]** Sun J, Shi H, Wang Z et al. Inferring novel lncRNA–disease associations based on a random walk model of a lncRNA functional similarity network, Molecular Biosystems 2014;10(8):2074-2081. [**[Download]**](https://pubs.rsc.org/en/content/articlelanding/2014/mb/c3mb70608g/unauth "Click") 

2. **[RWRHLD]** Zhou M, Wang X, Li J et al. Prioritizing candidate disease-related long non-coding RNAs by walking on the heterogeneous lncRNA and disease network, Molecular Biosystems 2015;11(3):760-769. [**[Download]**](https://pubs.rsc.org/en/content/articlelanding/2015/mb/c4mb00511b/unauth "Click") 

3. **[IRWRLDA]** Chen X, You Z-H, Yan G-Y et al. IRWRLDA: improved random walk with restart for lncRNA-disease association prediction, Oncotarget 2016;7(36):57919-57931. [**[Download]**](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5295400/ "Click") 

4. **[GrwLDA]** Gu C, Liao B, Li X et al. Global network random walk for predicting potential human lncRNA-disease associations, Scientific Reports 2017;7(1):12442. [**[Download]**](https://www.nature.com/articles/s41598-017-12763-z "Click") 

5. **[BRWLDA]** Yu G, Fu G, Lu C et al. BRWLDA: bi-random walks for predicting lncRNA-disease associations, Oncotarget 2017;8(36):60429-60446. [**[Download]**](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5601150/ "Click") 

6. **[BiWalkLDA]** Hu J, Gao Y, Li J et al. A novel algorithm based on bi-random walks to identify disease-related lncRNAs, BMC Bioinformatics 2019;20(18):569. [**[Download]**](https://link.springer.com/article/10.1186/s12859-019-3128-3 "Click") [**[Code]**](https://github.com/jhu99/BiwalkLDA "Click") 

7. **[LDA-LNSUBRW]** Xie G, Jiang J, Sun Y. LDA-LNSUBRW: lncRNA-disease association prediction based on linear neighborhood similarity and unbalanced bi-random walk, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2020:1-1. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9184233 "Click") [**[Code]**](https://github.com/JIAWEI1234/LDA-LNSUBRW "Click") 

8. **[HAUBRW]** Xie G, Wu C, Gu G et al. HAUBRW: Hybrid algorithm and unbalanced bi-random walk for predicting lncRNA-disease associations, Genomics 2020;112(6):4777-4787. [**[Download]**](https://www.sciencedirect.com/science/article/pii/S0888754320309101 "Click") 

9. **[LION]** Sumathipala M, Maiorino E, Weiss ST et al. Network Diffusion Approach to Predict LncRNA Disease Associations Using Multi-Type Biological Networks: LION, Frontiers in Physiology 2019;10. [**[Download]**](https://www.frontiersin.org/articles/10.3389/fphys.2019.00888/full "Click") 

10. **[MHRWR]** Zhao X, Yang Y, Yin M. MHRWR: Prediction of lncRNA-Disease Associations Based on Multiple Heterogeneous Networks, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(6):2577-2585. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9001212 "Click") [**[Code]**](https://github.com/yangyq505/MHRWR "Click")

11. **[IDHI-MIRW]** Fan X-N, Zhang S-W, Zhang S-Y et al. Prediction of lncRNA-disease associations by integrating diverse heterogeneous information sources with RWR algorithm and positive pointwise mutual information, BMC Bioinformatics 2019;20(1):87. [**[Download]**](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-019-2675-y "Click") [**[Code]**](https://github.com/NWPU-903PR/IDHI-MIRW "Click") 

12.**[LRWRHLDA]** Wang L, Shang M, Dai Q et al. Prediction of lncRNA-disease association based on a Laplace normalized random walk with restart algorithm on heterogeneous networks, BMC Bioinformatics 2022;23(1):5. [**[Download]**](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-021-04538-1 "Click") [**[Code]**](https://github.com/wang-124/LRWRHLDA "Click")

13. **[IIRWR]** Wang L, Xiao Y, Li J et al. IIRWR: Internal Inclined Random Walk With Restart for LncRNA-Disease Association Prediction, IEEE Access 2019;7:54034-54041. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/8698839 "Click") 

14. **[LRWHLDA]** Li J, Zhao H, Xuan Z et al. A Novel Approach for Potential Human LncRNA-Disease Association Prediction Based on Local Random Walk, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(3):1049-1059. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/8798690 "Click") 

### Flow propagation and label propagation
1. **[LncRDNetFlow]** Zhang J, Zhang Z, Chen Z et al. Integrating Multiple Heterogeneous Networks for Novel LncRNA-Disease Association Inference, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2019;16(2):396-406. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/7919243 "Click") 

2. **[LLCLPLDA]** Xie G, Huang S, Luo Y et al. LLCLPLDA: a novel model for predicting lncRNA–disease associations, Molecular Genetics and Genomics 2019;294(6):1477-1486. [**[Download]**](https://link.springer.com/article/10.1007/s00438-019-01590-8 "Click") 

### Network inference
1. **[Ping et al]** Ping P, Wang L, Kuang L et al. A Novel Method for LncRNA-Disease Association Prediction Based on an lncRNA-Disease Association Network, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2019;16(2):688-693. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/8338419 "Click") 

### Other network propagation algorithms
1. **[Yang et al]** Yang X, Gao L, Guo X et al. A Network Based Method for Analysis of lncRNA-Disease Associations and Prediction of lncRNAs Implicated in Diseases, PLOS ONE 2014;9(1):e87797. [**[Download]**](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0087797 "Click") 

2. **[TPGLDA]** Ding L, Wang M, Sun D et al. TPGLDA: Novel prediction of associations between lncRNAs and diseases via lncRNA-disease-gene tripartite graph, Scientific Reports 2018;8(1):1065. [**[Download]**](https://www.nature.com/articles/s41598-018-19357-3 "Click") [**[Code]**](https://github.com/USTC-HIlab/TPGLDA "Click") 

3. **[IDLDA]** Wang Q, Yan G. IDLDA: An Improved Diffusion Model for Predicting LncRNA–Disease Associations, Frontiers in genetics 2019;10. [**[Download]**](https://www.frontiersin.org/articles/10.3389/fgene.2019.01259/full "Click") 

4. **[NCPLDA]** Li G, Luo J, Liang C et al. Prediction of LncRNA-Disease Associations Based on Network Consistency Projection, IEEE Access 2019;7:58849-58856. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/8705296 "Click") [**[Code]**](https://github.com/ghli16/NCPLDA "Click") 

5. **[LDAI-ISPS]** Zhang Y, Chen M, Li A et al. LDAI-ISPS: LncRNA–Disease Associations Inference Based on Integrated Space Projection Scores, International journal of molecular sciences 2020;21(4). [**[Download]**](https://www.mdpi.com/1422-0067/21/4/1508 "Click") 

6. **[LDAH2V]** Deng L, Li W, Zhang J. LDAH2V: Exploring Meta-Paths Across Multiple Networks for lncRNA-Disease Association Prediction, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(4):1572-1581. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/8897023 "Click") 

7. **[SVDNVLDA]** Li J, Li J, Kong M et al. SVDNVLDA: predicting lncRNA-disease associations by Singular Value Decomposition and node2vec, BMC Bioinformatics 2021;22(1):538. [**[Download]**](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-021-04457-1 "Click") [**[Code]**](https://github.com/iALKing/SVDNVLDA "Click") 

## Matrix factorization- and completion-based methods
### Matrix factorization
1. **[MFLDA]** Fu G, Wang J, Domeniconi C et al. Matrix factorization-based data fusion for the prediction of lncRNA–disease associations, Bioinformatics 2017;34(9):1529-1537. [**[Download]**](https://academic.oup.com/bioinformatics/article/34/9/1529/4708235?login=true "Click")  [**[Code]**](http://www.sdu-idea.cn/codes.php?name=MFLDA "Click") 

2. **[WMFLDA]** Wang Y, Yu G, Wang J et al. Weighted matrix factorization on multi-relational data for LncRNA-disease association prediction, Methods 2020;173:32-43. [**[Download]**](https://www.sciencedirect.com/science/article/abs/pii/S1046202319300386 "Click")  [**[Code]**](http://mlda.swu.edu.cn/codes.php?name=WMFLDA "Click") 

3. **[DNILMF-LDA ]** Li Y, Li J, Bian N. DNILMF-LDA: Prediction of lncRNA-Disease Associations by Dual-Network Integrated Logistic Matrix Factorization and Bayesian Optimization, Genes 2019;10(8). [**[Download]**](https://www.mdpi.com/2073-4425/10/8/608 "Click") 

4. **[PMFILDA]** Xuan Z, Li J, Yu J et al. A Probabilistic Matrix Factorization Method for Identifying lncRNA-Disease Associations, Genes 2019;10(2). [**[Download]**](https://www.mdpi.com/2073-4425/10/2/126 "Click") 

5. **[WGRCMF]** Liu JX, Cui Z, Gao YL et al. WGRCMF: A Weighted Graph Regularized Collaborative Matrix Factorization Method for Predicting Novel LncRNA-Disease Associations, IEEE Journal of Biomedical and Health Informatics 2021;25(1):257-265. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9063536 "Click") 

6. **[LDGRNMF]** Wang M-N, You Z-H, Wang L et al. LDGRNMF: LncRNA-disease associations prediction based on graph regularized non-negative matrix factorization, Neurocomputing 2021;424:236-245. [**[Download]**](https://www.sciencedirect.com/science/article/abs/pii/S0925231220302526 "Click") 

### Matrix completion
1. **[SIMCLDA]** Lu C, Yang M, Luo F et al. Prediction of lncRNA–disease associations based on inductive matrix completion, Bioinformatics 2018;34(19):3357-3364. [**[Download]**](https://academic.oup.com/bioinformatics/article/34/19/3357/4987142?login=true "Click") [**[Code]**](https://github.com//bioinfomaticsCSU/SIMCLDA "Click") 

2. **[GMCLDA]** Lu C, Yang M, Li M et al. Predicting Human lncRNA-Disease Associations Based on Geometric Matrix Completion, IEEE Journal of Biomedical and Health Informatics 2020;24(8):2420-2429.  [**[Download]**](https://ieeexplore.ieee.org/abstract/document/8928551 "Click") [**[Code]**](https://github.com/bioinfomaticsCSU/GMCLDA "Click") 

## Deep learning-based methods
### Full connected neural network
1. **[NNLDA]** Hu J, Gao Y, Li J et al. Deep Learning Enables Accurate Prediction of Interplay Between lncRNA and Disease, Frontiers in genetics 2019;10. [**[Download]**](https://www.frontiersin.org/articles/10.3389/fgene.2019.00937/full "Click") [**[Code]**](https://github.com/gao793583308/NNLDA "Click") 

2. **[DMFLDA]** Zeng M, Lu C, Fei Z et al. DMFLDA: A Deep Learning Framework for Predicting lncRNA–Disease Associations, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(6):2353-2363. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9054949 "Click") [**[Code]**](https://github.com/CSUBioGroup/DMFLDA "Click")

3. **[SDLDA]** Zeng M, Lu C, Zhang F et al. SDLDA: lncRNA-disease association prediction based on singular value decomposition and deep learning, Methods 2020;179:73-80. [**[Download]**](https://www.sciencedirect.com/science/article/abs/pii/S1046202320300013 "Click") [**[Code]**](https://github.com/CSUBioGroup/SDLDA "Click") 

### Convolutional neural network
1. **[CNNLDA]** Xuan P, Cao Y, Zhang T et al. Dual Convolutional Neural Networks With Attention Mechanisms Based Method for Predicting Disease-Related lncRNA Genes, Frontiers in genetics 2019;10. [**[Download]**](https://www.frontiersin.org/articles/10.3389/fgene.2019.00416/full "Click") 

2. **[LDApred]** Xuan P, Jia L, Zhang T et al. LDAPred: A Method Based on Information Flow Propagation and a Convolutional Neural Network for the Prediction of Disease-Associated lncRNAs, International journal of molecular sciences 2019;20(18). [**[Download]**](https://www.mdpi.com/1422-0067/20/18/4458 "Click") 

3. **[iLncRNAdis-FB]** Wei H, Liao Q, Liu B. iLncRNAdis-FB: Identify lncRNA-Disease Associations by Fusing Biological Feature Blocks Through Deep Neural Network, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021;18(5):1946-1957. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/8950120 "Click") 

4. **[MCA-Net]** Zhang Y, Ye F, Gao X. MCA-Net: Multi-feature coding and attention convolutional neural network for predicting lncRNA-disease association, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021:1-1. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9492012 "Click") 

### Autoencoder
1. **[CNNDLP]** Xuan P, Sheng N, Zhang T et al. CNNDLP: A Method Based on Convolutional Autoencoder and Convolutional Neural Network with Adjacent Edge Attention for Predicting lncRNA–Disease Associations, International journal of molecular sciences 2019;20(17). [**[Download]**](https://www.mdpi.com/1422-0067/20/17/4260 "Click") 

2. **[LDNFSGB]** Zhang Y, Ye F, Xiong D et al. LDNFSGB: prediction of long non-coding rna and disease association using network feature similarity and gradient boosting, BMC Bioinformatics 2020;21(1):377. [**[Download]**](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-03721-0 "Click") [**[Code]**](https://github.com/MLMIP/LDNFSGB "Click") 

3. **[LDASR]** Guo Z-H, You Z-H, Wang Y-B et al. A Learning-Based Method for LncRNA-Disease Association Identification Combing Similarity Information and Rotation Forest, iScience 2019;19:786-795. [**[Download]**](https://www.sciencedirect.com/science/article/pii/S2589004219303086 "Click") 

4. **[MAN]** Su X, You Z, Yi H. Prediction of LncRNA-Disease Associations Based on Network Representation Learning. In: 2020 IEEE International Conference on Bioinformatics and Biomedicine (BIBM). 2020, p.1805-1812. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9313139 "Click") 

5. **[VADLP]** Sheng N, Cui H, Zhang T et al. Attentional multi-level representation encoding based on convolutional and variance autoencoders for lncRNA–disease association prediction, Briefings in Bioinformatics 2020;22(3). [**[Download]**](https://academic.oup.com/bib/article-abstract/22/3/bbaa067/5841901?login=false "Click") 

### Generative adversarial network
1. **[BiGAN]** Yang Q, Li X. BiGAN: LncRNA-disease association prediction based on bidirectional generative adversarial network, BMC Bioinformatics 2021;22(1):357. [**[Download]**](https://link.springer.com/article/10.1186/s12859-021-04273-7 "Click") [**[Code]**](https://github.com/TomasYang001/BiGAN-lncRNA-disease-associations-prediction "Click")

## Graph neural network-based methods
### Graph feature extraction
1. **[GCNLDA]** Xuan P, Pan S, Zhang T et al. Graph Convolutional Network and Convolutional Neural Network Based Method for Predicting lncRNA-Disease Associations, Cells 2019;8(9). [**[Download]**](https://www.mdpi.com/2073-4409/8/9/1012 "Click") 

2. **[GAERF]** Wu Q-W, Xia J-F, Ni J-C et al. GAERF: predicting lncRNA-disease associations by graph auto-encoder and random forest, Briefings in Bioinformatics 2021;22(5). [**[Download]**](https://academic.oup.com/bib/article-abstract/22/5/bbaa391/6067881 "Click") 


3. **[MLGCNET]** Wu QW, Cao RF, Xia J et al. Extra Trees Method for Predicting LncRNA-Disease Association Based on Multi-layer Graph Embedding Aggregation, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021:1-1. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9540266 "Click") [**[Code]**](https://github.com/QingwWu/MLGCNET "Click")

4. **[MGATE]** Sheng N, Huang L, Wang Y et al. Sheng N, Huang L, Wang Y et al. Multi-channel graph attention autoencoders for disease-related lncRNAs prediction, Briefings in Bioinformatics 2022;23(2). [**[Download]**](https://academic.oup.com/bib/article-abstract/23/2/bbab604/6519791 "Click") [**[Code]**](https://github.com/sheng-n/MGATE "Click")

5. **[GANLDA]** Lan W, Wu X, Chen Q et al. GANLDA: Graph attention network for lncRNA-disease associations prediction, Neurocomputing 2022;469:384-393. [**[Download]**](https://www.sciencedirect.com/science/article/abs/pii/S0925231221011012 "Click") 

6. **[GTAN]** Xuan P, Zhan L, Cui H et al. Graph Triple-Attention Network for Disease-related LncRNA Prediction, IEEE Journal of Biomedical and Health Informatics 2021:1-1. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9625721 "Click") 

7. **[PANDA]** Silva ABOV, Spinosa EJ. Graph Convolutional Auto-Encoders for predicting novel lncRNA-Disease associations, IEEE/ACM Transactions on Computational Biology and Bioinformatics 2021:1-1. [**[Download]**](https://ieeexplore.ieee.org/abstract/document/9395216 "Click") 


### Graph matrix completion
1. **[GAMCLDA]** Wu X, Lan W, Chen Q et al. Inferring LncRNA-disease associations based on graph autoencoder matrix completion, Computational Biology and Chemistry 2020;87:107282. [**[Download]**](https://www.sciencedirect.com/science/article/abs/pii/S1476927119310114 "Click") 

2. **[GCRFLDA]** Fan Y, Chen M, Pan X. GCRFLDA: scoring lncRNA-disease associations using graph convolution matrix completion with conditional random field, Briefings in Bioinformatics 2021;23(1). [**[Download]**](https://academic.oup.com/bib/article-abstract/23/1/bbab361/6363052?login=false "Click") [**[Code]**](https://github.com/jademyC1221/GCRFLDA "Click")

3. **[HGATLDA]** Zhao X, Zhao X, Yin M. Heterogeneous graph attention network based on meta-paths for lncRNA–disease association prediction, Briefings in Bioinformatics 2021;23(1). [**[Download]**](https://academic.oup.com/bib/article-abstract/23/1/bbab407/6377515?login=false "Click") 

4. **[VGAELDA]** Shi Z, Zhang H, Jin C et al. A representation learning model based on variational inference and graph autoencoder for predicting lncRNA-disease associations, BMC Bioinformatics 2021;22(1):136. [**[Download]**](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-021-04073-z "Click") [**[Code]**](https://github.com/zhanglabNKU/VGAELDA "Click")


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
```
@article{SN_LDA,
  title={Data resources and computational methods for lncRNA-disease association prediction},
  author={Nan Sheng, Lan Huang, Yuting Lu, Hao Wang, Lili Yang, Ling Gao, Xuping Xie, Yuan Fu, Yan Wang},
  journal={Computers in Biology and Medicine},
  year={2023},
  publisher={Elsevier}
}
## cite
Sheng N, Huang L, Lu Y et al. Data resources and computational methods for lncRNA-disease association prediction, Computers in Biology and Medicine 2023:106527.
```
If you would like to help contribute this list, please feel free to contact me by email:

* Email: shengnan21@mails.jlu.edu.cn
