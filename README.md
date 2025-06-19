<div align="center">

# Software Test Effort Estimation using Ensemble Learning

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![Scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![XGBoost](https://img.shields.io/badge/XGBoost-006600?style=for-the-badge&logo=xgboost&logoColor=white)

</div>

## 📝 Overview

This project explores the application of ensemble machine learning algorithms to enhance the accuracy of software test effort estimation. Traditional estimation methods often rely on expert judgment or historical data, which can be subjective and unreliable as project complexity increases. This work leverages several machine learning models to provide a more precise and scalable solution for predicting the time, resources, and cost required for software testing activities.

## 🎯 Problem Statement

In software engineering, accurate test effort estimation is critical for managing project schedules and allocating resources efficiently. Conventional approaches often fail to capture the intricacies of modern software systems, leading to inaccurate predictions. This project aims to overcome these limitations by conducting a comparative analysis of multiple machine learning algorithms to identify the most effective strategy for estimating software test effort.

## 🛠️ Methodology

The methodology for this project involved several key stages:

1.  **Data Collection:** The dataset was sourced from the PROMISE Repository of Software Engineering Databases, a well-known resource for software engineering data.

2.  **Data Preprocessing:** The dataset, which comprises up to 81 records and 13 attributes, was preprocessed to handle missing values and scale numerical features. 'Effort' was designated as the target variable.

3.  **Feature Extraction:** A correlation matrix and the SHAP (SHapley Additive exPlanations) framework were employed to analyze and select the most significant features for the prediction task.

4.  **Model Training:** Four distinct ensemble learning models were chosen for evaluation:

    * XGBoost
    * LightGBM
    * A Stacked Ensemble
    * Random Forest

5.  **Evaluation:** The performance of each model was quantitatively analyzed and compared using standard regression metrics, including Mean Squared Error (MSE), Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R2 Score.

## 📊 Results

The comparative analysis showed that while all tested models were promising, the Random Forest algorithm demonstrated superior performance.

| **Algorithm** | **RMSE** | **MSE** | **MAE** | **R2 score** |
| :----------------- | :--------- | :--------- | :--------- | :----------- |
| XGBoost            | 0.3004     | 0.9025     | 0.2081     | 0.2926       |
| LightGBM           | 0.2514     | 0.6322     | 0.1887     | 0.5044       |
| Stacked Ensemble   | 0.2574     | 0.6628     | 0.2120     | 0.48         |
| **Random Forest** | **0.2306** | **0.5318** | **0.1781** | **0.5831** |

The **Random Forest** model achieved the lowest error metrics and the highest R2 score, indicating its effectiveness in capturing the variance in the data and providing the most accurate predictions.

## 🚀 How to Run

To run this project, you can use the provided Jupyter Notebook (`ensemble_try.ipynb`).

### Prerequisites

* Python 3.x
* Jupyter Notebook or Google Colab

### Installation

1.  Clone the repository:
    ```bash
    git clone [your-repo-link]
    ```

2.  Install the required dependencies. The primary dependencies are listed in the notebook and can be installed via pip.
    ```bash
    pip install pandas scikit-learn xgboost lightgbm shap
    ```

### Execution

1.  **Download the dataset:** The dataset used for this project is `02.desharnais.csv` from the PROMISE repository. You can download it directly from [this link](http://promise.site.uottawa.ca/SERepository/datasets/desharnais.arff) (note: it will download as an `.arff` file which may need to be converted to `.csv`, or you can find a `.csv` version online). Place the file in the project's root directory.

2.  Open `software_ensemble.ipynb` in Jupyter or Google Colab.

3.  Run the cells sequentially to load the data, train the models, and view the evaluation results.

## 💻 Technologies Used

* **Languages:** Python
* **Libraries:**
    * Pandas
    * NumPy
    * Scikit-Learn
    * XGBoost
    * LightGBM
    * SHAP
    * Matplotlib

## 📜 License

This project is released under the MIT License. It was developed as part of an academic requirement and is shared for educational and research purposes. See the `LICENSE` file for more details.
