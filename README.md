# SSFGM-Model
This repository contains the source code for the paper Multimodal Geometric Learning-based Antimicrobial Peptide Prediction Enhanced by AlphaFold2 Structures and Surface Features
![image](https://github.com/ggcameronnogg/SSFGM-Model/blob/main/model.png)
<br/>
Please see our manuscript for more details.<br/>

## Requirements
Python version: 3.10.12<br/>
Numpy version: 1.23.1<br/>
Biopython version: 1.79<br/>
torch version: 1.12.1<br/>
PyTorch Geometric version: 2.5.2<br/>
Scikit-learn version: 1.1.2<br/>
ESM version: 2.0.0<br/>
re version: 2.2.1<br/>
Transformers version: 4.41.1

## Data
The datasets for this paper are Benchmark Dataset 1 and Benchmark Dataset 2, which can be viewed in the Data directory.

## Usage
#### Sequence features Extraction
refer to the coding in the Embedding-Method folder.

#### Structure Features Extraction
## Alphafolf Colab Notebook <a href="https://colab.research.google.com/drive/1vco6QQgs6eYJq5XmvQejZyQQDwXkPEu7" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

### Molecular Surface Features Extraction
## Docker tutorial for MaSIF.
## Installation

```
docker pull pablogainza/masif:latest
docker run -it pablogainza/masif
```
You now start a local container with MaSIF. The first step should be to update the repository to make sure you have the latest version (in case the image has not been update):

```
root@b30c52bcb86f:/masif# git pull 
```

### MaSIF-site

### Running MaSIF-site on a single protein from a PDB id

Go into the MaSIF site data directory. 
```
root@b30c52bcb86f:/masif# cd data/masif_site/
root@b30c52bcb86f:/masif/data/masif_site# 
```

We will now run MaSIF site on chain A of PDB id 4ZQK. It is important to always input a chain and a PDB id. The first step consists of preparing the data and it is the slowest part of the process. It consists of downloading the pdb, extracting the chain, protonating it, computing the molecular surface and PB electrostatics, and decomposing the protein into patches (about 1 minute on a 120 residue protein): 

```
root@b30c52bcb86f:/masif/data/masif_site# ./data_prepare_one.sh 4ZQK_A
Downloading PDB structure '4ZQK'...
Removing degenerated triangles
Removing degenerated triangles
4ZQK_A
Reading data from input ply surface files.
Dijkstra took 2.28s
Only MDS time: 18.26s
Full loop time: 28.54s
MDS took 28.54s
```

If you want to run a prediction on multiple chains (e.g. a multidomain protein) you can do so by concatenting all chains (e.g., 4ZQK_AB). You can also run this command on a specific file (i.e. not on a downloaded file) using the --file flag: 

```
root@b30c52bcb86f:/masif/data/masif_site# ./data_prepare_one.sh --file /path/to/myfile/4ZQK.pdb 4ZQK_A
```




## Training The Example Data

## Surface Features Extruction
