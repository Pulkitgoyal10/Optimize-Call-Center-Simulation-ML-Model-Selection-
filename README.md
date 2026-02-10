# Optimizing Call Center Operations: Simulation, ML Modeling, and TOPSIS Ranking

## 📌 Project Overview
This project demonstrates the integration of **Discrete Event Simulation (DES)**, **Machine Learning (ML)**, and **Multi-Criteria Decision Making (MCDM)**. 

We simulate a **Call Center environment** using `SimPy` to generate a synthetic dataset of 1000 operational days. Using this data, we train five different Machine Learning models to predict the **Average Wait Time** for customers. Finally, we apply **TOPSIS** (Technique for Order of Preference by Similarity to Ideal Solution) to rank the ML models and identify the best one based on multiple performance metrics ($R^2$, RMSE, MAE).

---

## ⚙️ Methodology

### Step 1: Simulation (SimPy)
We used the `SimPy` library to model a **Single-Server Queue (M/M/c)** system.
- **Scenario:** Customers arrive at random intervals and request service from a limited number of agents.
- **Parameters:**
  - `Number of Agents` (2-6): Resources available.
  - `Service Time` (5-15 mins): Time taken to resolve a query.
  - `Arrival Interval` (2-6 mins): Frequency of incoming calls.
- **Output:** `Average Wait Time` for 1000 different simulation runs.

### Step 2: Machine Learning (Scikit-Learn)
We treated this as a **Regression Problem** to predict *Wait Time*.
**Models Trained:**
1. Linear Regression
2. Random Forest Regressor
3. Gradient Boosting Regressor
4. K-Neighbors Regressor
5. Decision Tree Regressor

### Step 3: Model Selection (TOPSIS)
We evaluated the models using a custom TOPSIS package (`Topsis-Pulkit-102303800`).
- **Criteria:** $R^2$ Score (Maximize), RMSE (Minimize), MAE (Minimize).
- **Weights:** `1,1,1`
- **Impacts:** `+,-,-`

---

## Sample Simulated Data

<img width="446" height="354" alt="image" src="https://github.com/user-attachments/assets/c01a90ed-a915-49b7-9dd2-975f84854fba" />

---

## Sample Model Performance

<img width="569" height="204" alt="image" src="https://github.com/user-attachments/assets/569a7176-e3f3-450e-ab84-3522eed92b19" />

---

## Sample Result Ranking

<img width="629" height="198" alt="image" src="https://github.com/user-attachments/assets/8d5fe413-3620-4a8e-91c7-20f6b70dfad3" />


---
## 🛠️ Installation & Usage

To replicate this project, install the required dependencies:

```bash
pip install simpy pandas numpy scikit-learn matplotlib seaborn
pip install Topsis-Pulkit-102303800
