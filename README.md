# Bayesian Decision-Analytic Framework for ERM Prevention in DME

This repository contains a standalone Python implementation of a Bayesian decision-analytic framework used to reinterpret borderline clinical trial evidence. It applies conjugate normal-update mechanics to evaluate **Faricimab T&E vs. Aflibercept** for epiretinal membrane (ERM) prevention in diabetic macular edema (DME), utilizing aggregate data derived from published trial data (Jaffe et al., *Retina* 2025).

## Key Features
* **Primary Bayesian Analysis:** Executes a conjugate normal update using a weakly regularizing prior to determine posterior medians and 95% credible intervals.
* **Clinical Thresholding:** Computes the exact posterior probability of achieving predefined clinically meaningful relative risk reductions.
* **Hypothesis Testing:** Quantifies evidence strength utilizing Bayes Factor analysis ($H_1: \text{OR} < 1.0$ vs. $H_0: \text{OR} \ge 1.0$).
* **ROPE Analysis:** Computes the probability that the treatment effect falls within a Region of Practical Equivalence ($\text{OR } 0.95 \text{ to } 1.05$).
* **Decision-Curve Analysis:** Computes and compares net clinical benefits across threshold probabilities to determine strategy preferences.
* **Sensitivity Analysis:** Tests the robustness of conclusions across multiple clinical priors (Skeptical, Primary, Optimistic, and Flat).

## Requirements & Setup

Ensure you have Python installed along with the required scientific computing libraries:

```bash
pip install numpy pandas scipy matplotlib seaborn
## Usage

Simply run the script in any Python environment (or as a Jupyter Notebook cell) to print the statistics tables and export five publication-ready validation plots:

```bash
python bayesian_analysis.py

```

### Generated Artifacts

* `Figure1_Prior_Posterior_ROPE.png` - Prior/Posterior probability density curves with ROPE bounds.
* `Figure2_Sensitivity.png` - Probability of any protective effect across varied priors.
* `Figure3_Bayes_Factor.png` - Standardized evidence metrics (Bayes Factors) across priors.
* `Figure4_Forest_Plot.png` - Frequentist Confidence Interval vs. Bayesian Credible Interval.
* `Figure5_Decision_Curve.png` - Net Benefit analysis across clinical decision thresholds.

```

```
