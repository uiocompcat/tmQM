![tmQM_Figure](https://user-images.githubusercontent.com/51946437/91875604-fabc5300-ec7b-11ea-9b0d-b6b308dc942b.png)

This repository contains the quantum geometries ([data/tmQM_X1.xyz.gz](data/tmQM_X1.xyz.gz) and [data/tmQM_X2.xyz.gz](data/tmQM_X2.xyz.gz)) and properties ([data/tmQM_y.csv](data/tmQM_y.csv)) of the 86,665 transition metal complexes in the tmQM dataset.

More information is available in our paper in [JCIM](https://pubs.acs.org/doi/10.1021/acs.jcim.0c01041) or the preprint on [ChemRxiv](https://chemrxiv.org/articles/preprint/The_tmQM_Dataset_-_Quantum_Geometries_and_Properties_of_86k_Transition_Metal_Complexes/12894818/1).

**UPDATE**: The tmQM dataset now includes the atomic natural charges (at the DFT(TPSSh-D3BJ/def2-SVP) level) and Wiberg bond orders (at the GFN2-xTB level). All data is available for download from the [UiO Computational Catalysis Group website](https://www.uiocompcat.info/tmqmdataset).

## Data
###### [data/tmQM_X1.xyz.gz](data/tmQM_X1.xyz.gz) and [data/tmQM_X2.xyz.gz](data/tmQM_X2.xyz.gz)
- Contains the Cartesian coordinates of all metal complexes optimized at the GFN2-xTB level in .xyz format.
- Additional information such as the molecular size, CSD code, charge, spin, stoichiometry and metal node degree is also included.
- The geometries are split into two files compressed by gzip.

###### [data/tmQM_y.csv](data/tmQM_y.csv)
- Contains the quantum properties computed at the DFT(TPSSh-D3BJ/def2-SVP) level.
- Properties included are electronic energy, dispersion energy, dipole moment, natural charge of the metal center, HOMO-LUMO gap, HOMO energy, LUMO energy and polarizability (at the GFN2-xTB level of theory).

###### [data/Benchmark2_TPSSh_Opt.xyz](data/Benchmark2_TPSSh_Opt.xyz)
- Contains the Cartesian coordinates of all metal complexes of benchmark 2 optimized at the DFT(TPSSh-D3BJ/def2-SVP) level in .xyz format.
- Additional information such as the molecular size and CSD code is also included.

---

[![CC BY NC 4.0][cc-by-nc-image]][cc-by-nc]

This work is licensed under a
[Creative Commons Attribution-NonCommercial 4.0 International License][cc-by-nc].

[cc-by-nc]: http://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-image]: https://i.creativecommons.org/l/by-nc/4.0/88x31.png
