# Inferring Quality of Experience (QoE) in Video Streaming

---

Measuring Quality of Experience (QoE) in video streaming is essential for network providers and content delivery platforms to optimize user satisfaction.  This project aims to **infer end-user Quality of Experience (QoE) metrics** such as **rebuffering ratio**, **average chunk size**, and **video resolution**, directly from  **packet level features** extracted from raw network traffic.  We train and evaluate several machine learning models such as Random Forest and Support Vector Machine to predict QoE.  Our results show that it is possible to estimate video quality without access to a video player or application internals, enabling QoE monitoring in real world networks.
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
- `src/models/avg_format_plus_trutee.ipynb`: training of RF classifier on raw packet data and video logs to classify resolution.
- `src/models/avg_chunk_size_rebuffering_regressor.ipynb`: training of RF/Linear regressor on raw packet data and video logs to calculate rebuffering ratio.
