# PDB-to-Pharmacophore Constraint Benchmark (Public Artifacts)

This repository demonstrates a **fast, explainable, patent-pending PDB-to-scaffold hypothesis workflow**. Starting from public Protein Data Bank structures, the pipeline exports spatial pharmacophore anchors, generator-ready JSON constraints, and optional linked scaffold hypotheses—with wall-clock runtimes on the order of **~2 minutes** per target on classical hardware.

**We are not claiming a drug.** Nothing in this repository asserts therapeutic efficacy, clinical safety, immunogenicity, or readiness for development. The artifacts support **research, audit, and benchmark review** of an automated structure-to-hypothesis workflow.

Repository: [github.com/bahman2017/pdb-to-pharmacophore-benchmark](https://github.com/bahman2017/pdb-to-pharmacophore-benchmark)

## What We Demonstrate

| Property | Description |
|----------|-------------|
| **Fast** | End-to-end PDB ingestion → anchor export → scaffold hypothesis in **~1.7–1.8 min** (Golden Set reference: 5CEZ) |
| **Explainable** | Every anchor carries coordinates, inferred pharmacophore type, confidence, and nearest receptor residues |
| **Patent-pending** | Core PDB-to-scaffold hypothesis workflow is **subject to an active patent filing** |
| **Workflow-only** | Outputs are **computational scaffold hypotheses**, not validated medicines or lead compounds |

## Featured Success Case — HIV-1 Env CD4-Binding-Site Computational Scaffold Hypothesis

The **Golden Set** for PDB **5CEZ** documents an **end-to-end computational case study** for our **patent-pending PDB-to-scaffold hypothesis workflow**—a **physics-informed** path from native glycosylated Env processing through Pharm2Mol constraint export to a **693.45 Da** linked **computational scaffold hypothesis**, achieved via **TDF ground-state search without target-specific machine learning training**.

This case study is **not a drug claim**. It showcases a **fast, explainable** workflow that **constructs a long-span scaffold across glycan-proximal anchor geometry** while retaining auditable pharmacophore anchors in the native pocket coordinate frame.

| Metric (PDB 5CEZ) | Result |
|-------------------|--------|
| Wall-clock time | **1.74 min** |
| Glycan atoms retained | **645** |
| Anchor retention (vs stripped reference) | **91.7%** |
| Pharmacophore anchors | **12** |
| Final linked computational scaffold hypothesis | **693.45 Da** |
| Target-specific ML training | **None** (physics-informed TDF) |

**Artifacts:** [`case_studies/hiv_therapeutic_5cez/`](case_studies/hiv_therapeutic_5cez/)

- `5CEZ_native_linked_candidate.sdf` — **placeholder SDF** (header + IP notice only; full 693.45 Da structure available upon authorized request)
- `constraints.json` — 12 Pharm2Mol pharmacophore anchors (process metadata; publicly published)
- `README.md` — full end-to-end computational case study documentation

## ⚖️ IP & Patent Status

The **computational scaffold hypothesis** produced by the [`hiv_therapeutic_5cez`](case_studies/hiv_therapeutic_5cez/) case study sits within a workflow that is **subject to an active patent filing**. The public repository contains a **truncated placeholder SDF** — not the full atomic coordinates of the linked **693.45 Da** hypothesis structure.

This repository demonstrates workflow automation **for research, audit, and benchmark purposes only**. It does **not** license product development, therapeutic use, or commercial exploitation without separate written permission.

**Any commercial use or derivative development based on this specific molecular scaffold requires explicit authorization.**

The **full-fidelity SDF** (complete 3D structure in native pocket coordinates) is available **upon authorized request** for qualified research, audit, or due-diligence review. Contact the repository owner to request access.

Researchers and auditors should read this notice **before** requesting the proprietary hypothesis structure. The published `constraints.json` documents the **explainable PDB-to-constraint workflow** and anchor geometry; it does not constitute a drug or efficacy claim.

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

> **Note:** The Golden Set case study publishes **constraint JSON** and a **placeholder SDF** (no proprietary coordinates). The full linked computational scaffold hypothesis is available upon authorized request. Other example bundles remain anchor-only.

## Important Disclaimers

**Not a drug.** We do not claim a therapeutic product, clinical candidate, or validated medicine. All scaffold outputs are **computational hypotheses** produced by an automated workflow.

**Workflow demonstration only.** These artifacts show fast, explainable, patent-pending **PDB-to-scaffold hypothesis** automation. They do not establish safety, efficacy, immunogenicity, neutralization, or clinical relevance.

**Patent-pending workflow.** The underlying PDB-to-scaffold hypothesis methodology is disclosed under pending intellectual property protection for portfolio evaluation only. See [⚖️ IP & Patent Status](#️-ip--patent-status) above.

**Public PDB provenance.** Source structures are publicly available Protein Data Bank entries. Users should cite the original PDB depositions and associated publications when reusing these materials.

**Portfolio purpose.** This repository is shared for portfolio, resume, and non-commercial technical evaluation in AI, life sciences, scientific software, and research engineering contexts.

## Repository Layout

```
case_studies/      # Golden Set computational case studies (HIV-1 5CEZ scaffold hypothesis workflow)
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
