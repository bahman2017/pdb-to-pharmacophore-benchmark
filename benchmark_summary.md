# Benchmark Summary

| Target | Benchmark type | Context | Runtime | Anchors | Output artifact types | Public-safe claim |
|--------|----------------|---------|---------|---------|------------------------|-------------------|
| `3PTB` | Ligand-removed trypsin active-site recovery | 298 K, pH 7.4 | ~1.77 min | 12 | JSON constraints, generation plan, pharmacophore PDB, HTML viewer | Demonstrates apo-style active-site-adjacent anchor recovery from a classic serine protease structure; not a drug-design validation |
| `9TZD` | Retrospective de novo enzyme / KempTIM1 benchmark; acidic-context stress test | 310 K, pH 6.5 | ~1.7 min | 8 | JSON constraints, generation plan, pharmacophore PDB, HTML viewer | Demonstrates context-aware constraint export on a public de novo enzyme structure; not a clinical or therapeutic validation |
| `5CEZ_clean` | Viral protein epitope-surface constraint mapping demo (glycan-stripped) | 310 K, pH 7.4 | ~1.73 min | 12 | JSON constraints, generation plan, pharmacophore PDB, HTML viewer | Demonstrates epitope-adjacent surface anchor mapping on a glycan-stripped viral glycoprotein demo structure; not immunogen design or efficacy evidence |

## Notes

- Runtimes are approximate wall-clock values from local benchmark runs on classical hardware.
- Anchor counts refer to exported pharmacophore constraint points in each example bundle.
- Feature labels (`hydrophobic_aromatic`, `hbond_donor_acceptor`, etc.) are heuristic and explainable, not experimental measurements.
