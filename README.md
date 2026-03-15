# Topological Grand Unification: Confinement and Electroweak Physics from $U(4)$
**Volume 1 Computational Framework**

This repository contains the official mathematical and computational proofs for the $U(4)$ Topological Grand Unified Theory, developed by Dimitris Mastoridis, Konstantinos Kalogirou, and Panos Razis. 

The scripts provided here demonstrate that the Standard Model gauge couplings and the 17-order-of-magnitude fermion mass hierarchy are not arbitrary. Instead, they emerge deterministically from the topological phase boundaries and geometric harmonics of a $U(4)$ vacuum.

---

## The Topological Thresholds: $\Theta_S$ vs $\Theta_D$
A critical aspect of the $U(4)$ unification framework is how it handles the vacuum phase transition at the 259 TeV melting scale. The theory strictly separates the boundary matching into two distinct physical mechanisms: one perturbative (blindly calculable) and one non-perturbative (extracted via boundary matching).

### 1. The Scalar Mass Splitting ($\Theta_S$) - 100% First Principles
The $\Theta_S$ vector `[-0.073, -1.098, -0.732]` is **not a fitted parameter**. It is derived *ab initio* from pure Lie algebra and the geometric boundaries of the vacuum. 
* By identifying the four scalar Warden fields as a $(3,2)$ bi-doublet with hypercharge $Y = +1/6$, their specific fractional contributions to the gauge beta functions ($\Delta b_i$) are rigidly fixed by their Casimir invariants.
* When these exact group-theory integers are multiplied by the logarithmic mass gap bridging the Warden scale (8.2 TeV) and the melting scale (259 TeV), the $\Theta_S$ threshold natively drops out of the mathematics. It requires zero experimental inputs.

### 2. The Transverse Decoupling ($\Theta_D$) - The Non-Perturbative Boundary
Unlike the scalar Wardens, the transverse valence gluons in the Cho-Duan-Ge decomposition acquire a **dynamical constituent mass** from their interaction with the magnetic background.
* Because this dynamical mass generation is a strongly-coupled, non-perturbative phenomenon (the Yang-Mills mass gap), there is currently no exact analytical equation in quantum field theory to calculate their specific screening magnitude from scratch.
* **The Solution:** We determine $\Theta_D$ through rigorous **Top-Down / Bottom-Up Matching**. We anchor the observed electroweak reality ($\sin^2 \theta_W = 0.23125$) and run the 3-loop RGEs upward, while simultaneously running the $U(4)$ symmetric phase downward from the GUT scale ($3.2 \times 10^{16}$ GeV). $\Theta_D$ is extracted as the exact mathematical residual required to bridge the non-perturbative gap. 

**Validation:** The ultimate theoretical proof of this framework is that when this gap is calculated, the math naturally forces the Strong force residual to be negative ($\Theta_D^{(3)} \approx -1.57$). The equations blindly discover that the QCD sector requires **anti-screening** to bridge the vacuum, perfectly aligning with established quantum mechanical reality. Lacking a Lattice Gauge Theory supercomputer simulation of the $U(4)$ vacuum, this matching protocol serves as the exact physical boundary condition for Volume 1.

---

## Repository Structure

This repository is divided into four executable proofs:

### 1. `01_Gauge_Unification.py`
**The 3-Loop Gauge Unification Engine**
Demonstrates that the fundamental forces perfectly unify at $M_{GUT} = 3.2 \times 10^{16}$ GeV. This engine integrates the 3-loop Renormalization Group Equations (RGEs) incorporating precise $\overline{\text{MS}}$ top-quark matching and the Cho-Duan-Ge topological screening at the 259 TeV melting scale. It outputs a zero-variance intersection landing exactly on the experimental weak mixing angle $\sin^2 \theta_W = 0.23125$.

### 2. `02_Topological_Thresholds.py`
**The First-Principles Scalar Mass Splitting ($\Theta_S$)**
Calculates the $\Theta_S$ threshold vector strictly from $U(4)$ Casimir invariants. By placing four scalar Warden fields into a $(3,2)_{+1/6}$ bi-doublet, the exact geometric shift drops out from the 8.2 TeV to 259 TeV mass gap.

### 3. `03_Flavor_Spectrum.py`
**The Topological Flavor Predictor (Error Propagation)**
Proves that the fermion masses are pure geometry. Using a single unified coupling at $M_{GUT}$, the integer topological winding numbers ($W$), and the Clebsch-Gordan rational fractions, this 2-loop Yukawa RGE solver deterministically crushes the flavor states. This rigorous statistical version propagates $\pm 1\sigma$ experimental uncertainties from the Particle Data Group through the 14 orders of magnitude of non-linear RGE flow, establishing the strict theoretical error bands for the mass predictions.

### 4. `04_Flavor_Deterministic.py`
**The Pure Forward Simulation (Central Values)**
A streamlined, deterministic counterpart to Script 3. Stripped of the statistical error bands, this clean code isolates the pure geometric DNA of the theory. It performs a flawless 3-phase descent from the GUT scale to the electroweak reality, demonstrating exactly how the unshadowed mathematical mechanism natively generates the 17-order-of-magnitude mass spectrum using only the vacuum tilt ($\lambda \approx 0.225$) as a geometric anchor.

---

## Dependencies & Execution
* Python 3.8+
* `numpy`
* `scipy`

To run any of the mathematical proofs, simply execute the python file in your terminal. For example:
`python 01_Gauge_Unification.py`
