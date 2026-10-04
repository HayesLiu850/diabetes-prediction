# Diabetes Prediction Model

I used R to explore the relationship between health measurements and diabetes, and built a logistic regression model that estimates the likelihood of a patient having diabetes.Inspired by the GeeksforGeeks tutorial "Diabetes Prediction using R". My implementation uses tidyverse and caret's preProcess, and I wrote the evaluation and prediction function myself.

## What I did
- Visualised the data with ggplot2 (outcome distribution, pregnancies and BMI by outcome)
- Scaled the features and split the data 70/30 into training and testing sets
- Built a logistic regression model with glm
- Evaluated it with precision, recall and F1-score
- Wrote a function that takes a patient's measurements and returns the estimated likelihood

## Data
Pima Indians Diabetes dataset (originally from the National Institute of Diabetes and Digestive and Kidney Diseases). I used the CSV linked in the GeeksforGeeks tutorial "Diabetes Prediction using R

## Results
- Precision: 0.7
- Recall: 0.62
- F1-score: 0.65

## Files
- `diabetes_report.Rmd`: the R Markdown source
- `index.html`: the knitted report
- `diabetes.csv`: the dataset

## How to run
1. Install R and the packages tidyverse, caret and Metrics.
2. Put `diabetes.csv` in the same folder as the `.Rmd` file.
3. Open the `.Rmd` in RStudio and click Knit.

## Limitations
- The dataset is small (768 patients) and covers one population: women aged 21 and over of Pima Indian heritage, so the model may not generalise to others.
- In several columns (glucose, blood pressure, skin thickness, insulin, BMI) a value of 0 is not physiologically possible and really means "not measured". I did not clean these.
- Results come from a single 70/30 split and a fixed 0.5 cutoff.
- This is a learning project and not medical advice.
