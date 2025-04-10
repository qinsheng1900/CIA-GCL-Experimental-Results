# CIA-GCL-Experimental-Results
## 1.T-test results

**Table 1: T-test results on three datasets compared with all baselines**.**Note:** Significance levels(Sig. level) are indicated as follows: p < 0.05 (\*), *p* < 0.01 (\*\*), *p* < 0.001 (\*\*\*), *p* ≥ 0.05 (n.s., not significant). Although our performance on a single dataset is close to that of some other methods, **the overall performance** on the three datasets **is statistically significantly different from** that of other comparison methods.

| Dataset                | ABIDE1   |             | ABIDE2   |             | ADHD200  |             |  ALL     |              |
|:----------------------:|:--------:|:-----------:|:--------:|:-----------:|:--------:|:-----------:|:--------:|:------------:|
| Method                 | p-value  | Sig. level  | p-value  | Sig. level  | p-value  | Sig. level  | p-value  | Sig. level   |
| RF(2008)               | 2.00E-08 | ***         | 9.40E-05 | ***         | 1.70E-03 | ***         | 1.80E-07 | ***          |
| SVM(2010)              | 1.10E-04 | ***         | 4.30E-05 | ***         | 4.00E-03 | **          | 6.20E-07 | ***          |
| BrainNetCNN(2017)      | 2.40E-07 | ***         | 3.40E-04 | ***         | 3.90E-02 | *           | 2.90E-06 | ***          |
| BNC-DGHL(2022)         | 2.50E-02 | *           | 3.30E-02 | *           | 6.80E-02 | n.s.        | 3.30E-03 | **           |
| GATE(2022)             | 2.40E-03 | **          | 9.30E-02 | n.s.        | 6.60E-03 | **          | 1.50E-03 | ***          |
| BrainUSL(2023)         | 2.40E-05 | ***         | 1.60E-03 | ***         | 1.30E-02 | *           | 9.00E-08 | ***          |
| BrainGB(2023)          | 3.80E-04 | ***         | 3.40E-02 | *           | 7.50E-03 | **          | 2.20E-04 | ***          |
| DHML(2023)             | 1.40E-01 | n.s.        | 9.80E-05 | ***         | 5.70E-02 | n.s.        | 6.80E-04 | ***          |
| CI-GNN(2024)           | 2.50E-04 | ***         | 5.30E-01 | n.s.        | 3.90E-02 | *           | 3.50E-03 | **           |
| METAFormer(2023)[1]    | 1.77E-03 | **          | 1.69E-03 | **          | 1.87E-03 | **          | 7.17E-03 | **           |
| CIGA(2022)[2]          | 1.21E-03 | **          | 2.94E-02 | *           | 6.61E-04 | ***         | 4.00E-08 | ***          |
| BrainIB(2024)[3]       | 1.93E-06 | ***         | 9.63E-02 | n.s.        | 1.15E-02 | *           | 6.64E-04 | ***          |
| BrainNetTF(2022)[4]    | 1.39E-04 | ***         | 6.22E-03 | **          | 6.91E-03 | **          | 9.52E-04 | **           |
| BoIT(2023)[5]          | 1.72E-05 | ***         | 9.29E-01 | n.s.        | 8.92E-03 | **          | 4.24E-03 | **           |
| Contrasformer(2024)[6] | 2.00E-06 | ***         | 5.87E-04 | ***         | 6.87E-02 | n.s.        | 1.11E-03 | **           |


