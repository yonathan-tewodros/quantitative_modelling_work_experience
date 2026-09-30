# Quantitative Modelling in Python

## Work Experience Notebook

This repository contains a practical introduction to **quantitative modelling using Python**.

The notebook is designed for someone with limited experience of quantitative modelling. It starts with the fundamentals and gradually builds towards regression, machine learning and time-series forecasting.

The emphasis is not on memorising Python commands or statistical formulas. Instead, the aim is to understand **how analysts approach a modelling problem** and why different modelling techniques are appropriate in different situations.

---

## What you'll learn

The notebook covers:

1. **Python and data analysis**

   * Loading and inspecting data
   * Summary statistics
   * Missing values
   * Correlations
   * Data visualisation

2. **Ordinary Least Squares (OLS) regression**

   * Dependent and independent variables
   * Regression coefficients
   * Intercepts
   * Residuals
   * $R^2$ and adjusted $R^2$
   * P-values and statistical significance
   * Making predictions

3. **Model evaluation**

   * Training and test data
   * Mean Absolute Error (MAE)
   * Root Mean Squared Error (RMSE)
   * $R^2$
   * Overfitting and underfitting

4. **Alternative regression models**

   * Ridge regression
   * Lasso regression

5. **Classification**

   * Logistic regression
   * Probabilities
   * Classification thresholds
   * Accuracy and confusion matrices

6. **Machine learning**

   * Random forests
   * Nonlinear relationships
   * Feature importance

7. **Time-series modelling**

   * Time as an additional dimension
   * Lagged variables
   * Chronological train/test splits
   * Forecasting
   * Look-ahead bias

8. **Mini-project**

   * Building a simple commodity-price forecasting model
   * Using price, demand, inventory and sentiment
   * Comparing modelling approaches
   * Thinking critically about model assumptions and forecasting information

---

## Getting started

### 1. Install Python

You will need Python 3 installed on your computer.

A convenient option is to use **Anaconda**, although a standard Python installation also works.

### 2. Install the required packages

Open a terminal and run:

```bash
pip install numpy pandas matplotlib seaborn statsmodels scikit-learn jupyter
```

If you are using a Jupyter notebook, you can alternatively run:

```python
%pip install numpy pandas matplotlib seaborn statsmodels scikit-learn
```

> **Note:** The package is called `scikit-learn`, but it is imported in Python using `sklearn`.

### 3. Open the notebook

Open:

```text
quantitative_modelling_work_experience.ipynb
```

You can run it using:

* Jupyter Notebook
* JupyterLab
* VS Code with the Jupyter extension
* another compatible notebook environment

---

## How to use the notebook

The notebook is designed to be interactive.

You will find three types of sections:

### Read

These sections explain a concept before you use it.

### Run

These sections contain working Python code demonstrating the concept.

### Your turn

These sections contain exercises where you should try something yourself before looking at the solution or continuing.

Don't worry if you don't understand everything immediately. The objective is to **experiment with the code and ask questions**.

---

## The modelling workflow

The notebook follows a simplified version of a real quantitative modelling workflow:

```text
Define the question
        ↓
Understand the data
        ↓
Explore the relationships
        ↓
Build a simple model
        ↓
Check assumptions
        ↓
Evaluate the model
        ↓
Try alternative approaches
        ↓
Test on unseen data
        ↓
Interpret the results
        ↓
Communicate the conclusions
```

One of the most important lessons is that **building the model is only part of the job**.

A good quantitative analyst also needs to understand:

* where the data came from
* what the variables actually measure
* whether the assumptions are reasonable
* whether the results make sense
* whether the model generalises to new data
* what limitations the analysis has

---

## Important concepts

### Correlation is not causation

Two variables can move together without one causing the other.

For example, two variables might both be driven by a third variable.

Regression can help us quantify relationships, but simply obtaining a statistically significant coefficient does not automatically establish causation.

### More complicated does not necessarily mean better

A random forest or other machine-learning model may capture relationships that a linear regression cannot.

However, a simple model can sometimes be preferable because it is:

* easier to understand
* easier to explain
* easier to diagnose
* less prone to overfitting
* more appropriate for the available data

The best model depends on the **question, data and objective**.

### Out-of-sample performance matters

A model can fit historical data extremely well while performing poorly on new observations.

This is why we separate training and test data and evaluate models on observations they did not use during fitting.

### Time-series data are different

When predicting the future, we must respect the order of observations.

We cannot normally train on future observations and test on the past.

This introduces concepts such as:

* lagged variables
* forecasting horizons
* look-ahead bias
* autocorrelation
* stationarity

---

## Final mini-project

The final section puts everything together.

You are given a synthetic commodity-price dataset containing:

* commodity price
* demand
* inventory
* sentiment

Your task is to investigate whether these variables can help explain and forecast commodity prices.

You should think about:

> **What information would actually have been available at the time the forecast was made?**

This is particularly important in real-world forecasting.

For example, if an economic indicator is published three months after the period it describes, it may not be available when making a forecast today.

---

## Questions to think about

As you work through the notebook, consider:

1. Why might a model with a high $R^2$ still be a poor forecasting model?
2. Why doesn't correlation necessarily imply causation?
3. What happens when two explanatory variables contain very similar information?
4. Why might a simple model sometimes be preferable to a complicated one?
5. Why is a random train/test split potentially problematic for time-series data?
6. What happens if an explanatory variable is only available after the forecast date?
7. Why might sentiment provide useful information at a higher frequency than some fundamental variables?
8. What would you want to know before building a real commodity-price model?

---

## A note on the data

The datasets used in the notebook are **synthetic**.

They are deliberately constructed to demonstrate modelling concepts without requiring external data sources.

The results should therefore not be interpreted as real-world economic or financial forecasts.

The final commodity example is intended to demonstrate the modelling process rather than provide an actual commodity-price prediction.

---

## Suggested approach

Don't try to rush through the notebook.

For each model, ask yourself three questions:

### 1. What problem does this model solve?

For example:

> OLS can estimate a linear relationship between an outcome and explanatory variables.

### 2. What assumptions does it make?

For example:

> OLS relies on assumptions about the relationship between the explanatory variables and the error term.

### 3. How do we know whether the model is useful?

For example:

> We can evaluate its performance on observations that weren't used to fit it.

If you can answer those three questions, you're learning much more than simply learning how to run the Python code.

---

## Required packages

The notebook uses:

```text
numpy
pandas
matplotlib
seaborn
statsmodels
scikit-learn
```

These can be installed with:

```bash
pip install numpy pandas matplotlib seaborn statsmodels scikit-learn
```

---

## Enjoy the modelling!

The main objective of this exercise is to develop **curiosity about data**.

When you see a dataset, don't immediately ask:

> "Which machine-learning model should I use?"

Instead, start with:

> **"What am I trying to understand, what does the data tell me, and what assumptions am I making?"**

That mindset is at the heart of quantitative analysis.
