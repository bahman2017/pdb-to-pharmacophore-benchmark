# Methodology (Non-Confidential Overview)

This document describes the **public-safe** benchmark workflow at a high level. It intentionally omits proprietary formulas, model architectures, training procedures, and implementation code.

## Workflow Stages

1. **Public PDB input**
   - Fetch a publicly deposited structure identifier (e.g., `3PTB`, `9TZD`, `5CEZ`).

2. **Structure preprocessing (when applicable)**
   - Remove ligands, waters, cryoprotectants, and/or glycan HETATM records depending on the benchmark scenario.
   - Produce an apo-style or ligand-removed input suitable for surface/void mapping demos.

3. **Context metadata**
   - Attach non-confidential context labels such as temperature and pH.
   - Context is recorded in exported JSON for explainability.

4. **Anchor generation**
   - Generate spatial anchor points representing candidate pharmacophore locations.
   - Anchors are exported as dummy-atom coordinates (PDB `DU` records).

5. **Pharmacophore feature labeling**
   - Assign heuristic feature classes (e.g., hydrophobic/aromatic, hydrogen-bond donor/acceptor) based on nearby receptor residues.
   - Labels are explainable and intended for downstream constraint consumers.

6. **Artifact export**
   - JSON constraints for generator-ready pipelines
   - Markdown planning summary
   - Pharmacophore PDB point file
   - HTML 3D viewer for inspection

## What Is Not Described Here

- Internal optimizers, PINN loss definitions, or TDF physics
- Proprietary scoring, ranking, or molecule-generation logic
- Any generated small-molecule structures or linked scaffolds