## 2.New comparative experiment
**Table 2.1: Comparative experiments of new methods of ABIDE I, ABIDE II, ADHD200 on AAL atlas under Table1's setting** (a)self-supervised method (METAFormer 2023) (Self-supervised method based on masked autoencoder);(b)two approaches targeting OOD generalization (CIGA 2022，BrainIB 2024); (c)two methods for fMRI analysis (BrainNetTF 2022，BolT 2023);(d)contrastive learning-based models (Contrasformer 2024)
| Dataset | Method           | Accuracy (\%)          | Precision (\%)         | Recall (\%)            | F1-score (\%)          | bAcc (\%)              | AUC (\%)               | Avg (\%)                |
|:-------:|:----------------:|:----------------------:|:----------------------:|:----------------------:|:----------------------:|:----------------------:|:----------------------:|:-----------------------:|
| ABIDE I | METAFormer(2023)[1]    | 70.31±2.86             | 71.80±3.20             | 74.38±6.64             | 72.85±3.29             | 69.91±2.80             | 72.29±3.54             | 71.18±2.91              |
|         | CIGA(2022)[2]          | 66.96±1.64             | 69.55±2.42             | 57.84±6.20             | 62.92±3.43             | 66.75±1.69             | 67.53±2.81             | 65.26±4.22              |
|         | BrainIB(2024)[3]       | 69.97±2.82             | 71.07±4.19             | 70.70±4.61             | 70.74±2.90             | 69.63±3.15             | 73.44±4.35             | 70.92±1.34              |
|         | BrainNetTF(2022)[4]    | 70.66±4.93             | 70.79±6.07             | 69.35±7.4              | 69.71±5.07             | 70.64±4.37             | 70.68±5.58             | 70.30±0.61              |
|         | BoIT(2023)[5]          | 69.43±2.93             | 69.16±3.22             | 72.78±4.79             | 70.83±3.00             | 69.34±2.93             | 72.58±2.79             | 70.68±1.64              |
|         | Contrasformer(2024)[6] | 68.9±2.33              | 67.68±3.96             | 70.91±6.04             | 68.70±2.74             | 68.86±2.23             | 70.68±2.64             | 69.29±1.24              |
|         | **CIA-GCL**      | **73.42±2.75**         | **73.82±3.23**         | **74.91±5.63**             | **74.21±3.03**         | **73.38±2.76**         | **76.28±3.74**         | **74.34±1.10**          |
|ABIDE II  | METAFormer(2023)[1]    | 69.10±3.17             | 68.34±3.91             | 64.00±7.66             | 65.89±4.41             | 69.04±3.21             | 70.88±4.36            | 67.88±2.49             |
|          | CIGA(2022)[2]          | 66.40±3.22             | 63.01±3.16             | 68.32±13.39            | 64.85±7.92             | 66.54±3.72             | 66.63±3.94            | 65.53±2.81             |
|          | BrainIB(2024)[3]       | 68.92±3.60             | 66.73±6.70             | 68.13±10.74            | 66.65±4.19             | 68.58±3.22             | 69.83±4.61            | 68.29±1.96             |
|          | BrainNetTF(2022)[4]    | 66.62±4.17             | 68.70±7.05             | 65.73±13.35            | 65.01±5.77             | 65.30±4.61             | 67.86±4.92            | 66.54±1.47             |
|          | BoIT(2023)[5]          | 69.69±2.22             | 69.83±3.44             | **72.79±4.88**         | **71.13±2.02**         | 68.45±2.35             | 71.42±3.32            | 70.33±1.66             |
|          | Contrasformer(2024)[6] | 69.79±2.99             | 67.39±8.16             | 57.86±8.87             | 61.78±6.25             | 67.94±3.50             | 70.02±3.67            | 65.78±4.92             |
|          | **CIA-GCL**      | **72.09±2.47**         | **72.67±3.49**         | 64.39±9.14             | 68.94±4.74             | **71.45±2.71**         | **72.58±2.41**        | **70.51±3.25**         |
|ADHD200  | METAFormer(2023)[1]    | 70.27±2.54             | 73.00±7.87             | 44.09±10.01             | 54.66±9.45             | 62.63±4.83             | 69.13±4.65             | 62.29±11.09             |
|         | CIGA(2022)[2]          | 67.73±2.44             | 61.95±6.04             | 43.25±17.31             | 48.40±12.75            | 62.75±4.97             | 64.01±2.95             | 58.02±9.79              |
|         | BrainIB(2024)[3]       | 70.07±1.56             | 60.69±2.54             | 56.47±8.48              | 58.10±4.11             | 67.10±2.15             | 67.28±2.72             | 63.29±5.60              |
|         | BrainNetTF(2022)[4]    | 70.33±3.38             | 70.89±11.15            | 38.95±13.78             | 48.33±12.31            | 64.10±4.92             | 69.21±7.42             | 60.3±13.45              |
|         | BoIT(2023)[5]          | 69.03±2.74             | 61.13±3.64             | 54.16±7.94              | 54.66±4.89             | 66.19±3.30             | 70.29±4.09             | 62.58±7.07              |
|         | Contrasformer(2024)[6] | 72.19±2.65             | 62.68±5.76             | 59.53±12.73             | 60.26±7.32             | 68.54±4.06             | 72.63±3.41             | 65.97±5.91              |
|         | **CIA-GCL**      | **75.21±2.57**         | **79.40±10.59**        | **58.75±11.73**             | **69.80±8.87**         | **69.93±4.01**         | **73.51±4.01**         | **71.10±7.03**         |


