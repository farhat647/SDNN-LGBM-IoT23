Yes — now that Scenario 1 has been removed, I would also remove the old A4M, B1.5M, C4M, and D1.5M presentation from the dataset-availability text. It would otherwise make the repository look as if all four datasets are still part of the final experimental design.
The current manuscript uses only the row-disjoint IoT-23 setup with a 4,000,000-record development dataset and a separate 1,500,000-record independent test dataset, plus the ToN-IoT benchmark with 100,000 records split into 70,000 training, 15,000 validation, and 15,000 test records.     FarhatJ1_For_Sure_Final_3(1)     FarhatJ1_For_Sure_Final_3(1)
I would revise your repository text to this:
Dataset Description
The datasets provided in this repository are derived from the publicly available IoT-23 and ToN-IoT network-security datasets used in the experimental evaluation of:
“SDNN-LGBM: A Two-Stage Architecture for Multi-Class IoT Attack Detection under Extreme Rarity”
IoT-23
The IoT-23 data were reconstructed from the original labeled network-traffic captures and converted into structured tabular format using Zeek-derived features. The resulting data were processed through a consistent cleaning, preprocessing, and validation pipeline to preserve feature consistency, label integrity, and the natural class imbalance of the original traffic.
The final IoT-23 evaluation uses two strictly row-disjoint datasets:
- Development dataset: 4,000,000 records
- Independent test dataset: 1,500,000 records
- Input features: 14 numeric features
- Number of classes: 16
The development dataset is used for training and validation, while the independent test dataset is reserved exclusively for final evaluation. Stable row identifiers were used during dataset reconstruction to verify that there are zero shared records between the development and independent test datasets.
ToN-IoT
To provide evaluation on a second public IoT security benchmark, the study also uses a processed ToN-IoT dataset with a different feature space and class taxonomy.
The prepared ToN-IoT dataset contains:
- Total dataset: 100,000 records
- Training set: 70,000 records
- Validation set: 15,000 records
- Independent test set: 15,000 records
- Input features: 25
- Number of classes: 9
The ToN-IoT data are processed separately using training-fitted missing-value imputation and feature standardization. The 15,000-record test partition is reserved exclusively for final evaluation.
These datasets support large-scale multiclass intrusion-detection experiments under severe class imbalance and enable evaluation of the same SDNN-LGBM architectural principle across two different IoT security benchmarks.
Data Access
The processed datasets associated with this study are available through the following institutional repository:
Download link:
https://studentutsedu-my.sharepoint.com/:f:/g/personal/farhat_ullah_student_uts_edu_au/IgALfnxxlRY1Q4U3A0kdqHjeAfiDA7V7-RqrRwWDZJ8lffw?e=VSsCMQ
