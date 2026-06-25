# Hands-On: Crystal Field Theory Derivation

As mentioned before in the README.md file (Seriously... if you haven't read it leave IMMEDIATELY, you will not understand a thing) this page will contain the complete mathematical derivation of the 5th Power Rule in Crystal Field Theory. This is the "advanced" version of what I explained in the main README, here, we get into the actual math... so buckle up and let's skip the fancy intro.

## Table of Contents

1. The Point Charge Electrostatic Model (PCEM)
2. Expanding with Spherical Harmonics (Laplace Expansion)
3. The Crystal Field Parameters (Bₖᵩ)
4. Why the 5th Power Rule Emerges
5. Calculating the Energy Splitting (Δ)
6. Matrix Elements for d-Orbitals
7. When the Rule Breaks Down (Low Symmetry)

## Part 1. The Point Charge Electrostatic Model (PCEM)

### The Basic Idea

The PCEM is the simplest approximation we can use to know how ligands affect the electrons on a metal center. It treats each ligand as a point charge (a tiny electron) and uses Coulomb's Law to calculate the electrostatic potential.

### The Potential Energy Equation

The electrostatic potential (V) felt by a d-electron at position **r** due to all the ligands is:

$$V = \sum_{L = 1}^{N} \frac{Z_{L}e^{2}}{\lvert \mathbf{r} - \mathbf{R}_{L} \rvert}$$

**Where:**

| Symbol | Meaning | Units |
|--------|---------|-------|
| $( V \)$ | Electrostatic potential felt by the d-electron | Joules (J) |
| $( Z_{L} \)$ | Net charge of ligand L | Coulombs (C) |
| $( e \)$ | Elementary charge (1.602 × 10⁻¹⁹ C) | Coulombs (C) |
| $\( \mathbf{R}_{L} \)$ | Position vector of ligand L | Meters (m) |
| $\( \mathbf{r} \)$ | Position vector of the d-electron | Meters (m) |
| $\( N \)$ | Number of ligands | Dimensionless |

### Seen as an Approximation

- **Works good for:** Predicting patterns and relative energies
- **It sucks for:** Exact numerical values (can't predict exact splitting in cm⁻¹)
- **Then what's the problem?** Real ligands are NOT point charges - they have their own electron clouds and complex shapes... so we expand.

## Part 2. Expanding with Spherical Harmonics (Laplace Expansion)

### The Problem with Coulomb's Law

Coulomb's law as written above is difficult to solve because it mixes:
- **Radial dependence** (how distance affects the potential)
- **Angular dependence** (how direction affects the potential)

So we must handle them independently.

### The Solution: Laplace Expansion

We can expand $\(1/\lvert \mathbf{r} - \mathbf{R}_{L} \rvert\)$ as an infinite series of spherical harmonics:

$$\frac{1}{\lvert \mathbf{r} - \mathbf{R}_{L} \rvert} = \sum_{k = 0}^{\infty}\sum_{q = -k}^{k}\frac{4\pi}{2k + 1}\frac{r^k}{R_L^{k+1}} Y_k^{q*}(\theta,\phi)Y_k^{q}(\theta_L,\phi_L)$$

**Breaking this down:**

| Term | Meaning |
|------|---------|
| $\( \frac{r^k}{R_L^{k+1}} \)$ | Radial part - depends on distances |
| $\( Y_k^{q*}(\theta,\phi)Y_k^{q}(\theta_L,\phi_L) \)$ | Angular part - depends on directions |
| $\( \frac{4\pi}{2k+1} \)$ | Normalization factor |

**Note:** This expansion is valid when $\( r < R_L \)$ (the electron is closer to the metal than the ligands).

### What Are Spherical Harmonics?

Spherical harmonics $\( Y_k^q \)$ are special functions that describe how something varies over a sphere. They're the 3D equivalent of sine and cosine functions.

**Key properties:**
- They're **orthogonal** (different ones don't interfere)
- They form a **complete basis** (we can build any angular function from them)
- They're **eigenfunctions** of the angular part of Laplace's equation

With that in mind NOW we can actually get the whole ligand information (parameters) to get our rule...

## Part 3. The Crystal Field Parameters (Bₖᵩ)

### From Expansion to Parameters

When we substitute the Laplace expansion back into the potential V, we can group terms into crystal field parameters $\( B_{kq} \)$:

$$B_{kq} = \sum_{L=1}^{N} Z_L e^{2} \sqrt{\frac{4\pi}{2k+1}} \frac{\langle r^k \rangle}{R_L^{k+1}} Y_k^{q}(\theta_L,\phi_L)$$

**What each part means:**

| Term | Meaning |
|------|---------|
| $\( B_{kq} \)$ | Crystal field parameter containing ligand information |
| $\( \langle r^k \rangle \)$ | Radial expectation value for the d-electron |
| $\( \frac{1}{R_L^{k+1}} \)$ | Distance dependence (this is where the power rules come from!) |

### Quantum Mechanical Selection Rules

For d-electrons (which have angular momentum quantum number \( l = 2 \)), only certain k values contribute:

| k value | Name | Dependence | Status |
|---------|------|------------|--------|
| k = 0 | Monopole | $\( 1/R^1 \)$ | Overall energy shift |
| k = 1 | Dipole | Forbidden | Cancels |
| k = 2 | Quadrupole | $\( 1/R^3 \)$ | Survives in some symmetries |
| k = 3 | Octupole | Forbidden | Cancels |
| k = 4 | Hexadecapole | $\( 1/R^5 \)$ | THE 5TH POWER RULE! |

**Why this happens:** Quantum mechanics tells us that for l = 2 electrons, only even k values from 0 to 2l (which is 4) can contribute. Odd values are forbidden by selection rules.

And here we are left with what we want...

## Part 4. Why the 5th Power Rule Emerges

For an **octahedral complex**, the k=2 terms cancel out due to symmetry. 

Why?

- In an octahedral complex, the ligands are at positions that are symmetric (like the faces of a cube)
- These positions cause the $\( B_{20} \) and \( B_{22} \)$ terms to sum to zero
- This is a direct consequence of the octahedral point group $(\( O_h \))$

<img width="50%" height="50%" alt="clipboard_e876086846312c968a88dda5f4c22b53c" src="https://github.com/user-attachments/assets/59d85659-06f1-41aa-99cf-4ec211cfaf31" />


### The Surviving Term

We're left with the k=4 term as the dominant contributor:

$$B_{40} = \sum_{L=1}^{N} Z_L e^{2} \sqrt{\frac{4\pi}{9}} \frac{\langle r^4 \rangle}{R_L^5} Y_4^{0}(\theta_L,\phi_L)$$

**And finally... we are left with the crucial observation:**

$$B_{40} \propto \frac{1}{R^5}$$

This is the **5th power rule**

And now the only thing remaining is to prove it...

## Part 5. Calculating the Energy Splitting (Δ)

### From Parameters to Energy

To get the actual energy splitting, we need to calculate the matrix elements of the crystal field potential.

### The General Formula

For an electron configuration $\( l^N \)$ (N electrons in l orbitals), the matrix element is:

$$\langle I^{N}\alpha SLM_{S}M_{L}|V|I^{N}\alpha^{\prime}S^{\prime}L^{\prime}M_{S}^{\prime}M_{L}^{\prime}\rangle = \sum_{k q}(-1)^{L - M_{L}}\begin{pmatrix} L & k & L^{\prime} \\ -M_{L} & q & M_{L}^{\prime} \end{pmatrix} \langle I\| C^{k}\| I\rangle \langle I^{N}\alpha SL\| U^{k}\| I^{N}\alpha^{\prime}S^{\prime}L^{\prime}\rangle B_{kq}\delta_{S M_{S},S^{\prime}M_{S}^{\prime}}$$

**But this is too complex to read so let's break this down:**

| Term | Meaning |
|------|---------|
| $(...)$ | 3-j symbol (angular coupling, tabulated) |
| $\( \langle L\| C^k \| L\rangle \)$ | Reduced matrix element (constant for given L,k) |
| $\( \langle I^{N}\alpha SL\| U^{k}\| I^{N}\alpha^{\prime}S^{\prime}L^{\prime}\rangle \)$ | Reduced matrix element for the electron configuration |

### Reduced Matrix Elements for d-Orbitals

For d-orbitals (L=2), the reduced matrix elements are:

| k value | $\( \langle 2\| C^k \| 2\rangle \)$ |
|---------|-----------------------------------|
| k = 0 | $\( \sqrt{5} \)$ |
| k = 2 | $\( -\sqrt{5} \)$ |
| k = 4 | $\( \sqrt{5} \)$ |

### What is the Matrix for d-Orbitals in Octahedral Symmetry

For an octahedral complex, the matrix elements of the crystal field potential for the five d-orbitals are:

| M_L | 2 | 1 | 0 | -1 | -2 |
|-----|---|---|---|----|----|
| **2** | $\( \frac{2}{7}B_{40} \)$ | 0 | $\( \frac{2}{7}B_{40} \)$ | 0 | $\( \frac{2}{7}B_{40} \)$ |
| **1** | 0 | $\( -\frac{4}{7}B_{40} \)$ | 0 | $\( \frac{2}{7}B_{40} \)$ | 0 |
| **0** | $\( \frac{2}{7}B_{40} \)$ | 0 | $\( \frac{2}{7}B_{40} \)$ | 0 | $\( \frac{2}{7}B_{40} \)$ |
| **-1** | 0 | $\( \frac{2}{7}B_{40} \)$ | 0 | $\( -\frac{4}{7}B_{40} \)$ | 0 |
| **-2** | $\( \frac{2}{7}B_{40} \)$ | 0 | $\( \frac{2}{7}B_{40} \)$ | 0 | $\( \frac{2}{7}B_{40} \)$ |

### Calculating the Splitting

The crystal field splitting Δ is the energy difference between the \( e_g \) and \( t_{2g} \) orbitals:

$$\Delta = E(e_g) - E(t_{2g})$$

From the matrix:

- The $\( e_g \)$ orbitals (dₓ²₋ᵧ² and d₂²) have energy $\( \frac{2}{7}B_{40} \)$
- The $\( t_{2g} \)$ orbitals (dₓᵧ, dₓ₂, dᵧ₂) have energy $\( -\frac{4}{7}B_{40} \)$

$$\Delta = \frac{2}{7}B_{40} - \left(-\frac{4}{7}B_{40}\right) = \frac{6}{7}B_{40} = \frac{2}{7}B_{40}$$

So:

$$\Delta = \frac{2}{7}B_{40} - \left(-\frac{4}{7}B_{40}\right) = \frac{6}{7}B_{40}$$

Since $\( B_{40} \propto \frac{1}{R^5} \)$, we get:

$$\Delta \propto \frac{1}{R^5}$$

**This is it... The 5th power rule**

Is that it? No, this is just ideally... real symmetry must also address for imperfections and of course... failure.

## Part 7. When the Rule Breaks Down (Low Symmetry)

The 5th power rule works beautifully for perfect octahedral symmetry. But real molecules aren't perfect... Why?

- Different ligand types (not all identical)
- Different bond lengths (some shorter, some longer)
- Distorted angles (not exactly 90°)

And when the symmetry is broken...

$$B_{20} \neq 0 \quad \text{and} \quad B_{22} \neq 0$$

These \( k=2 \) terms don't cancel out anymore, which adds a $\( 1/R^3 \)$ dependence.

And now finally we can adress for real life scenarios

### The General Formula for Low Symmetry

The total splitting becomes a mix of 3rd and 5th power terms:

$$\Delta = A \cdot \frac{1}{R^3} + B \cdot \frac{1}{R^5}$$

Where:
- \( A \) and \( B \) are constants determined by the specific symmetry
- The $\( 1/R^3 \)$ term comes from $\( B_{20} \)$ and $\( B_{22} \)$
- The $\( 1/R^5 \)$ term comes from $\( B_{40} \)$

### Why This Matters

This mix of 3rd and 5th power rules is what makes luminescent materials (like those in LEDs and phosphors) work. The colors they emit depend on exactly how these terms combine.

**Example: Cerium-doped garnets (Ce³⁺)**
- Ce³⁺ has configuration [Xe]4f¹5d⁰
- The 5d orbital is sensitive to crystal field (unlike 4f)
- In high symmetry: 5th power rule works
- In low symmetry (garnets): Rule breaks down, mix of 3rd and 5th powers

And that is all... simple right? Hopefully you all read this and be as traumatized as I was trying to break this down the best possible:)

### References:

Song, Z., & Liu, Q. (2022). Basic crystal field theory—A simple and useful tool to understand the structure-property relationship in luminescent materials. *Optical Materials: X*, *16*, 100189. https://doi.org/10.1016/j.omx.2022.100189

*   **Why I used it:** The primary source for the crystal field theory framework and the explanation of how the 5th power rule works in different symmetries.

Libretexts. (2021, October 20). 4.2: Point groups. Retrieved from https://chem.libretexts.org/Bookshelves/Inorganic_Chemistry/Inorganic_Chemistry_(LibreTexts)/04%3A_Symmetry_and_Group_Theory/4.02%3A_Point_Groups

*   **Why I used it:** This reference helped me understand why the k=2 terms cancel out in octahedral symmetry. It's all about group theory and character tables.