**Table 2.2: Comparative experiments of all methods of ABIDE 1,ABIDE II and ADHD200 on AAL atlas under Table1's setting** 

| Dataset | Method           | Accuracy (\%)          | Precision (\%)         | Recall (\%)            | F1-score (\%)          | bAcc (\%)              | AUC (\%)               | Avg (\%)                |
|:-------:|:----------------:|:----------------------:|:----------------------:|:----------------------:|:----------------------:|:----------------------:|:----------------------:|:-----------------------:|
| ABIDE I | RF(2008)               | 62.02±4.72             | 63.28±5.33             | 63.02±3.79             | 63.01±3.53             | 62.00±4.81             | 66.60±5.96             | 62.79±0.48              |
|         | SVM(2010)              | 65.12±2.93             | 65.49±4.15             | 60.81±5.01             | 62.93±3.44             | 65.03±2.93             | 70.83±4.79             | 62.67±6.75              |
|         | BrainNetCNN(2017)      | 68.88±3.23             | 70.21±5.29             | 71.13±13.8             | 69.48±5.37             | 68.85±3.22             | 72.39±4.09             | 70.16±1.39              |
|         | BNC-DGHL(2022)         | 70.5±3.30              | 70.48±4.13             | 76.32±3.29             | 73.27±2.52             | 70.40±3.09             | 73.99±3.46             | 72.49±2.44              |
|         | GATE(2022)             | 71.67±2.95             | 71.93±4.92             | 74.68±6.08             | 72.99±2.55             | 71.42±3.03             | 73.04±4.62             | 72.62±1.21              |
|         | Com-BrainTF(2023)      | 70.14±4.38             | 70.28±4.32             | 72.83±4.15             | 70.01±4.49             | 70.00±4.65             | 71.67±6.16             | 70.82±1.17              |
|         | BrainGB(2023)          | 71.07±4.92             | 72.79±8.02             | 72.90±6.20             | 70.80±4.47             | 70.93 ±4.79            | 74.93±5.10             | 72.24±1.62              |
|         | DHML(2023)             | 71.52±2.93             | 71.19±3.23             | **77.14±3.23**         | 73.92±2.43             | 71.27±3.38             | 74.72±3.34             | 73.29±2.40             |
|         | CI-GNN(2024)           | 71.89±2.91             | 70.49±2.98             | 73.37±4.80             | 70.58±2.21             | 71.44±2.75             | 73.32±3.62             | 71.85±1.27              |
|         | METAFormer(2023)[1]    | 70.31±2.86             | 71.80±3.20             | 74.38±6.64             | 72.85±3.29             | 69.91±2.80             | 72.29±3.54             | 71.18±2.91              |
|         | CIGA(2022)[2]          | 66.96±1.64             | 69.55±2.42             | 57.84±6.20             | 62.92±3.43             | 66.75±1.69             | 67.53±2.81             | 65.26±4.22              |
|         | BrainIB(2024)[3]       | 69.97±2.82             | 71.07±4.19             | 70.70±4.61             | 70.74±2.90             | 69.63±3.15             | 73.44±4.35             | 70.92±1.34              |
|         | BrainNetTF(2022)[4]    | 70.66±4.93             | 70.79±6.07             | 69.35±7.4              | 69.71±5.07             | 70.64±4.37             | 70.68±5.58             | 70.30±0.61              |
|         | BoIT(2023)[5]          | 69.43±2.93             | 69.16±3.22             | 72.78±4.79             | 70.83±3.00             | 69.34±2.93             | 72.58±2.79             | 70.68±1.64              |
|         | Contrasformer(2024)[6] | 68.9±2.33              | 67.68±3.96             | 70.91±6.04             | 68.70±2.74             | 68.86±2.23             | 70.68±2.64             | 69.29±1.24              |
|         | **CIA-GCL**      | **73.42±2.75**         | **73.82±3.23**         | 74.91±5.63             | **74.21±3.03**         | **73.38±2.76**         | **76.28±3.74**         | **74.34±1.10**          |
| ABIDE II | RF(2008)               | 62.56±2.67             | 62.71±4.29             | 48.87±2.97             | 54.83±2.55             | 61.68±2.56             | 66.60±5.96            | 59.54±6.47             |
|          | SVM(2010)              | 64.78±3.75             | 63.79±5.3              | 56.53±6.83             | 59.75±4.9              | 64.25±3.88             | 69.13±3.62            | 63.04±4.36             |
|          | BrainNetCNN(2017)      | 67.75±2.72             | 69.74±5.70             | 56.92±9.87             | 61.87±5.57             | 67.21±2.72             | 69.59±3.89            | 65.51±5.08             |
|          | BNC-DGHL(2022)         | 68.53±3.73             | 68.53±3.73             | 66.31±4.73             | 66.46±5.35             | 70.15±6.31             | 68.39±3.67            | 68.09±1.50             |
|          | GATE(2022)             | 69.51±2.76             | 71.21±2.97             | 65.64±6.88             | 68.83±2.94             | 70.33±5.25             | 70.87±4.55            | 69.37±2.02             |
|          | Com-BrainTF(2023)      | 68.91±2.29             | 69.12±1.95             | 62.92±9.42             | 68.34±2.87             | 68.80±6.50             | 70.40±4.72            | 68.08±2.62             |
|          | BrainGB(2023)          | 69.23±3.33             | 67.37±4.61             | 65.97±6.45             | 66.34±3.89             | 69.01±3.28             | 71.33±4.12            | 68.21±2.03             |
|          | DHML(2023)             | 69.22±3.19             | 69.37±5.16             | 63.39±11.13            | 65.45±5.27             | 68.82±3,17             | 69.48±3.43            | 67.62±2.57             |
|          | CI-GNN(2024)           | 70.04±2.62             | 70.22±3.59             | 69.56±5.28             | 68.85±3.60             | 69.93±3.39             | 69.13±4.82            | 69.62±0.54             |
|          | METAFormer(2023)[1]    | 69.10±3.17             | 68.34±3.91             | 64.00±7.66             | 65.89±4.41             | 69.04±3.21             | 70.88±4.36            | 67.88±2.49             |
|          | CIGA(2022)[2]          | 66.40±3.22             | 63.01±3.16             | 68.32±13.39            | 64.85±7.92             | 66.54±3.72             | 66.63±3.94            | 65.53±2.81             |
|          | BrainIB(2024)[3]       | 68.92±3.60             | 66.73±6.70             | 68.13±10.74            | 66.65±4.19             | 68.58±3.22             | 69.83±4.61            | 68.29±1.96             |
|          | BrainNetTF(2022)[4]    | 66.62±4.17             | 68.70±7.05             | 65.73±13.35            | 65.01±5.77             | 65.30±4.61             | 67.86±4.92            | 66.54±1.47             |
|          | BoIT(2023)[5]          | 69.69±2.22             | 69.83±3.44             | **72.79±4.88**         | **71.13±2.02**         | 68.45±2.35             | 71.42±3.32            | 70.33±1.66             |
|          | Contrasformer(2024)[6] | 69.79±2.99             | 67.39±8.16             | 57.86±8.87             | 61.78±6.25             | 67.94±3.50             | 70.02±3.67            | 65.78±4.92             |
|          | **CIA-GCL**      | **72.09±2.47**         | **72.67±3.49**         | 64.39±9.14             | 68.94±4.74             | **71.45±2.71**         | **72.58±2.41**        | **70.51±3.25**         |
| ADHD200 | RF(2008)               | 63.88±3.28             | 54.52±10.37            | 21.67±9.99              | 30.14±11.37            | 55.53±4.19             | 60.72±7.9              | 47.74±17.46             |
|         | SVM(2010)              | 66.48±3.99             | 62.9±12.19             | 28.25±7.83              | 38.49±8.51             | 58.91±4.37             | 67.58±7.91             | 53.77±16.41             |
|         | BrainNetCNN(2017)      | 70.71±4.15             | 61.69±5.90             | 59.30±12.29}            | 59.90±7.94             | 68.47±5.21             | 70.02±6.20             | 65.01±5.27              |
|         | BNC-DGHL(2022)         | 70.25±3.88             | 59.76±4.40             | **62.37±11.41**      | 60.82±7.54             | 68.68±5.29             | 68.39±7.27             | 65.05±4.57              |
|         | GATE(2022)             | 72.02±3.55             | 71.27±6.09             | 45.18±17.04             | 52.82±14.87            | 66.67±6.01             | 69.31±9.42             | 62.88±11.17             |
|         | Com-BrainTF(2023)      | 71.78±4.50             | 70.38±4.33             | 56.71±17.17             | 68.28±7.69             | 68.77±6.89             | 69.75±6.96             | 67.61±5.48              |
|         | BrainGB(2023)          | 71.91±2.89             | 71.51±9.69             | 45.56±9.96              | 54.62±6.65             | 66.01±3.49             | 71.63±6.30             | 63.54±11.02             |
|         | DHML(2023)             | 72.87±2.71             | 66.34±5.54             | 57.23±10.12             | 63.02±5.87             | 69.78±3.82             | 72.96±3.91             | 67.03±6.15              |
|         | CI-GNN(2024)           | 71.03±3.05             | 61.32±5.08             | 53.44±10.84             | 66.93±4.26             | 67.93±4.26             | 71.95±2.97             | 65.43±6.97              |
|         | METAFormer(2023)[1]    | 70.27±2.54             | 73.00±7.87             | 44.09±10.01             | 54.66±9.45             | 62.63±4.83             | 69.13±4.65             | 62.29±11.09             |
|         | CIGA(2022)[2]          | 67.73±2.44             | 61.95±6.04             | 43.25±17.31             | 48.40±12.75            | 62.75±4.97             | 64.01±2.95             | 58.02±9.79              |
|         | BrainIB(2024)[3]       | 70.07±1.56             | 60.69±2.54             | 56.47±8.48              | 58.10±4.11             | 67.10±2.15             | 67.28±2.72             | 63.29±5.60              |
|         | BrainNetTF(2022)[4]    | 70.33±3.38             | 70.89±11.15            | 38.95±13.78             | 48.33±12.31            | 64.10±4.92             | 69.21±7.42             | 60.3±13.45              |
|         | BoIT(2023)[5]          | 69.03±2.74             | 61.13±3.64             | 54.16±7.94              | 54.66±4.89             | 66.19±3.30             | 70.29±4.09             | 62.58±7.07              |
|         | Contrasformer(2024)[6] | 72.19±2.65             | 62.68±5.76             | 59.53±12.73             | 60.26±7.32             | 68.54±4.06             | 72.63±3.41             | 65.97±5.91              |
|         | **CIA-GCL**      | **75.21±2.57**         | **79.40±10.59**        | 58.75±11.73             | **69.80±8.87**         | **69.93±4.01**         | **73.51±4.01**         | **71.10±7.03**         |

