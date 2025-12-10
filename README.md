# AssumpHelp

AssumpHelp is a Python-based linear regression helper designed to make statistical assumptions, regression fitting, model summaries, and diagnostic checks easier for beginners and students.
It provides clear summaries, structured outputs, and a simple class-based design that organizes your full regression workflow.

[![Python 3.7+](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## Features

-Simple class-based interface (Hypothesis)
-Automatically fits OLS linear regressions
-Generates statsmodels-style summaries
-Computes regression assumptions (linearity, residual behavior)
-Provides prediction utilities
-Supports NumPy, Pandas, and arrays
-Easy to extend for school or beginner ML projects
-Clean and readable notebook workflow0=\k0\k

---

# Installation
Since this is a notebook-based project, dependencies must be installed manually.
# Install required packages:
```bash
pip install numpy pandas matplotlib scikit-learn statsmodels tqdm pyyaml requests
```
If you cloned the repository:

```bash
git clone https://github.com/yourusername/AssumpHelp.git
cd AssumpHelp
pip install -r requirements.txt
```
#   Using Our Library
```python
from hypothesis import Hypothesis
import numpy as np
import statsmodels.api as sm

# Example sample data
x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])

# Fit model
model = Hypothesis(x, y)
summary = model.fit()

# Show summary
print(summary)

# Predict using new data
prediction = model.predict(np.array([6, 7, 8]))
print(prediction)
```
# Example Output
```txt
OLS Regression Results  
============================================================
Dep. Variable:                      y   
Model:                            OLS   
Method:                 Least Squares   
No. Observations:                   5   
Df Residuals:                       3   
Df Model:                           1    
============================================================
coef    std err    t      p>|t|   [0.025   0.975]
-------------------------------------------------
β0      1.5000     0.7906   1.8974   0.1535
β1      0.7000     0.2280   3.0702   0.0547
============================================================
R-squared:                       0.7588
AIC:                            10.7319
BIC:                             9.9465
============================================================
```
# Summary:

1. Linearity (Check for a straight-line relationship)

Statistical Test: Ramsey RESET Test (Outputs the F-statistic and p-value).

Visual Plot: Residuals vs Fitted Plot (Look for a random scatter of points, a curve means a violation).

2. Homoscedasticity (Check for equal spread of errors)

Statistical Test: Breusch-Pagan Test (Outputs the BP-statistic and p-value).

Visual Plot: Scale-Location Plot (Look for a flat, horizontal line; a fanning shape means unequal spread).

3. Normality (Check if errors follow a bell curve)

Statistical Test: Shapiro-Wilk Test (Outputs the W-statistic and p-value).

Visual Plot: Normal Q-Q Plot (Check that most points follow the diagonal line; significant bending means non-normal errors).

4. Independence (Check for uncorrelated errors)

Statistical Test: Durbin-Watson (DW) Statistic (Outputs a single value for interpretation).

Visual Plot: Residuals vs Order Plot (Look for a random scatter of points over the observation index; patterns mean autocorrelation).
# Project Structure
```txt
├── AssumpHelp/
│   ├── __init__.py
│   ├── hypothesis.py
│   ├── linearity.py
│   ├── homoscedasticity.py
│   ├── normality.py
│   ├── independence.py
│   ├── utilities.py
│   ├── DiagnosticSummary.py  <-- Class for the final report
│   ├── linplot_interpretation_guide.txt
│   ├── homplot_interpretation_guide.txt
│   ├── normplot_interpretation_guide.txt
│   ├── indepplot_interpretation_guide.txt
│   └── test                   
├── examples/
│   └── (e.g., usage_notebook.ipynb)
├── tests/
│   └── sample
├── README.md
├── requirements.txt
├── setup.py
└── LICENSE
```


# When to Use AssumpHelp

Use this project if you want:

-A simple linear regression helper
-Easy-to-read summaries
-Minimal code complexity
-Perfect for school projects, assignments, and beginner ML learning


# Core Developers 
# (Creator of the Hypothesis class and full regression notebook.)
**[Kirsten Roise G. Moog & Rodel P. Badilla Jr.]** --> Inceptionist & Structural Design 
- Designed clean separation of concerns  
- Implementing codes engine  
- Created visualization tools
- Enhanced plotting capabilities  

**[James Walte Prollo, Zell Caamino, Hannah Dennisse Y. AQUE]** --> Testing & Documentation 
- Encouragement/Guidance (Encourage, Guide, and Back (support))
- Built comprehensive test suite  
- Wrote user documentation.
- Quality assurance  


# Special Thanks
- We are inspired to go beyond mere prediction; we seek the deep understanding and comprehensive diagnostics that only a robust statistical approach can  provide
  influend style by Statistical regression diagnostic assumptions. 




---
# Support
- Email: moog.kirstenroise@gmail.com
- Issues: GitHub Issues  
- Discussions: GitHub Discussions  
---

# Version 1.0 (Current)
-Basic OLS regression
-Statsmodels summary
-Prediction support

