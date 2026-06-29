# PDB-to-Pharmacophore Constraint Benchmark (Public Artifacts)

This repository contains non-confidential benchmark artifacts from a lightweight PDB-to-pharmacophore constraint workflow. The workflow converts ligand-stripped or apo-style protein structures into explainable spatial anchor points, inferred pharmacophore features, generator-ready JSON constraints, and 3D visualization artifacts. This is not a validated drug discovery product and does not claim therapeutic efficacy. The benchmark is intended to demonstrate scientific AI workflow automation, protein-structure analysis, and downstream molecule-design constraint generation. A lightweight, training-free PDB-to-pharmacophore constraint benchmark that demonstrates explainable active-site and epitope-adjacent anchor generation from public protein structures.

## What This Repository Contains

- Public benchmark examples derived from PDB structures (`3PTB`, `9TZD`, `5CEZ`)
- Explainable pharmacophore constraint JSON files
- Candidate-generation planning markdown (high-level, non-proprietary)
- Pharmacophore point-cloud PDB files (`DU` dummy anchors)
- Interactive HTML 3D viewers (py3Dmol-based)
- Non-confidential methodology, limitations, validation-metric notes, and sanitization documentation

## What This Repository Does NOT Contain

- Core engine source code, proprietary formulas, PINN optimizers, or scoring internals
- Bio2Physics, Pharm2Mol, molecule generation, fragment linking, or ADMET implementation code
- Generated small molecules, scaffolds, SDF/SMILES files, or synthesized candidate structures
- Wet-lab data, clinical claims, or efficacy conclusions
- Private repository paths, credentials, or machine-specific environment details

## Important Disclaimers

**No therapeutic claims.** These artifacts demonstrate workflow automation and structural constraint export only. They do not establish safety, efficacy, immunogenicity, neutralization, or clinical relevance.

**No molecule/scaffold disclosure.** This public repository intentionally excludes de novo generated molecules and linked scaffolds. Only explainable anchor points and constraint metadata are published.

**Public PDB provenance.** Source structures are publicly available Protein Data Bank entries. Users should cite the original PDB depositions and associated publications when reusing these materials.

**Portfolio purpose.** This repository is shared for portfolio, resume, and non-commercial technical evaluation in AI, life sciences, scientific software, and research engineering contexts.

## Repository Layout

```
examples/          # Per-target benchmark bundles
docs/              # Non-confidential methodology and limitations
benchmark_summary.md
THIRD_PARTY_DATA_NOTICE.md
```

## Quick Start

1. Open `benchmark_summary.md` for a cross-target overview.
2. Browse `examples/<target>/artifacts/` for JSON, PDB, HTML, and planning files.
3. Read `docs/limitations.md` before interpreting feature labels or anchor coordinates.

## License

See `LICENSE` for terms of use.
