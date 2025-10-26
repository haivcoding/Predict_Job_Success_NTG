# Predicting Success Rate for Job Listings  in the Northern Territory
## Acknowledgements
This project was developed in collaboration with Cong Do Le, Van Hieu Tran, Khai Quang Thang at Charles Darwin University (CDU).
# Context
In many labour-markets — including in Australia — the successful filling of job vacancies depends on a mix of job-design, applicant supply, and local workforce conditions. Studies using online job-advertisement data have shown factors such as salary, education requirements, experience demands and posting intensity are strong predictors of whether roles are filled or become skill-shortages.

At the same time, broader social-environmental features — for example local education attainment, crime rates or neighbourhood socioeconomic disadvantage — may influence both the available applicant base and the attractiveness or retention of a job role (a kind of “neighbourhood effect”).

The project proposes to build a predictive model of job-fulfilment (vacancy filled or not) based on advertised job characteristics and to explore whether social factors (like crime or education levels in the region) add explanatory power.

# Objective
* **Predict the likelihood of a job vacancy being successfully filled** based on key features in job advertisements such as salary, department, classification level, vacancy type, and region.
* **Examine the influence of social factors** (e.g. crime rates, education levels) on job fulfilment outcomes across different Northern Territory regions.

# Dataset
1. **Advertised NTG Jobs (Mar 2019 – Feb 2021)**
   Contains detailed job advertisement information including department, salary range, classification level, employment type, region, number of applicants, and vacancy status.
   *Source:* [https://data.nt.gov.au/dataset/advertised-ntg-jobs](url)

2. **Crime by Region (2019 – 2021)**
   Provides aggregated crime statistics by region, representing a social indicator that may influence job attraction and fulfilment.
   *Source:* NT Police, Fire and Emergency Services annual crime data.

3. **Education Levels (2019 – 2021)**
   Includes regional data on educational attainment, such as the percentage of population with tertiary or vocational qualifications.
   *Source:* [https://data.nt.gov.au/dataset/?q=education](url)
.
# Methodology
1. **Data Pre-processing**

   * Cleaned missing or inconsistent job fields (e.g. salary range, department names).
   * Normalised social indicator variables (crime and education) for comparison across regions.
   * Encoded categorical job attributes (vacancy type, classification, department, etc.) for model input.

2. **Exploratory Data Analysis (EDA)**

   * Analysed feature distributions, correlations, and relationships between job characteristics and fulfilment rates.
   * Visualised regional variations in job fulfilment, crime rates, and education levels.

3. **Model Development**

   * Tested several machine learning models: **Naive Bayes, Logistic Regression, Decision Tree, Random Forest, K-NN, and ANN**.
   * Identified **Random Forest** as the best-performing model with **74.08% accuracy** using the top 8 features after feature selection and hyperparameter tuning.

4. **Socioeconomic Impact Analysis**

   * Integrated regional crime and education variables to examine whether these social factors improve predictive accuracy or explain fulfilment disparities between urban and remote areas.

5. **Insights & Application**

   * Identified key determinants of successful job fulfilment.
   * Provided data-driven recommendations to improve recruitment strategies in NTG departments.

# Key findings & Recommendations
1. **Recruitment Challenges**

* Approximately **24.12% of NT businesses reported vacancies in 2023**, equating to around **7,000 unfilled positions**.
* As of 2024, there were **2,233 vacancies in Darwin** and **996 across regional NT**, showing the persistent challenge of attracting and retaining workers in regional and remote areas.

---

2. **Predictive Modelling Outcomes**

* The project aimed to predict whether a job vacancy would be **successfully filled** using features extracted from job advertisements.
* Multiple models were tested, including **Naive Bayes (NB), Logistic Regression (LR), Decision Tree (DT), Random Forest (RF), K-Nearest Neighbours (K-NN)** and **Artificial Neural Network (ANN)**.
* The **Random Forest model** produced the **best performance**, achieving **74.08% accuracy** after:

  * **SMOTE** data balancing,
  * **Feature selection**, and
  * **Hyperparameter optimisation** (via Random and Grid Search).

---

3. **Top Predictive Features**

From over 50 variables, the **five most influential factors** (based on Random Forest feature importance ranking) were:

1. **Number of Applicants**
2. **Salary Range**
3. **Department**
4. **Classification Level**
5. **Vacancy Type**

Less influential factors included **Region**, **Number of Vacancies**, and **Remoteness**.

---

4. **Feature Selection Insight**

* Forward feature selection indicated that **only 8 features** were sufficient to achieve near-optimal predictive accuracy (74.08%), improving efficiency without significant loss in model performance.
* This demonstrates that a small subset of meaningful job attributes can effectively explain job fulfilment likelihood.

---

5. **Case Testing**

Two sample job cases were tested to validate model behaviour:

* **Case 1:** Ongoing (Permanent) – Full Time – $80K – Department of Health – Management level – Central Region – Very Remote → **Predicted Success**
* 
<img width="896" height="471" alt="image" src="https://github.com/user-attachments/assets/1ea1d82f-3851-4ce9-858c-c1dfc195ac69" />

* **Case 2:** Fixed (Temporary) – Full Time – $120K – Department of Trade, Business and Innovation – Intermediate level – Darwin Region – Outer Regional → **Predicted Failure**
* 
<img width="882" height="471" alt="image" src="https://github.com/user-attachments/assets/e44d33ed-38ac-4d68-8541-90a171e494a3" />

  * When job characteristics (e.g. region, pay structure, position type) were adjusted, the model predicted improved fulfilment likelihood, showing its potential to guide **strategic job-ad design**.

<img width="906" height="494" alt="image" src="https://github.com/user-attachments/assets/315cb3ce-ce7d-4adb-940e-58117030d963" />

<img width="944" height="477" alt="image" src="https://github.com/user-attachments/assets/9815e3f3-f666-4827-9b7a-3792b0fd5ad7" />

6. **Conclusions**

* Predictive analytics can reliably estimate the **probability of job fulfilment** using existing job-ad data.
* Incorporating **social variables** (e.g. crime, education) may further enhance model interpretability by explaining **regional workforce disparities**.
* Findings can support **data-driven recruitment policies** to increase the success rate of NTG job fulfilment, particularly in **remote and hard-to-fill sectors**.

<img width="2075" height="1193" alt="image" src="https://github.com/user-attachments/assets/1a0b38a3-727b-439a-903e-ba9456f331aa" />







