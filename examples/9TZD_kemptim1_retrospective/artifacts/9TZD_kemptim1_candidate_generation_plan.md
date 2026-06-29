# Candidate Generation Plan: 9TZD

## Target profile
- Pharmacophore anchor points: **8**
- Receptor chains: **1**
- Inferred feature types: hydrophobic_aromatic

## Recommended generation modes
- A deeper, well-defined anchor field supports **small-molecule** de novo design with standard pharmacophore-guided generators.
- Combine spatial anchors from TDF with inferred chemical features below.
- For enzyme active sites, prioritize ligands that reproduce the anchor geometry.
- For flat or exposed epitopes, favor larger scaffolds with conformational preorganization.

## Baseline generation filters
1. **No severe protein clash** — reject poses with receptor overlap above tolerated vdW thresholds.
2. **Cover at least 3 pharmacophore points** — partial matches are allowed only for exploratory runs.
3. **Functional disruption** — prioritize chemotypes predicted to block binding, catalysis, or PPI formation.

## Constraint points
- Point 1: `hydrophobic_aromatic` at (-16.34, 2.15, 6.65) Å [confidence 0.95; nearby: ILE114A, VAL117A, ILE172A, LEU194A, LEU115A, ALA175A, LEU193A, ALA95A, ALA3A]
- Point 2: `hydrophobic_aromatic` at (-19.34, -10.35, 5.15) Å [confidence 0.90; nearby: ARG46A, LEU49A, ALA45A, ASP67A, ILE68A, ARG16A, ASP24A]
- Point 3: `hydrophobic_aromatic` at (-20.34, -12.35, 8.65) Å [confidence 0.95; nearby: ARG47A, LEU13A, ILE48A, ILE22A, ALA20A, ALA15A, ARG46A, ASP24A, ASP21A, TYR4A]
- Point 4: `hydrophobic_aromatic` at (-19.84, -11.35, 8.15) Å [confidence 0.95; nearby: ALA45A, ARG16A, ILE48A, LEU40A, LEU12A, ASP24A, ASP21A, ALA20A, LEU49A, LEU13A, TYR4A, ARG46A, ALA15A]
- Point 5: `hydrophobic_aromatic` at (-15.34, 2.65, 12.15) Å [confidence 0.95; nearby: LEU127A, ALA119A, MET173A, LEU182A, ALA196A]
- Point 6: `hydrophobic_aromatic` at (-15.34, -0.35, 11.15) Å [confidence 0.95; nearby: ASP24A, ALA5A, ALA3A, ALA196A, PHE174A, VAL124A, VAL195A, LEU49A, SER176A]
- Point 7: `hydrophobic_aromatic` at (-21.84, -8.85, 4.65) Å [confidence 0.95; nearby: ALA20A, GLU1A, ILE2A, ILE48A, ALA3A, ARG46A, ARG16A]
- Point 8: `hydrophobic_aromatic` at (-9.84, 3.15, 7.65) Å [confidence 0.95; nearby: LEU104A, PRO72A, VAL117A, ALA118A, VAL71A, MET173A, ASP73A, ALA95A, LEU115A, ALA70A, TRP128A]
