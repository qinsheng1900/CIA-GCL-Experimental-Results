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

**Table 2: Comparative experiments of other methods of ABIDE 1 on AAL atlas under Table1's setting** (a)self-supervised method (METAFormer 2023) (Self-supervised method based on masked autoencoder);(b)two approaches targeting OOD generalization (CIGA 2022，BrainIB 2024); (c)two methods for fMRI analysis (BrainNetTF 2022，BolT 2023);(d)two contrastive learning-based models (A-GCL 2023，Contrasformer 2024)

| Dataset | Method           | Accuracy (\%)          | Precision (\%)         | Recall (\%)            | F1-score (\%)          | bAcc (\%)              | AUC (\%)               | Avg (\%)                |
|:-------:|:----------------:|:----------------------:|:----------------------:|:----------------------:|:----------------------:|:----------------------:|:----------------------:|:-----------------------:|
| ABIDE I | RF               | 62.02±4.72             | 63.28±5.33             | 63.02±3.79             | 63.01±3.53             | 62.00±4.81             | 66.60±5.96             | 62.79±0.48              |
|         | SVM              | 65.12±2.93             | 65.49±4.15             | 60.81±5.01             | 62.93±3.44             | 65.03±2.93             | 70.83±4.79             | 62.67±6.75              |
|         | BrainNetCNN      | 68.88±3.23             | 70.21±5.29             | 71.13±13.8             | 69.48±5.37             | 68.85±3.22             | 72.39±4.09             | 70.16±1.39              |
|         | BNC-DGHL         | 70.5±3.30              | 70.48±4.13             | \underline{76.32±3.29} | 73.27±2.52             | 70.40±3.09             | 73.99±3.46             | 72.49±2.44              |
|         | GATE             | 71.67±2.95             | 71.93±4.92             | 74.68±6.08             | 72.99±2.55             | 71.42±3.03             | 73.04±4.62             | 72.62±1.21              |
|         | Com-BrainTF      | 70.14±4.38             | 70.28±4.32             | 72.83±4.15             | 70.01±4.49             | 70.00±4.65             | 71.67±6.16             | 70.82±1.17              |
|         | BrainGB          | 71.07±4.92             | \underline{72.79±8.02} | 72.90±6.20             | 70.80±4.47             | 70.93 ±4.79            | \underline{74.93±5.10} | 72.24±1.62              |
|         | DHML             | 71.52±2.93             | 71.19±3.23             | \textbf{77.14±3.23}    | \underline{73.92±2.43} | 71.27±3.38             | 74.72±3.34             | \underline{73.29±2.40}  |
|         | CI-GNN           | \underline{71.89±2.91} | 70.49±2.98             | 73.37±4.80             | 70.58±2.21             | \underline{71.44±2.75} | 73.32±3.62             | 71.85±1.27              |
|         | METAFormer[1]    | 70.31±2.86             | 71.80±3.20             | 74.38±6.64             | 72.85±3.29             | 69.91±2.80             | 72.29±3.54             | 71.18±2.91              |
|         | CIGA[2]          | 66.96±1.64             | 69.55±2.42             | 57.84±6.20             | 62.92±3.43             | 66.75±1.69             | 67.53±2.81             | 65.26±4.22              |
|         | BrainIB[3]       | 69.97±2.82             | 71.07±4.19             | 70.70±4.61             | 70.74±2.90             | 69.63±3.15             | 73.44±4.35             | 70.92±1.34              |
|         | BrainNetTF[4]    | 70.66±4.93             | 70.79±6.07             | 69.35±7.4              | 69.71±5.07             | 70.64±4.37             | 70.68±5.58             | 70.30±0.61              |
|         | BoIT[5]          | 69.43±2.93             | 69.16±3.22             | 72.78±4.79             | 70.83±3.00             | 69.34±2.93             | 72.58±2.79             | 70.68±1.64              |
|         | Contrasformer[6] | 68.9±2.33              | 67.68±3.96             | 70.91±6.04             | 68.70±2.74             | 68.86±2.23             | 70.68±2.64             | 69.29±1.24              |
|         | \textbf{CIA-GCL} | \textbf{73.42±2.75}    | \textbf{73.82±3.23}    | 74.91±5.63             | \textbf{74.21±3.03}    | \textbf{73.38±2.76}    | \textbf{76.28±3.74}    | \textbf{74.34±1.10}     |
| ABIDE II | RF                                     | 62.56±2.67             | 62.71±4.29             | 48.87±2.97             | 54.83±2.55             | 61.68±2.56                               | 66.60±5.96                               | 59.54±6.47                                |
|          | SVM                                    | 64.78±3.75             | 63.79±5.3              | 56.53±6.83             | 59.75±4.9              | 64.25±3.88                               | 69.13±3.62                               | 63.04±4.36                                |
|          | BrainNetCNN                            | 67.75±2.72             | 69.74±5.70             | 56.92±9.87             | 61.87±5.57             | 67.21±2.72                               | 69.59±3.89                               | 65.51±5.08                                |
|          | BNC-DGHL                               | 68.53±3.73             | 68.53±3.73             | 66.31±4.73             | 66.46±5.35             | 70.15±6.31                               | 68.39±3.67                               | 68.09±1.50                                |
|          | GATE                                   | 69.51±2.76             | \underline{71.21±2.97} | 65.64±6.88             | 68.83±2.94             | \underline{70.33±5.25}                   | 70.87±4.55                               | 69.37±2.02                                |
|          | Com-BrainTF                            | 68.91±2.29             | 69.12±1.95             | 62.92±9.42             | 68.34±2.87             | 68.80±6.50                               | 70.40±4.72                               | 68.08±2.62                                |
|          | BrainGB                                | 69.23±3.33             | 67.37±4.61             | 65.97±6.45             | 66.34±3.89             | 69.01±3.28                               | 71.33±4.12                               | 68.21±2.03                                |
|          | DHML                                   | 69.22±3.19             | 69.37±5.16             | 63.39±11.13            | 65.45±5.27             | 68.82±3,17                               | 69.48±3.43                               | 67.62±2.57                                |
|          | CI-GNN                                 | \underline{70.04±2.62} | 70.22±3.59             | \underline{69.56±5.28} | 68.85±3.60             | 69.93±3.39                               | 69.13±4.82                               | 69.62±0.54                                |
|          | METAFormer[1]                          | 69.10±3.17             | 68.34±3.91             | 64.00±7.66             | 65.89±4.41             | 69.04±3.21                               | 70.88±4.36                               | 67.88±2.49                                |
|          | CIGA[2]                                | 66.40±3.22             | 63.01±3.16             | 68.32±13.39            | 64.85±7.92             | 66.54±3.72                               | 66.63±3.94                               | 65.53±2.81                                |
|          | BrainIB[3]                             | 68.92±3.60             | 66.73±6.70             | 68.13±10.74            | 66.65±4.19             | 68.58±3.22                               | 69.83±4.61                               | 68.29±1.96                                |
|          | BrainNetTF[4]                          | 66.62±4.17             | 68.70±7.05             | 65.73±13.35            | 65.01±5.77             | 65.30±4.61                               | 67.86±4.92                               | 66.54±1.47                                |
|          | BoIT[5]                                | 69.69±2.22             | 69.83±3.44             | extbf{72.79±4.88}      | \textbf{71.13±2.02」    | 68.45±2.35                               | \underline{71.42±3.32                    | \underline{70.33±1.66                     |
|          | Contrasformer[6]                       | 69.79±2.99             | 67.39±8.16             | 57.86±8.87             | 61.78±6.25             | 67.94±3.50                               | 70.02±3.67                               | 65.78±4.92                                |
|          | \textbf{CIA-GCL} \cellcolor[gray]{0.9} | \textbf{72.09±2.47}    | \textbf{ 72.67±3.49}   | 64.39±9.14             | \underline{68.94±4.74} | \textbf{71.45±2.71}\cellcolor[gray]{0.9} | \textbf{72.58±2.41}\cellcolor[gray]{0.9} | \textbf{70.51±3.25} \cellcolor[gray]{0.9} |
| ADHD200 | RF                                     | 63.88±3.28                               | 54.52±10.37                               | 21.67±9.99              | 30.14±11.37                              | 55.53±4.19                               | 60.72±7.9                                | 47.74±17.46                               |
|         | SVM                                    | 66.48±3.99                               | 62.9±12.19                                | 28.25±7.83              | 38.49±8.51                               | 58.91±4.37                               | 67.58±7.91                               | 53.77±16.41                               |
|         | BrainNetCNN                            | 70.71±4.15                               | 61.69±5.90                                | \underline{59.30±12.29} | 59.90±7.94                               | 68.47±5.21                               | 70.02±6.20                               | 65.01±5.27                                |
|         | BNC-DGHL                               | 70.25±3.88                               | 59.76±4.40                                | extbf{62.37±11.41}      | 60.82±7.54                               | 68.68±5.29                               | 68.39±7.27                               | 65.05±4.57                                |
|         | GATE                                   | 72.02±3.55                               | 71.27±6.09                                | 45.18±17.04             | 52.82±14.87                              | 66.67±6.01                               | 69.31±9.42                               | 62.88±11.17                               |
|         | Com-BrainTF                            | 71.78±4.50                               | 70.38±4.33                                | 56.71±17.17             | 68.28±7.69                               | 68.77±6.89                               | 69.75±6.96                               | \underline{67.61±5.48}                    |
|         | BrainGB                                | 71.91±2.89                               | 71.51±9.69                                | 45.56±9.96              | 54.62±6.65                               | 66.01±3.49                               | 71.63±6.30                               | 63.54±11.02                               |
|         | DHML                                   | \underline{72.87±2.71}                   | 66.34±5.54                                | 57.23±10.12             | 63.02±5.87                               | \underline{69.78±3.82}                   | \underline{72.96±3.91}                   | 67.03±6.15                                |
|         | CI-GNN                                 | 71.03±3.05                               | 61.32±5.08                                | 53.44±10.84             | \underline{66.93±4.26}                   | 67.93±4.26                               | 71.95±2.97                               | 65.43±6.97                                |
|         | METAFormer[1]                          | 70.27±2.54                               | \underline{73.00±7.87}                    | 44.09±10.01             | 54.66±9.45                               | 62.63±4.83                               | 69.13±4.65                               | 62.29±11.09                               |
|         | CIGA[2]                                | 67.73±2.44                               | 61.95±6.04                                | 43.25±17.31             | 48.40±12.75                              | 62.75±4.97                               | 64.01±2.95                               | 58.02±9.79                                |
|         | BrainIB[3]                             | 70.07±1.56                               | 60.69±2.54                                | 56.47±8.48              | 58.10±4.11                               | 67.10±2.15                               | 67.28±2.72                               | 63.29±5.60                                |
|         | BrainNetTF[4]                          | 70.33±3.38                               | 70.89±11.15                               | 38.95±13.78             | 48.33±12.31                              | 64.10±4.92                               | 69.21±7.42                               | 60.3±13.45                                |
|         | BoIT[5]                                | 69.03±2.74                               | 61.13±3.64                                | 54.16±7.94              | 54.66±4.89                               | 66.19±3.30                               | 70.29±4.09                               | 62.58±7.07                                |
|         | Contrasformer[6]                       | 69.03±2.74                               | 61.13±3.64                                | 54.16±7.94              | 54.66±4.89                               | 66.19±3.30                               | 70.29±4.09                               | 62.58±7.07                                |
|         | \textbf{CIA-GCL} \cellcolor[gray]{0.9} | \textbf{75.21±2.57}\cellcolor[gray]{0.9} | \textbf{79.40±10.59}\cellcolor[gray]{0.9} | 58.75±11.73             | \textbf{69.80±8.87}\cellcolor[gray]{0.9} | \textbf{69.93±4.01}\cellcolor[gray]{0.9} | \textbf{73.51±4.01}\cellcolor[gray]{0.9} | \textbf{71.10±7.03 }\cellcolor[gray]{0.9} |


**Table 5: Comparative experiments of other methods of ABIDE I, ABIDE II, ADHD200 on AAL atlas under Table2's setting**
| Dataset | Method           | Accuracy   | Precision  | Recall     | F1-score   | bAcc       | AUC        | Avg         |
|:-------:|:----------------:|:----------:|:----------:|:----------:|:----------:|:----------:|:----------:|:-----------:|
| ABIDE I | METAFormer[1]    | 70.13±3.40 | 69.60±1.56 | 72.26±8.13 | 67.88±4.34 | 69.47±3.78 | 71.13±5.15 | 70.08±1.50  |
|         | CIGA[2]          | 65.51±1.97 | 64.32±4.19 | 63.17±2.06 | 63.65±1.54 | 65.35±1.78 | 66.74±3.40 | 64.79±1.33  |
|         | BrainIB[3]       | 64.92±1.34 | 61.27±1.42 | 66.06±9.45 | 63.89±8.98 | 63.32±2.88 | 61.59±1.17 | 63.51±1.86  |
|         | BrainNetTF[4]    | 66.63±1.56 | 65.98±3.24 | 65.75±5.13 | 68.04±2.86 | 66.83±4.30 | 67.97±1.80 | 66.87±0.96  |
|         | BoIT[5]          | 65.71±1.50 | 65.27±1.42 | 64.26±5.63 | 64.62±2.05 | 65.50±1.01 | 69.08±2.64 | 65.74±1.73  |
|         | Contrasformer[7] | 70.50±2.83 | 73.14±6.80 | 67.19±5.60 | 70.73±4.41 | 70.78±2.95 | 69.54±4.11 | 70.31±1.93  |
|         | CIA-GCL          | 72.03±0.90 | 74.12±3.57 | 69.92±3.31 | 71.86±1.51 | 72.08±1.65 | 74.26±3.43 | 72.38±1.62  |
| ABIDE II | METAFormer    | 66.18±2.33 | 64.32±6.68 | 73.60±11.12 | 67.97±2.23  | 66.48±2.38 | 67.01±0.18 | 67.59±3.17  |
|          | CIGA          | 68.11±3.20 | 71.61±9.12 | 62.60±13.97 | 67.36±10.32 | 66.45±2.81 | 67.72±3.62 | 67.31±2.90  |
|          | BrainIB       | 68.46±3.13 | 72.14±8.44 | 64.89±16.37 | 68.02±12.17 | 65.99±2.01 | 65.6±2.45  | 67.50±2.67  |
|          | BrainNetTF    | 67.59±2.25 | 70.29±7.35 | 64.25±9.21  | 66.93±7.57  | 66.16±2.43 | 66.12±1.97 | 66.87±1.98  |
|          | BoIT          | 66.84±1.47 | 70.10±4.24 | 60.57±8.76  | 64.56±3.72  | 66.71±1.55 | 67.26±2.03 | 66.01±3.18  |
|          | Contrasformer | 69.81±2.05 | 70.18±3,36 | 68.98±10.25 | 69.25±6.43  | 65.47±4.54 | 66.99±0.95 | 68.45±1.82  |
|          | CIA-GCL       | 71.51±2.94 | 70.83±4.63 | 77.87±15.94 | 73.97±9.73  | 66.52±5.24 | 68.81±5.72 | 71.59±3.98  |
| ABIDE II | METAFormer    | 66.18±2.33 | 64.32±6.68 | 73.60±11.12 | 67.97±2.23  | 66.48±2.38 | 67.01±0.18 | 67.59±3.17  |
|          | CIGA          | 68.11±3.20 | 71.61±9.12 | 62.60±13.97 | 67.36±10.32 | 66.45±2.81 | 67.72±3.62 | 67.31±2.90  |
|          | BrainIB       | 68.46±3.13 | 72.14±8.44 | 64.89±16.37 | 68.02±12.17 | 65.99±2.01 | 65.6±2.45  | 67.50±2.67  |
|          | BrainNetTF    | 67.59±2.25 | 70.29±7.35 | 64.25±9.21  | 66.93±7.57  | 66.16±2.43 | 66.12±1.97 | 66.87±1.98  |
|          | BoIT          | 66.84±1.47 | 70.10±4.24 | 60.57±8.76  | 64.56±3.72  | 66.71±1.55 | 67.26±2.03 | 66.01±3.18  |
|          | Contrasformer | 69.81±2.05 | 70.18±3,36 | 68.98±10.25 | 69.25±6.43  | 65.47±4.54 | 66.99±0.95 | 68.45±1.82  |
|          | CIA-GCL       | 71.51±2.94 | 70.83±4.63 | 77.87±15.94 | 73.97±9.73  | 66.52±5.24 | 68.81±5.72 | 71.59±3.98  |


**Table 6: Comparative experiments of other methods of ADHD on AAL atlas under Table2's setting**
| Dataset | Method        | Accuracy   | Precision   | Recall      | F1-score    | bAcc       | AUC        | Avg          |
|:-------:|:-------------:|:----------:|:-----------:|:-----------:|:-----------:|:----------:|:----------:|:------------:|
| ADHD200 | METAFormer    | 67.22±2.01 | 71.16±12.90 | 39.90±0.22  | 43.76±10.57 | 59.21±0.98 | 63.58±3,88 | 57.38±13.02  |
|         | CIGA          | 67.27±1.75 | 69.78±4.47  | 21.24±14.06 | 30.71±17.30 | 57.70±4.55 | 59.60±7.98 | 51.05±20.16  |
|         | BrainIB       | 68.43±1.93 | 58.76±4.27  | 33.44±9.67  | 42.27±9.18  | 60.18±3.80 | 64.03±3.76 | 54.52±13.62  |
|         | BrainNetTF    | 66.85±2.81 | 63.54±3.90  | 37.36±7.44  | 40.03±10.65 | 56.39±5.62 | 63.16±4.08 | 54.56±12.77  |
|         | BoIT          | 66.87±1.39 | 68.28±6.14  | 25.72±3.13  | 37.08±3.40  | 60.81±3.14 | 64.31±3.65 | 53.85±17.93  |
|         | Contrasformer | 68.05±1.35 | 60.37±5.54  | 43.10±16.63 | 48.33±11.32 | 62.75±3.87 | 68.15±4.18 | 58.46±10.45  |


[1] Mahler L, Wang Q, Steiglechner J, et al. Pretraining is all you need: A multi-atlas enhanced transformer framework for autism spectrum disorder classification[C]//International Workshop on Machine Learning in Clinical Neuroimaging. Cham: Springer Nature Switzerland, 2023: 123-132.

[2] Chen Y, Zhang Y, Bian Y, et al. Learning causally invariant representations for out-of-distribution generalization on graphs[J]. Advances in Neural Information Processing Systems, 2022, 35: 22131-22148.

[3] Zheng K, Yu S, Li B, et al. Brainib: Interpretable brain network-based psychiatric diagnosis with graph information bottleneck[J]. IEEE Transactions on Neural Networks and Learning Systems, 2024.

[4] Kan X, Dai W, Cui H, et al. Brain network transformer[J]. Advances in Neural Information Processing Systems, 2022, 35: 25586-25599.

[5] Bedel H A, Sivgin I, Dalmaz O, et al. BolT: Fused window transformers for fMRI time series analysis[J]. Medical image analysis, 2023, 88: 102841.

[6] Xu J, He K, Lan M, et al. Contrasformer: a brain network contrastive transformer for neurodegenerative condition identification[C]//Proceedings of the 33rd ACM International Conference on Information and Knowledge Management. 2024: 2671-2681.

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
