# Fenwei Plain Energy and Technology Data

## Overview

This repository provides supporting datasets for system dynamics modeling, energy scenario analysis, and interactions among clean-production and low-carbon technologies in the Fenwei Plain.

## Data files

| File | Contents |
|---|---|
| `CIM_qualitative_and_quantitative_assignment.xlsx` | Pairwise interaction assessments for 131 clean-production and low-carbon technologies, including interaction directions, strengths, and technological explanations. |
| `Fenwei_Plain_SD_Model_Data.xlsx` | System dynamics model variables, simulation results, equations, and energy scenario data for 13 cities in the Fenwei Plain. |

## Data structure

### Technology cross-impact matrix (CIM)

The `CIM_qualitative_and_quantitative_assignment.xlsx` workbook contains two worksheets:

- **Qualitative matrix assignment:** Technology pairs, directional scores, and brief explanations of their interactions.
- **Quantitative matrix assignment:** Technology pairs, interaction-strength scores, and brief explanations of the assigned strengths.

The **directional score** indicates whether an interaction is promoting (`1`), negligible (`0`), or constraining (`-1`). The **strength score** represents a weak (`0.25`), moderate (`0.50`), or strong (`0.75`) interaction. Together, these scores describe the signed interaction coefficients used in the 131 × 131 CIM. The explanations summarize the technological basis for each pairwise assessment.

### System dynamics (SD) model

The `Fenwei_Plain_SD_Model_Data.xlsx` workbook contains five worksheets:

- **Parameters and Variables:** Model variable names and symbols.
- **Endogenous Simulation:** Observed and simulated values and relative errors (2010–2020).
- **System Dynamics Equations:** City-specific equations for endogenous variables.
- **Exogenous Scenarios:** Historical data (2010–2020) and projected exogenous variables under the energy transition, baseline, and energy security scenarios (2025–2060).
- **Endogenous Analysis:** Model error statistics (MAPE).

## Citation

If you use these datasets, please cite the associated study and this repository.
