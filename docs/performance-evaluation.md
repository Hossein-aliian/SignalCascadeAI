# Performance Evaluation

## Overview

This page summarizes selected historical internal evaluation results reported during the development of SignalCascadeAI.

The values below are reproduced as reported. They are not independently audited or a guarantee of future performance.

## Model-Level OOF ROC-AUC

| Model | OOF ROC-AUC |
|---|---:|
| XGBoost | 0.8548 |
| LightGBM | 0.8529 |
| CatBoost | 0.8428 |
| GRU | 0.8331 |
| Meta-model | 0.8685 |

## Ensemble Evaluation

| Evaluation Stage | Metric | Reported Result |
|---|---|---:|
| Final Stacker — Phase 1 (80/20) | AUC | 0.8973 |

The precise evaluation-set definition and protocol for this Phase 1 result should accompany any more detailed external interpretation.

## OOF-Based Backtesting

| Metric | Reported Result |
|---|---:|
| Precision@14 | 0.9077 |
| Recall@14 | 0.4783 |
| Average Return After Signal | 0.3461 |
| Production Success Rate | 0.81 |

The figures are shown without converting or reinterpreting their units. In particular, the return unit and calculation convention, and the exact definition of Production Success Rate, have not been specified in this public summary.

## Evaluation Context

- Model-level ROC-AUC values are reported as OOF results.
- The reported backtesting workflow uses OOF-based predictions.
- Results reflect historical internal experiments and depend on the dataset, evaluation design, and market regime.
- Metrics should be compared only when their definitions, horizons, and evaluation protocols are consistent.
- Historical results do not imply or guarantee future returns or predictive performance.

## Interpretation Cautions

Precision, recall, ROC-AUC, return-related measures, and operational success measures describe different aspects of a predictive system. They should not be treated as interchangeable.

Before using the return-related or production success figures in formal external research, their calculation definitions, units, and evaluation scope should be documented.

## Reproducibility and Confidentiality

The public repository does not include source code, datasets, model artifacts, feature definitions, training configurations, or the proprietary procedures used to produce these results.

The purpose of this page is transparent high-level reporting, not independent reproduction.
