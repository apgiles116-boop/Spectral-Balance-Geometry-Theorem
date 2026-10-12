# Mathematical foundations

**Status:** Established identities and a precisely delimited geometric implication. This is not yet a new rigidity theorem.

## Signed graphs and switching

For a simple signed graph Σ=(V,E,σ), let S be its symmetric signed adjacency matrix: Sᵢⱼ = σᵢⱼ when {i,j} is an edge, and zero otherwise. Given signs εᵢ∈{±1}, let D=diag(εᵢ). Vertex switching is S↦DSD.

- Cycles have switching-invariant sign products.
- Balance: every cycle has positive sign product; equivalent to switching to all-positive.
- Antibalance: a cycle of length k has sign product (−1)^k; equivalent to switching to all-negative.
- Switching preserves the spectrum of S exactly.

## PSD spectral–Gram trace inequality [PROVED — STANDARD]

Let mᵢ lie in any Euclidean space, Mᵢⱼ=mᵢ·mⱼ and C=tr M. For all real symmetric S,

\[
\lambda_{\min}(S) C \le \operatorname{tr}(SM) \le \lambda_{\max}(S) C.
\]

The proof is immediate from M ⪰ 0 and spectral order. For signed adjacency matrices, tr(SM) = 2 ∑_{{i,j}∈E} σᵢⱼ mᵢ·mⱼ.

The expression is switching-invariant if S↦DSD and M↦DMD. This is a general linear-algebra lemma, not claimed to be novel.

**A conditional energy-lower-bound template:** If independent geometric constraints establish tr(SM) ≤ −η + κC with η>0 and κ>λmin(S), then C ≥ η/(κ−λmin(S)). This implication follows by rearrangement, but *η and κ must be derived from actual contact constraints*. The template alone does not establish positive energy.

## Endpoint decomposition [PROVED — EXACT NECESSARY CONDITION]

For unit vectors xᵢ⁺,xᵢ⁻ set mᵢ=(xᵢ⁺+xᵢ⁻)/2 and zᵢ=(xᵢ⁺−xᵢ⁻)/2. Then mᵢ·zᵢ=0 and ‖mᵢ‖²+‖zᵢ‖²=1.

If (mᵢ+s zᵢ)·(mⱼ+t zⱼ) ≤ 1/2 for all s,t∈{±1}, then averaging inequalities for (s,t) and (−s,−t) gives mᵢ·mⱼ+st(zᵢ·zⱼ) ≤ 1/2. Taking both values st=±1 proves

\[
m_i\cdot m_j + |z_i\cdot z_j| \le \frac12.
\]

Beware: these necessary conditions do not by themselves guarantee a valid spherical code, nor can abstract graph antibalance force any mᵢ to be nonzero.

## Auditing a proposed antibalanced four-edge energy bound [OPEN]

A previous exploratory claim was C(4−C)≥1/4 for a special four-pair contact pattern. This **cannot hold for an arbitrary antibalanced K₄ merely because the signs are antibalanced**: take mᵢ=0 for every i. Before use, we must:

1. Specify the eight actual endpoints and which contact inequalities/equalities they satisfy.
2. Prove the asserted sign and summation relationships from those endpoint constraints.
3. Verify the Gram PSD and rank restrictions.
4. Attempt counterexamples and check equality cases.
5. Only then decide whether there is a new theorem.

Until these steps succeed, label the inequality **[UNVERIFIED]**.

## Bibliography

- F. Harary, *On the notion of balance of a signed graph*, Michigan Mathematical Journal 2 (1953/54), 143–146.
- T. Zaslavsky, *Signed graphs*, Discrete Applied Mathematics 4 (1982), 47–74.
