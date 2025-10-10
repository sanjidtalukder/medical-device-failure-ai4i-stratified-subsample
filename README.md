# 🧠 Beyond Accuracy: Building Trustworthy AI for Predictive Maintenance of Critical Care Medical Devices

> **Author:** Sanjid Talukder  
> **Affiliation:** Department of Computer Science & Engineering, Dhaka International University  
> **Keywords:** Predictive Maintenance · Intensive Care Unit (ICU) · Machine Learning · LightGBM · Overfitting Prevention · Clinical AI · Group K-Fold Validation  

---

## 📘 Abstract

Unanticipated failures of medical devices in intensive care units compromise patient safety and disrupt clinical operations. Conventional maintenance strategies—whether based on fixed schedules or reactive repairs—often prove inefficient, either consuming resources unnecessarily or permitting critical breakdowns.  

This study introduces a **predictive framework** that applies **machine learning methods** to forecast ICU device malfunctions, with **explicit safeguards against overfitting**, a common limitation in healthcare AI.  

A dataset of **2,000 operational records**, enriched with **engineered clinical and mechanical indicators**, was analyzed using **LightGBM, XGBoost, Random Forest, and Gradient Boosting**.  
Through a **rigorous validation pipeline**—combining **Group K-Fold**, **temporal holdouts**, **redundancy reduction**, and **synthetic perturbation testing**—the models maintained robust generalization (AUC ≈ 0.95) with recall rates exceeding 94%.  

The **LightGBM** model demonstrated near-perfect performance (AUC: 0.9990, training time: 0.64 s) while preserving interpretability and efficiency.  
Minimal performance degradation (0.06%) after feature elimination confirmed that predictions stemmed from genuine signal rather than spurious correlations.  

> This repository presents both a specialized **ICU device failure prediction system** and a **transferable methodological template** for building **clinically trustworthy AI**.

---

## ⚙️ Methodology Overview
## 1. Data Acquisition & Preparation

Source: 2,000 ICU device operational records

Enriched with clinical + mechanical indicators

Cleaning included outlier capping, null imputation, and correlation pruning

---

## 2. Feature Engineering

Computed mechanical stress, temperature differentials, power load, and usage cycles

Normalized distributions to mitigate sensor bias

Redundancy reduction to avoid leakage across devices.

---

## 3. Modeling Algorithms

| Algorithm             | Rationale                            | Key Strength                    |
| --------------------- | ------------------------------------ | ------------------------------- |
| **LightGBM**          | Gradient boosting on leaf-wise trees | High speed, low memory          |
| **XGBoost**           | Robust ensemble learning             | Handles imbalance, fine-tunable |
| **Random Forest**     | Interpretability baseline            | Handles noisy data              |
| **Gradient Boosting** | Benchmark comparison                 | Stability vs complexity         |

---

## 4. Validation Framework

* Group K-Fold Cross Validation (device-level isolation)

* Temporal Holdout (future data integrity)

* Synthetic Perturbation Tests (robustness evaluation)

* Leakage Detection and Feature Redundancy Audits

---

## 📈 Key Results

| Metric                 |  LightGBM  | XGBoost | Random Forest | Gradient Boost |
| :--------------------- | :--------: | :-----: | :-----------: | :------------: |
| **AUC (Group K-Fold)** | **0.9990** |  0.9948 |     0.9712    |     0.9487     |
| **Recall (%)**         |  **99.74** |  97.22  |     95.88     |      94.36     |
| **Training Time (s)**  |  **0.64**  |   1.23  |      3.45     |      4.01      |

✅ LightGBM achieved the best trade-off between performance, interpretability, and efficiency.
🔒 Overfitting safeguards validated via synthetic noise injection and cross-device evaluation.

---

## 🧠 Insights & Contributions

📌 Introduced overfitting prevention protocols specialized for healthcare datasets

🩺 Developed a clinically aligned evaluation strategy prioritizing recall/sensitivity

⚙️ Delivered a reproducible predictive maintenance pipeline for ICU environments

🔬 Contributed a trust-oriented AI validation template applicable beyond healthcare

---

## 🧮 Tech Stack

| Category            | Tools                                                                             |
| ------------------- | --------------------------------------------------------------------------------- |
| **Languages**       | Python (3.11)                                                                     |
| **Libraries**       | `LightGBM`, `XGBoost`, `scikit-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn` |
| **Validation**      | Group K-Fold, Synthetic Perturbation Testing                                      |
| **Environment**     | JupyterLab / VS Code                                                              |
| **Version Control** | Git & GitHub                                                                      |

---

## 🧩 Future Work

Integrate real-time data streaming from IoT medical sensors.

Deploy explainable AI modules (SHAP, LIME) for clinician interpretability.

Extend validation to multi-institutional datasets for broader generalizability.

---

## 🛡️ Ethical Statement

This research emphasizes patient safety, data privacy, and transparency.
No personally identifiable patient data were used.
All datasets are synthetic or anonymized for ethical compliance.

---

🧾 Citation 
If you use this dataset or findings in your work, please cite:
Sabbir Ahmed, Mst. Romana Khanom, Sanjid Talukder, and Md. Abdul Bashed M.A(2025).
Beyond Accuracy: Building Trustworthy AI for Predictive Maintenance of Critical Care Medical Devices.
Available at: https://github.com/sanjidtalukder/Beyond-Accuracy-Building-Trustworthy-AI-for-Predictive-Maintenance-of-Critical-Care-Medical-Devices

---
