# SDNN-LGBM-IoT23
Proposed SDNN-LGBM for large-scale IoT intrusion detection.
SDNN–LGBM: Scalable Hybrid Deep Learning for Large-Scale IoT Intrusion Detection
Abstract-Level Summary

This repository provides a fully reproducible implementation of SDNN–LGBM, a hybrid deep learning framework for large-scale, multiclass intrusion detection in IoT network traffic. The model integrates a class-imbalance–aware deep neural network (DNN) with a LightGBM decision refinement layer operating on learned logit representations.

The framework is evaluated under two rigorously defined large-scale experimental scenarios using the IoT-23 dataset, enabling systematic comparison against a conventional DNN baseline under realistic distributional and generalization constraints.

Research Motivation

Deep learning–based intrusion detection systems (IDS) frequently report strong in-dataset performance but degrade under:

Severe class imbalance

Ultra-rare attack categories

Distribution shift

Fully disjoint evaluation settings

This project addresses these limitations by:

Investigating logit-space stacking for decision refinement

Analyzing macro vs. weighted metric divergence under extreme imbalance

Evaluating robustness under a strict 100% unseen test setting

The study emphasizes scalable experimentation on multi-million flow datasets rather than curated balanced subsets.

Experimental Design

Two large-scale evaluation scenarios are implemented:

Scenario 1 (S1): Standard Large-Scale Train–Test Split

Represents conventional large-sample evaluation while preserving natural class imbalance.

Scenario 2 (S2): Fully Disjoint Test Setting

Enforces strict separation between training and testing distributions, simulating real-world deployment conditions where test flows are entirely unseen.

Both scenarios compare:

Conventional DNN

Stacked DNN + LightGBM (SDNN–LGBM)

Methodological Contributions
1. Logit-Space Stacking Architecture

The SDNN–LGBM framework:

Trains an imbalance-aware DNN backbone

Extracts pre-softmax logits

Trains a LightGBM meta-learner on the logit space

Refines nonlinear decision boundaries across classes

This architecture leverages:

Representation learning (deep neural features)

Gradient-boosted tree decision refinement

Improved stability under class skew

2. Extreme Imbalance Analysis

The evaluation explicitly investigates:

Near-singleton test classes

Macro vs. weighted metric divergence

Minority-class sensitivity

The statistical impact of tiny-support categories on aggregate metrics

Unlike many IDS studies, this work does not remove ultra-rare classes, enabling realistic assessment of deployment behavior.

3. Large-Scale Reproducibility

The implementation supports:

Multi-million flow processing

Stratified splitting

Sample weighting

Explicit scenario control

Class-wise metric reporting

All experiments are designed to be fully reproducible with documented preprocessing and training pipelines.

Key Findings

SDNN–LGBM consistently outperforms conventional DNN in weighted F1-score and class-wise stability.

The hybrid architecture demonstrates robustness in fully disjoint evaluation (Scenario 2).

Performance degradation in macro metrics is shown to be driven primarily by extreme low-support classes rather than systemic model failure.

The stacking approach improves decision calibration in logit space compared to softmax-only classification.

Practical and Operational Relevance

This framework is applicable to:

Enterprise-scale IDS deployment

IoT gateway monitoring systems

Industrial IoT (IIoT) environments

Smart infrastructure networks

SOC (Security Operations Center) alert pipelines

The hybrid architecture is particularly valuable in operational settings where:

Rare attacks carry high impact

False alarms must be minimized

Traffic distributions evolve

Models must generalize beyond training data

Intended Audience

This repository is intended for:

Researchers in IoT network security

Graduate students studying imbalance-aware ML

Security practitioners investigating scalable IDS

ML researchers exploring hybrid deep + tree architectures

Dataset Availability

The experiments use IoT-23 network traffic.
Due to size constraints, datasets are not included in this repository and must be obtained from the official source.
