# Covariant Kinetic Geometrodynamics (CKGD)

![Status](https://img.shields.io/badge/Status-Theoretical_Framework-blue.svg)
![Formalism](https://img.shields.io/badge/Formalism-BSSN_%2F_ADM-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

> **"Mass is Invariant. Geometry does the Accounting."**

The Accounting of E =γmc2 

In CKGD, the Lorentz Factor is not a scalar multiplier but a tensor operation. We decompose the observer’s 4velocity gradient ∇νuµ: 

- Expansion θ: Corresponds to the BSSN trace K. 

- Shear σµν: Corresponds to A˜ij (The Lorentz Squeeze). 

- Vorticity ωµν: Corresponds to the curl of the Shift βi (Gravitomagnetism).

Instead of treating the Lorentz factor as a kinematic modifier of the object, CKGD treats it as a **Geometric Perceptron**: a frame-dependent shearing of the spacetime manifold that stores kinetic energy in the **Velocity of Curvature**.

Standard relativity posits that energy increases by γ. The energy of motion is relative to an observer, it is not a fixed value. CKGD posits that the geometry deforms by A˜ij. The Hamiltonian constraint enforces this balance: H = 0 =⇒ A˜ijA˜ij ≈ 16π(γ2 − 1)ρ. The kinetic energy is physically stored in the squared magnitude of the shear tensor A˜ij. The Perceptron is the geometric mechanism that converts relative velocity βi into extrinsic curvature.
**Covariant Kinetic Geometrodynamics (CKGD)** is a foundational re-interpretation of General Relativity that replaces the phenomenological concept of "Relativistic Mass" ($M = \gamma m$) with geometric curvature. 

---

## 📄 Abstract

Standard pedagogy suggests that as an object approaches the speed of light, its mass increases to account for the divergence in kinetic energy. Modern differential geometry rejects this view, treating mass as a strict scalar invariant ($P^\mu P_\mu = -m^2$). This creates a conceptual gap: *Where is the "weight" of kinetic energy stored?*

**CKGD resolves this via the "Lorentz Perceptron Hypothesis":**
1.  **Mass Invariance:** Rest mass ($m$) is immutable. It never changes, regardless of velocity.
2.  **The Perceptron:** The Lorentz factor ($\gamma$) is not a physical alteration of the object, but a geometric projection of the observer's frame.
3.  **Gravitational Accounting:** To satisfy the Einstein Field Equations without changing $m$, the **Extrinsic Curvature ($K_{ij}$)** of the spacetime slice must evolve non-linearly.

This repository contains the rigorous mathematical formulation of CKGD, utilizing the **(3+1) ADM decomposition** and the **BSSN (Baumgarte-Shapiro-Shibata-Nakamura)** formalism to ensure numerical stability at ultra-relativistic velocities ($v \to c$).

---

## ⚖️ Comparison: Standard GR vs. CKGD

| Feature | Standard Interpretation | CKGD Interpretation |
| :--- | :--- | :--- |
| **Rest Mass ($m$)** | Scalar Invariant | Scalar Invariant |
| **Relativistic Mass** | $M = \gamma m$ (Heuristic) | **Non-Existent** (Rejected) |
| **Kinetic Energy** | Stored in the Object ($T_{00}$) | Stored in the **Shear Tensor ($\tilde{A}_{ij}$)** |
| **Lorentz Factor** | Time Dilation / Length Contraction | **Geometric Projection / Shear** |
| **Frame Dragging** | Effect of angular momentum | **Intrinsic effect of linear translation** |

---

## 📐 Mathematical Framework

This framework utilizes the **BSSN Formalism** to describe "Moving Geometry" without singularity formation.

### The Metric Split ((3+1) ADM)
Spacetime is foliated into spatial hypersurfaces $\Sigma_t$ evolved by a timelike normal vector $n^\mu$:
$$ ds^2 = -\alpha^2 dt^2 + \gamma_{ij} (dx^i + \beta^i dt)(dx^j + \beta^j dt) $$

*   **$\gamma_{ij}$ (Intrinsic Metric):** The "Shape" of space (Rest Gravity).
*   **$\beta^i$ (Shift Vector):** The "Flow" of coordinates (The Perceptron).

### The Master Evolution Equation
The core of CKGD is the evolution of the **Conformal Traceless Shear ($\tilde{A}_{ij}$)**. This equation describes how relative motion generates gravitational effects:

$$ \partial_t \tilde{A}_{ij} = \underbrace{e^{-4\phi} [ -D_i D_j \alpha + \alpha R_{ij} ]^{TF}}_{\text{Static Force}} + \underbrace{\alpha(K \tilde{A}_{ij} - 2\tilde{A}_{il}\tilde{A}^l_j)}_{\text{Kinetic Interaction}} + \mathcal{L}_{\beta} \tilde{A}_{ij} $$

The non-linear term **$-2\tilde{A}_{il}\tilde{A}^l_j$** represents the **Kinetic Interaction Vertex**, proving that the collision of curvature velocities generates new gravitational depth.

---

## 🔍 Visualizing the "Perceptron"

Imagine an observer watching a sphere fly past at $0.99c$.

*   **Standard View:** The sphere is flattened (Lorentz Contraction) and becomes 7x heavier ($M=\gamma m$).
*   **CKGD View:**
    *   The sphere remains a rigid sphere of mass $m$.
    *   The **Spacetime Slice** ($\Sigma_t$) shears around the object.
    *   The observer looks through a "Geometric Lens" (The Perceptron) created by the Shift Vector $\beta^i$.
    *   This lens focuses the gravitational field into a transverse "pancake," increasing the local curvature intensity without creating new matter.

---

## 📂 Repository Contents

| File / Directory | Description |
| :--- | :--- |
| `manuscript/CKGD_Manuscript.tex` | The complete, maximalist LaTeX source code derived using BSSN. |
| `manuscript/CKGD_Manuscript.pdf` | (Release) The compiled preprint. |
| `diagrams/` | TikZ source code for spacetime foliation diagrams. |

---

## ❓ Scientific Context & FAQ

**Is this "Modified Gravity"?**
No. CKGD is a specific interpretation of **Standard General Relativity**, reformulated using the variables of Numerical Relativity (BSSN). It does not add new fields to the Lagrangian; it rigorously defines how the standard metric tensor evolves under boost transformations.

**Does it predict Anti-Gravity?**
No. As derived in Section 4 of the manuscript, the Lorentz factor appears as $\gamma^2$ in the stress-energy tensor. Since $\gamma^2$ is always positive for $v < c$, the geometric adjustment results in **Hyper-Attraction** (deepening the well), not Repulsion.

---

## 🚀 Usage

To compile the manuscript from source, you will need a standard LaTeX distribution (TeX Live, MiKTeX, or MacTeX).

```bash
git clone [https://github.com/YourUsername/CKGD.git](https://github.com/YourUsername/CKGD.git)
cd CKGD/manuscript
pdflatex CKGD_Manuscript.tex
pdflatex CKGD_Manuscript.tex  # Run twice for cross-references
