# Assignment of the 131 × 131 Technology Cross-Impact Matrix

## Overview

This repository provides the pairwise assignment information used to construct the cross-impact matrix (CIM) for 131 clean-production and low-carbon technologies considered in the Fenwei Plain study.

The dataset documents the interaction between each pair of technologies from two complementary dimensions:

1. **interaction direction**, represented by a qualitative directional score; and
2. **interaction strength**, represented by a quantitative score.

For each technology pair, a brief technological explanation is also provided to document the basis for the assigned values.

The purpose of releasing these data is to improve the transparency, traceability, and reproducibility of the technology-interaction assessment and subsequent CIM-based analysis.

---

## Data structure

The Excel workbook contains two worksheets:

- `Qualitative matrix assignment`
- `Quantitative matrix assignment`

Both worksheets use the same technology names and technology-pair ordering.

### Qualitative matrix assignment

This worksheet records the direction of the interaction between each pair of technologies.

| Column | Description |
|---|---|
| `Technology 1` | The first technology in the technology pair |
| `Technology 2` | The second technology in the technology pair |
| `Directional Score` | Qualitative direction of the interaction |
| `Brief Explanation` | Brief technological rationale supporting the assigned direction |

### Quantitative matrix assignment

This worksheet records the relative strength of the interaction between each pair of technologies.

| Column | Description |
|---|---|
| `Technology 1` | The first technology in the technology pair |
| `Technology 2` | The second technology in the technology pair |
| `Quantitative Score` | Numerical value representing the relative interaction strength |
| `Brief Explanation` | Brief technological rationale supporting the assigned strength |

---

## Qualitative directional score

The qualitative interaction direction is represented by the directional score \(D_{ij}\):

\[
D_{ij} \in \{-1, 0, 1\}
\]

where:

| Directional score | Interpretation |
|---:|---|
| `1` | Promoting interaction |
| `0` | Negligible or no significant interaction |
| `-1` | Constraining interaction |

A positive interaction indicates that the two technologies can facilitate coordinated deployment or improve technological compatibility, system integration, resource utilization, energy efficiency, or emission-control performance.

A negative interaction indicates potential technological incompatibility, competition for resources or infrastructure, conflicting process requirements, or other mechanisms that may constrain coordinated deployment.

A score of zero indicates that no meaningful cross-technology interaction is identified.

---

## Quantitative interaction score

The relative interaction strength is represented by the quantitative score \(S_{ij}\):

\[
S_{ij} \in \{0.25,\;0.50,\;0.75\}
\]

The three levels are interpreted as:

| Quantitative score | Interaction strength |
|---:|---|
| `0.25` | Weak |
| `0.50` | Moderate |
| `0.75` | Strong |

The quantitative score describes the relative magnitude of the technological relationship between a pair of technologies. It is assessed independently from the interaction direction.

Therefore, the directional score determines **whether the interaction is promoting, constraining, or negligible**, whereas the quantitative score represents **how strong the underlying technological relationship is**.

---

## Construction of the cross-impact matrix

The final cross-impact coefficient between technologies \(i\) and \(j\) is calculated by combining the interaction direction and interaction strength:

\[
C_{ij}=D_{ij}\times S_{ij}
\]

where:

- \(C_{ij}\) is the final cross-impact coefficient between technologies \(i\) and \(j\);
- \(D_{ij}\) is the qualitative directional score; and
- \(S_{ij}\) is the quantitative interaction-strength score.

Accordingly, the possible non-zero CIM values are:

\[
C_{ij}\in
\{-0.75,-0.50,-0.25,\;0.25,0.50,0.75\}
\]

and

\[
C_{ij}=0
\]

when no significant interaction is identified.

For example:

| Direction | Strength | CIM coefficient |
|---:|---:|---:|
| `1` | `0.75` | `0.75` |
| `1` | `0.50` | `0.50` |
| `1` | `0.25` | `0.25` |
| `0` | any assigned strength | `0` |
| `-1` | `0.25` | `-0.25` |
| `-1` | `0.50` | `-0.50` |
| `-1` | `0.75` | `-0.75` |

The resulting coefficients are then organized according to the fixed ordering of the 131 technologies to construct the final \(131 \times 131\) cross-impact matrix:

\[
\mathbf{C}=
\begin{bmatrix}
C_{11} & C_{12} & \cdots & C_{1,131}\\
C_{21} & C_{22} & \cdots & C_{2,131}\\
\vdots & \vdots & \ddots & \vdots\\
C_{131,1} & C_{131,2} & \cdots & C_{131,131}
\end{bmatrix}
\]

Self-interactions are not treated as cross-technology effects, and therefore the diagonal elements of the final CIM are set to:

\[
C_{ii}=0
\]

---

## Basis for technology-interaction assessment

The pairwise technology relationships were assessed by considering multiple potential interaction mechanisms, including:

- technology compatibility;
- emission-pathway compatibility;
- energy-source coupling;
- carbon-flow coupling;
- energy-consumption synergy;
- technology-integration potential;
- combustion adaptability;
- pollution-control interactions;
- energy-efficiency synergy;
- system integration; and
- emission coupling.

These criteria were used to identify both the direction and relative strength of the interaction between technologies.

The `Brief Explanation` column provides the technological rationale associated with each pairwise assignment and enables individual technology links to be traced and reviewed.

---

## Interpretation of the CIM

The sign and absolute magnitude of \(C_{ij}\) have different meanings.

The **sign** represents the interaction direction:

\[
C_{ij}>0
\]

indicates a promoting interaction,

\[
C_{ij}<0
\]

indicates a constraining interaction, and

\[
C_{ij}=0
\]

indicates no significant interaction.

The absolute value:

\[
|C_{ij}|
\]

represents the relative interaction strength. Larger absolute values therefore indicate stronger technology interactions.

For example, \(C_{ij}=0.75\) represents a strong promoting interaction, whereas \(C_{ij}=-0.75\) represents a strong constraining interaction.

---

## Reproducibility

The released assignment tables provide the underlying pairwise information required to reconstruct the CIM.

The matrix can be reproduced through the following procedure:

1. identify the corresponding `Technology 1` and `Technology 2`;
2. obtain the directional score \(D_{ij}\) from the qualitative assignment table;
3. obtain the quantitative score \(S_{ij}\) from the quantitative assignment table;
4. calculate \(C_{ij}=D_{ij}S_{ij}\); and
5. arrange all \(C_{ij}\) values according to the predefined ordering of the 131 technologies.

This structure allows the assignment of each individual technology pair to be independently inspected and reproduced.

---

## Data use

The dataset is provided as supporting material for the associated study on coordinated deployment of clean-production and low-carbon technologies in the Fenwei Plain.

It can be used for:

- reconstruction of the 131 × 131 cross-impact matrix;
- verification of individual technology-pair assignments;
- sensitivity and robustness analysis of technology interactions;
- assessment of alternative interaction assumptions; and
- further research on coordinated technology deployment.

---

## Notes

Technology names and their ordering are consistent with those used in the associated model and supplementary materials.

The `Brief Explanation` field is intended to provide a concise technological rationale for each assignment rather than an exhaustive review of the corresponding technologies.

The qualitative and quantitative assignments should therefore be interpreted jointly when reconstructing the final CIM.

---

## Citation

If these data are used in subsequent research, please cite the associated publication and this repository.
