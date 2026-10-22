# delhivery-delay-intelligence-capstone-pulkit
# Logistics Delay Prediction Project

This repository contains an end-to-end data science pipeline designed to clean logistics data, perform exploratory data analysis, train predictive models for shipment delays, and package the final model for inference.

## 📁 Repository Structure

```text
repository/
├── README.md                  # Project overview and documentation
├── requirements.txt           # Python dependencies
├── generate_data.py           # Script to generate synthetic logistics data
├── data/                      # Data directory (ignored by git if large)
│   ├── hubs.csv               # Distribution hub metadata
│   ├── raw_shipments.csv      # Raw historical shipments
│   ├── new_shipments.csv      # Unseen data for prediction
│   └── modelling_table.csv    # Final cleaned features used for training
├── src/
│   └── shipment_prep.py       # Modular data processing functions
├── part_a_clean_eda.py        # Step A: Data cleaning & EDA
├── part_b_regression.py       # Step B: Continuous delay time regression
├── part_c_classification.py   # Step C: Binary delay classification
├── part_d_segments.py         # Step D: Customer/Route segment analysis
├── package_model.py           # Serializes and saves the final pipeline
├── predict_delay.py           # Production inference script
└── models/                    # Saved artifacts
    ├── delay_model.pkl        # Trained model file
    ├── delay_threshold.csv    # Threshold limits for classification
    ├── feature_order.csv      # Required tracking order of features
    └── impute_values.csv      # Default values for missing data handling
```

## 🚀 Getting Started

### 1. Prerequisites
Ensure you have Python 3.8+ installed. 

### 2. Installation
Clone the repository and install the required dependencies:
```bash
git clone https://github.com
cd your-repo-name
pip install -r requirements.txt
```

### 3. Running the Pipeline
Run the scripts in alphabetical order to execute the pipeline:

1. **Generate Data:** `python generate_data.py`
2. **EDA & Cleaning:** `python part_a_clean_eda.py`
3. **Train Models:** `python part_b_regression.py` and `python part_c_classification.py`
4. **Package Model:** `python package_model.py`
5. **Predict New Delays:** `python predict_delay.py`

## 🛠️ Tech Stack
* **Python** (Pandas, NumPy, Scikit-Learn)
* **Visualization:** Matplotlib, Seaborn
* **Model Deployment:** Pickle
