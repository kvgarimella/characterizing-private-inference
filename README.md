# Characterizing and Optimizing End-to-End Systems for Private Inference

The goal of this project is to understand (and optimize) the system-level bottlenecks of private inference protocols under varying workloads. This repo contains the codes for our paper. The high-level directories are:

1. `garbled_circuits`: contains the raw data for benchmarking ReLU Garbling and Evaluation on the embedded device and the server
2. `layer_parallel_HE`: contains our code and the raw data for enabling layer-parallel homomorophic evaluation of linear layers
3. `simulator`: our PI simulator used to generate plots and results from the paper
4. `artifact` : contains scripts to generate key figures in the paper

Please refer to the READMEs within each subdirectory to learn how we collected data and how to run the simulator.

## Installation
First, clone this repo:
```bash
git clone https://github.com/kvgarimella/characterizing-private-inference.git
```
Then, change directories and install the Python dependencies:
```bash
cd  characterizing-private-inference
pip install -r requirements.txt
```
As a simple test, navigate to the `simulator/experiments` sub-directory and run:
```bash
cd simulator/experiments
python simulate_server_garbler.py
```
This will run a single simulation of the Server-Garbler protocol and store the results in a directory called `tmp`.

## Artifact Evaluation
Please refer to the README within the `artifact` directory. 

## Contributors
- Karthik Garimella - Python, Rust, C++
- [Zahra Ghodsi](https://ghodsi.me/) - Rust, C++

