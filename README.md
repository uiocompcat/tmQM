# tmQM: 2024 release

This repository contains the quantum chemical properties, including geometries, natural atomic charges and Wiberg bond orders of the 108k transition metal complexes (TMCs) in the last version of the **tmQM** dataset. This collection includes all 30 transition metals across the 3d, 4d and 5d series, combined with more than 30k different ligands.

![108k_tmQM_Web_Figure](https://github.com/user-attachments/assets/aad441fb-42e1-4086-b2ed-24565c201d17)

The **tmQM** dataset contains organometallic, bioinorganic, and Werner complexes. Structures were extracted from the 2024 release of the Cambridge Structural Database (CSD) with a series of filters, yielding mononuclear TMCs with charges in the range [-1, 0, 1]. Electronic structure properties, including the energy, dipole moment, polarizability, and HOMO–LUMO gap, were all computed for the closed-shell singlet state. Two levels of theory were used: GFN2-xTB (geometries) and DFT (single-point properties).

The 2024 version of the **tmQM** dataset is an extension of the original **tmQM** dataset reported in this article: [The tmQM Dataset - Quantum Geometries and Properties of 86k Transition Metal Complexes](https://pubs.acs.org/doi/10.1021/acs.jcim.0c01041). **tmQM** has also been used to derive a 60k graph dataset ([**tmQMg**](https://pubs.rsc.org/en/content/articlelanding/2023/dd/d2dd00129b)) and a 30k ligand library ([**tmQMg-L**](https://www.nature.com/articles/s43588-024-00616-5)), both derived from NBO analysis.

The purpose of **tmQM** is to provide the scientific community with a reliable source for developing and testing machine learning models for the exploration of the TMC chemical space.

The **tmQM** dataset is also available for download from the [UiO Computational Catalysis Group website](https://www.uiocompcat.info/tmqmdataset).

## tmQM data files
###### [tmQM/tmQM_X1.xyz.gz](tmQM/tmQM_X1.xyz.gz), [tmQM/tmQM_X2.xyz.gz](tmQM/tmQM_X2.xyz.gz) and [tmQM/tmQM_X3.xyz.gz](tmQM/tmQM_X3.xyz.gz)
- Contain the Cartesian coordinates of all 108k TMCs optimized at the GFN2-xTB level.
- Additional information such as the molecular size, CSD code, charge, spin, stoichiometry and metal node degree is also included.
- Data is split into three files compressed by gzip.

###### [tmQM/tmQM_y.csv](tmQM/tmQM_y.csv)
- Contains the quantum chemical properties of the 108k TMCs computed at the DFT(TPSSh-D3BJ/def2-TZVP) level.
- The DFT properties included are the electronic energy, dispersion energy, dipole moment, natural charge at the metal center, HOMO-LUMO gap, HOMO energy, and LUMO energy. The  polarizability is at the GFN2-xTB level of theory.

###### [tmQM/tmQM_X.q](tmQM/tmQM_X.q)
- Contains the natural atomic charges of the 108k TMCs calculated at the DFT(TPSSh-D3BJ/def2-TZVP) level.

###### [tmQM/tmQM_X1.BO](tmQM/tmQM_X1.BO), [tmQM/tmQM_X2.BO](tmQM/tmQM_X2.BO) and [tmQM/tmQM_X3.BO](tmQM/tmQM_X3.BO)
- Contain the Wiberg bond orders and atomic valence indices of the 108k TMCs calculated at the GFN2-xTB level.
- Data is split into three files compressed by gzip.


## old_tmQM: 2020 release
###### [old_tmQM/old_tmQM_X1.xyz.gz](old_tmQM/old_tmQM_X1.xyz.gz) and [old_tmQM/old_tmQM_X2.xyz.gz](old_tmQM/old_tmQM_X2.xyz.gz)
- Contains the Cartesian coordinates of the 86k TMCs optimized at the GFN2-xTB level.
- Additional information such as the molecular size, CSD code, charge, spin, stoichiometry and metal node degree is also included.
- Data is split into two files compressed by gzip.
- This and all data below is from the 2020 release of the CSD.

###### [old_tmQM/old_tmQM_y.csv](tmQM/tmQM_y.csv)
- Contains the quantum chemical properties of the 86k TMCs computed at the DFT(TPSSh-D3BJ/def2-SVP) level.
- The DFT properties included are the electronic energy, dispersion energy, dipole moment, natural charge at the metal center, HOMO-LUMO gap, HOMO energy, and LUMO energy. The  polarizability is at the GFN2-xTB level of theory.

###### [old_tmQM/Benchmark2_TPSSh_Opt.xyz](old_tmQM/Benchmark2_TPSSh_Opt.xyz)
- Contains the Cartesian coordinates of all TMCs of [benchmark 2](https://pubs.acs.org/doi/10.1021/acs.jcim.0c01041) optimized at the DFT(TPSSh-D3BJ/def2-SVP) level.
- Additional information such as the molecular size and CSD code is also included.

## Further technical details
The 2024 release of the CSD contains structural data for over 1.3M chemical compounds, of which nearly 0.5M include transition metals. However, not all 0.5M transition metal-containing structures are suited for **tmQM**. TMCs were thus selected and curated using these filters:
- **Chemical composition filter:** Mononuclear TMCs including any of the 30 transition metals bonded to any of these elements: B, C, Si, N, P, As, O, S, Se, F, Cl, Br, and I, and including at least one C atom.
- **Geometry filters (I):** Non-polymeric and with 3D coordinates available, excluding disordered structures.
- **Geometry filters (II):** Heaviest fragment with a transition metal; excludes co-crystalizing molecules (_e.g._, solvents and counterions).

- **Electronic structure filters:** Neutral and ±1 charged TMCs with an even number of electrons.

- **Curation filter (I):** Only the TMCs for which both the xTB and DFT calculations converged.

- **Curation filter (II):** The 7% TMCs with the largest deviation of the xTB geometry relative to the CSD structure were excluded (normalized by _r_ factor and number of atoms).

- **Curation filter (III):** xTB-optimized geometries without any H atom, or with C atoms with missing Hs, were excluded using the filter developed by Ulissi and Blau in [this article](https://pubs.acs.org/doi/10.1021/acs.jcim.3c01226).

- **Curation filter (IV):** xTB-optimized geometries with missing Hs, as well as dissociated, isolated ligands, were excluded using a C-focused multi-radii geometric filter.
