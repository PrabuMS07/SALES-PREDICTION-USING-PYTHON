

# 📈 Sales Prediction using Python 🐍

This project uses a Linear Regression model built with Python and Scikit-learn to predict product sales based on advertising spending across different media channels (TV, Radio, Newspaper).

## 📝 Project Overview

This repository contains a Python script (`your_script_name.py` - *please rename appropriately*) that performs the following:

1.  **Loads Data:** Reads the `advertising.csv` dataset (included in the repository).
2.  **Data Preparation:** Selects `TV`, `Radio`, and `Newspaper` spending as features (X) and `Sales` as the target variable (y).
3.  **Train-Test Split:** Divides the data into training (80%) and testing (20%) sets to evaluate the model's performance on unseen data (`random_state=42` ensures reproducibility).
4.  **Model Training:** Creates and trains a `LinearRegression` model using the training data.
5.  **Prediction:** Uses the trained model to predict sales figures for the test data.
6.  **Evaluation:** Calculates and prints the following performance metrics:
    *   **Mean Squared Error (MSE):** Measures the average squared difference between actual and predicted sales.
    *   **R-squared (R2) Score:** Indicates the proportion of the variance in sales that is predictable from the advertising features.
7.  **Coefficient Analysis:** Displays the coefficients learned by the model for each advertising channel (TV, Radio, Newspaper), indicating the estimated change in sales for a one-unit increase in spending on that channel, holding others constant.

## 💾 Dataset

*   **File:** `advertising.csv` (Included in this repository)
*   **Columns:**
    *   `TV`: Advertising dollars spent on TV for a single product in a given market (in thousands of dollars).
    *   `Radio`: Advertising dollars spent on Radio.
    *   `Newspaper`: Advertising dollars spent on Newspaper.
    *   `Sales`: Sales of a single product in a given market (in thousands of units).

## ✨ Features & Target

*   **Features (X):** `TV`, `Radio`, `Newspaper`
*   **Target Variable (y):** `Sales`

## ⚙️ Technologies & Libraries

*   Python 3.x
*   Pandas
*   Scikit-learn (`train_test_split`, `LinearRegression`, `mean_squared_error`, `r2_score`)

## 🛠️ Setup & Installation (using VS Code)

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/PrabuMS07/SALES-PREDICTION-USING-PYTHON.git
    cd SALES-PREDICTION-USING-PYTHON
    ```
2.  **Open Folder:** Open the cloned folder in Visual Studio Code (`File` > `Open Folder...`).
3.  **Python Interpreter:** Ensure you have a Python 3 interpreter selected in VS Code.
4.  **Terminal:** Open the integrated terminal in VS Code (`View` > `Terminal` or `Ctrl + \``).
5.  **(Optional but Recommended) Create Virtual Environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows PowerShell: .\venv\Scripts\Activate.ps1 or cmd: venv\Scripts\activate.bat
    ```
6.  **Install Dependencies:** Create a `requirements.txt` file in the folder with this content:
    ```txt
    pandas
    scikit-learn
    ```
    Then run the installation command in the terminal:
    ```bash
    pip install -r requirements.txt
    ```
7.  **Dataset:** The `advertising.csv` file is already included in the repository.

## ▶️ Usage (within VS Code)

1.  Make sure you have completed the Setup steps (and activated the virtual environment if created).
2.  Open your Python script file (e.g., `sales_predictor.py` - **you'll need to save the script code you provided into a `.py` file**) in the VS Code editor.
3.  Run the script from the VS Code terminal:
    ```bash
    python your_script_name.py
    ```
    *(Replace `your_script_name.py` with the actual name of your Python file)*

4.  **Output:** The script will print the following directly into the VS Code Terminal:
    *   The first 5 rows of the dataset (`data.head()`).
    *   The calculated `Mean Squared Error`.
    *   The calculated `R-squared` score.
    *   A table showing the `Coefficient` for each feature (TV, Radio, Newspaper).

## 📊 Interpreting the Results

*   **MSE:** Lower values indicate a better fit (less average error).
*   **R-squared:** Values closer to 1 suggest that the model explains a larger proportion of the variance in sales. An R2 of 0.90, for example, means 90% of the variability in sales can be explained by the variations in TV, Radio, and Newspaper advertising spend in this model.
*   **Coefficients:** These numbers estimate how much sales are expected to increase for each $1000 increase in advertising spend on that specific channel, assuming spending on the other channels remains constant. For example, a TV coefficient of 0.05 suggests that for every additional $1000 spent on TV ads, sales are predicted to increase by 0.05 thousand units (or 50 units), holding Radio and Newspaper spending constant.

## 💡 Potential Future Improvements

*   **Feature Scaling:** While Linear Regression isn't always strictly required to have scaled features (unlike distance-based models), scaling (`StandardScaler` or `MinMaxScaler`) can sometimes help with interpreting coefficients if features have vastly different scales and can be important for other model types or regularization.
*   **Explore Other Models:** Test other regression models (e.g., Ridge, Lasso, Random Forest Regressor, Gradient Boosting Regressor) to see if they provide better performance.
*   **Feature Engineering:** Investigate interaction terms (e.g., does TV advertising become more effective when combined with Radio advertising?) or non-linear transformations.
*   **Cross-Validation:** Implement k-fold cross-validation for a more robust estimate of the model's performance on unseen data.
*   **Visualization:** Add plots using `matplotlib` or `seaborn` to visualize the data (scatter plots of features vs. sales), residuals, etc.

---
