# HFS-GF: High-Fidelity Synthesis via Generative Flow

**[Under Review]** | **[Project Page (Coming Soon)]** | **[Paper (Coming Soon)]**

 **"HFS-GF: A High-Fidelity Simulation-Driven Generative Framework for Synthesizing and Analyzing Layered Encrypted Traffic"**.

*Zihan Xia*

---

## Abstract

*The analysis of layered encrypted traffic, such as
VPN-over-Tor, is critical for network security, yet this field of
study is severely constrained by a profound scarcity of large-
scale, accurately labeled, real-world datasets. Legal, ethical,
and technical barriers render the direct collection of such
data nearly impossible, creating a fundamental impasse for
traditional supervised learning methodologies. To address this
critical data scarcity challenge, this paper proposes a novel, end-
to-end generative framework, the High-Fidelity Simulation-Driven
Generative Framework (HFS-GF). Our framework first employs
a High-Fidelity Synthesis Engine (HFSE) to model the causal
processes of VPN encapsulation—including protocol overhead,
Path MTU Discovery (PMTUD)-induced fragmentation, and FQ-
CoDel queuing delays—on real Tor website fingerprints, thereby
generating a theoretically sound data distribution. Subsequently,
a time-series generative model learns this high-fidelity distribution
to produce a large-scale synthetic dataset that preserves temporal
dynamics. We validate the utility of our synthetic data through a
highly challenging 95-class Website Fingerprinting (WF) task. A
classifier trained exclusively on our synthetic data achieves an ac-
curacy of 71.82% in identifying real, layered-encapsulated traffic,
decisively outperforming the 1.05% random-guess baseline. This
result provides the first strong, quantitative evidence that website
fingerprints remain detectable even after double encapsulation.
More broadly, the HFS-GF framework establishes a powerful
and verifiable benchmark generation tool for future research in
encrypted traffic analysis where real data is unavailable. We
publicly release our framework and dataset to the research
community to foster reproducible research.*

## Project Structure
    HFS-GF-reproducibility/
    ├── data/                # Data directory (ignored by Git)
    ├── experiments/         # Scripts to run experiments
    ├── notebooks/           # Jupyter notebooks for analysis and visualization
    ├── results/             # Output directory (ignored by Git)
    ├── src/                 # Main source code for HFS-GF
    ├── .gitignore           # Specifies files ignored by Git
    ├── LICENSE              # License file (e.g., MIT, Apache 2.0)
    └── README.md            # This file
    └── requirements.txt     # Python dependencies

## Installation

1. Clone this repository:
    ```bash
   git clone [https://github.com/YourUsername/HFS-GF-reproducibility.git](https://github.com/YourUsername/HFS-GF-reproducibility.git)
   cd HFS-GF-reproducibility

2.Create a conda environment and install dependencies:
    ```bash
    conda create --name hfs-gf python=3.9
    conda activate hfs-gf
    pip install -r requirements.txt

## Usage
    later put  

## train
    ```bash
    python experiments/train.py --config [path_to_config]

## Inference
    python experiments/inference.py --checkpoint [path_to_model] --input [path_to_input]

## Citation
If you find our work useful, please consider citing:

    @article{yourlastname2025hfs,
  title={HFS-GF: A High-Fidelity Simulation-DrivenGenerative Framework for Synthesizing and Analyzing Layered Encrypted Traffic},
  author={Zihan Xia},
  journal={Journal or Conference Name},
  year={2025}
}