# Golden Set Case Study — HIV-1 Env CD4-Binding Site Therapeutic Scaffold (PDB 5CEZ)

This folder documents the **validated end-to-end campaign** for a **693.45 Da** epitope-anchored therapeutic scaffold targeting the HIV-1 envelope CD4-binding site. The workflow demonstrates how a **physics-informed**, **training-free** TDF ground-state search bridges long-span glycan gaps on native glycosylated Env—without target-specific machine learning.

> **Intellectual property notice:** This candidate scaffold is protected by a **patent filing** and is published here solely as a portfolio Golden Set artifact. No therapeutic efficacy, clinical safety, or immunogenicity claims are made.

## End-to-End Campaign

| Stage | Description | Artifact |
|-------|-------------|----------|
| **1. Apo-PDB ingestion** | Native PDB `5CEZ` downloaded; protein ATOM records retained with **645 glycan HETATM atoms** (NAG/BMA/MAN shield) | `examples/5CEZ_env_glycan_stripped_optional/` (stripped reference); native run in benchmark suite |
| **2. Bio2Physics context** | Human blood microenvironment: **310 K**, **pH 7.4**; glycan-aware electrostatic boundary conditions | `constraints.json` → `target_profile` |
| **3. TDF-PINN ground-state search** | Phase-gated thermodynamic flux equilibrium (no target-specific ML training) localizes CD4bs pharmacophore minima through the glycan shield | 12 spatial anchors |
| **4. Pharm2Mol constraint export** | Explainable pharmacophore features mapped to generator-ready JSON (`hydrophobic_aromatic`, `hbond_donor_acceptor`, `negative_ionizable`) | `constraints.json` |
| **5. De novo fragment placement** | Spatially aligned chemical fragments at each anchor (TDF-PINN Vertical II) | `5CEZ_native_denovo_fragments.sdf` (benchmark suite) |
| **6. Fragment linking & 3D assembly** | Distance-based bridging with carbon spacers across **long-span glycan gaps**; restrained MMFF/UFF relaxation | `5CEZ_native_linked_candidate.sdf` |
| **7. Phase-Quantum QUBO refinement** *(optional downstream)* | Combinatorial fragment-linking QUBO + entangled TDF sampling for discrete scaffold selection | Phase-Quantum `DrugDiscoveryPipeline` |

## Performance Summary (PDB 5CEZ)

| Metric | Value |
|--------|-------|
| Wall-clock time | **1.74 min** |
| Glycan atoms retained | **645** |
| Anchor retention (vs glycan-stripped reference) | **91.7%** |
| Pharmacophore anchors exported | **12** |
| Final linked scaffold | **693.45 Da** |
| Target-specific ML training | **None** (physics-informed TDF ground-state search) |

## Files in This Folder

| File | Description |
|------|-------------|
| `constraints.json` | Pharm2Mol-exported pharmacophore constraints (12 anchors) with validation metadata |
| `5CEZ_native_linked_candidate.sdf` | Final 3D molecular scaffold in native pocket coordinates (~x −361, y 232) |
| `README.md` | This end-to-end campaign summary |

## Physics-Informed Design Principles

1. **No evolutionary MSA dependency** — thermodynamic minima are inferred from electrostatics and void-filling physics on the input structure.
2. **Glycan-aware boundaries** — native glycan shield atoms are retained so anchors must penetrate realistic epitope occlusion.
3. **Explainable constraints** — every anchor carries coordinates, inferred type, confidence, and nearest receptor residues.
4. **Restrained chemical assembly** — fragment linking respects valence and 3D distance heuristics; coordinates remain in the original PDB frame.

## Reproducing the Campaign

From the `tdf-benchmark-suite` repository:

```bash
python run_blind_test_5CEZ_native.py --target-case hiv-therapeutic
python run_denovo_generation.py --target-case hiv-therapeutic
python run_fragment_linking.py --target-case hiv-therapeutic
```

Or via the batch runner (defaults to the 5CEZ Golden Set validation):

```bash
python -m tdf_benchmark_suite.runner --target-case hiv-therapeutic
```

## Related Public Examples

- Stripped epitope reference: [`examples/5CEZ_env_glycan_stripped_optional/`](../examples/5CEZ_env_glycan_stripped_optional/)
- Cross-target overview: [`benchmark_summary.md`](../benchmark_summary.md)

## Citations & Provenance

- PDB [5CEZ](https://www.rcsb.org/structure/5CEZ) — publicly deposited HIV-1 Env structure.
- See [`THIRD_PARTY_DATA_NOTICE.md`](../THIRD_PARTY_DATA_NOTICE.md) for data-use terms.
