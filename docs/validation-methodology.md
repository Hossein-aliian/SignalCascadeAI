# Validation Methodology

## Overview

Financial time-series evaluation requires careful control of when information becomes available. SignalCascadeAI treats temporal integrity and leakage prevention as core engineering requirements.

The following summary describes the validation approach at a high level. It is not an implementation guide.

## Out-of-Fold Workflows

Out-of-Fold (OOF) workflows are used in model training and predictive evaluation.

The project also uses OOF-based outputs in downstream ensemble evaluation and backtesting. This is intended to keep evaluation grounded in predictions generated through the defined validation workflow.

## Temporal Information Alignment

The methodology incorporates explicit temporal shifting, including a Shift-1 mechanism, to support prediction-time information alignment.

The exact implementation semantics and data transformations are proprietary and are not described in this public document.

## Purge-Window Controls

Purge-window mechanisms are used in temporal validation and are aligned with the applicable decision horizon.

Specific window sizes, split arrangements, and implementation details are intentionally withheld.

## Leakage-Aware Engineering

Leakage prevention is considered across multiple aspects of the research workflow, including feature preparation, temporal validation, model evaluation, and backtesting.

The term **leakage-resistant** is used deliberately: it describes the engineering objective and controls without making an absolute claim that any empirical system is universally free of leakage.

## Evaluation Scope

Reported model-level OOF metrics, ensemble evaluation results, and backtesting outcomes are summarized in [Performance Evaluation](performance-evaluation.md).

Those results should be interpreted within their stated evaluation context. They do not establish that future market behavior will match historical observations.

## Confidentiality

This document does not publish:

- Exact split or fold construction
- Purge-window lengths
- Feature timing or transformation rules
- Internal target or label construction
- Model training configurations
- Operational data-flow details

These omissions are intentional protections for the proprietary system.
