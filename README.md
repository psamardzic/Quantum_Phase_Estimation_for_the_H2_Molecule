# Quantum_Phase_Estimation_H2

Authored a project utilizing the **QAT** Python library to implement a Quantum Phase Estimation algorithm for calculating the ground state energy of a dihydrogen molecule. This repository contains the code and simulation framework for constructing the molecular Hamiltonian and performing the estimation on a quantum simulator. Below is an overview of the included files and how to use the code.

## File Structure

* **main.ipynb**: The primary Jupyter notebook containing the full implementation, including the modelisation of the $H_2$ molecule, the construction of the Trotterized evolution operator, and the QPE circuit.
* **h2_data.npz**: This file contains the pre-calculated molecular data (integrals and nuclear repulsion energy) required to build the Hamiltonian.

## Running the Code

To run the simulation, follow these steps:

1. Open the `main.ipynb` notebook in a Jupyter environment.
2. Ensure you have the necessary libraries installed (`qat`, `numpy`, and `matplotlib`).
3. Locate the configuration section in the code where the simulation parameters are defined.
4. Modify the following variables to set up the program according to your precision requirements:
    * **n_phase_bits**: Change this value to adjust the precision of the phase estimation (e.g., 5, 6, or 7).
    * **n_trotter**: Adjust this value to set the number of steps for the Trotter-Suzuki decomposition.
5. Execute the cells sequentially to build the circuit, run the simulation, and visualize the resulting energy spikes.

**Important**: Ensure the `h2_data.npz` file is located in the same directory as the notebook before running the program to ensure the molecular Hamiltonian loads correctly.
