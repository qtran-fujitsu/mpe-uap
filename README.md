# Universality of Many-body Projected Ensemble for Learning Quantum Data Distribution

## Introduction

This repository contains the code implementation for the paper *"Universality of Many-body Projected Ensemble for Learning Quantum Data Distribution"* (https://arxiv.org/abs/2601.18637). The codebase provides tools and scripts to replicate the experiments described in the paper, focusing on learning quantum data distributions using the Many-body Projected Ensemble (MPE) framework.

## Repository Structure

The codebase is organized into the following modules:

- **data**: Utility functions for generating quantum data used in the experiments.
- **model**: JAX-based implementation of the Many-body Projected Ensemble (MPE) class, including training utility functions.
- **utils**: Utility functions for implementing quantum circuits using TensorCircuit, computing Wasserstein and MMD distances, and calculating the Vendi score.
- **main**: Scripts `main_gen_demo.py` and `main_gen_mol_uncon.py` for generating multi-clustered quantum states and QM9 quantum states, respectively.
- **datasets**: Directory containing filtered data from the QM9 dataset.
- **postprocess**: Functions for plotting and analyzing experimental results.
- **runscripts**: Shell scripts to execute the experiments.

## Prerequisites

To run the code, ensure the following requirements are met:

- Python version <= 3.10.12
- JAX version <= 0.6.1
- Additional dependencies are listed in `requirements.txt`.

Install the required packages using:

```bash
pip install -r requirements.txt
```

## Running the Experiments

Two scripts are provided to replicate the experiments described in the paper:

1. **Multi-cluster Quantum States**:
   To train the model on multi-cluster quantum states, execute:

   ```bash
   sh runscripts/demo_train_multi_cluster.sh
   ```

2. **QM9 Dataset**:
   To train the model on the QM9 dataset, execute:

   ```bash
   sh runscripts/demo_train_qm9_MPE_mol_7_2.sh
   ```

## Post-processing Results

To visualize and analyze the experimental results, navigate to the `postprocess` directory and run the following scripts:

- For multi-cluster quantum states:

  ```bash
  python postprocess/plot_eval_loss_multi_cluster.py
  ```

- For QM9 dataset:

  ```bash
  python postprocess/plot_eval_loss_qm9.py
  ```

## Contributing

We welcome contributions to enhance the codebase. Please submit pull requests or open issues to suggest improvements, report bugs, or add new features.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
