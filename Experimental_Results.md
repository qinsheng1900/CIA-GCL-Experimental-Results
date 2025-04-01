# CIA-GCL-Experimental-Results
## 1.T-test results

**Table 1: T-test results on three datasets compared with baselines**.**Note:** Significance levels(Sig. level) are indicated as follows: p < 0.05 (\*), *p* < 0.01 (\*\*), *p* < 0.001 (\*\*\*), *p* ≥ 0.05 (n.s., not significant). Although our performance on a single dataset is close to that of some other methods, **the overall performance** on the three datasets **is statistically significantly different from** that of other comparison methods.

|   Dataset   |  ABIDE1  |            |  ABIDE2  |            |  ADHD200 |            |   ALL    |            |
| :---------: | :------: | :--------: | :------: | :--------: | :------: | :--------: | :------: | :--------: |
|   Method    | p-value  | Sig. level | p-value  | Sig. level | p-value  | Sig. level | p-value  | Sig. level |
|     RF      | 2.00E-08 |    ***     | 9.40E-05 |    ***     | 1.70E-03 |    ***     | 1.80E-07 |    ***     |
|     SVM     | 1.10E-04 |    ***     | 4.30E-05 |    ***     | 4.00E-03 |     **     | 6.20E-07 |    ***     |
| BrainNetCNN | 2.40E-07 |    ***     | 3.40E-04 |    ***     | 3.90E-02 |     *      | 2.90E-06 |    ***     |
|  BNC-DGHL   | 2.50E-02 |     *      | 3.30E-02 |     *      | 6.80E-02 |    n.s.    | 3.30E-03 |     **     |
|    GATE     | 2.40E-03 |     **     | 9.30E-02 |    n.s.    | 6.60E-03 |     **     | 1.50E-03 |    ***     |
|  BrainUSL   | 2.40E-05 |    ***     | 1.60E-03 |    ***     | 1.30E-02 |     *      | 9.00E-08 |    ***     |
|   BrainGB   | 3.80E-04 |    ***     | 3.40E-02 |     *      | 7.50E-03 |     **     | 2.20E-04 |    ***     |
|    DHML     | 1.40E-01 |    n.s.    | 9.80E-05 |    ***     | 5.70E-02 |    n.s.    | 6.80E-04 |    ***     |


## 2.New comparative experiment

**Table 2: Comparative experiments of other methods of ABIDE 1 and AAL atlas** (a)self-supervised method (METAFormer 2023) (Self-supervised method based on masked autoencoder);(b)two approaches targeting OOD generalization (CIGA 2022，BrainIB 2024); (c)two methods for fMRI analysis (BrainNetTF 2022，BolT 2023);(d)two contrastive learning-based models (A-GCL 2023，Contrasformer 2024)

|  Dataset  |               Method               |  Accuracy  | Precision  |  Recall   | F1-score  |   bAcc   |   AUC    |   Avg    |
|:---------:|:----------------------------------:|:----------:|:----------:|:---------:|:---------:|:--------:|:--------:|:--------:|
| ABIDE I |  METAFormer (2023)[1]   | 70.31±2.86 | 71.80±3.20 | 74.38±6.64 | 72.85±3.29 | 69.91±2.80 | 72.29±3.54 | 71.18±2.91 |
|         |     CIGA（2022）[2]      | 66.96±1.64 | 69.55±2.42 | 57.84±6.20 | 62.92±3.43 | 66.75±1.69 | 67.53±2.81 | 65.26±4.22 |
|         |    BrainIB（2024）[3]    | 69.97±2.82 | 71.07±4.19 | 70.70±4.61 | 70.74±2.90 | 69.63±3.15 | 73.44±4.35 | 70.92±1.34 |
|         |  BrainNetTF（2022）[4]   | 70.66±4.93 | 70.79±6.07 | 69.35±7.4  | 69.71±5.07 | 70.64±4.37 | 70.68±5.58 | 70.30±0.61 |
|         |     BoIT（2023）[5]     | 69.43±2.93 | 69.16±3.22 | 72.78±4.79 | 70.83±3.00 | 69.34±2.93 | 72.58±2.79 | 70.68±1.64 |
|         |    A-GCL（2023） [6]   | 72.19±2.05 | 70.76±3.98 | 73.52±2.83 | 73.00±3.77 | 70.14±2.80 | 75.46±3.05 | 72.51±1.93 |
|         | Contrasformer（2024）[7] | 68.90±2.33 | 67.68±3.96 | 70.91±6.04 | 68.70±2.74 | 68.86±2.23 | 70.68±2.64 | 69.29±1.24 |


