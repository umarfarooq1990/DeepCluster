# Intelligent Navigation of Potential Energy Surfaces: Leveraging Deep Reinforcement Learning Paradigms for Accelerated Discovery of Stable Nickel Nanoclusters [Ni.pdf](https://github.com/user-attachments/files/25721426/Ni.pdf)



## Overview
This repository contains the implementation of the **DeepCluster Agent**, designed for the identification of Nickel (Ni) nanoclusters using **Deep Reinforcement Learning (DRL)**. The model aims to efficiently explore nanocluster configurations and optimize for desired properties.

The code is adapted from [**clusgym_drl**](https://github.com/rajeshkochi444/clusgm_drl). We thank the authors for making the code available on github. We modified the code to work with Nickel nanoclusters and renamed it to Deepcluster.

## How to Run the Code

### 1. Set Up the Environment
To begin, set up the required environment using the provided Conda YAML configuration file. Run the following command to create the environment:

```bash
conda env create -f Deepcluster.yml
```

### 2. Activate the Environment
Once the environment is set up, activate it using the following command:

```bash
conda activate Deepcluster
```

### 3. Configure the Nanocluster Composition
Next, configure the composition of the nanocluster you wish to simulate. This can be done by editing the `Deepcluster.py` file and setting the desired nanocluster composition.

For **Nickel** nanoclusters, adjust the `eleNums` variable to specify different cluster sizes as needed. 

- **Ni10 Nanocluster:**
  ```python
  eleNames = ['Ni']
  eleNums = [10]
  ```

- **Ni13 Nanocluster:**
  ```python
  eleNames = ['Ni']
  eleNums = [13]
  ```

- **Ni20 Nanocluster:**
  ```python
  eleNames = ['Ni']
  eleNums = [20]
  ```

- **Ni38 Nanocluster:**
  ```python
  eleNames = ['Ni']
  eleNums = [38]
  ```

### 4. Run the Simulation
Once you've configured the nanocluster composition, you can run the simulation by executing the following command:

```bash
python Deepcluster.py
```

This will initiate the DeepCluster Agent to simulate and optimize the nanocluster configurations based on the specified parameters.

---

### Note
Any nanocluster configuration can be simulated by changing the `eleNames` and `eleNums` parameters in the script. This includes **monometallic**, **bimetallic**, **trimetallic**, **quaternary**, and **quinary** alloy compositions. Simply specify the desired elements and their respective atomic counts in the `eleNames` and `eleNums` lists to customize the simulation.

### Open Source Code
This project is open-source, and we encourage you to use and contribute to it. The code is available under the **MIT License**. Feel free to fork, modify, and distribute the code as needed. We welcome contributions and feedback from the community to improve the functionality and performance of the model.
