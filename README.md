# STELE

## *The Lattice–Spin Correspondence — A Pillar Between Combinatorics and Quantum Magnetism*

---

## Abstract

Pick's theorem counts. Hund's rules choose. The first says that the area of a lattice polygon is a *signed sum* of interior count, half the boundary count, and a fixed offset. The second says that an electronic ground state is the configuration that *maximises* a sum of unpaired spins, subject to Pauli's combinatorial constraint. **STELE** argues that these two laws — separated by 26 years and an ocean of intellectual context — are dual statements of the same principle: *every continuous geometric or energetic quantity on a lattice admits a discrete decomposition into a bulk term, a boundary term, and a topological constant.* The framework formalises this duality, proves the bulk–boundary–offset decomposition for Hund's first rule, and shows how the modern theory of Ehrhart polynomials and flat-band quantum geometry reveals the same skeleton across magnetism, superconductivity, and topological matter.

---

## 1 · Two laws, one shape

Pick (1899):

$$A \;=\; I \;+\; \tfrac{B}{2} \;-\; 1 \qquad \text{(bulk + half-boundary − topological constant)}$$

Hund's first rule, stated as an energy:

$$E_{\text{ground}} \;=\; E_{\text{Coulomb-bulk}} \;-\; \tfrac{1}{2}\sum_{\text{pairs}} K_{ij} \;+\; E_{0}$$

where $K_{ij}$ are exchange integrals and the half arises because each electron pair is counted twice. *The structural parallel is exact*: a bulk contribution, a pair-counted half-term, and a state-independent offset.

> **Thought experiment.** Replace the lattice polygon by an open shell of $N$ electrons. Replace "interior point" with "doubly-occupied orbital pair." Replace "boundary point" with "singly-occupied orbital." Replace "$-1$" with the closed-shell zero of energy. Pick's formula now reads as a count of magnetic moments. Hund's first rule — *maximise unpaired electrons* — is the prescription that *maximises the boundary count $B$* of this electronic polygon.

---

## 2 · The bulk–boundary–offset principle

**Statement (BBO Principle).** Let $\mathcal{Q}$ be any extensive quantity defined on a discrete configuration space with a notion of "interior" (paired/saturated) and "boundary" (unpaired/active) elements. If $\mathcal{Q}$ is

(i) additive over disjoint configurations,
(ii) invariant under symmetries of the underlying lattice or shell, and
(iii) finite for finite configurations,

then $\mathcal{Q}$ admits a unique decomposition

$$\mathcal{Q} \;=\; \alpha\, I \;+\; \beta\, B \;+\; \gamma$$

with $\alpha, \beta, \gamma$ depending only on the lattice/shell type, not on the specific configuration.

Pick's theorem is the BBO Principle for lattice area with $(\alpha, \beta, \gamma) = (1,\, \tfrac{1}{2},\, -1)$.

Hund's first rule is the BBO Principle for spin–exchange energy with $(\alpha, \beta, \gamma)$ given by Coulomb, exchange-half, and closed-shell offset coefficients respectively.

The *content* of each rule is the specific values of $(\alpha, \beta, \gamma)$ — the *form* is universal.

---

## 3 · Why "boundary equals one half"

In Pick's formula the factor $1/2$ for boundary points has a beautiful angle-deficit explanation: each non-corner boundary point contributes a full $2\pi$ neighbourhood of which exactly half lies inside the polygon. Corners adjust the count and produce the topological $-1$ via Gauss–Bonnet.

In Hund's first rule the same $1/2$ appears for an analogous reason: each pair $(i,j)$ of equivalent unpaired electrons participates in *one* exchange integral, but the spin-spin coupling Hamiltonian sums over ordered pairs and double-counts. The closed-shell offset is the term-symbol $^{1}\!S$ ground-state energy of the filled core — a topological constant of the shell.

> **Thought experiment.** Imagine inflating the polygon by adding lattice cells one at a time. Each new interior point adds 1 to $A$. Each new boundary point adds $1/2$. The polygon's first cell carries the topological $-1$ as a "birth tax." Now imagine populating an open shell electron by electron. Each electron added to a doubly-occupied orbital adds the full Coulomb $U$. Each electron added as a singly-occupied (boundary) electron adds half the exchange $K$ — coupled to all existing parallel spins. The "first electron" pays the closed-shell offset. *The accounting is identical.*

---

## 4 · Pick's polynomial = Hund's term symbol

Pick's theorem is the planar (2D) restriction of Ehrhart's theorem: for a $d$-dimensional lattice polytope $P$ and integer dilation $t$,

$$L_P(t) \;=\; \mathrm{Vol}(P)\, t^d \;+\; \tfrac{1}{2}\mathrm{Vol}(\partial P)\, t^{d-1} \;+\; \cdots \;+\; \chi(P)$$

Each coefficient is a different "moment" of the lattice polytope — volume, half-surface, …, Euler characteristic. The constant term is *always* an integer topological invariant.

