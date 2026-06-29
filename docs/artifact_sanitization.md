# Artifact Sanitization Policy

Public exports are produced by an automated sanitization step before publication.

## Removed From Public Artifacts

- Core engine / research source code
- Proprietary formulas, thresholds, and optimizer internals
- Generated molecules, scaffolds, SDF/SMILES, and linked candidate structures
- Absolute local paths (e.g., macOS user home directories, Linux home directories, Windows drive paths)
- Internal repository paths and private branch references
- `physical_boundary_conditions` blocks and `context_source` fields in JSON
- Therapeutic, vaccine, clinical, and efficacy-oriented wording

## Retained In Public Artifacts

- Explainable pharmacophore constraint JSON (coordinates, feature types, nearby residues, confidence)
- High-level candidate-generation planning markdown
- Pharmacophore PDB point files
- HTML viewers for 3D inspection
- Non-confidential methodology and limitation documentation

## Verification

The build script scans the export directory for forbidden file types and residual local paths. Publication should proceed only after a `PASS` validation report.
