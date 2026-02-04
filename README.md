# Credit Card Approval Policy Design  
_Logistic Regression, Fisher Scoring, and Bayesian Robustness_

## Why this repository contains both a report and a policy-oriented presentation

This project originated as a final assignment for a Computational Statistics course at Bocconi University.
The academic requirement was to implement, from scratch, both frequentist and Bayesian estimation
methods for Generalized Linear Models — specifically logistic regression via Fisher Scoring
and Bayesian logistic regression via Random Walk Metropolis–Hastings.

The resulting report is therefore intentionally **theory-heavy**:
it includes analytical derivations, algorithmic details, convergence diagnostics,
and implementation choices required in a rigorous academic setting.

During development, the same technical work was reframed and extended into a
**decision-oriented credit approval problem**, closer to a real-world risk and policy setting.
This second layer focuses not on estimation alone, but on how model outputs
(probabilities and rankings) can be translated into operational approval policies
under asymmetric business costs.

For this reason, the repository contains two complementary artifacts:

- **Technical Report (Academic)**  
  Complete statistical documentation:
  derivations, Fisher scoring, MCMC via RW Metropolis–Hastings, diagnostics,
  and parameter interpretation.

- **Policy-Oriented Analysis / Presentation**  
  Decision-focused narrative:
  calibrated probabilities, cost-sensitive threshold selection,
  sensitivity analysis, operational three-way policies,
  segment diagnostics, and rule-based benchmarks.

In short:

- **Report** = statistical foundations and methodological rigor  
- **Policy analysis** = decision-making, trade-offs, and operational deployment

---

## What the project does

Using the CreditCard dataset, the project models credit card approval decisions via logistic regression.
The model is estimated using Fisher Scoring (MLE), with a Bayesian formulation used as a robustness check.

Rather than focusing solely on predictive accuracy, the analysis:
- evaluates probability calibration and ranking quality,
- explicitly models asymmetric costs of decision errors,
- selects approval thresholds by minimizing expected cost,
- extends binary decisions into a three-way policy
  (auto-approve / manual review / auto-decline),
- benchmarks the resulting policy against simple rule-based heuristics.

The final outcome is not a classifier, but a **transparent, cost-aware approval policy**
that is interpretable, stable, and operationally realistic.

---

## Repository structure

