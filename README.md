# ProtUni_Mapping
Mapping the Protein Universe using Deep Learning Variational Autoencoder.

Note: Training done using google colab

## Requierements

- tensorflow                    2.7.0
- keras                         2.7.0
- matplotlib                    3.2.2
- numpy                         1.19.5
- pandas                        1.1.5

## Clone the Repository

```shell
$ git clone https://github.com/fshokor/ProtUni_Mapping.git
$ cd ProtUni_Mapping
```

## Data set
- `arti_exp_real_fold_df.csv` :
    - Randomly generated sequences
    - Sequences generated with expected probability
    - Real biological sequences with fold class ([SCOPe](http://scop.berkeley.edu/downloads/scopeseq-2.08/astral-scopedom-seqres-gd-sel-gs-bib-40-2.08.fa))
- `diseases_df.csv`: sequences with associated disease
- `function_domain_df.csv`: sequences with function and domain (Eukaryota, Bacteria, Viruses and Archaea)
- `protein_types_df.csv`: sequences with structure

    

## Notebooks
- `data_generation.ipynb`
    - Generate random sequences 
    - Generate sequences with expected probability
    - Mutate sequences randomly
    - Muatate sequence based on blossum transition matrix
- `dataframe.ipynb`
    - Generate dataframe for each sequences type
- `embedding.ipynb`
    - Genrate sequence embeddings
- `split_data.ipynb `
    - Split data into train, validation and test
- `VAE_model.ipynb`
    - Build and train VAE lstm model
- `encoding.ipynb`
    - Encode embeddings using VAE model
    - Reduce dimensionality using tSNE
    - Generate new dataframe with the coordinates
- `Projection.ipynb` 
    - Map Protein Universe 

**References:**
1. Fox NK, Brenner SE, Chandonia JM. 2014. SCOPe: Structural Classification of Proteins—extended, integrating SCOP and ASTRAL data and classification of new structures. Nucleic Acids Research 42:D304-309. doi: 10.1093/nar/gkt1240.
2. Elnaggar, A., Heinzinger, M., Dallago, C., Rehawi, G., Wang, Y., Jones, L., Gibbs, T., Feher, T., Angerer, C., Steinegger, M., Bhowmik, D., and Rost B., (2021) ProtTrans: Toward Understanding the Language of Life Through Self-Supervised Learning. IEEE TRANS PATTERN ANALYSIS & MACHINE INTELLIGENCE, VOL. 14, NO. 8, https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9477085 
