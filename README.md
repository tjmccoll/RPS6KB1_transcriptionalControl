# Bioinformatic inference of the exercise-responsive control of p70 S6 kinase through *RPS6KB1* expression
## Overview
This study applies the [Causal Reasoning pipeline for Network identification using Integer VALue programming (CARNIVAL) tool](https://saezlab.github.io/CARNIVAL/), developed by the Saez Lab, to infer the transcriptional control of *RPS6KB1* following acute aerobic or resistance exercise. We used two complimentary approaches: 
1. The **standard CARNIVAL approach** was applied to infer the signaling networks that control transcription factors targeting *RPS6KB1* downstream of canonical exercise-sensitive proteins (e.g., AMPK isoforms, CaMKs, MAP3Ks).
2. The **inverse CARNIVAL approach** was applied to identify potential upstream signaling networks that may control the transcription factors targeting *RPS6KB1*.

This tool is being developed by the [Clarke Laboratory for Quantitative Exercise Biology](https://www.sfu.ca/clarkelab-bpk.html). Further information can be found in the following study.

> (update with BioRxiv link)

## Getting started
The 'McColl_2025_rps6kb1TranscriptionalControl_250819' folder contains all the files generated in this manuscript.

### Installation
Download the package to a local folder (e.g., '~/RPS6KB1_transcriptionalControl/') by extracting the ZIP file or by running the following terminal command: 
```
git clone https://github.com/tjmccoll/MuscleProteinSynthesisKineticModel.git
```
CARNIVAL requires an interaction solver for the network optimizer. Here, we have used IBM ILOG Cplex, which is freely available through the Academic Initiative ([available here](https://www.ibm.com/products/ilog-cplex-optimization-studio)). CARNIVAL can also use other solvers including Gurobi and CBC-COIN, which are further disucssed on the [CARNIVAL source page](https://saezlab.github.io/CARNIVAL/).

### Running the code
To simulate the manuscript code:
1. Open the 'McColl_2025_RPS6KB1txnlControl_stdCarnival_250819.Rmd' or 'McColl_2025_RPS6KB1txnlControl_invCarnival_250819.Rmd' R Markdown file from the 'R file' folder. These R files run the standard or inverse CARNIVAL approaches, respectively.
2. Update the 'repo_root' variable on line 6 to the file path that contains the locally saved 'McColl_2025_rps6kb1TranscriptionalControl_250819' folder.
3. Run each section of the script.
4. The CARNIVAL network inference code (section 6) includes details for commenting in/out lines of code to run CARNIVAL with either the aerobic or resistance exercise data.

### File list
#### Dickinson_2018
* 'GSE107934_RAW': contains the raw RNAseq count data from Dickinson et al. 2018
#### Outputs
* 'carnivalNetworks': contains folders for the file outputs for the standard and inverse CARNIVAL network inference using the aerobic or resistance exercise data.
* 'Data': data files generated within the code are saved here.
* 'dorothea': DoRothEA specific outputs are saved here.
* 'Figures': figures generated within the code are saved here.
* 'omnipath': details of the OmniPath prior knowledge network are saved here.
* 'progeny': PROGENy specific outputs are saved here.
#### R file
* The stdCARNIVAL or invCARNIVAL R markdown files are contained here.
#### Support
* Various support functions for the markdown files are contained here.

## Contact
tmccoll@sfu.ca

## Citation
If you use the simulations and analyses in this repository, please cite the paper:
> **(ADD CITATION INFO)**
