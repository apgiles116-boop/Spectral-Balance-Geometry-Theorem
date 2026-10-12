# BSGF research roadmap

This is a set of testable questions, not a statement of completed discoveries.

## Phase I — proof audit (priority)

- Recover the full hypotheses behind the proposed Type-E four-edge antibalance inequality C(4−C)≥1/4.
- Check orientation switching against the *actual* signed endpoint constraints, rather than arbitrary assigned signs.
- Find a direct rigorous proof or a counterexample.
- Keep a reproducible record of failures and scope limitations.

**Exit criterion:** a theorem statement with complete hypotheses and proof, or a documented retraction.

## Phase II — constrained signed Gram optimization

For a fixed signed contact graph, minimize C=tr M subject to explicit geometric contact constraints and M ⪰ 0 (and, where needed, block Gram and rank ≤ n). Distinguish SDP relaxations from exact realizability. Search for analytic spectral dual certificates, finite algebraic reductions and equality classifications.

**Question:** Can a switching-invariant spectral or stress condition force C>0 when certain contacts are specified?

## Phase III — second-order geometry

Study the Hessian of active spherical contact constraints and the rigidity/stress matrices. Explore local kernel modes, prestress stability and second-order obstructions, without assuming D₅ uniqueness or a particular Type-E labeling.

## Phase IV — frequency (exploratory)

Specify a model (mass, stiffness and active contacts), compute the generalized eigenmodes, and perturb the contact network. Record where hard-sphere unilateral constraints invalidate a conventional spring approximation.

**Question:** Can frequencies reveal a new *rigorous* obstruction, rather than simply visualize classical rigidity?

## Phase V — transfer back to the originating problem

Only apply an independently established theorem after verifying its hypotheses for the 5D branch at issue. Preserve the Type-E matching-scope qualification: a mass-localization result for **some** matching does not apply to **all** matchings.

Originating repository: https://github.com/apgiles116-boop/5D-Kissing-Number-Research

## Evidence rules

Every result must be categorized as exact proof, standard theorem, verified finite computation, conditional derivation, numerical observation or open conjecture. No novelty or global kissing-number claim follows merely from a promising connection.
