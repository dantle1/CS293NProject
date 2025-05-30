# Inferring Quality of Experience (QoE) in Video Streaming

This project aims to **infer end-user Quality of Experience (QoE) metrics** such as **rebuffering ratio**, **average chunk size**, and **video resolution**, directly from **network traffic features**. The goal is to enable **passive QoE monitoring** to support ISPs, CDNs, and researchers in understanding and improving video streaming quality at scale.

---

## Project Objectives

- **Predict QoE metrics** without access to video player or application logs.
- Extract meaningful features from **network-level traces** (e.g., packet counts, packet sizes, inter-arrival times).
- Train and evaluate **machine learning models** (e.g., Random Forest, SVM, Linear Regression).
- Validate inference accuracy against ground truth metrics from known video sessions.
- Use explainability tools like TrusteeML to further analyze the decision choices of the models.

---
File Descriptions

- pcap_qoe: set of raw pcap files and video logs. used to train and evaluate models.
- puffer_6M_profile_on50: folders containing sample raw pcap files and video logs.  used to define preprocessing and mapping.

---
Deployment Instructions
- All jupyter notebooks in **src** folder, open in Google Colab to run
- `src/preprocessing_mapping/Jaber_Dataset_Trial_Run.ipynb`: pcap and video log mapping + dataset preprocessing
- `src/preprocessing_mapping/Jaber_Dataset_Trial_Run_(all_pcaps).ipynb`: provides all the actual pcap and video log mapping + dataset preprocessing.
