# State Purification

Lean 4 formalization of results on the entanglement cost of distributed quantum state purification.

## Main reported result

In the setting of the paper, any finite-dimensional pure resource enabling a PPT instrument to attain the optimal global purification gain has entanglement entropy at least one ebit.

The theorem
`physicalOperationalAttainment_arbitraryPure_implies_one_le_entanglementEntropy`
is in [ArbitraryPureOperationalNecessity.lean](EntanglementPurification/ArbitraryPureOperationalNecessity.lean).
The formalization follows the same core argument as the appendix proof.

## Build and check

Requires Lean `v4.30.0` (managed by elan). Dependency revisions are pinned in `lakefile.toml` and `lake-manifest.json`.

Run from the repository root:

```sh
lake exe cache get
lake build
lake env lean AxiomAudit.lean
```

The project uses [Lean-QIT](https://github.com/QuAIR/Lean-QIT) and [Mathlib](https://github.com/leanprover-community/mathlib4). Lake retrieves the dependencies; the `.lake` cache is not included.
