# Incuded files
All files must be put in the same folder than the notebooks
- Original model (from BIGGs) and decoupled model of 'e. coli core'
- Lists of (originally) reversible and irreversible reactions
- A dictionary that returns, for each originally reversible reaction, the index of its inverse in the decoupled model

FLFS-FC computes the EFMs and store them in a compressed format as frozensets of indices in the decoupled mode. If you prefer getting them as indices from the original model, you will also need another dictionary called toNonDecoupled
