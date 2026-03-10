# Lithium-ion Battery SOH Estimation

This repository contains the Python implementation of the battery state-of-health (SOH) estimation model described in the paper:

"Practical SOH Estimation Based on Feasible Feature Weighted Li-ion Battery Model"

## Project Background

Lithium-ion battery state-of-health (SOH) reflects the degradation level of a battery and is critical for battery management systems. However, SOH cannot be measured directly and must be estimated from observable signals such as voltage and current.

This project implements a feature-based SOH estimation approach using easily accessible charging data.

The method extracts several health-related features from battery charging curves and combines them using a weighted model to estimate battery capacity degradation.

## My Contribution

In this project, I contributed to the following components:

- Implemented the full data analysis and modeling pipeline in Python
- Developed the feature extraction code from experimental battery data
- Implemented the weighted SOH estimation model
- Conducted the modeling experiments and generated figures
- Wrote the first draft of the manuscript

The experimental battery aging protocol and data collection were designed and conducted by collaborators in the electrical engineering lab.

## Method Overview

The model estimates battery capacity using several health features extracted from charging data.

Health features include:

- **CHT**: charging time from 4.0V to 4.2V
- **Ratio_cccv**: ratio between constant-current and constant-voltage charging capacity
- **Rohm**: internal ohmic resistance

These features are correlated with battery aging and used to build a weighted estimation model.

The capacity prediction model is:

Q = w1 f(CHT) + w2 f(Ratio_cccv) + w3 f(Rohm)

where weights are determined based on the coefficient of determination (R²) between each feature and battery capacity.