**Table 2.3: Comparative experiments of new methods of ABIDE I, ABIDE II, ADHD200 on AAL atlas under Table2's setting** 

| Dataset | Method           | Accuracy (\%)          | Precision (\%)         | Recall (\%)           | F1-score (\%)          | bAcc (\%)              | AUC (\%)               | Avg (\%)                |
|:-------:|:----------------:|:----------------------:|:----------------------:|:---------------------:|:----------------------:|:----------------------:|:----------------------:|:-----------------------:|
| ABIDE I | METAFormer(2023)[1]    | 70.13±3.40             | 69.60±1.56             | 72.26±8.13            | 67.88±4.34             | 69.47±3.78             | 71.13±5.15             | 70.08±1.50              |
|         | CIGA(2022)[2]          | 65.51±1.97             | 64.32±4.19             | 63.17±2.06            | 63.65±1.54             | 65.35±1.78             | 66.74±3.40             | 64.79±1.33              |
|         | BrainIB(2024)[3]       | 64.92±1.34             | 61.27±1.42             | 66.06±9.45            | 63.89±8.98             | 63.32±2.88             | 61.59±1.17             | 63.51±1.86              |
|         | BrainNetTF(2022)[4]    | 66.63±1.56             | 65.98±3.24             | 65.75±5.13            | 68.04±2.86             | 66.83±4.30             | 67.97±1.80             | 66.87±0.96              |
|         | BoIT(2023)[5]          | 65.71±1.50             | 65.27±1.42             | 64.26±5.63            | 64.62±2.05             | 65.50±1.01             | 69.08±2.64             | 65.74±1.73              |
|         | Contrasformer(2024)[6] | 70.50±2.83             | 73.14±6.80             | 67.19±5.60            | 70.73±4.41             | 70.78±2.95             | 69.54±4.11             | 70.31±1.93              |
|         | **CIA-GCL**            | **72.03±0.90**         | **74.12±3.57**         | **69.92±3.31**        | **71.86±1.51**         | **72.08±1.65**         | **74.26±3.43**         | **72.38±1.62**          |
| ABIDE II | METAFormer(2023)[1]        | 66.18±2.33             | 64.32±6.68             | 73.60±11.12             | 67.97±2.23              | 66.48±2.38             | 67.01±0.18             | 67.59±3.17              |
|          | CIGA(2022)[2]              | 68.11±3.20             | 71.61±9.12             | 62.60±13.97             | 67.36±10.32             | 66.45±2.81             | 67.72±3.62             | 67.31±2.90              |
|          | BrainIB(2024)[3]           | 68.46±3.13             | **72.14±8.44**         | 64.89±16.37             | 68.02±12.17             | 65.99±2.01             | 65.6±2.45              | 67.50±2.67              |
|          | BrainNetTF(2022)[4]        | 67.59±2.25             | 70.29±7.35             | 64.25±9.21              | 66.93±7.57              | 66.16±2.43             | 66.12±1.97             | 66.87±1.98              |
|          | BoIT(2023)[5]              | 66.84±1.47             | 70.10±4.24             | 60.57±8.76              | 64.56±3.72              | 66.71±1.55             | 67.26±2.03             | 66.01±3.18              |
|          | Contrasformer(2024)[6]     | 69.81±2.05             | 70.18±3,36             | 68.98±10.25             | 69.25±6.43              | 65.47±4.54             | 66.99±0.95             | 68.45±1.82              |
|          | **CIA-GCL**                | **71.51±2.94**         | 70.83±4.63             | **77.87±15.94**         | **73.97±9.73**          | **66.52±5.24**          | **68.81±5.72**    | **71.59±3.98**               |
| ADHD200  | METAFormer(2023)[1]        | 67.22±2.01             | **71.16±12.90**        | 39.90±0.22             | 43.76±10.57             | 59.21±0.98             | 63.58±3,88             | 57.38±13.02              |
|         | CIGA(2022)[2]              | 67.27±1.75             | 69.78±4.47             | 21.24±14.06            | 30.71±17.30             | 57.70±4.55             | 59.60±7.98             | 51.05±20.16              |
|         | BrainIB(2024)[3]           | 68.43±1.93             | 58.76±4.27             | 33.44±9.67             | 42.27±9.18              | 60.18±3.80             | 64.03±3.76             | 54.52±13.62              |
|         | BrainNetTF(2022)[4]        | 66.85±2.81             | 63.54±3.90             | 37.36±7.44             | 40.03±10.65             | 56.39±5.62             | 63.16±4.08             | 54.56±12.77              |
|         | BoIT(2023)[5]              | 66.87±1.39             | 68.28±6.14             | 25.72±3.13             | 37.08±3.40              | 60.81±3.14             | 64.31±3.65             | 53.85±17.93              |
|         | Contrasformer(2024)[6]     | 68.05±1.35             | 60.37±5.54             | 43.10±16.63            | 48.33±11.32             | 62.75±3.87             | 68.15±4.18             | 58.46±10.45              |
|         | **CIA-GCL**                | **71.32±1.05**         | 64.77±3.28             | **51.17±9.23**         |  **56.09±5.89**          | **66.63±5.92**         | **68.97±2.35**         | **63.16±7.85**           |

