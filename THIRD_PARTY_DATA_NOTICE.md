# Third-Party Data Notice

## Source Structures

This repository includes **derived benchmark artifacts** based on publicly available Protein Data Bank (PDB) structures. The original coordinate files are **not** redistributed here unless explicitly included as a small pharmacophore point file derived from benchmark output.

| Example folder | PDB ID | Description |
|----------------|--------|-------------|
| `examples/3PTB_trypsin_ligand_removed` | `3PTB` | Bovine trypsin (public structure; ligand removed in benchmark preprocessing) |
| `examples/9TZD_kemptim1_retrospective` | `9TZD` | KempTIM1 de novo enzyme benchmark structure (public deposition) |
| `examples/5CEZ_env_glycan_stripped_optional` | `5CEZ` | Viral envelope glycoprotein demo structure (glycans stripped for apo-style surface mapping) |

## Attribution

If you reuse these artifacts, please cite:

1. The **original PDB entry** and its primary publication(s).
2. Any third-party libraries used to view artifacts (e.g., py3Dmol in HTML viewers).

This repository provides non-confidential, derived constraint JSON, markdown plans, pharmacophore PDB points, and HTML viewers. It does **not** claim ownership of the underlying experimental structures.

## No Affiliation

This portfolio repository is independent and is not endorsed by the PDB, RCSB, or the authors of the source structures unless separately stated.
