# 📊 A/B Testing Simulation with Statistical Power Analysis

> **Statistical Experimentation / Hypothesis Testing**

An experiment exploring how **A/B testing and statistical power analysis** can be used to evaluate whether a change in a product experience leads to a statistically significant improvement in conversion rate.

The project simulates user behavior for **control and treatment groups**, applies a **two-proportion z-test**, performs **power analysis**, and uses **Monte Carlo simulation** to validate empirical statistical power and Type I error.

---

## 🔍 What I Explored

This experiment focused on understanding the complete workflow of a statistical A/B test:

* 🧪 **Hypothesis Testing** — comparing conversion rates between two groups
* 📐 **Power Analysis** — determining the required sample size
* 📏 **Effect Size** — measuring the magnitude of the expected improvement
* 🎲 **User Simulation** — generating conversion outcomes using binomial trials
* 🔁 **Monte Carlo Simulation** — validating empirical statistical power and Type I error
* 📊 **Statistical Interpretation** — evaluating both significance and effect size

---

## 🏗️ A/B Testing Workflow

The overall workflow can be represented as:

```text
Define Baseline Conversion Rate
            │
            ▼
      Define Expected
         Effect
            │
            ▼
      Power Analysis
            │
            ▼
    Determine Sample Size
            │
            ▼
     Simulate User Data
        ┌───┴───┐
        ▼       ▼
    Control  Treatment
        │       │
        └───┬───┘
            ▼
  Two-Proportion Z-Test
            │
            ▼
  Statistical Significance
            │
            ▼
   Monte Carlo Simulation
            │
       ┌────┴────┐
       ▼         ▼
Empirical Power  Type I Error
```

This workflow demonstrates how **experimental design, statistical testing, and simulation-based validation** can be combined in an A/B testing experiment.

---

## 🧪 Hypothesis Testing

The experiment uses a **two-proportion z-test** to determine whether the conversion rates of the control and treatment groups differ significantly.

The hypotheses are:

```text
H₀: pA = pB

H₁: pA ≠ pB
```

where:

* `pA` = conversion rate of the control group
* `pB` = conversion rate of the treatment group

The resulting **p-value** is compared against the selected significance level to determine whether the observed difference provides sufficient evidence to reject the null hypothesis.

---

## 📐 Statistical Power Analysis

Power analysis is performed before simulation to estimate the sample size required to detect a meaningful difference between the two conversion rates.

The analysis considers:

* Baseline conversion rate
* Expected conversion-rate improvement
* Significance level `α`
* Desired statistical power
* Effect size

This helps ensure that the experiment has a sufficient number of observations to detect the expected effect.

---

## 🎲 User Behavior Simulation

Synthetic user behavior is generated using **binomial trials**.

Each simulated user produces a binary outcome:

```text
User
 │
 ├── Conversion → 1
 │
 └── No Conversion → 0
```

Separate conversion probabilities are defined for the control and treatment groups, allowing different experimental scenarios to be simulated and evaluated.

---

## 🔁 Monte Carlo Validation

The statistical experiment is repeated multiple times using Monte Carlo simulation.

This allows the theoretical properties of the hypothesis test to be compared with empirical results.

The simulation evaluates:

* **Empirical Statistical Power** — how frequently a true effect is detected
* **Empirical Type I Error** — how frequently a false positive occurs when the null hypothesis is true

The results provide an additional validation of the statistical methodology used in the experiment.

---

## 📊 Effect Size — Cohen's h

The experiment uses **Cohen's h** to quantify the difference between the control and treatment conversion rates.

Effect size provides additional context beyond statistical significance by describing the magnitude of the observed or expected difference.

This is important because a statistically significant result does not necessarily represent a practically meaningful improvement.

---

## 📁 Repository Structure

```text
ab-testing-simulation/
│
├── ab_testing_simulation.ipynb
├── requirements.txt
└── README.md
```

### File Description

* `ab_testing_simulation.ipynb` → Complete A/B testing experiment and analysis
* `requirements.txt` → Required Python dependencies
* `README.md` → Project documentation

---

## ▶️ Run the Project

Clone the repository:

```bash
git clone https://github.com/prachiputhran/ab-testing-simulation.git
cd ab-testing-simulation
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Launch the Jupyter Notebook:

```bash
jupyter notebook ab_testing_simulation.ipynb
```

---

## 🛠️ Technologies

* **Python**
* **NumPy** — numerical computation and simulation
* **SciPy** — statistical testing
* **Statsmodels** — power analysis and statistical methods
* **Matplotlib** — data visualization
* **Seaborn** — statistical visualization
* **Jupyter Notebook** — experimentation environment

---

## 🧠 What I Learned

This experiment provided practical experience with the statistical foundations of controlled experimentation.

Key concepts explored include:

* Designing an A/B test using control and treatment groups
* Performing two-proportion hypothesis testing
* Using power analysis for sample-size planning
* Measuring effect size using Cohen's h
* Simulating conversion behavior using binomial distributions
* Validating statistical behavior through Monte Carlo simulation
* Understanding the relationship between statistical significance, power, and Type I error

The overall experimentation workflow can be summarized as:

> **Design → Simulate → Test → Validate → Interpret**

---

## 📚 Reference

[svg](https://github.com/prachiputhran/ab-testing-simulation#-reference)

* [Statsmodels Documentation](https://www.statsmodels.org/?utm_source=chatgpt.com)
* [SciPy Documentation](https://docs.scipy.org/doc/scipy/?utm_source=chatgpt.com)
* [NIST/SEMATECH e-Handbook of Statistical Methods](https://www.itl.nist.gov/div898/handbook/?utm_source=chatgpt.com)