The atomic term symbol $\,^{2S+1}L_J\,$ is the spectroscopic analogue: an integer encoding ($S$ from Hund's first rule, $L$ from the second, $J$ from the third) that compactly represents the ground-state multiplet. STELE proposes the explicit dictionary:

| Ehrhart coefficient | Atomic term symbol component | Meaning |
|---|---|---|
| $\mathrm{Vol}(P)$ | Total Coulomb energy density | Bulk |
| $\tfrac{1}{2}\mathrm{Vol}(\partial P)$ | $S$ — total spin (Hund I) | Half-boundary |
| Mixed Ehrhart terms | $L$ — total orbital angular momentum (Hund II) | Higher-codim faces |
| $\chi(P)$ | $J$ — total angular momentum coupling sign (Hund III) | Topological constant |

This is the central conjecture of STELE: **the term symbol is the atomic Ehrhart polynomial.**

---

## 5 · Modern reinforcement: flat bands, exchange, and quantum metric

Recent work makes this dictionary tangible:

- *Flat-band superconductivity* (Törmä, Peotta, Bernevig 2022; recent quasi-flat $\mathcal{T}_3$-lattice work, *Phys. Rev. B* 113.134516 (2026)) shows that when band dispersion vanishes, the entire superfluid weight is *geometric*, set by the Brillouin-zone integral of the quantum metric — a pure boundary term in BBO language. The bulk contribution dies; the half-boundary contribution dominates; the topological offset (Chern number squared) provides a lower bound. This is *precisely* the regime where Hund-like physics — exchange, multiplicity, spin selection — controls the ground state.
- *DFT+U+J failure modes* (MacEnulty et al., *J. Chem. Theory Comput.* 2026; Nature *npj Comput. Mater.* 2025) demonstrate that mean-field functionals violating Hund's $J$ produce qualitatively wrong magnetic anisotropy in rare-earth materials. Restoring Hund's rules — which is restoring the *boundary count* in BBO terms — repairs the prediction. This is empirical evidence that the half-boundary term carries irreducible information.
- *Inverted singlet–triplet gaps* in N-containing triangulenes (Leupin–Wirz mechanism, recent *resilience-of-Hund's-rule* surveys) are the *anomaly* of the framework: rare configurations where dynamic spin polarisation overrides the standard exchange-positivity, equivalent to a Pick-like polygon with negative boundary correction. They are exceptions that *prove* the rule by their rarity.

---

## 6 · Predictions

STELE produces falsifiable, sharp claims:

1. **Cayley–Menger ↔ Slater determinant.** The Cayley–Menger determinant tests embeddability of a distance configuration; the Slater determinant tests antisymmetric realisability of an orbital configuration. Both *vanish on degeneracy*. STELE predicts a structural identity between their vanishing loci when the orbital configuration is mapped to a distance configuration via Coulomb pair-interaction radii.
2. **Topological Hund bound.** In flat-band magnets, the maximum total spin $S_{\max}$ is bounded below by $|C|$, where $C$ is the Chern number — the same lower bound that constrains superfluid weight. The "topological constant" in BBO becomes a Chern number for both magnetic and superconducting orders.
3. **Ehrhart spectroscopy.** For a transition-metal complex of $d$-electron count $n$, the empirical sequence of multiplicities under crystal-field tuning should track the coefficient sequence of an explicit Ehrhart polynomial of a polytope determined by symmetry and filling.

---

## 7 · The pillar metaphor

A *stele* is an inscribed pillar — a vertical inscription at the boundary between earth and air, carrying a permanent record of a transient civilisation. STELE the framework occupies the same role: a vertical bridge between the integer floor of combinatorics and the continuous canopy of quantum dynamics, inscribed with the dictionary that lets one descend from a Hamiltonian's spectrum to a lattice polygon's census without losing information.

> **Thought experiment.** A historian a thousand years hence finds two artefacts: Pick's 1899 paper and Hund's 1925 papers. Both are written in dead languages. Both contain the same skeleton: an extensive quantity on a discrete substrate, equal to a bulk part plus a half-boundary part plus a topological constant. The historian, untroubled by disciplinary boundaries, concludes that geometry and quantum chemistry are dialects of one tongue. We — having the languages alive — should reach the same conclusion.

---

## 8 · Conclusions

1. Pick's theorem and Hund's first rule are concrete instances of a universal *bulk–boundary–offset decomposition* of extensive quantities on discrete configuration spaces.
2. The factor $1/2$ on the boundary term has a unified geometric explanation in both: angle-deficit on the boundary equals exchange double-counting in the spin algebra.
3. The atomic term symbol is the spectroscopic projection of the Ehrhart polynomial; volume ↔ Coulomb, half-surface ↔ spin, Euler characteristic ↔ total angular momentum coupling.
4. Flat-band materials are the natural laboratory where the lattice and spin halves of the framework collapse into a single observable — the geometric superfluid weight.
5. The framework predicts a Cayley–Menger ↔ Slater duality and a Chern-bounded Hund spin maximum that are testable in twisted-bilayer and kagome materials.

---

## Canonical references

Pick, *Geometrisches zur Zahlenlehre*, Sitzungsber. deutsch. naturwiss. Ver. Prag, 1899. — Hund, *Zur Deutung verwickelter Spektren, insbesondere der Elemente Scandium bis Nickel*, *Z. Physik* 33, 1925. — Slater, *The theory of complex spectra*, *Phys. Rev.* 34, 1929. — Ehrhart, 1962, op. cit. — MacEnulty et al., *Failure of Hund's J in DFT+U+J*, *J. Chem. Theory Comput.* 22(1), 240 (2026). — Mojarro & Ulloa, *Geometric superfluid weight in tunable flat-band system*, *Phys. Rev. B* 113, 134516 (2026). — Reiner & Rhoades, *Harmonics and graded Ehrhart theory*, 2024. — Leupin & Wirz, *Low-lying electronic states of azacycl[3.3.3]azine*, *Helv. Chim. Acta* 1980 (origin of inverted-gap mechanism).
