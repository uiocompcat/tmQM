![tmQM_Figure](https://user-images.githubusercontent.com/51946437/91875604-fabc5300-ec7b-11ea-9b0d-b6b308dc942b.png)

This repository contains the quantum geometries ([data/tmQM_X1.xyz.gz](data/tmQM_X1.xyz.gz) and [data/tmQM_X2.xyz.gz](data/tmQM_X2.xyz.gz)) and properties ([data/tmQM_y.csv](data/tmQM_y.csv)) of the 86,665 transition metal complexes in the tmQM dataset.

More information is available in our paper on [ChemRxiv](https://chemrxiv.org/articles/preprint/The_tmQM_Dataset_-_Quantum_Geometries_and_Properties_of_86k_Transition_Metal_Complexes/12894818/1).

## Data
###### [data/tmQM_X1.xyz.gz](data/tmQM_X1.xyz.gz) and [data/tmQM_X2.xyz.gz](data/tmQM_X2.xyz.gz)
- Contains the Cartesian coordinates of all metal complexes optimized at the DFTB(GFN2-xTB) level in .xyz format.
- Additional information such as the molecular size, CSD code, charge, spin, stoichiometry and metal node degree is also included.
- The geometries are split into two files compressed by gzip.

###### [data/tmQM_y.csv](data/tmQM_y.csv)
- Contains the quantum properties computed at the DFT(TPSSh-D3BJ/def2-SVP) level.
- Properties included are electronic energy, dispersion energy, dipole moment, natural charge of the metal center, HOMO-LUMO gap, HOMO energy, LUMO energy and polarizability (at the DFTB(GFN2-xTB) level of theory).
