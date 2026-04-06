# Credit-Risk-Modelling-and-Work-Queue-Optimization

Built an ML-Powered Credit Risk Scoring System to Optimize Credit Hub Operations

In most lending institutions, credit appraisal still runs on a first-come-first-served (FIFO) model. During month-end, when file inflow spikes 3x, appraisers are overwhelmed, TATs blow up, and premium customers wait in the same queue as clear-cut rejections.

I tried building a machine learning system around this.

# The Problem:
•  Manual credit assessment: 3-5 days per file

•  Applicant drop-offs due to slow turnaround

•  No differentiation between a premium P1 customer and a high-risk P4 file

•  Credit hub productivity tanks during peak periods

# What I Built:
An ML-based credit risk prediction system that classifies 42,000+ loan applications into 4 risk segments (P1 to P4) and routes them into intelligent work queues.

# Technical Approach:
•  Merged CIBIL bureau data (62 features) with customer demographics (26 features)

•  Feature selection using VIF, ANOVA, and Chi-Square tests — reduced 79 features to the most predictive set

•  Handled class imbalance (P2-dominant dataset) with balanced sample weighting

•  Trained Gradient Boosting Classifier with RandomizedSearchCV hyperparameter tuning

•  Validated with 5-Fold Cross Validation using F1 Macro scoring 

# The Smart Queue System:
•  P1 (Premium) → FAST_TRACK: 4-hour TAT, auto-assigned to senior appraiser

•  P2 (Standard) → NORMAL QUEUE: 36-hour TAT

•  P3 (Complex) → REVIEW_NEEDED: 48-hour TAT, routed to experienced appraisers

•  P4 (Clear Decisions) → QUICK APPROVE/REJECT: 24-hour TAT
