# PyAMICA

PyAMICA is a Python-based implementation of AMICA (Adaptive Mixture Independent Component Analysis) for EEG data processing, fully operable within WSL (Windows Subsystem for Linux) and without any dependency on MATLAB. This repository provides a streamlined pipeline to preprocess EEG data, execute AMICA, and seamlessly import results into Python for further analysis.

## Features

- Pure Python-based AMICA processing—no MATLAB required
- Step-by-step installation and setup guide for WSL and VS Code
- Integration of AMICA into Python pipelines using `subprocess`
- Suitable for EEG and neuroscience research applications

## Installation Guide

### **1. Install Intel OneAPI Toolkits in WSL**

Follow the instructions provided in the [Intel OneAPI Installation Guide](#) to install the Base and HPC Toolkits in your WSL environment.

### **2. Compile AMICA**

Navigate to the `amica` directory and compile the source code:

```bash
cd amica
mpiifort -qopenmp -mkl -O3 -fpp -DMKL amica15.f90 funmod2.f90 -o amica15_wsl
