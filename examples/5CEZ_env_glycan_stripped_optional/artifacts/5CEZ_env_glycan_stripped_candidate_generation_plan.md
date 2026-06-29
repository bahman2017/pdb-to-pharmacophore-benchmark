# Candidate Generation Plan: 5CEZ_CLEAN

## Target profile
- Pharmacophore anchor points: **12**
- Receptor chains: **6**
- Inferred feature types: hbond_donor_acceptor, hydrophobic_aromatic, negative_ionizable

## Recommended generation modes
- Multi-chain receptor detected. Prioritize **PPI disruptors**, **macrocycles**, or **peptidomimetics** that span the interface.
- Combine spatial anchors from TDF with inferred chemical features below.
- For enzyme active sites, prioritize ligands that reproduce the anchor geometry.
- For flat or exposed epitopes, favor larger scaffolds with conformational preorganization.

## Baseline generation filters
1. **No severe protein clash** — reject poses with receptor overlap above tolerated vdW thresholds.
2. **Cover at least 3 pharmacophore points** — partial matches are allowed only for exploratory runs.
3. **Functional disruption** — prioritize chemotypes predicted to block binding, catalysis, or PPI formation.

## Constraint points
- Point 1: `hydrophobic_aromatic` at (-362.32, 232.85, 1.97) Å [confidence 0.75; nearby: LEU342G, VAL270G, GLU340G, LYS347G, GLN348G]
- Point 2: `hydrophobic_aromatic` at (-363.32, 232.35, 5.47) Å [confidence 0.90; nearby: VAL346G, TRP395G, TRP338G, LYS347G]
- Point 3: `hbond_donor_acceptor` at (-349.82, 232.85, 7.97) Å [confidence 0.90; nearby: THR455G, GLY471G, PRO470G, ARG469G, LEU285G, ASN283G, VAL286G, GLN258G]
- Point 4: `hydrophobic_aromatic` at (-361.82, 232.35, 9.97) Å [confidence 0.95; nearby: TRP338G, TRP395G, LEU390G, SER393G, GLY343G, PHE361G, THR341G, ASN339G, PHE391G]
- Point 5: `negative_ionizable` at (-349.32, 233.35, 3.97) Å [confidence 0.60; nearby: ARG273G, ASN283G]
- Point 6: `hydrophobic_aromatic` at (-349.82, 233.35, 1.97) Å [confidence 0.95; nearby: LEU452G, ILE272G, SER274G, MET271G, GLN287G, ASN283G, TRP96G, ILE453G, LEU454G]
- Point 7: `hbond_donor_acceptor` at (-348.82, 238.85, 11.97) Å [confidence 0.90; nearby: SER256G, HIS374G, GLY471G, ILE453G, LEU260G, GLY472G, THR373G, SER375G]
- Point 8: `hydrophobic_aromatic` at (-349.82, 233.35, 2.97) Å [confidence 0.95; nearby: ILE453G, LEU454G, ASN283G, ILE272G, SER274G, GLN287G, MET271G]
- Point 9: `hbond_donor_acceptor` at (-352.82, 245.35, -1.03) Å [confidence 0.95; nearby: GLN287G, THR450G, ASN262G, ALA266G, SER481G]
- Point 10: `hydrophobic_aromatic` at (-353.82, 233.35, -1.53) Å [confidence 0.75; nearby: GLN287G, VAL286G, VAL270G]
- Point 11: `hbond_donor_acceptor` at (-349.32, 240.35, 12.47) Å [confidence 0.75; nearby: SER375G, LEU260G, THR373G, LEU261G]
- Point 12: `hbond_donor_acceptor` at (-349.82, 243.85, 0.47) Å [confidence 0.95; nearby: THR450G, GLN287G, ASN478G, LEU260G, ASN262G, TYR484G]
