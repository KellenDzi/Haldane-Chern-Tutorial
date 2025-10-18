# Haldane Chern Number Walkthrough

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)

---

## 🧩 Repository Description

A **pedagogical Jupyter notebook** deconstructing the calculation of the **Chern number**, from the **Haldane model** to a reusable implementation of the **Fukui–Hatsugai–Suzuki (FHS)** method.

While powerful packages for calculating topological invariants exist, their inner workings can be a black box for students and researchers.  
This project aims to be a **transparent, educational guide** bridging the gap between the **formal theory** of topological phases and the **practical code** that computes them.

---

## 🧠 Why This Repository Name?

The name `haldane-chern-walkthrough` was chosen because it:

- Emphasizes **education and clarity** over optimization.  
- Uses the **Haldane model** as the central pedagogical example.  
- The term “**walkthrough**” signals detailed, step-by-step explanations.  
- Allows for **reusable code** components while keeping a didactic focus.

---

## 🎯 Overview

### What This Repo Contains

- 🧭 **Step-by-Step Walkthrough:**  
  A comprehensive Jupyter notebook building from the basics of the Haldane model to the calculation of its Chern number, explaining the *why* and *how* throughout.

- 🔍 **Method Deconstruction:**  
  A clear breakdown of the **Fukui–Hatsugai–Suzuki (FHS)** method — a lattice-gauge approach for numerical Chern number computation.

- ♻️ **Reusable FHS Engine:**  
  A clean, modular Python function implementing the FHS method, easily adaptable to any tight-binding Hamiltonian.

- 🎓 **Focus on Understanding:**  
  Not an optimized package, but a **learning resource** prioritizing transparency and pedagogy.

---

## ⚙️ Existing Packages Context

### Popular Packages Implementing the FHS or Similar Methods
| Package | Language | Description |
|----------|-----------|-------------|
| **Z2Pack** | Python | Computes Chern and Z₂ invariants; production-grade |
| **PythTB** | Python | Tight-binding with Berry phase calculations |
| **TBPLaS** | Python | For low-dimensional tight-binding systems |
| **WannierTools** | Fortran/Python | For topological materials and Wannier analysis |
| **TopologicalQuantization.jl** | Julia | Specialized for topological invariants |

**Our Unique Value:**  
An **educational, deconstructed** version for those who want to *understand* the FHS method, not just use it.

---

## 📁 Repository Structure

```
haldane-chern-walkthrough/
├── notebooks/
│   └── Haldane_Chern_Number_Tutorial.ipynb     # Main educational notebook
├── src/
│   ├── __init__.py
│   ├── fhs_method.py                           # Reusable FHS implementation
│   └── haldane_model.py                        # Haldane model Hamiltonian
├── examples/
│   └── custom_hamiltonian_demo.ipynb           # Example extension to other models
├── docs/
│   └── theory_background.md                    # Supplementary theoretical background
└── tests/
    └── test_fhs_method.py                      # Unit tests for the FHS implementation
```

---

## 🚀 Quick Start

### Prerequisites
```bash
python >= 3.8
numpy
matplotlib
scipy
jupyter
```

### Installation

Clone the repository:
```bash
git clone https://github.com/your-username/haldane-chern-walkthrough.git
cd haldane-chern-walkthrough
```

Install dependencies:
```bash
pip install -r requirements.txt
```

Launch the tutorial notebook:
```bash
jupyter notebook notebooks/Haldane_Chern_Number_Tutorial.ipynb
```

---

## 🧪 Key Learning Outcomes

### Haldane Model Fundamentals
- Construct the **Haldane Hamiltonian** in momentum space  
- Understand **complex next-nearest-neighbor hopping**  
- See how **time-reversal symmetry is broken** without a net magnetic field  

### Berry Phase Physics
- Derive **Berry connection** and **Berry curvature**  
- Interpret the **Chern number** as the integral of curvature  
- Visualize **topological phase transitions** in the Haldane model  

### Fukui–Hatsugai–Suzuki (FHS) Method
- Formulate on a **discretized Brillouin zone**  
- Compute **U(1) link variables** and **lattice field strength**  
- Implement numerically on a finite k-grid  

### Practical Implementation
- Handle **gauge invariance** in numerical settings  
- Test **convergence** with varying grid resolutions  
- Validate results with **known topological phase diagrams**

---

## 💻 Code Usage

### Basic FHS Method Example
```python
from src.fhs_method import calculate_chern_number
from src.haldane_model import HaldaneModel
import numpy as np

# Initialize Haldane model in topological phase
model = HaldaneModel(t1=1.0, t2=0.1, m=0, phi=np.pi/2)

# Calculate Chern number using FHS method
chern_number = calculate_chern_number(
    hamiltonian_func=model.get_hamiltonian,
    nx=50,  # k-points in x-direction
    ny=50   # k-points in y-direction
)

print(f"Chern number: {chern_number}")  # Should be ±1 in topological phase
```

### Extending to Custom Hamiltonians
```python
def custom_hamiltonian(kx, ky):
    """Define your own 2D Hamiltonian here"""
    # Must return the Bloch Hamiltonian matrix at (kx, ky)
    return ...

chern = calculate_chern_number(custom_hamiltonian, nx=50, ny=50)
```

---

## 📊 Example Results

The tutorial demonstrates:

- Chern number calculation across **Haldane’s phase diagram**  
- Visualization of **Berry curvature** in the Brillouin zone  
- **Topological phase transitions** as parameters vary  
- **Convergence behavior** with different k-grid resolutions  

---

## 🤝 Comparison with Existing Packages

| Package | Focus | Our Difference |
|----------|--------|----------------|
| Z2Pack | Production-grade, high precision | We focus on clarity and pedagogy |
| PythTB | General tight-binding framework | We specialize in topology education |
| WannierTools | Materials-oriented | We emphasize transparency in computation |

Our repository serves as a **stepping stone** toward mastering these more complex tools.

---

## 🎓 Learning Path

1. Start with `notebooks/Haldane_Chern_Number_Tutorial.ipynb`  
2. Read supporting theory in `docs/theory_background.md`  
3. Experiment with `examples/custom_hamiltonian_demo.ipynb`  
4. Explore reusable code in `src/fhs_method.py`  

---

## 🛠️ Development

Contributions are welcome!  
Areas for improvement include:

- Additional Hamiltonian examples  
- Performance optimization  
- Visualization enhancements  
- Extended documentation  

---

## 📚 References

- Haldane, F. D. M. (1988). *Model for a Quantum Hall Effect without Landau Levels.*  
- Fukui, T., Hatsugai, Y., & Suzuki, H. (2005). *Chern Numbers in Discretized Brillouin Zone.*  
- Bernevig, B. A., & Hughes, T. L. (2013). *Topological Insulators and Topological Superconductors.*

---

## 📄 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Inspired by excellent pedagogical resources in the **topological matter** community  
- Thanks to contributors, testers, and students who continue improving this resource
