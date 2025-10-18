# Haldane Chern Number Walkthrough

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

A pedagogical Jupyter notebook deconstructing the calculation of the Chern number, from the Haldane model to a reusable implementation of the Fukui-Hatsugai-Suzuki (FHS) method.

## 🎯 Overview

While powerful packages for calculating topological invariants exist, their inner workings can be a black box for students and researchers. This project serves as a transparent, educational guide that bridges the gap between the formal theory of topological phases and the practical code that computes them.

**Key Features:**

- 🧭 **Step-by-Step Walkthrough** from basic concepts to full implementation
- 🔍 **FHS Method Deconstruction** with detailed mathematical explanations
- ♻️ **Reusable Code Components** adaptable to other Hamiltonians
- 📚 **Educational Focus** prioritizing understanding over optimization

## 📁 Repository Structure

haldane-chern-walkthrough/
├── notebooks/
│   └── Haldane_Chern_Number_Tutorial.ipynb  # Main educational notebook
├── src/
│   ├── __init__.py
│   ├── fhs_method.py           # Reusable FHS implementation
│   └── haldane_model.py        # Haldane model Hamiltonian
├── examples/
│   └── custom_hamiltonian_demo.ipynb  # Example of extending to other models
├── docs/
│   └── theory_background.md    # Supplementary theoretical background
└── tests/
    └── test_fhs_method.py      # Unit tests for the FHS implementation


## 🚀 Quick Start

### Prerequisites

python>=3.8
numpy
matplotlib
scipy
jupyter
