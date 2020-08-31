# tmQM dataset
This repository contains the coordinates ([data/tmQM_X1.xyz.gz](data/tmQM_X1.xyz.gz) and [data/tmQM_X2.xyz.gz](data/tmQM_X2.xyz.gz)) and properties ([data/tmQM_y.csv](data/tmQM_y.csv)) of the 116,332 structures in the tmQM dataset.

More information is available in our paper on ChemRxiv (add link).

## Data
###### [data/tmQM_X1.xyz.gz](data/tmQM_X1.xyz.gz) and [data/tmQM_X2.xyz.gz](data/tmQM_X2.xyz.gz)
- Contains the Cartesian coordinates of all metal complexes optimized at the DFTB(GFN2-xTB) level in .xyz format.
- Additional information such as the molecular size, CSD code, charge, spin, stoichiometry and metal node degree is also included.
- The geometries are split into two files compressed by gzip.

###### [data/tmQM_y.csv](data/tmQM_y.csv)
- Contains quantum properties computed at the DFT(TPSSh-D3BJ/def2-SVP) level.
- Properties included are electronic energy, dispersion energy, dipole moment, natural charge of the metal center, HOMO-LUMO gap, HOMO energy, LUMO energy and polarizability (at the DFTB(GFN2-xTB) level of theory).