[1] Mahler L, Wang Q, Steiglechner J, et al. Pretraining is all you need: A multi-atlas enhanced transformer framework for autism spectrum disorder classification[C]//International Workshop on Machine Learning in Clinical Neuroimaging. Cham: Springer Nature Switzerland, 2023: 123-132.

[2] Chen Y, Zhang Y, Bian Y, et al. Learning causally invariant representations for out-of-distribution generalization on graphs[J]. Advances in Neural Information Processing Systems, 2022, 35: 22131-22148.

[3] Zheng K, Yu S, Li B, et al. Brainib: Interpretable brain network-based psychiatric diagnosis with graph information bottleneck[J]. IEEE Transactions on Neural Networks and Learning Systems, 2024.

[4] Kan X, Dai W, Cui H, et al. Brain network transformer[J]. Advances in Neural Information Processing Systems, 2022, 35: 25586-25599.

[5] Bedel H A, Sivgin I, Dalmaz O, et al. BolT: Fused window transformers for fMRI time series analysis[J]. Medical image analysis, 2023, 88: 102841.

[6] Zhang S, Chen X, Shen X, et al. A-GCL: Adversarial graph contrastive learning for fMRI analysis to diagnose neurodevelopmental disorders[J]. Medical Image Analysis, 2023, 90: 102932.

[7] Xu J, He K, Lan M, et al. Contrasformer: a brain network contrastive transformer for neurodegenerative condition identification[C]//Proceedings of the 33rd ACM International Conference on Information and Knowledge Management. 2024: 2671-2681.

**Figure 1: Comparative experiments of all methods of ABIDE 1 and AAL atlas**

![image](https://github.com/qinsheng1900/CIA-GCL-Experimental-Results/blob/main/Visualization%20of%20all%20methods.png)

## 3.Summary of Notations
**Table 4: Notations and their descriptions**

|               Symbol               |                            Meaning                           |
| :--------------------------------: |:------------------------------------------------------------:|
| $\mathcal{G}$                      | Brain graph data set                                         |
| $\mathcal{E}，\acute{\mathcal{E}}$ | Environment set                                              |
| $V$                                | The set of nodes in the graph                                |
| $E$                                | The set of edges in the graph                                |
| $G,G^{ori}$                        | Original brain graph data                                    |
| $G^c,G^{inv}$                      | Invariant subgraph                                           |
| $G^s,G^{ms}$                       | Spurious subgraph，mixed spurious subgraph                   |
| $G^a,G^{a_1},G^{a_2}$              | Brain Augmented graph                                        |
| $n$                                | Number of brain regions                                      |
| $d$                                | Node feature dimensions in brain graph                       |
| $p,q$                              | The probability of an edge being selected                    |
| **$\mathcal{M}$**                  | Brain graph mask                                             |
| $k$                                | The k-th subject                                             |
| $\boldsymbol{z}$                   | Graph-level features                                         |
| $A$                                | Adjacency matrix of a graph                                  |
| $\boldsymbol{e}$                   | Environment                                                  |
| $e$                                | An edge in the graph                                         |
| $r,\lambda$                        | Maximum edge ratio to select，Hyperparameters in loss functions |
| $I(,)$                             | Invariant subgraph extractor                                 |
| $\Phi(\cdot)$                      | Trade-off hyper-parameters                                   |
| $g(\cdot)$                         | Graph Encoder                                                |
| $w(\cdot)$                         | Predictor                                                    |
