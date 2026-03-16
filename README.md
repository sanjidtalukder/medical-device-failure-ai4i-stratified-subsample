# Modified Machine Failure Dataset

## Overview

This repository contains a **Modified Machine Failure Dataset** designed for research in **predictive maintenance, machine learning, and industrial data analysis**. The dataset includes machine operational parameters, environmental conditions, engineered features, and rule-based indicators to help analyze machine behavior and predict failures.

The dataset is useful for developing and evaluating **machine learning models for failure prediction and anomaly detection in industrial systems**.

---

## Dataset File

* **File Name:** `Modified_Machine_Failure_Dataset.csv`
* **Format:** CSV
* **Rows:** 2000
* **Columns:** 29

Each row represents a **single machine operational observation** with associated sensor measurements and failure indicators.

---

## Dataset Features

### Identification Columns

| Column     | Description                                          |
| ---------- | ---------------------------------------------------- |
| UDI        | Unique dataset identifier                            |
| Product ID | Product identifier for each machine                  |
| Type       | Machine type (L = Low, M = Medium, H = High quality) |
| id         | Internal record identifier                           |

---

### Sensor Measurements

| Column                  | Description                             |
| ----------------------- | --------------------------------------- |
| Air temperature [K]     | Ambient air temperature in Kelvin       |
| Process temperature [K] | Process temperature of the machine      |
| Rotational speed [rpm]  | Rotational speed of the machine         |
| Torque [Nm]             | Torque applied during machine operation |
| Tool wear [min]         | Tool wear duration in minutes           |

---

### Failure Labels

| Column            | Description                          |
| ----------------- | ------------------------------------ |
| Machine failure   | Original failure indicator           |
| Machine failure.1 | Secondary failure label              |
| failure           | Final target variable for prediction |

---

### Rule-Based Indicators

| Column           | Description                                  |
| ---------------- | -------------------------------------------- |
| rule_tachycardia | Indicator for abnormal high-speed behavior   |
| rule_tachypnea   | Indicator for abnormal operational condition |
| rule_temp        | Temperature rule violation                   |
| rule_wbc         | Additional anomaly detection rule            |

---

### Aggregated Risk Indicators

| Column              | Description                                          |
| ------------------- | ---------------------------------------------------- |
| clinical_flag       | Flag triggered when abnormal conditions occur        |
| meets_clinical_rule | Indicates if system meets predefined rule conditions |
| clinical_risk_score | Aggregated risk score from rule indicators           |

---

### Engineered Features

| Column                  | Description                                    |
| ----------------------- | ---------------------------------------------- |
| thermal_gradient        | Difference between process and air temperature |
| power_estimate          | Estimated mechanical power output              |
| wear_rate_indicator     | Indicator of tool wear rate                    |
| operating_regime        | Machine operational state                      |
| seq_index               | Sequential observation index                   |
| time_since_last_failure | Time since last failure event                  |
| temp_stability          | Stability of temperature readings              |
| wear_acceleration       | Rate of increase in tool wear                  |
| operating_hours_proxy   | Estimated machine operating hours              |

---

### Encoded Feature

| Column       | Description                        |
| ------------ | ---------------------------------- |
| Type_encoded | Numerical encoding of machine type |

---

## Target Variable

The primary prediction target is:

```
failure
```

Where:

* **0 → No Failure**
* **1 → Machine Failure**

This makes the dataset suitable for **binary classification problems**.

---

## Possible Applications

This dataset can be used for:

* Predictive maintenance research
* Machine failure prediction
* Industrial machine learning applications
* Anomaly detection
* Feature engineering experiments
* Model benchmarking

---

## Example Usage (Python)

```python
import pandas as pd

# Load dataset
df = pd.read_csv("Modified_Machine_Failure_Dataset.csv")

# Display first rows
print(df.head())

# Dataset shape
print(df.shape)

# Target distribution
print(df['failure'].value_counts())
```

---

## License

This dataset is provided for **research and educational purposes only**.

---


