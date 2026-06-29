# Candidate Generation Plan: 3PTB_CLEAN

## Target profile
- Pharmacophore anchor points: **12**
- Receptor chains: **1**
- Inferred feature types: hbond_donor_acceptor, hydrophobic_aromatic, negative_ionizable

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
- Point 1: `hbond_donor_acceptor` at (-4.20, 11.28, 17.52) Å [confidence 0.90; nearby: GLN192A, ILE16A, VAL213A, CYS220A, TYR228A, VAL17A, ASN143A]
- Point 2: `hydrophobic_aromatic` at (-4.20, 11.28, 30.02) Å [confidence 0.95; nearby: LEU33A, GLY43A, TRP141A, GLY193A, ILE73A, VAL31A]
- Point 3: `hbond_donor_acceptor` at (-4.20, 14.78, 22.52) Å [confidence 0.75; nearby: GLY142A, ASN143A, TYR151A]
- Point 4: `hydrophobic_aromatic` at (6.30, 1.78, 31.02) Å [confidence 0.95; nearby: VAL52A, ASN48A, VAL53A, TYR29A, ILE121A, VAL31A, SER120A, GLY44A, ALA119A]
- Point 5: `hydrophobic_aromatic` at (-4.20, 10.28, 17.02) Å [confidence 0.95; nearby: TYR228A, ILE16A, VAL17A, VAL213A, ILE138A, LEU158A, CYS220A, GLN192A]
- Point 6: `hydrophobic_aromatic` at (8.80, 1.78, 18.52) Å [confidence 0.95; nearby: VAL199A, PRO124A, CYS232A, LYS204A, PHE181A, LYS230A, THR229A, CYS201A, ILE212A]
- Point 7: `hbond_donor_acceptor` at (-4.20, 14.28, 21.02) Å [confidence 0.90; nearby: SER195A, SER190A, GLY142A, ASN143A, CYS220A, VAL213A]
- Point 8: `negative_ionizable` at (-1.70, 14.78, 29.02) Å [confidence 0.60; nearby: HIS40A, GLY43A, LEU33A, GLY193A, CYS58A, SER195A]
- Point 9: `hbond_donor_acceptor` at (-4.20, 13.78, 20.02) Å [confidence 0.75; nearby: CYS220A, SER195A, VAL213A, ASN143A, GLY142A, ILE16A]
- Point 10: `hydrophobic_aromatic` at (7.80, 1.78, 30.02) Å [confidence 0.95; nearby: VAL53A, VAL52A, ILE121A, SER120A, LEU209A, TYR29A]
- Point 11: `hydrophobic_aromatic` at (8.80, 12.78, 29.52) Å [confidence 0.95; nearby: SER54A, ALA56A, ILE106A, SER88A, ILE103A, ILE89A, VAL90A, TYR59A, CYS58A, VAL53A]
- Point 12: `hydrophobic_aromatic` at (-1.20, 0.28, 18.02) Å [confidence 0.90; nearby: VAL199A, LYS159A, PRO198A, SER139A, ALA160A]
