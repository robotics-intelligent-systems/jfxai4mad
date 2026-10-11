# Natality-Incentive Probability Model — Research Proposal

## Status and provenance

Source: `docs/Para estructurar un enfoque.txt`, migration entry **64**.
Review date: **10 October 2026**. Original retained in
[Git history](https://github.com/robotics-intelligent-systems/jfxai4mad/blob/ea27e17f52d592ebc55f4ce41bf2384be5a4e752/docs/Para%20estructurar%20un%20enfoque.txt).

- Commit: `ea27e17f52d592ebc55f4ce41bf2384be5a4e752`.
- Git blob: `ccad8cebc3554d83831cb158f11c696e4559ea73`.
- SHA-256: `5b7a2ed4de4aa8ef347a5a4975ffc3557d2526a5dbccfa6d73059582084a4aa6`.


This note processes the source's first component: a GitHub-hosted probabilistic
model of fiscal subsidies, parental leave and direct support. The second component
and the user's requested **age-13 focus for Djibouti, GitHub and Discord** are
documented in the [companion threshold review](../child-protection/age-13-djibouti-github-discord-and-travel-review.md).
Platform-account eligibility and travel permissions do not define the modeled
fertility outcome.

## Proposed repository layout

The draft suggests a separate `natality-incentive-model` repository. No repository
or executable model is created by this documentary migration.

```text
natality-incentive-model/
├── README.md
├── requirements.txt                 # pandas, numpy, pymc, scikit-learn candidates
├── data/
│   ├── historical_births.csv         # demographic baseline by cohort
│   └── policy_costs.csv              # fiscal/social policy costs
├── models/
│   ├── bayesian_inference.py
│   └── simulation.py                 # proposed Monte Carlo scenarios
└── outputs/
    └── probability_curves.png        # proposed visualization, not a result
```

The four packages are unpinned source suggestions, not installed dependencies.
Versions, licenses, input units, provenance and reproducibility must be recorded
before an implementation is released.

## Source code, normalized for readability

The function, constants and sampling call below preserve the supplied sketch.
Comments are translated; this is **unexecuted exploratory code**.

```python
import numpy as np
import pymc as pm

def run_natality_simulation(incentive_budget_per_capita, historical_data):
    with pm.Model() as model:
        # Hypothetical priors for baseline and incentive response.
        alpha = pm.Normal("alpha", mu=1.2, sigma=0.3)
        beta = pm.Normal("beta", mu=0.05, sigma=0.01)
        expected_tfr = alpha + beta * incentive_budget_per_capita
        obs = pm.Normal(
            "obs", mu=expected_tfr, sigma=0.1, observed=historical_data
        )
        trace = pm.sample(
            2000, return_inferencedata=False, target_accept=0.9
        )
    return trace
```

## Model interpretation and gaps

These findings follow from the sketch, rather than an executed experiment:

| Item | Meaning or unresolved limitation |
| --- | --- |
| `expected_tfr` | A linear mean for total fertility rate, not a probability between zero and one. TFR and crude birth rate are different measures. |
| Input data | `historical_births.csv` suggests counts, but the likelihood expects outcomes on the same scale as the proposed TFR mean. Cohort/time definitions and denominators are missing. |
| Budget | Currency, price year, population denominator, exposure period and scaling are unspecified. A fixed scalar budget identifies only the combination alpha + beta × budget from that likelihood. |
| Priors | 1.2, 0.3, 0.05, 0.01 and observation sigma 0.1 are hypothetical constants; no calibration evidence is supplied. The beta prior strongly favors positive response. |
| Likelihood | A normal outcome can generate negative TFR values; aggregation, measurement error and a suitable support/link require review. |
| Policy effect | Fitting an association alone does not establish the causal impact of subsidies or parental leave. |
| Sampling | No seed, explicit chain/tuning configuration, diagnostics or predictive checks are specified. |
| Imports and artifacts | NumPy is unused in the sketch; pandas/scikit-learn, Monte Carlo scenarios and the output chart have no implementation here. |

PyMC documents sampling controls including seeds, chains and convergence checks;
the original call is retained without claiming current-version compatibility.
[PyMC sampling reference](https://www.pymc.io/projects/docs/en/stable/api/generated/pymc.sample.html)

OECD research examines family-policy/fertility associations in a cross-country
panel, providing contextual research rather than calibration of this sketch.
[OECD study](https://www.oecd.org/en/publications/fertility-employment-and-family-policy_326844f0-en.html)

## Proposed validation and reporting

1. Define aggregate outcomes, eligible policy population, cohort/year units,
   observation uncertainty and a lawful source dataset.
2. Match the likelihood to the outcome; calibrate and stress-test priors.
3. Use varying policy exposures and a defensible comparison design for any causal
   claim; document confounding, lags and selection.
4. Pin dependencies and record seed, sampling settings, diagnostics and posterior
   predictive checks.
5. Define policy success explicitly, for example a population-level outcome
   exceeding a stated delta under a specified budget horizon. Report posterior
   uncertainty; distinguish predictive scenarios from causal estimates.
6. Review results before publishing curves. Do not infer individual reproductive
   decisions from platform profiles or account-age eligibility.

No demographic data were imported, no MCMC was run and no probability of policy
success was estimated. Related planning:
[Tourism and young-household incentives](../../strategy/tourism-and-young-household-incentives.md).
[Research index](../README.md) · [Documentation index](../../README.md)
