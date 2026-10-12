# Spectral Balance–Geometry Theorem
## Switching-Invariant Energy Bounds and Geometric Rigidity

**Status: an open research programme, not a proved new theorem.**

This repository explores whether **signed-graph balance and switching**, **spectral theory**, **positive-semidefinite Gram matrices**, and **spherical contact geometry** can together yield quantitative rigidity or energy obstructions. We also investigate a fourth direction: **frequency**, meaning normal modes and the propagation of perturbations through contact networks.

Our working acronym is **BSGF**:

| | Research area | Core objects |
|---|---|---|
| **B** | **Balance** | Harary balance/antibalance, signed-graph switching |
| **S** | **Spectral** | Signed adjacency eigenvalues, spectral gaps |
| **G** | **Geometry** | PSD Gram matrices, unit-sphere contact inequalities, rigidity |
| **F** | **Frequency** | Linearized mechanical modes and perturbation propagation (exploratory) |

The project name is **aspirational**: no general theorem called the Spectral Balance–Geometry Theorem is claimed to have been proved.

### Origins

The idea emerged from our investigation of signed endpoint-contact patterns in a hypothetical 41-point spherical code in five dimensions. Our primary 5D research remains at:

[5D-Kissing-Number-Research](https://github.com/apgiles116-boop/5D-Kissing-Number-Research)

This repository develops the general mathematical questions independently. A signed-graph observation here does **not** automatically prove a kissing-number obstruction, and a computational observation about Type E is **not** automatically a general theorem.

## 1. Established balance and spectral facts

Let Σ be a signed simple graph on r vertices with edge signs σᵢⱼ ∈ {−1,+1} and signed adjacency matrix S.

- **Balanced** means every cycle has positive sign product. Equivalently, switching signs at vertices can transform every edge to positive.
- **Antibalanced** means every cycle of length k has sign product (−1)^k. Equivalently, switching can transform every edge to negative.
- Switching by a diagonal sign matrix D sends S to DSD, preserving eigenvalues.

These are established signed-graph results, not discoveries made in this repository.

### Spectral–Gram energy bound — [PROVED — STANDARD]

For arbitrary Euclidean vectors m₁,…,mᵣ, let Mᵢⱼ = mᵢ·mⱼ and C = tr M = ∑ᵢ‖mᵢ‖². Since M is PSD,

\[
\boxed{\lambda_{\min}(S)C\le
2\sum_{\{i,j\}\in E(\Sigma)}\sigma_{ij}\,(m_i\cdot m_j)
\le\lambda_{\max}(S)C.}
\]

**Proof.** The symmetric matrix inequalities λmin(S)I ⪯ S ⪯ λmax(S)I imply corresponding trace inequalities against M ⪰ 0. Also tr(SM) = 2 ∑ σᵢⱼ(mᵢ·mⱼ). Under simultaneous switching of S and M, the trace and the eigenvalues are unchanged.

**Limit:** This inequality alone cannot force C > 0, because mᵢ = 0 is admissible for every signed graph. A nonzero geometric lower bound requires additional proven contact constraints.

## 2. Spherical endpoint geometry — [PROVED — EXACT NECESSARY CONDITION]

For unit-vector pairs xᵢ⁺ = mᵢ + zᵢ and xᵢ⁻ = mᵢ − zᵢ, we have

\[
m_i\cdot z_i=0,\qquad \|m_i\|^2+\|z_i\|^2=1.
\]

If **all four cross-endpoint contacts** between pairs i and j satisfy xᵢˢ·xⱼᵗ ≤ 1/2 for s,t ∈ {−1,+1}, then

\[
m_i\cdot m_j+|z_i\cdot z_j|\le\tfrac12.
\]

This necessary inequality follows by averaging the two endpoint inequalities whose signs select ±zᵢ·zⱼ. Its applicability depends on the *actual selected endpoint pairs and valid contact constraints*.

## 3. Frequency as a research direction — [MODEL, NOT A KISSING-NUMBER THEOREM]

For a chosen mechanical model with fixed active contacts, rigidity matrix R, positive-semidefinite spring weights W and positive mass matrix \(\mathcal M\), the linear stiffness approximation is K = RᵀWR, with modes satisfying

\[
K u=\omega^2 \mathcal M u.
\]

Hard-sphere contacts are unilateral rather than ordinary bilateral springs. Contact activation, prestress and second-order feasibility matter. **No equivalence between spring-model frequencies and spherical-code feasibility is currently claimed.**

## 4. Priority questions

1. **Audit** the earlier proposed antibalanced four-edge bound C(4−C) ≥ 1/4. Antibalance *by itself* cannot imply this; its exact geometric hypotheses and derivation must be independently validated before use.
2. Seek sharp **switching-invariant energy bounds** incorporating explicit contact inequalities, Gram rank and equality conditions.
3. Identify whether graph spectral gaps plus second-order rigidity can prohibit geometric realizations.
4. Develop carefully defined frequency models and test what they add beyond static rigidity.
5. Carry independently proved, applicable conclusions back to the 5D kissing-number study.

## Proof-status policy

- **[PROVED — EXACT]** A complete argument is supplied under explicit hypotheses.
- **[PROVED — STANDARD]** Established result or immediate consequence; novelty is **not** claimed.
- **[VERIFIED — FINITE]** Reproducible finite computation, with scope and code specified.
- **[CONDITIONAL]** Requires assumptions or upstream claims not proved here.
- **[NUMERICAL]** Experiment or floating-point evidence, not a proof.
- **[CONJECTURE]** Plausible statement awaiting proof.
- **[OPEN]** Not settled.

Negative computational results and corrections should be retained and documented. Neither a checked script nor a plausible analogy is a substitute for a proof of the relevant mathematical statement.

See [research foundations](research/foundations.md) and [research roadmap](research/roadmap.md).

## References and background

- F. Harary, *On the notion of balance of a signed graph*, Michigan Mathematical Journal **2** (1953/54), 143–146.
- T. Zaslavsky, *Signed graphs*, Discrete Applied Mathematics **4** (1982), 47–74.
- Originating 5D investigation: [5D-Kissing-Number-Research](https://github.com/apgiles116-boop/5D-Kissing-Number-Research).

**Public research notes: corrections, independent verification and constructive scrutiny are welcome.**
