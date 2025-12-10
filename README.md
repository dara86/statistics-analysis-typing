# Data Science Portfolio
**Author:** Darragh Coyle
**Focus:** Statistical Inference, , and Data Visualization  
**Contact:** [Your LinkedIn Profile URL] | [Your Email]

## 📄 [Download Full Statistical Report (PDF)](./report.pdf)

# ⌨️ Man vs. Keyboard: A Statistical Audit of Human Performance

![Status](https://img.shields.io/badge/Status-Completed-success)
![Tools](https://img.shields.io/badge/Tools-R%20|%20Bayesian%20Inference%20|%20Regression-blue)
![Data](https://img.shields.io/badge/Data-Original%20(N=30)-green)

> **The Question:** Does "practice make perfect," or do environmental factors like caffeine and music play a larger role in motor learning efficiency?

## 📄 [Read the Full Statistical Report (PDF)](./report.pdf)

---

## 1. Executive Summary & Business Value
**Objective:** To optimize personal productivity and typing efficiency by identifying statistically significant performance drivers.
**Context:** In a data science career involving heavy keyboard usage, even a marginal increase in typing efficiency or accuracy translates to significant long-term time savings.
**Key Result:** Contrary to popular belief, the "Mozart Effect" was debunked for my workflow; listening to music **decreased** the probability of a high-performance session by **8.3%**.

---

## 2. Data Collection (Originality)
*Unlike standard datasets (e.g., Titanic, Iris), this project utilizes a novel, self-generated dataset.*
* **Source:** Longitudinal study over 4 weeks ($N=30$ trials).
* **Tools:** TypingTest.com (Data Generation), Excel/CSV (Data Entry).
* **Variables:**
    * **Performance:** WPM (Words Per Minute), Accuracy (%).
    * **Environment:** Caffeine (Y/N), Music (Y/N), Time of Day, Location (Public/Private).

---

## 3. Methodology (Rigor)
This analysis moves beyond simple descriptive statistics (averages) to inferential statistical modeling.

| Question | Statistical Test | Justification |
| :--- | :--- | :--- |
| **Does practice predict speed?** | `Linear Regression` | Modeled the learning curve to quantify exact WPM gain per trial. |
| **Does music help focus?** | `Bayesian Inference` | Updated prior beliefs ($P=0.5$) with observed data to calculate posterior probability. |
| **Do I work better in public?** | `Fisher's Exact Test` | Used due to small sample sizes in the contingency table to test independence. |

---

## 4. Key Findings & Actionable Insights
### 📉 The "Mozart Effect" is Negative
Using Bayes' Theorem, I calculated the posterior probability of a successful run (WPM > Median) given music was playing:
* **Prior Belief:** 50% chance of success.
* **Posterior Probability:** **41.7%** chance of success.
* **Action:** Deep work sessions requiring high precision should be done in silence.

### 📉 Practice $\neq$ Improvement
* **Result:** Linear regression showed a significant positive trend ($p=0.039$), but the $R^2$ was only **0.113**.
* **Interpretation:** Repetition explains only 11% of the variance. 89% of improvement is likely driven by **technique correction** (ergonomics) rather than volume of practice.

### 🏠 The "Public Workspace" Fallacy
* **Result:** I am statistically more likely to work in public during the day ($OR=0.167$).
* **Constraint:** This was identified as a confounding variable—libraries are closed at night, forcing private work, rather than a behavioral preference.

---

## 5. Visualizations
*(See full report for detailed R-generated plots)*

*Figure 1: Bayesian update showing the shift in probability when music is introduced.*

---

## 6. Reproducibility
To verify these results or apply this methodology to your own data:

1. **Load Data:**
   ```r
   df <- read.csv("data/typing_log.csv")

