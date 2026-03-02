Dataset Description

The datasets provided in this repository are derived from the publicly available IoT-23 network traffic corpus, which contains over 325 million labeled network flow records collected from real-world IoT malware capture scenarios. The original dataset was obtained in .tar.gz format and includes labeled PCAP files accompanied by Zeek-generated .labeled log structures.

All Zeek logs were converted into structured CSV format and processed through a rigorous multi-stage cleaning, normalization, and validation pipeline to ensure feature consistency, label integrity, and suitability for large-scale modeling. The preprocessing framework preserves the natural class imbalance characteristics of IoT-23 while enabling controlled and reproducible experimentation.

To support the experimental evaluation presented in:

“SDNN-LGBM: A Robust Two-Stage Architecture for Multi-Class IoT Attack Detection under Extreme Rarity,”

the following curated large-scale subsets were constructed from the full IoT-23 corpus:

A4M – 4 million samples

B1.5M – 1.5 million samples

C4M – 4 million samples

D1.5M – 1.5 million samples

These datasets enable scalable multiclass intrusion detection experiments under realistic class imbalance and deployment-oriented evaluation conditions.

Data Access

The processed datasets associated with this study are available through the following institutional repository:

Download link:
https://studentutsedu-my.sharepoint.com/:f:/g/personal/farhat_ullah_student_uts_edu_au/IgALfnxxlRY1Q4U3A0kdqHjeAfiDA7V7-RqrRwWDZJ8lffw?e=VSsCMQ
