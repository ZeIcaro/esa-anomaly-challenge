# esa-anomaly-challenge

This is my Data Science project for the "MA412-Outils mathématiques avancés pour la science des données etl a prise de décision" course at the 7th semester of IPSA (Aero 4 - Systèmes).

The chosen dataset was provided by ESA and can be found on Kaggle at:
https://www.kaggle.com/competitions/esa-adb-challenge/

The project is based on the competition "Spacecraft Anomaly Challenge on ESA dataset", which is based on the European Space Agency Anomaly Detection Benchmark (ESA-ADB) dataset, released in 2024 and publicly available on Zenodo https://zenodo.org/records/12528696.

This project will be done purely for studies and self-development, as the official competition started on Mar 13, 2025 and finished on Jun 11, 2025.

From the original ESA Challenge webpage on Kaggle"

"
DESCRIPTION

In 2021, ESA's European Space Operations Centre initiated a project to outline a clear direction for AI implementation in mission operations. This initiative led to the creation of the Artificial Intelligence for Automation (A2I) Roadmap [2], developed by a team of over 70 specialists at ESOC, with support from an industry consortium. The roadmap underwent further validation and refinement in collaboration with the European space and IT sectors.

Over the years, the A2I Roadmap evolved into the AI and Data Foundation Project that focuses on five key capabilities, one of which is ''Automated system health monitoring and control''. Anomaly detection plays a critical role in this capability, as early detection of anomalies can prevent potential dangers to the spacecraft.

In this Challenge, your objective is to identify the anomalies experienced by one of ESA's missions using Artificial Intelligence. We hope that this unique Challenge that uses real world data will allow researchers and scientists from academia, research institutes, national and international space agencies, and industry to develop and benchmark novel approaches for anomaly detection for spacecraft telemetry data."

DATA

The dataset represents several years of real sensor measurements collected from a large spacecraft operated by the European Space Agency. It is a single long continuous multivariate time series data of 87 mission-critical parameters. The dataset was carefully annotated for anomalies and rare events based on the original flight control reports and several iterations of manual and algorithm-driven refinement of labels [1].

Your task is to find all anomalous time points in the test set (binary decision, 0 - normal point, 1 - anomalous point, see the sample_submission.parquet file) while minimizing the number of false alarms.

EVALUATION METRIC

Submissions are evaluated using the corrected event-wise F0.5 score for anomaly detection in time series introduced by Sehili & Zhang [3] and adopted as a primary metric in the ESA-ADB benchmark [1]. The metric is a harmonic mean of corrected event-wise precision and event-wise recall, with precision having 2 times higher importance than recall:

Event-wise precision and recall treat each continuous anomalous segment as a single event, regardless of its size. A segment is considered an event-wise true positive TPe if at least one of its samples is detected; otherwise, it is an event-wise false negative FNe. Any continuous detection that does not overlap with an anomalous segment is counted as an event-wise false positive FPe. Additionally, due to the correction applied to the event-wise precision, each falsely detected sample FPt decreases the value of the corrected event-wise precision relatively to the number of nominal sample Nt.

"

