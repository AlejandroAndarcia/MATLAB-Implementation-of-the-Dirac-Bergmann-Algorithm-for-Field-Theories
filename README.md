# MATLAB-Implementation-of-the-Dirac-Bergmann-Algorithm-for-Field-Theories

**Brief description.**  
This MATLAB toolbox provides a set of utilities for **tensorial and functional symbolic calculus** on top of MATLAB’s Symbolic Math Toolbox, including indexed partial-derivative wrappers, distribution-aware integrals involving Dirac deltas (and their derivatives), and field-theory Poisson/Dirac brackets.


> **Acknowledgment.** Parts of this codebase and documentation were developed **with the assistance of ChatGPT**.

---

## Features

- Symbolic support for **indexed partial derivatives** (field-style wrappers) with optional covariant-derivative mode.  
- Distribution-aware **integrals involving Dirac deltas and their derivatives**, e.g., terms like `A(y)*d_i(dirac(x-y))`, handled consistently when MATLAB’s native `int` is not.  
- Field-theory **Poisson brackets** based on functional derivatives, with automated expansion, contraction, and simplification steps.  
- Field-theory **Dirac brackets** with constraint-matrix construction and inversion, yielding reduced (constrained) dynamics.


**Main functions (non-exhaustive):**

- `fieldDerivative` — Builds a symbolic *field-style* partial-derivative wrapper and applies basic differentiation rules (linearity, product rule, power rule) by parsing the expression as text. 
- `solveFieldDerivative` — Post-processes the symbolic derivative wrappers produced by `fieldDerivative`, converting functional-derivative patterns into Kronecker deltas and Dirac deltas.
- `FInt` — Evaluates distributional integrals involving Dirac deltas and their derivatives (e.g., terms like `A(y)*d_i(dirac(x-y))`), correcting cases where MATLAB’s native `int` does not handle derivatives of the Dirac delta as expected.
- `FPoissonBrackets` — Computes field Poisson brackets.
- `FDiracBrackets` — Computes field Dirac brackets.
---

## Requirements

- **MATLAB** (R2021a or later recommended).  
- **Symbolic Math Toolbox**.   

> If you find a version incompatibility, please open an issue with your MATLAB release number.

---

## Installation

1. Download the toolbox file (`FieldDiracFormalism - ToolBox.mltbx`) from this repository.  
2. Double-click it; confirm the installation.  
3. The functions will be available on your MATLAB path.

## Files in this repository

- **`FieldDiracFormalism - ToolBox.mltbx`** — MATLAB toolbox package containing the functions. Install it and call the functions directly from your code.  
- **`guide.pdf`** — User guide describing the main functions, inputs/outputs, and usage tips.
- **`Example.mlx`** — Worked example showing how to use the toolbox to analyze noncommutative Maxwell electrodynamics with external sources, with step-by-step comments explaining the workflow and the functions used.

---

## Cite

If this code helps your research, please cite this repository (and optionally the accompanying guide).

---

## Contributing, questions, and feedback

Contributions are welcome!

**Contact:** If you have any doubts about the program, need help reproducing results, or want to propose improvements, please contact me. Any suggestion or bug report is appreciated and helps improve the code.

---
