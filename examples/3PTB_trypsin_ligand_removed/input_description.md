# 3PTB — Trypsin Ligand-Removed Benchmark

## Overview

Classic apo active-site recovery demonstration using a public trypsin structure (PDB `3PTB`).

## Preprocessing

- Public trypsin structure
- Ligands, waters, and non-protein HETATM records removed before anchor export
- Apo-style void-centered constraint mapping

## Context Metadata

- Temperature: 298 K
- pH: 7.4

## Public-Safe Claim

This example demonstrates **active-site-adjacent anchor recovery** on a well-studied serine protease scaffold. It is a workflow and visualization benchmark only—not a drug-design validation, potency prediction, or therapeutic claim.

## Artifacts

See `artifacts/` for JSON constraints, a high-level generation plan, pharmacophore PDB points, and an HTML viewer.
