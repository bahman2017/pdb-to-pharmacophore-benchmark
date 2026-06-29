# Validation Metrics (Planned / Portfolio Roadmap)

The following metrics are appropriate for evaluating this class of PDB-to-pharmacophore constraint benchmarks without disclosing proprietary engine internals.

| Metric | Description |
|--------|-------------|
| Anchor-to-known-ligand distance | Distance from exported anchors to a reference ligand or catalytic motif when available |
| Contact-map overlap | Overlap between anchor neighborhoods and known functional residue contacts |
| False-positive surface anchor count | Number of anchors far from reference functional sites |
| Anchor clustering | Spatial clustering quality and minimum separation between anchors |
| Runtime | Wall-clock time to produce the public artifact bundle |
| Reproducibility | Stability of anchor sets across repeated runs with fixed inputs |
| Comparison with pocket finders | Qualitative comparison to geometry-based pocket detection tools |
| Comparison with pharmacophore tools | Qualitative comparison to pharmacophore editors/generators |

## Interpretation Guidance

Metrics should be reported as **benchmark diagnostics**, not as therapeutic performance indicators.
