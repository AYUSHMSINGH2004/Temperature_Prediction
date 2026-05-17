# 🌡️ Temperature Prediction using Linear Regression

## 📌 Project Overview
This project focuses on predicting environmental **temperature** based strictly on **humidity** data. By leveraging atmospheric sensor data, the project establishes a baseline relationship between these two meteorological variables using a Linear Regression model.

## 📊 Dataset
The model is trained on the `humidity.csv` dataset, which contains hourly or daily environmental sensor readings. 

**Dataset Highlights:**
* The raw dataset contains a total of 701,548 entries.
* **Features:** Includes `sensor_id`, `lat`, `lon`, and `pressure`.
* **Independent Variable (X):** `humidity`.
* **Target Variable (y):** `temperature`.
* Temperatures in the dataset range from -145.12 to 61.17, while humidity ranges from 0.0 to 100.0.

## ⚙️ Workflow & Methodology
1. **Data Ingestion:** Loaded the raw sensor data using Pandas.
2. **Exploratory Data Analysis (EDA):** Generated summary statistics and visualized the relationship between humidity and temperature using a Seaborn scatter plot.
3. **Data Preprocessing:** Cleaned the dataset by dropping rows with missing values using `dropna()`. 
4. **Model Training:** Split the data into 80% training and 20% testing sets (using `random_state=42`) and trained a **Linear Regression** model using Scikit-Learn.
5. **Evaluation:** Tested the model's accuracy on the testing set using standard statistical metrics.

## 📈 Results & Performance
The simple linear regression model was evaluated against the unseen test data, yielding the following results:
* **Mean Squared Error (MSE):** 144.08
* **R-squared (R2) Score:** 0.26

*Note: A scatter plot visualizing the predicted regression line against the actual test data is available in the notebook to show the model's fit.*

## 🛠️ Technologies Used
* **Python** * **Pandas** & **NumPy** (Data manipulation and analysis)
* **Scikit-Learn** (Machine Learning modeling and evaluation)
* **Matplotlib** & **Seaborn** (Data visualization)
* **Jupyter Notebook** (Development environment)

## 🚀 How to Run Locally
1. Clone the repository and navigate to the project directory.
2. Ensure you have the required libraries installed:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn jupyter
3. Open the Jupyter Notebook:
   ``` bash
   jupyter notebook "Completed_Temperature Prediction_Test.ipynb"

4. Run all cells to view the data processing, model training, and evaluation plots.

🔮 Future Scope

While this simple linear regression model provides a foundational look at the data, weather patterns are complex. Future iterations of this project will consider using polynomial regression or time-series models to capture more complex, non-linear relationships.
