# 🗾 Exploratory Data Analaysis (EDA) on the Heart Failure Prediction dataset

The [Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction) is a publicly available dataset which is a collection of clinical data used to predict the presence of heart disease.

---

## 🔑 Key objectives

-   Our main objective is to perform `Univariate`, `Bivariate`, and `Multivariate` analysis to see what features are important to predict heart disease in a patient.

-   We'll check out the dataset and see if there are any missing values in it.

-   Then, we'll plot individual features into `countplot` and `histplot` using `matplotlib` and `seaborn`.

-   We'll plot two and more features at once too.

-   Lastly, we'll see which features are correlated using `Pearson's correlation algorithm` and `heatmap`.

---

## 📊 Observations from the EDA

-   First, the dataset is loaded using `pandas` and it is explored to see it's contents.

-   There weren't any missing values but some wrong values for `Cholesterol` and `Blood Pressure` features were found.

---

### From the `Univariate` analysis, the following results were observed:

1.  **Heart Disease**: There are more patients with heart disease. There are about `400` patients without heart disease and `500` patients with heart disease.

2.  **Gender**: There are significantly more male patients than female patients.

3.  **Age Distribution**: Minimum age and maximum age of patients are `28` and `77` respectively. Most patients are in the age group of `50-60`.

4.  **Resting Blood Pressure**: Majority patients have their blood pressure in the range of `125` to `150`.

5.  **Type of Chest Pain**: Among all the four different types of heart pain, most patients have `Asymptomatic (ASY)` pain in their chest.

---

### From the `Bivariate` analysis, we saw the following:

1.  **Gender, & Heart Disease**: Male patients have a higher chance of having heart disease rather than female patients.

2.  **Chest Pain Type, & Heart Disease**: Among all the different types of chest pain type, the patients with `Asymptomatic (ASY)` pain have the highest chance of having heart disease.

3.  **Blood Pressure, & Heart Disease**: Patients with blood pressure in the range of `125` to `140` have high probability of getting heart disease.

4.  **Blood Sugar, & Heart Disease**: Patients with less than or equal to `120 mg/dl` blood sugar level have a fifty-fifty chance of having heart disease. Whereas, patients with more than `120 mg/dl` blood sugar are more likely having heart disease.

5.  **Cholesterol, & Heart Disease**: Cholesterol level of `100-300` in patients are signs of patients having heart disease.

---

### After the `Multivariate` anaysis, we can see:

1.  **Blood Sugar, Chest Pain Type, & Heart Disease**: Patients with blood sugar level more than `120 mg/dl` and `Asymptomatic (ASY)` pain in their chest have a high chance of having heart disease.

2.  **ECG, Angina, & Heart Disease**: Patients who have `Angina` by doing exercise and have ECG results as `ST` have the highest chance of getting heart disease.

3.  **Gender, Chest Pain Type, Angina, & Heart Disease**: The plot shows that `male` patients with `Asymptomatic (ASY)` pain who have `Angina` by doing exercise have the highest chance of having heart disease.

4.  **Paitplot**: We also plot all the numerical features in pair-wise using `pairplot` and saw all the different types of charts and plots.

### Correlation Heatmap

-   We plotted the correlation matrix using `Pearson's correlation algorithm` and `seaborn.heatmap` for the numerical features.

-   The matrix has both positive and negetive correlation between pairs of features.

-   Among all of them, the maximum positive correlation of `0.40` was seen between `Oldpeak` and `HeartDisease` features.

-   The maximum negetive correlation of `-0.40` was seen between `MaxHR` and `HeartDisease` features.

-   There are two pairs who have the minimum correlation value of `0.05`
    -   `Oldpeak` and `Cholesterol`
    -   `FastingBS` and `Oldpeak`

---

## 🎬 Conclusion

-   We can conclude that their are many features that are related with each other with this EDA.

-   This EDA can help us understand how heart disease can be avoided and predicted.

-   All of the study was related to this dataset only, and may not be `100%` correct in the real world.
