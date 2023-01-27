# FLFS-FC

Supplementary information related to publication ["Flux Coupling and the Objective Functions’ Length in EFMs"](https://www.mdpi.com/2218-1989/10/12/489)
 published in Metabolites.


The necessary notebooks required to execute this algorithm are included in the 'notebooks' folder.

FLFS-FC.ipynb contains the main program to execute the FLFS-FC algorithm

To use it, you need a decoupled network (i.e. all reactions must be irreversible) and several other files containing:
- List of originally reversible and irreversible ones
- A dictionary that returns, for each originally reversible reaction, the index of its inverse in the decoupled model

FLFS-FC computes the EFMs and store them in a compressed format as frozensets of indices in the decoupled mode. If you prefer getting them as indices from the original model, you will also need another dictionary called toNonDecoupled

In order to get the decoupled model from an original one and all the associated files, you need the notebook decouplingModel.ipynb. These files must be put in the same directory that FLFS-FC.ipynb.

In its present state, both notebooks are prepared to work with the model 'e. coli core' that can be obtained from BIGGs

We have also included the necessary files to work with this model (they are computed from the non-compressed model) in the folder 'Example files'.

## Bibtex


```
@article{guil2020flux,
  title={Flux Coupling and the Objective Functions’ Length in EFMs},
  author={Guil, Francisco and Hidalgo, Jos{\'e} F and Garc{\'\i}a, Jos{\'e} M},
  journal={Metabolites},
  volume={10},
  number={12},
  pages={489},
  year={2020},
  abstract={Structural analysis of constraint-based metabolic network models attempts to find the network’s properties by searching for subsets of suitable modes or Elementary Flux Modes (EFMs). One useful approach is based on Linear Program (LP) techniques, which introduce an objective function to convert the stoichiometric and thermodynamic constraints into a linear program (LP), using additional constraints to generate different nontrivial modes. This work introduces FLFS-FC (Fixed Length Function Sampling with Flux Coupling), a new approach to increase the efficiency of generation of large sets of different EFMs for the network. FLFS-FC is based on the importance of the length of the objective functions used in the associated LP problem and the imposition of additional negative constraints. Our proposal overrides some of the known drawbacks associated with the EFM extraction, such as the appearance of unfeasible problems or multiple repeated solutions arising from different LP problems.},
  publisher={MDPI}
}