**Table 2.4: Comparative experiments of all methods of ABIDE I, ABIDE II, ADHD200 on AAL atlas under Table2's setting** 

| Dataset | Method           | Accuracy (\%)          | Precision (\%)         | Recall (\%)           | F1-score (\%)          | bAcc (\%)              | AUC (\%)               | Avg (\%)                |
|:-------:|:----------------:|:----------------------:|:----------------------:|:---------------------:|:----------------------:|:----------------------:|:----------------------:|:-----------------------:|
| ABIDE I | RF(2008)               | 63.58±4.83             | 63.06±5.81             | 59.95±3.03            | 61.26±1.57             | 63.23±3.87             | 67.8±3.65              | 63.15±2.67              |
|         | SVM(2010)              | 64.92±3.95             | 63.58±6.03             | 64.05±3.73            | 63.62±2.67             | 64.66±3.15             | 68.00±2.88             | 64.81±1.66              |
|         | BrainNetCNN(2017)      | 67.97±0.86             | 69.35±6.55             | 60.35±12.57           | 63.78±6.81             | 67.36±1.57             | 70.24±2.19             | 66.51±3.75              |
|         | BNC-DGHL(2022)         | 68.56±1.33             | 66.52±2.71             |  68.2±3.59            | 67.34±3.09             | 68.22±1.31             | 70.44±1.70             | 68.21±1.32              |
|         | GATE(2022)             | 67.76±1.74             | 64.6±3.55              | 66.86±4.93            | 65.63±3.53             | 66.93±2.75             | 69.16±1.74             | 66.82±1.59              |
|         | Com-BrainTF(2023)      | 69.29±0.81             | 70.87±5.29             | 67.66±6.88            | 69.15±0.61             | 69.26±0.81             |  71.54±0.63            | 69.63±1.38              |
|         | BrainGB(2023)          | 69.91±1.17             | 68.11±3.02             | 68.16±10.27           | 68.01±6.70             | 69.13±1.78             | 69.68±1.96             | 68.83±0.85              |
|         | DHML(2023)             | 68.4±1.31              | 69.06±2.54             | 59.15±6.51            | 63.67±4.82             | 67.25±0.96             | 71.25±2.07             | 66.41±4.40              |
|         | CI-GNN(2024)           |  69.94±1.98            |  72.97±2.62            | 64.96±2.57            |  69.93±0.95            |  70.06±2.93            | 71.31±2.86             |  69.86±2.68             |
|         | METAFormer(2023)[1]    | 70.13±3.40             | 69.60±1.56             | 72.26±8.13            | 67.88±4.34             | 69.47±3.78             | 71.13±5.15             | 70.08±1.50              |
|         | CIGA(2022)[2]          | 65.51±1.97             | 64.32±4.19             | 63.17±2.06            | 63.65±1.54             | 65.35±1.78             | 66.74±3.40             | 64.79±1.33              |
|         | BrainIB(2024)[3]       | 64.92±1.34             | 61.27±1.42             | 66.06±9.45            | 63.89±8.98             | 63.32±2.88             | 61.59±1.17             | 63.51±1.86              |
|         | BrainNetTF(2022)[4]    | 66.63±1.56             | 65.98±3.24             | 65.75±5.13            | 68.04±2.86             | 66.83±4.30             | 67.97±1.80             | 66.87±0.96              |
|         | BoIT(2023)[5]          | 65.71±1.50             | 65.27±1.42             | 64.26±5.63            | 64.62±2.05             | 65.50±1.01             | 69.08±2.64             | 65.74±1.73              |
|         | Contrasformer(2024)[6] | 70.50±2.83             | 73.14±6.80             | 67.19±5.60            | 70.73±4.41             | 70.78±2.95             | 69.54±4.11             | 70.31±1.93              |
|         | **CIA-GCL**            | **72.03±0.90**         | **74.12±3.57**         | **69.92±3.31**        | **71.86±1.51**         | **72.08±1.65**         | **74.26±3.43**         | **72.38±1.62**          |
| ABIDE II | RF(2008)                | 60.44±5.27             | 68.10±12.47            | 56.18±11.66             | 60.2±3.71               | 62.42±1.3              | 66.28±1.77             | 62.27±4.35              |
|          | SVM(2010)               | 62.58±4.21             | 68.49±15.29            | 67.07±15.39             | 65.47±3.12              | 65.2±1.5               | 67.6±4.71              | 66.07±2.12              |
|          | BrainNetCNN(2017)       | 67.20±4.18             | 67.36±8.87             |  73.31±11.96            | 70.22±10.28             | 63.65±2.18             | 68.19±3.01             | 68.32±3.24              |
|          | BNC-DGHL(2022)          | 68.09±2.69             | **72.74±12.79**        | 67.92±6.89              | 69.69±6.86              | **68.32±2.25**         | 67.26±2.55             | 69.00±1.99              |
|          | GATE(2022)              | 67.83±2.15             | 60.6±9.88              | 66.53±14.11             | 62.26±6.10              | 63.26±3.52             | 65.7±2.21              | 64.36±2.76              |
|          | Com-BrainTF(2023)       | 69.34±3.24             | 67.09±1.67             | 69.60±19.07             | 64.94±4.02              | 64.79±4.40             | 67.10±0.85             | 67.14±2.06              |
|          | BrainGB(2023)           |  69.68±4.45            |  71.89±9.45            | 70.53±12.90             |  70.93±10.19            |  67.36±0.92            |  68.39±1.79            |  69.79±1.68             |
|          | DHML(2023)              | 68.39±3.04             | 69.20±3.98             | 70.62±15.40             | 68.47±14.05             | 63.98±1.20             | 65.19±3.84             | 67.64±2.52              |
|          | CI-GNN(2024)            | 68.14±2.35             | 66.28±2.43             | 62.63±8.61              | 63.89±3.68              | 66.81±2.50             | 67.32±2.82             | 65.85±2.13              |
|          | METAFormer(2023)[1]        | 66.18±2.33             | 64.32±6.68             | 73.60±11.12             | 67.97±2.23              | 66.48±2.38             | 67.01±0.18             | 67.59±3.17              |
|          | CIGA(2022)[2]              | 68.11±3.20             | 71.61±9.12             | 62.60±13.97             | 67.36±10.32             | 66.45±2.81             | 67.72±3.62             | 67.31±2.90              |
|          | BrainIB(2024)[3]           | 68.46±3.13             | 72.14±8.44             | 64.89±16.37             | 68.02±12.17             | 65.99±2.01             | 65.6±2.45              | 67.50±2.67              |
|          | BrainNetTF(2022)[4]        | 67.59±2.25             | 70.29±7.35             | 64.25±9.21              | 66.93±7.57              | 66.16±2.43             | 66.12±1.97             | 66.87±1.98              |
|          | BoIT(2023)[5]              | 66.84±1.47             | 70.10±4.24             | 60.57±8.76              | 64.56±3.72              | 66.71±1.55             | 67.26±2.03             | 66.01±3.18              |
|          | Contrasformer(2024)[6]     | 69.81±2.05             | 70.18±3,36             | 68.98±10.25             | 69.25±6.43              | 65.47±4.54             | 66.99±0.95             | 68.45±1.82              |
|          | **CIA-GCL**                | **71.51±2.94**         | 70.83±4.63             | **77.87±15.94**         | **73.97±9.73**          | 66.52±5.24             | **68.81±5.72**    | **71.59±3.98**               |
| ADHD200 | RF(2008)                | 60.35±6.83             | 41.03±15.54            | 7.02±4.8               | 11.34±7.46              | 49.44±3.71             | 49.58±7.05             | 36.46±22.04              |
|         | SVM(2010)               | 63±4.95                | 55.93±19.57            | 8.53±3.9               | 14.56±6.37              | 51.9±2.64              | 62.03±2.74             | 42.66±24.51              |
|         | BrainNetCNN(2017)       | 67.96±2.22             | 61.77±7.54             | 38.75±24.33            | 44.62±16.99             | 61.51±5.86             | 63.79±4.45             | 56.40±11.77              |
|         | BNC-DGHL(2022)          | 67.68±1.14             | 61.85±5.37             | 44.20±8.41             | 51.16±5.43              | 63.33±1.48             | 63.62±2.24             | 58.64±8.98               |
|         | GATE(2022)              | 67.5±1.58              | 62.36±14.01            | 30.3±17.12             | 42.93±14.14             | 60.66±3.41             | 62.86±5.44             | 54.44±14.54              |
|         | Com-BrainTF(2023)       | 69.02±0.32             |  69.04±0.94            | 31.51±15.03            | **60.11±5.45**          | 61.51±5.86             | 65.28±3.11             | 59.41±14.16              |
|         | BrainGB(2023)           | 68.29±1.23             | 66.31±4.17             | 32.52±13.95            | 45.84±10.84             | 61.98±4.94             | 63.92±1.14             | 56.48±14.20              |
|         | DHML(2023)              |  70.34±3.38            | **69.71±7.04**         | 38.63±6.37             | 46.67±15.41             | 62.98±10.63            | 68.39±5.40             |  59.45±13.51             |
|         | CI-GNN(2024)            | 68.57±1.25             | 58.58±5.50             |  49.33±1.27            | 50.23±3.75              |  64.08±1.23            |  64.57±2.48            | 59.23±7.98               |
|         | METAFormer(2023)[1]        | 67.22±2.01             | 71.16±12.90            | 39.90±0.22             | 43.76±10.57             | 59.21±0.98             | 63.58±3,88             | 57.38±13.02              |
|         | CIGA(2022)[2]              | 67.27±1.75             | 69.78±4.47             | 21.24±14.06            | 30.71±17.30             | 57.70±4.55             | 59.60±7.98             | 51.05±20.16              |
|         | BrainIB(2024)[3]           | 68.43±1.93             | 58.76±4.27             | 33.44±9.67             | 42.27±9.18              | 60.18±3.80             | 64.03±3.76             | 54.52±13.62              |
|         | BrainNetTF(2022)[4]        | 66.85±2.81             | 63.54±3.90             | 37.36±7.44             | 40.03±10.65             | 56.39±5.62             | 63.16±4.08             | 54.56±12.77              |
|         | BoIT(2023)[5]              | 66.87±1.39             | 68.28±6.14             | 25.72±3.13             | 37.08±3.40              | 60.81±3.14             | 64.31±3.65             | 53.85±17.93              |
|         | Contrasformer(2024)[6]     | 68.05±1.35             | 60.37±5.54             | 43.10±16.63            | 48.33±11.32             | 62.75±3.87             | 68.15±4.18             | 58.46±10.45              |
|         | **CIA-GCL**                | **71.32±1.05**         | 64.77±3.28             | **51.17±9.23**         |  56.09±5.89             | **66.63±5.92**         | **68.97±2.35**         | **63.16±7.85**           |



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
