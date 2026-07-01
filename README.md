# PDB-to-Pharmacophore Constraint Benchmark (Public Artifacts)

This repository contains non-confidential benchmark artifacts from a lightweight PDB-to-pharmacophore constraint workflow. The workflow converts ligand-stripped or apo-style protein structures into explainable spatial anchor points, inferred pharmacophore features, generator-ready JSON constraints, and 3D visualization artifacts. This is not a validated drug discovery product and does not claim therapeutic efficacy. The benchmark is intended to demonstrate scientific AI workflow automation, protein-structure analysis, and downstream molecule-design constraint generation.

Repository: [github.com/bahman2017/pdb-to-pharmacophore-benchmark](https://github.com/bahman2017/pdb-to-pharmacophore-benchmark)

## Featured Success Case — HIV-1 Env CD4-Binding-Site Computational Scaffold Hypothesis

The **Golden Set** for PDB **5CEZ** documents an **end-to-end computational case study**—a **physics-informed** workflow from native glycosylated Env processing through Pharm2Mol constraint export to a **693.45 Da** linked therapeutic-scaffold hypothesis—achieved via **TDF ground-state search without target-specific machine learning training**.

This candidate is **protected by a patent filing** and showcases the platform's capability to **construct a long-span scaffold across glycan-proximal anchor geometry** while retaining explainable pharmacophore anchors in the native pocket coordinate frame.

| Metric (PDB 5CEZ) | Result |
|-------------------|--------|
| Wall-clock time | **1.74 min** |
| Glycan atoms retained | **645** |
| Anchor retention (vs stripped reference) | **91.7%** |
| Pharmacophore anchors | **12** |
| Final linked therapeutic-scaffold hypothesis | **693.45 Da** |
| Target-specific ML training | **None** (physics-informed TDF) |

**Artifacts:** [`case_studies/hiv_therapeutic_5cez/`](case_studies/hiv_therapeutic_5cez/)

- `5CEZ_native_linked_candidate.sdf` — **placeholder SDF** (header + IP notice only; full 693.45 Da structure available upon authorized request)
- `constraints.json` — 12 Pharm2Mol pharmacophore anchors (process metadata; publicly published)
- `README.md` — full end-to-end computational case study documentation

## ⚖️ IP & Patent Status

The therapeutic-scaffold hypothesis generated in the [`hiv_therapeutic_5cez`](case_studies/hiv_therapeutic_5cez/) case study is **subject to an active patent filing**. The public repository contains a **truncated placeholder SDF** — not the full atomic coordinates of the linked **693.45 Da** candidate.

This artifact is published **for research, audit, and benchmark purposes only**. It is not licensed for product development, therapeutic use, or commercial exploitation without separate written permission.

**Any commercial use or derivative development based on this specific molecular scaffold requires explicit authorization.**

The **full-fidelity SDF** (complete 3D structure in native pocket coordinates) is available **upon authorized request** for qualified research, audit, or due-diligence review. Contact the repository owner to request access.

Researchers and auditors reviewing the HIV case study should read this notice **before** requesting or using the proprietary candidate structure. The published `constraints.json` describes the pharmacophore process and anchor geometry; it does not substitute for the protected final molecule.

## What This Repository Contains

- Public benchmark examples derived from PDB structures (`3PTB`, `9TZD`, `5CEZ`)
- **Golden Set case study** with placeholder scaffold SDF and published constraints (`case_studies/hiv_therapeutic_5cez/`)
- Explainable pharmacophore constraint JSON files
- Candidate-generation planning markdown (high-level, non-proprietary)
- Pharmacophore point-cloud PDB files (`DU` dummy anchors)
- Interactive HTML 3D viewers (py3Dmol-based)
- Non-confidential methodology, limitations, validation-metric notes, and sanitization documentation

## What This Repository Does NOT Contain

- Core engine source code, proprietary formulas, PINN optimizers, or scoring internals
- Bio2Physics, Pharm2Mol, molecule generation, fragment linking, or ADMET implementation code
- Wet-lab data, clinical claims, or efficacy conclusions
- Private repository paths, credentials, or machine-specific environment details

> **Note:** The Golden Set case study publishes **constraint JSON** and a **placeholder SDF** (no proprietary coordinates). The full linked therapeutic-scaffold hypothesis is available upon authorized request. Other example bundles remain anchor-only.

## Important Disclaimers

**No therapeutic claims.** These artifacts demonstrate workflow automation and structural constraint export only. They do not establish safety, efficacy, immunogenicity, neutralization, or clinical relevance.

**Patent-protected scaffold.** The 5CEZ linked candidate is disclosed under pending intellectual property protection for portfolio evaluation only. See [⚖️ IP & Patent Status](#️-ip--patent-status) above.

**Public PDB provenance.** Source structures are publicly available Protein Data Bank entries. Users should cite the original PDB depositions and associated publications when reusing these materials.

**Portfolio purpose.** This repository is shared for portfolio, resume, and non-commercial technical evaluation in AI, life sciences, scientific software, and research engineering contexts.

## Repository Layout

```
case_studies/      # Golden Set computational case studies (HIV-1 5CEZ therapeutic-scaffold hypothesis)
examples/          # Per-target benchmark bundles
docs/              # Non-confidential methodology and limitations
benchmark_summary.md
THIRD_PARTY_DATA_NOTICE.md
```

## Quick Start

1. Read the **Featured Success Case**: [`case_studies/hiv_therapeutic_5cez/README.md`](case_studies/hiv_therapeutic_5cez/README.md)
2. Open `benchmark_summary.md` for a cross-target overview.
3. Browse `examples/<target>/artifacts/` for JSON, PDB, HTML, and planning files.
4. Read `docs/limitations.md` before interpreting feature labels or anchor coordinates.

## Reproducing the 5CEZ Golden Set

From the companion `tdf-benchmark-suite` repository:

```bash
python -m tdf_benchmark_suite.runner --target-case hiv-therapeutic
```

This applies glycan-aware boundary conditions (**310 K**, **pH 7.4**) used in the patent-backed run.

## License

See `LICENSE` for terms of use.
