# SignalCascadeAI

### Financial Intelligence & Predictive Analytics for the Iranian Stock Market

**SignalCascadeAI** is an independently developed, proprietary financial machine learning system focused on quantitative research and predictive signal analysis in the Iranian stock market.

The project investigates market patterns associated with smart-money activity and seeks to identify equities that may exhibit significant price appreciation. It brings together financial data engineering, sequential deep learning, ensemble machine learning, specialized learning strategies, and leakage-resistant temporal evaluation.

> **Public technical showcase:** This repository documents selected research areas, engineering approaches, and reported evaluation outcomes. It does not contain the production source code, trained models, real market data, or proprietary implementation details.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Technical Approach](#technical-approach)
- [Temporal Validation & Information Integrity](#temporal-validation--information-integrity)
- [Reported Evaluation Results](#reported-evaluation-results)
- [Engineering Focus](#engineering-focus)
- [Technology Stack](#technology-stack)
- [Documentation](#documentation)
- [Repository Scope & Confidentiality](#repository-scope--confidentiality)
- [Author](#author)

---

## Project Overview

Financial markets are dynamic and non-stationary. Developing useful predictive systems in this environment requires careful treatment of temporal information, imbalanced outcomes, changing market behavior, and the practical cost of incorrect predictions.

SignalCascadeAI was designed as a multi-stage research system to:

- Analyze financial time-series and market behavior.
- Investigate patterns associated with accumulation and smart-money activity.
- Identify potentially significant price movements.
- Combine complementary machine learning models.
- Evaluate predictive signals through temporally disciplined validation and backtesting.

The system is tailored to the data characteristics and market structure of the Iranian stock market.

---

## Technical Approach

The project combines several machine learning paradigms rather than depending on a single estimator.

### Sequential deep learning

The system uses **PyTorch-based GRU networks** for sequential financial time-series modeling. The recurrent modeling component incorporates customized architectural configurations and task-specific hyperparameter optimization.

### Ensemble learning

The modeling ecosystem includes:

- XGBoost
- LightGBM
- CatBoost
- GRU-based recurrent neural networks
- Meta-model learning
- Ensemble-based predictive integration

The purpose of this combination is to leverage complementary modeling capabilities across different representations of financial data.

### Specialized learning strategies

The research includes high-level approaches designed for the asymmetric nature of financial prediction tasks:

- Customized convex weighting strategies
- Asymmetric loss optimization
- Magnitude-aware regression
- Decision-oriented predictive integration

These strategies are intended to improve the prioritization of potentially meaningful signals while controlling false-positive predictions. Their formulas, parameters, and implementation details are proprietary and are not disclosed in this repository.

---

## Temporal Validation & Information Integrity

Temporal integrity is treated as a system-wide engineering requirement.

The validation methodology includes:

- Out-of-Fold (OOF) training and prediction workflows.
- Explicit temporal shifting and Shift-1 information alignment.
- Purge-window mechanisms aligned with the decision horizon.
- Leakage-aware feature engineering.
- Temporal validation across modeling stages.
- OOF-based ensemble evaluation and backtesting.

These practices are intended to preserve the boundary between information available at prediction time and information that becomes available later. The methodology is described at a conceptual level; implementation-specific split logic and temporal parameters remain private.

---

## Reported Evaluation Results

The following figures are reported from the project's internal model evaluation and backtesting workflows.

### Model-level OOF ROC-AUC

| Model | OOF ROC-AUC |
|---|---:|
| XGBoost | 0.8548 |
| LightGBM | 0.8529 |
| CatBoost | 0.8428 |
| GRU | 0.8331 |
| Meta-model | 0.8685 |

### Ensemble evaluation

| Evaluation | Result |
|---|---:|
| Final Stacker — Phase 1 AUC | **0.8973** |

### OOF-based backtesting

| Metric | Reported result |
|---|---:|
| Precision@14 | 0.9077 |
| Recall@14 | 0.4783 |
| Average Return After Signal | 0.3461 |
| Production Success Rate | 0.81 |

**Interpretation and limitations**

- Model-level ROC-AUC values are reported from Out-of-Fold evaluation.
- Ensemble evaluation uses OOF-based predictive outputs.
- Backtesting was performed using OOF-based predictions.
- These are historical internal results, not guarantees of future performance.
- Return and production-success figures should not be interpreted beyond their underlying metric definitions. Their units and calculation conventions are not specified in this public summary.
- Results may vary with market regime, data coverage, execution assumptions, and evaluation methodology.

For additional context, see [Performance Evaluation](docs/performance-evaluation.md).

---

## Engineering Focus

Key engineering challenges considered during development include:

**Market non-stationarity** — modeling behavior that can change across market regimes and time periods.

**Class imbalance** — handling uneven outcome distributions without allowing aggregate metrics to obscure weaker cases.

**False-positive control** — accounting for the operational cost of incorrect predictive signals.

**Magnitude-aware prediction** — distinguishing potentially meaningful price movements from less significant outcomes.

**Temporal information integrity** — maintaining prediction-time information boundaries throughout feature engineering, training, evaluation, and backtesting.

---

## Technology Stack

| Area | Technologies |
|---|---|
| Programming | Python |
| Data processing | NumPy, Pandas |
| Deep learning | PyTorch, GRU |
| Machine learning | Scikit-learn |
| Gradient boosting | XGBoost, LightGBM, CatBoost |
| Evaluation | ROC-AUC and task-specific backtesting metrics |

---

## Documentation

The following documents provide additional context about the project's scope and engineering work:

| Document | Description |
|---|---|
| [Project Overview](docs/project-overview.md) | Motivation, objectives, and project scope |
| [System Capabilities](docs/system-capabilities.md) | High-level capabilities and research areas |
| [Technical Contributions](docs/technical-contributions.md) | Summary of selected technical approaches |
| [Validation Methodology](docs/validation-methodology.md) | Temporal validation and leakage-resistant evaluation principles |
| [Performance Evaluation](docs/performance-evaluation.md) | Reported metrics and evaluation context |
| [Engineering Challenges](docs/engineering-challenges.md) | Main research and engineering challenges |
| [Confidentiality](docs/confidentiality.md) | Intellectual property and disclosure boundaries |

---

## Repository Scope & Confidentiality

This repository is a **public technical showcase**, not the production software distribution.

It intentionally excludes:

- Proprietary source code and executable components.
- Trained model artifacts and private datasets.
- Internal module implementations and system orchestration.
- Custom mathematical formulations and optimization parameters.
- Feature definitions, transformations, and selection logic.
- Label-generation and decision-making methodologies.
- Private configurations, logs, and operational workflows.

The published material is intended for professional, research, and portfolio presentation. No part of this repository should be treated as a reproducible implementation of the production system.

**All rights reserved.**

---

## Author

**Hossein Alian**  
Financial Machine Learning | Quantitative Research | AI Systems Engineering

- [LinkedIn](https://www.linkedin.com/in/hossein-alian-465b5a224/)
- [GitHub](https://github.com/Hossein-aliian)

---

*Independent research and development at the intersection of financial markets, sequential machine learning, and quantitative intelligence systems.*
