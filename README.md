# HRIP-prediction-article2026
This is the repository to save jupyter notebook used in research article (under revision). 


This is the repository to share supporting information of python codes for reviewers.
The models described in this repository can

- predict numerous polymer's refractive index at D line (nD) from smaller-data-trained predictive model
- provide specific structures optimized for miltiple properties (e.g. $\mathit{n}_{D}$ and $\Delta
\varepsilon _{HOMO−LUMO}$) via generative approach
# What we provide here
- codes
- data
- other nesisities (license etc. )
# Requirements for MOBO
(We used different environment on Anaconda to make nD predictor. See repository of nd_predictor.)
- Python (>3.10)
- PyTorch==2.2.0+cu118
- Numpy==1.26.4
- DGL==2.4.0+cu118
- networkx==3.5
- rdkit==2025.9.3
- botorch==0.16.1
- statsmodels==0.14.5
# Quick start of our original \mathit{n}_{D}predictor with Molecule generation through MOBO on Google Colab
1. Upload the jupyter notebook below on Google Colab
2. MOBO_with_original_nD_predictor_and_GPU-assisted_DFT.ipynb
3. Connect to a session with GPU (T4 is enough)
4. Install requirements
5. ''' python 
!pip install -r requirements.txt
'''

7. Place two pickle files of $\mathit{n}_{D} predictor on \content or directory where currently you are
Run the code from scratch
You will see generated molecules as SMILES (Simplified Molecular Input Line Entry System, )
Download result csv file if you need
# referenced codes
## referenced papers for molecule generation
https://github.com/slab-it/FRATTVAE
## referenced documentation for bayesian optimization
https://botorch.org/docs/tutorials/multi_objective_bo/
## referenced github repository for variance inflation factor (VIF)
https://github.com/Apress/Practical-Explainable-AI-Using-Python
## referenced dataset
### training dataset
https://github.com/KanHatakeyama/RefractiveIndexGPT/forpub2.csv
### test and validation dataset 
->our original (see the paper for more details)
## DFT
https://github.com/pyscf/gpu4pyscf
