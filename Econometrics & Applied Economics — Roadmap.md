# Econometrics & Applied Economics — Roadmap

> Step-by-step learning roadmap with projects, resources, repo structure and milestones. Designed for beginners → advanced practitioners who want a reproducible portfolio for hiring or research.

---

## Table of contents

1. [Overview & outcomes](#overview--outcomes)
2. [How to use this roadmap](#how-to-use-this-roadmap)
3. [Prerequisites & setup](#prerequisites--setup)
4. [Learning timeline (suggested)](#learning-timeline-suggested)
5. [Core learning path (step-by-step)](#core-learning-path-step-by-step)
6. [Projects (detailed) — buildable portfolio items](#projects-detailed--buildable-portfolio-items)
7. [Advanced topics & research projects](#advanced-topics--research-projects)
8. [Tools, libraries & cheat-sheet](#tools-libraries--cheat-sheet)
9. [Data sources & reproducibility tips](#data-sources--reproducibility-tips)
10. [GitHub repo template & workflow](#github-repo-template--workflow)
11. [Evaluation rubric & next steps](#evaluation-rubric--next-steps)
12. [Suggested reading & courses (books & online)](#suggested-reading--courses)

---

## Overview & outcomes

By following this roadmap you will be able to:

* Understand and implement classical and modern econometric methods (OLS, IV, panel, time-series, causal inference).
* Design and execute applied empirical research projects with clean code, reproducible notebooks, visualizations, and a short write-up replicating an academic-style analysis.
* Use Python and/or R for data cleaning, estimation, inference, and forecasting.
* Communicate results professionally on GitHub (README, notebooks, figures, short paper).

Target audiences: undergraduates in economics, early data scientists wanting econometrics, research assistants, junior quants, and policy analysts.

---

## How to use this roadmap

1. Clone the repo template (see `GitHub repo template` section).
2. Follow the timeline most suited to your weekly availability (suggestions below).
3. For each topic: read the recommended short chapters/notes, work through guided notebooks, then complete the project linked to that stage.
4. Keep every project in its own folder with: `notebook`, `src/` scripts, `data/` (or data link), `results/` figures, and `README.md`.

---

## Prerequisites & setup

**Math & stats:**

* Basic calculus (derivatives) — helpful but not strict.
* Linear algebra (vectors, matrix algebra, inversion, eigenvalues) — important for multiple regression and PCA.
* Probability & statistics (distributions, expectation, variance, CLT, hypothesis testing).

**Coding:**

* Comfortable with one of: Python (preferred by many applied researchers) or R.
* Git & GitHub basics (commit, branch, pull request).
* Jupyter notebooks (or R Markdown / Quarto) for reproducible reports.

**Environment (suggested):**

* Python: 3.9+ with `pandas`, `numpy`, `statsmodels`, `linearmodels`, `scikit-learn`, `matplotlib`, `seaborn`, `econml`/`dowhy` (optional), `arch`, `pmdarima`.
* R: R 4.x with `tidyverse`, `plm`, `fixest`, `AER`, `lmtest`, `sandwich`, `urca`, `forecast`, `vars`.
* Use `conda` or `venv` and keep `requirements.txt` / `environment.yml` for reproducibility.

---

## Learning timeline (suggested)

> Timeline assumes \~12–15 hours/week. Adjust up/down depending on availability.

**Phase 0 — Prep (1–2 weeks):** Git, Python/R basics, Jupyter, refresh linear algebra & probability.

**Phase 1 — Fundamentals (6–8 weeks):** OLS, inference, heteroskedasticity, functional forms, model selection.

**Phase 2 — Applied microeconometrics (6–8 weeks):** Causal inference (IV, diff-in-diff, RDD), panel data, fixed effects.

**Phase 3 — Time series & forecasting (6–8 weeks):** ARIMA, stationarity, cointegration, VAR, forecasting practice.

**Phase 4 — Advanced & ML for causal/forecasting (8–12 weeks):** GMM, limited dependent variable models, treatment effect estimators, synthetic control, machine-learning methods for causal inference and forecasting.

**Capstone & publishing (4–8 weeks):** Replication of a published applied paper or original research, clean write-up, and polished GitHub repo.

Total: \~6–9 months for a solid portfolio (part-time). Intensify for full-time study.

---

## Core learning path (step-by-step)

### Stage A — Foundations (Week 1–6)

**Topics:** descriptive statistics, probability refresher, linear regression (simple & multiple), OLS derivation, Gauss–Markov assumptions, hypothesis testing, confidence intervals.

**Hands-on:** implement OLS from scratch (matrix formula) and using `statsmodels`/`lm()`; produce diagnostic plots (residuals, leverage, Cook's D).

**Mini-project A (Portfolio Item 1) — "Basline OLS analysis":**

* **Goal:** Analyze the relationship between education and wages using a cross-sectional dataset (e.g., public dataset like `Adult` or `CPS` sample).
* **Deliverables:** `notebook` with EDA, OLS estimations, diagnostics, short `README.md` with interpretation.
* **Skills practiced:** data cleaning, EDA, OLS, interpretation, plotting.

---

### Stage B — Violations of OLS & fixes (Week 7–10)

**Topics:** heteroskedasticity, clustered SEs, multicollinearity, omitted variable bias, functional form, transformations.

**Hands-on:** compute robust standard errors, implement variance-covariance estimators, run model selection (AIC/BIC), use polynomial/splines.

**Mini-project B (Portfolio Item 2) — "Heteroskedasticity & robust SEs":**

* Re-run Stage A with robust SEs and clustering (e.g., cluster by region/state).
* Add sensitivity analysis: alternate specifications, interaction terms, non-linear fit.

---

### Stage C — Causal inference & microeconometrics (Week 11–20)

**Topics:** instrument variables (IV/2SLS), difference-in-differences (DiD), regression discontinuity (RD), matching, propensity scores, panel data (fixed/random effects), Hausman test.

**Hands-on:** implement 2SLS (both `statsmodels` and `linearmodels`), DiD with event-study plots, running RDD using local linear regressions.

**Project C1 (Portfolio Item 3) — "IV: Education and Earnings":**

* Classic exercise: use an instrument (e.g., distance to college / quarter of birth — depending on dataset) to estimate causal returns to schooling.
* Deliverables: pre-analysis plan, code, figures, robustness checks (weak instrument tests, overidentification tests).

**Project C2 (Portfolio Item 4) — "DiD: Policy evaluation":**

* Use a natural experiment (minimum-wage change, policy rollout) to estimate treatment effects using DiD and event-study.
* Deliverables: notebook, common-trend checks, placebo tests, interpretation.

**Project C3 (Portfolio Item 5) — "RDD":**

* Find a dataset with a sharp cutoff (test scores, eligibility threshold) and estimate treatment effect with local polynomials and bandwidth sensitivity.

---

### Stage D — Panel data & longitudinal methods (Week 21–26)

**Topics:** fixed effects, random effects, difference estimators, dynamic panel (Arellano–Bond), correlated random effects, within transformation, clustered SEs.

**Project D (Portfolio Item 6) — "Panel: Wage dynamics or firm productivity":**

* Use panel data (e.g., panel of countries, firms, individuals) to estimate fixed-effects model, include time dummies, test for serial correlation, use Arellano-Bond if necessary.
* Deliverables: notebook with estimation, tests, interpretation; code packaged in `src/`.

---

### Stage E — Time series & forecasting (Week 27–34)

**Topics:** stationarity (ADF, KPSS), AR(p), MA(q), ARIMA, seasonal models, cointegration, VECM, VAR, impulse response functions, forecast evaluation (RMSE, MAPE), volatility modeling (ARCH/GARCH).

**Hands-on:** build forecasting pipelines with `statsmodels` (or R `forecast`) and `pmdarima`'s auto\_arima. Create rolling forecasts and backtests.

**Project E (Portfolio Item 7) — "Macro forecasting with FRED":**

* Choose macro variables (GDP, unemployment, inflation). Build a VAR/ARIMA forecasting model, evaluate with rolling windows, produce policy-relevant impulse responses.
* Deliverables: Jupyter notebook, forecasts, evaluation table, short notebook summary.

---

### Stage F — Modern causal methods & ML for economics (Week 35–44)

**Topics:** synthetic control, generalized synthetic control, double/debiased machine learning (DML), causal forests, heterogeneous treatment effects, uplift modeling. Also GMM and limited dependent models (logit, probit, tobit).

**Hands-on:** use `econml`/`grf` (R) for heterogenous effects, implement synthetic control for policy evaluation.

**Project F (Portfolio Item 8) — "Causal ML / HTE":**

* Apply causal forest or DML to estimate heterogeneous treatment effects in the DiD or RCT-style dataset.
* Deliverables: notebook with model tuning, HTE plots, policy takeaways.

---

### Stage G — Capstone (Week 45–56)

**Options:**

* **Replication:** pick a recent applied economics paper and replicate the main empirical table(s). Document data sources and differences.
* **Original applied research:** combine methods learned to answer a novel policy question. End with a short paper and presentation slide deck.

**Capstone deliverables:** full repo with `notebooks/`, `src/`, `results/`, figures, `paper/` (2–6 pages), and `README` explaining motivation, data, methods, and findings.

---

## Projects (detailed) — buildable portfolio items

For every project, follow this folder structure and documentation standards so recruiters/researchers can run your code easily.

**Standard project README checklist:**

* Motivation + research question
* Data source & link (or `scripts/download_data.py`)
* `requirements.txt` / `environment.yml`
* How to run (commands)
* Key findings (one paragraph)
* License

**Project difficulty & timeline estimation:** label each one `easy/medium/hard` and estimate `1–3 / 2–4 / 4–8 weeks` accordingly.

(Projects list repeated from previous sections — each includes datasets suggestions: World Bank, FRED, CPS, IPUMS, Kaggle, OECD, UCI.)

---

## Advanced topics & research projects

* Structural estimation (discrete choice, dynamic programming)
* Spatial econometrics (spatial lag, spatial error models)
* Bayesian econometrics (MCMC, Stan / PyMC)
* Nonlinear time series & high-frequency econometrics
* Micro-econometrics of networks and social interactions

**Advanced research capstone ideas:**

* Structural model of labor supply under policy change.
* Bayesian estimation of DSGE reduced form dynamics.
* Spatial diffusion of economic shocks and policy responses.

---

## Tools, libraries & cheat-sheet

**Python quick list:**

* Data: `pandas`, `numpy`
* Estimation: `statsmodels`, `linearmodels` (panel & IV), `scikit-learn` (ML parts)
* Causal ML: `econml`, `dowhy`, `causalml`
* Time-series: `statsmodels.tsa`, `arch`, `pmdarima`
* Visualization: `matplotlib`, `seaborn`, `plotly` (optional)

**R quick list:**

* Data wrangling: `tidyverse`
* Estimation: `plm`, `fixest`, `AER`
* Time series: `forecast`, `vars`, `urca`
* Causal inference: `MatchIt`, `rdrobust`, `Synth`, `did`

**Command-line / productivity:**

* `git`, `make` (optional), `pre-commit` hooks for linting, `nbstripout` for cleaning notebooks before committing.

---

## Data sources & reproducibility tips

**Public data sources:**

* FRED (Federal Reserve Economic Data) for macro time series
* World Bank / WDI for cross-country indicators
* IPUMS / CPS for micro-level household / labor surveys
* OECD for many country-level stats
* Kaggle / UCI for sample datasets when testing methods

**Reproducibility tips:**

* Provide data download scripts (if data is public) rather than storing heavy data in repo.
* Pin package versions, provide `requirements.txt` / `environment.yml`.
* Use notebooks for exploration and scripts for productionized analysis under `src/`.
* Add a `Binder` or `Dockerfile` if you want others to run your environment easily.

---

## GitHub repo template & workflow

**Suggested repo structure:**

```
README.md
LICENSE
requirements.txt
environment.yml
.gitignore
/data (or scripts to download)
/notebooks
/src
/results
/figures
/paper

```

**Workflow hints:**

* Keep long computations out of notebooks — wrap into `src/` scripts and call them.
* Use `notebooks/` for narrative and visual exploration only.
* Add clear contribution guidelines if collaborating.

---

## Evaluation rubric & next steps

**Rubric for judging a project:**

* Reproducibility: environment + data download scripts (0–20)
* Code quality: modular, documented, testable (0–20)
* Econometric rigor: correct assumptions, diagnostics, robustness checks (0–30)
* Communication: clear README, concise interpretation, and policy takeaway (0–20)
* Visuals & presentation: clarity and insightfulness of figures (0–10)

**Next steps:**

* Pick one `easy` project and finish it end-to-end within 1–2 weeks.
* Share the GitHub link and ask for a targeted code review.

---

## Suggested reading & courses

**Core books** (order of study):

1. *Introductory Econometrics: A Modern Approach* — Jeffrey M. Wooldridge (great for applied micro and causal inference)
2. *Mostly Harmless Econometrics* — Joshua Angrist & Jörn-Steffen Pischke (concise, intuitive causal methods)
3. *Introduction to Econometrics* — James H. Stock & Mark W. Watson (good mix of time-series and cross-section)
4. *Time Series Analysis* — James D. Hamilton (advanced time-series)
5. *Econometric Analysis* — William H. Greene (reference for several advanced topics)

**Useful online course types to search for:**

* University lectures on Econometrics (MIT OCW, LSE, Stanford)
* Coursera: econometrics introductory and applied courses
* edX / MicroMasters programs (macro & development economics specializations)

---

## Quick checklist to publish a finished project on GitHub

* [ ] Project folder has `README.md` describing the question and findings.
* [ ] `notebooks/` contains an explainer notebook with runnable cells.
* [ ] `src/` contains scripts and utilities; functions are reusable.
* [ ] `requirements.txt` or `environment.yml` included.
* [ ] Data access instructions or `scripts/download_data.py` included.
* [ ] Figures exported to `figures/` and referenced by README.
* [ ] Short `paper/` (2–6 pages) summarizing method and results.

---


