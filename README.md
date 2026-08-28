# Robust Aggregation for Federated Learning by Minimum γ-Divergence Estimation

Official implementation of the **γ-mean robust aggregator** for Byzantine-resilient federated learning.

**Paper:**  
Cen-Jhih Li, Pin-Han Huang, Yi-Ting Ma, Hung Hung, and Su-Yun Huang.  
"Robust Aggregation for Federated Learning by Minimum γ-Divergence Estimation."  
*Entropy*, 24(5):686, 2022.  
DOI: 10.3390/e24050686

## Overview

The **γ-mean** is a robust aggregation method derived from minimum γ-divergence estimation. It downweights outlying client updates and is designed to tolerate Byzantine clients in federated learning.

The simple γ-mean is computationally lightweight and suitable for high-dimensional neural-network updates. The aggregation procedure is implemented in NumPy and can be used as a drop-in robust alternative to standard averaging in federated learning experiments.

Parts of the experimental setup were adapted from:
https://github.com/amitport/Towards-Federated-Learning-with-Byzantine-Robust-Client-Weighting

## Datasets

The experiments include:

- MNIST
- Fashion-MNIST
- EMNIST
- Chest X-ray

The pneumonia chest X-ray dataset is not included in this repository and can be obtained from the original Kaggle dataset.

## Environment

Environment information is provided in:

`build_env.txt`

The experiments were developed and tested on Ubuntu 16.04, 18.04, and 20.04.

TensorFlow Federated is only required for the EMNIST experiments.

## Running the Experiments

Example commands for reproducing the experiments are provided in:

`cmd_run.txt`

The main experiment script is:

`run_experiment.py`

## Repository Structure

- `run_experiment.py` — main experiment script
- `util/experiment_runner.py` — experiment utilities and loading of previous results
- `util/server.py` — server and aggregation procedures
- `util/client.py` — federated client implementation
- `util/model.py` — neural-network models
- `prepare_data/` — dataset preparation utilities
- `aggregators_simulation.ipynb` — simulations of robust aggregation methods
- `mnist_results_plots.ipynb` — experiment analysis and result visualization
- `paper_entropy.pdf` — paper manuscript

## Results

Simulation results and federated-learning experiments are provided in:

- `aggregators_simulation.ipynb`
- `mnist_results_plots.ipynb`

After running the experiments, use `mnist_results_plots.ipynb` to reproduce the result plots.

## Citation

If you use this code or the γ-mean aggregator in your research, please cite:

```bibtex
@article{li2022robust,
  title={Robust aggregation for federated learning by minimum $\gamma$-divergence estimation},
  author={Li, Cen-Jhih and Huang, Pin-Han and Ma, Yi-Ting and Hung, Hung and Huang, Su-Yun},
  journal={Entropy},
  volume={24},
  number={5},
  pages={686},
  year={2022},
  publisher={MDPI},
  doi={10.3390/e24050686}
}
```
