# Benchmark Summary

| Target | Benchmark type | Context | Runtime | Anchors | Output artifact types | Public-safe claim |
|--------|----------------|---------|---------|---------|------------------------|-------------------|
| **`5CEZ_native` (Golden Set)** | **PDB-to-scaffold hypothesis workflow — HIV-1 Env CD4bs computational case study** | **310 K, pH 7.4, glycan-aware (645 atoms)** | **1.74 min** | **12 (91.7% retention)** | **Placeholder SDF + JSON constraints** (full 693.45 Da SDF via authorization) | **Fast, explainable, patent-pending workflow — not a drug claim** |
| `3PTB` | Ligand-removed trypsin active-site recovery | 298 K, pH 7.4 | ~1.77 min | 12 | JSON constraints, generation plan, pharmacophore PDB, HTML viewer | Demonstrates apo-style active-site-adjacent anchor recovery from a classic serine protease structure; not a drug-design validation |
| `9TZD` | Retrospective de novo enzyme / KempTIM1 benchmark; acidic-context stress test | 310 K, pH 6.5 | ~1.7 min | 8 | JSON constraints, generation plan, pharmacophore PDB, HTML viewer | Demonstrates context-aware constraint export on a public de novo enzyme structure; not a clinical or therapeutic validation |
| `5CEZ_clean` | Viral protein epitope-surface constraint mapping demo (glycan-stripped) | 310 K, pH 7.4 | ~1.73 min | 12 | JSON constraints, generation plan, pharmacophore PDB, HTML viewer | Demonstrates epitope-adjacent surface anchor mapping on a glycan-stripped viral glycoprotein demo structure; not immunogen design or efficacy evidence |

## Golden Set — HIV-1 Env CD4-Binding-Site Computational Scaffold Hypothesis (5CEZ)

See [`case_studies/hiv_therapeutic_5cez/README.md`](case_studies/hiv_therapeutic_5cez/README.md) for the full end-to-end computational case study. **We are not claiming a drug**—this Golden Set demonstrates a **fast (~1.74 min), explainable, patent-pending PDB-to-scaffold hypothesis workflow**, including:

- Apo-PDB processing with native glycan shield retention (**645 atoms**)
- Pharm2Mol export of **12** explainable pharmacophore anchors (`constraints.json` — publicly published)
- Final **693.45 Da** linked **computational scaffold hypothesis** (placeholder SDF in repo; **full-fidelity structure available upon authorized request**)
- **Physics-informed** TDF ground-state search — **no target-specific ML training**

## Notes

- Runtimes are approximate wall-clock values from local benchmark runs on classical hardware.
- Anchor counts refer to exported pharmacophore constraint points in each example bundle.
- Feature labels (`hydrophobic_aromatic`, `hbond_donor_acceptor`, etc.) are heuristic and explainable, not experimental measurements.
