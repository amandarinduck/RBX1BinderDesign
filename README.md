# Proteinbase x GEM RBX1 Binder Design Methods and Submission

Sequence from PDB 2LGV was cropped to modified RING H2 domain(auth seq ID V38-W101 of 2LGV) as determined by CD-search(accession: cd16485). Sequence was then refolded via AlphaFold3. Pairwise structure alignment(TM-Align) showed 2.08 RMSD when comparing refolded cropped structure to original PDB. This cropped structure was used as input for this binder design campaign. Hotspot residues were manually identified by observation in MolStarViewer, identifying patches of hydrophobic residues with sufficient amounts of accessible surface area. For this binder design campaign, specified hotspot residues in cropped input file were as follows:

-A35(corresponding to auth ID W72 in PDB 2LGV) -A36(corresponding to auth ID G73 in PDB 2LGV) -A37(corresponding to auth ID V74 in PDB 2LGV) -A64(corresponding to auth ID W101 in PDB 2LGV)

Binder Design Specifications

A local installation of FreeBindCraft with PyRosetta was used for this campaign(https://github.com/cytokineking/FreeBindCraft?ref=blog.escalante.bio), using the following settings:

-Miniprotein -Target chain: A -Hotspot Residues: A35,A36,A37,A64 -Min/Max Length: 65/150 aa -Number of Final Designs: 100 -Filter Settings: default_filters -Advanced Settings: default_4stage_multimer

The final compiled output of 100 binders was then filtered by average ipTM and ipSAE scores, using a cutoff of average ipTM > 0.8 AND average ipSAE > 0.6. This produced a final list of 34 binders for submission.
