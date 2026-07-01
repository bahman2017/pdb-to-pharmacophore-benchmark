# Benchmark Summary

| Target | Benchmark type | Context | Runtime | Anchors | Output artifact types | Public-safe claim |
|--------|----------------|---------|---------|---------|------------------------|-------------------|
| **`5CEZ_native` (Golden Set)** | **HIV-1 Env CD4bs therapeutic scaffold — end-to-end computational case study** | **310 K, pH 7.4, glycan-aware (645 atoms)** | **1.74 min** | **12 (91.7% retention)** | **Placeholder SDF + JSON constraints** (full 693.45 Da SDF via authorization) | **Physics-informed TDF workflow bridging glycan gaps; patent-protected — not clinical validation** |
| `3PTB` | Ligand-removed trypsin active-site recovery | 298 K, pH 7.4 | ~1.77 min | 12 | JSON constraints, generation plan, pharmacophore PDB, HTML viewer | Demonstrates apo-style active-site-adjacent anchor recovery from a classic serine protease structure; not a drug-design validation |
| `9TZD` | Retrospective de novo enzyme / KempTIM1 benchmark; acidic-context stress test | 310 K, pH 6.5 | ~1.7 min | 8 | JSON constraints, generation plan, pharmacophore PDB, HTML viewer | Demonstrates context-aware constraint export on a public de novo enzyme structure; not a clinical or therapeutic validation |
| `5CEZ_clean` | Viral protein epitope-surface constraint mapping demo (glycan-stripped) | 310 K, pH 7.4 | ~1.73 min | 12 | JSON constraints, generation plan, pharmacophore PDB, HTML viewer | Demonstrates epitope-adjacent surface anchor mapping on a glycan-stripped viral glycoprotein demo structure; not immunogen design or efficacy evidence |

## Golden Set — HIV-1 Therapeutic Scaffold (5CEZ)

See [`case_studies/hiv_therapeutic_5cez/README.md`](case_studies/hiv_therapeutic_5cez/README.md) for the full end-to-end computational case study documentation, including:

- Apo-PDB processing with native glycan shield retention (**645 atoms**)
- Pharm2Mol export of **12** pharmacophore anchors (`constraints.json` — publicly published)
- Final **693.45 Da** linked scaffold (placeholder SDF in repo; **full-fidelity structure available upon authorized request**)
- **Physics-informed** TDF ground-state search — **no target-specific ML training**

## Notes

- Runtimes are approximate wall-clock values from local benchmark runs on classical hardware.
- Anchor counts refer to exported pharmacophore constraint points in each example bundle.
- Feature labels (`hydrophobic_aromatic`, `hbond_donor_acceptor`, etc.) are heuristic and explainable, not experimental measurements.
