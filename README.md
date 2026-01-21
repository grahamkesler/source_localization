# source_localization on Infection Trees

This repository explores the problem of source localization on tree-structured networks using simulation and algorithmic reduction.The work examines both how infection sources can be inferred from partial observations and how the strategic placement of observer nodes affects the quality of that inference.

The analysis is conducted on randomly generated trees and compares multiple source-localization and observer-selection approaches motivated by network-theoretic principles.

---


## Project Overview

Given:
- a tree-structured network
- an unknown infection source
- stochastic spread along edges
- infection times observed at a small subset of nodes

The goal is to constrain the set of nodes that could plausibly be the infection source and then identify the most likely source using only observer data and network structure.

---

## Methodology

### Tree generation
Trees are generated either:
- as uniformly random **labeled** trees via Prüfer sequences, or
- as uniformly random **unlabeled** tree shapes, which are then arbitrarily labeled for simulation.

### Infection simulation
A source node is selected at random, and infection spreads stochastically along tree edges. Observer nodes record the time at which they become infected.

### Candidate Reduction and Source localization
Using only observer infection times and the tree structure, localization algorithms are applied to:
- identify feasible source nodes, and/or
- identify most likely source node(s).

---

## Key Questions Explored

- How accurately can a source be localized from partial infection timing data?
- How much does observer placement influence localization performance?
- Which network-theoretic heuristics are most effective for observer selection?
- How do results vary across different random tree realizations?

---

## Contents

- `notebooks/`  
  Jupyter notebooks containing simulations, analysis, and visualizations.

- `src/` *(optional)*  
  Helper functions for tree generation, observer selection, and reduction algorithms.

---

## Tools & Libraries

- Python
- NetworkX
- NumPy
- Matplotlib

---

## Motivation

Source localization arises in applications such as:
- epidemiology
- information diffusion
- rumor and malware spread

This project serves as a controlled simulation study demonstrating how structural insight and strategic measurement design can significantly improve inference under limited observability.

---

## How to Run

Clone the repository and open the notebooks locally, or upload them to Google Colab:

```bash
git clone https://github.com/your-username/your-repo-name.git
```

---

## Author

Graham Kesler O'Connor, PhD  
Applied Mathematics / Data Science


