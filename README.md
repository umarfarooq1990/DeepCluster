# Intelligent Navigation of Potential Energy Surfaces: Leveraging Deep Reinforcement Learning Paradigms for Accelerated Discovery of Stable Nickel Nanoclusters
[Intelligent Navigation of Potential Energy Surfaces Leveraging Deep Reinforcement Learning Paradigms for Accelerated Discovery of Stable Nickel Nanoclusters .pdf](https://github.com/user-attachments/files/25721472/Intelligent.Navigation.of.Potential.Energy.Surfaces.Leveraging.Deep.Reinforcement.Learning.Paradigms.for.Accelerated.Discovery.of.Stable.Nickel.Nanoclusters.pdf)

# Deepcluster Framework — A Proximal Policy Optimization (PPO) DRL Framework for Nanocluster Global Minimum Search (version 2.0).
## Overview
This repository contains the implementation of the **Deepcluster Agent**, employed for the identification of Nickel (Ni) nanoclusters using **Deep Reinforcement Learning (DRL)**. The aims is to efficiently explore GM nanocluster configurations.

This is a modified and adapted version of the DRL framework from:

**Exploring Nanocluster Potential Energy Surfaces via Deep Reinforcement Learning: Strategies for Global Minimum Search**<br>
Rajesh K. Raju <br>
 J. Phys. Chem. A 2024, 128, 9122−9134.
 The TRPO version of DRL framework is available at https://github.com/rajeshkochi444/clusgm_drl.
 
We thank the authors for making the code available on github.

---

## Key Modifications

This framework replaced the original TRPO agent with PPO agent for faster wall-clock convergence, better sample efficiency, and correct on-policy exploration. 
We modified the code to work with Nickel nanoclusters and named it to Deepcluster.

---


### PPO hyperparameters

| Parameter | Default | Description |
|---|---|---|
| `batch_size` | `64` | Episodes collected before each policy update |
| `learning_rate` | `3e-4` | Adam learning rate |
| `optimization_steps` | `10` | Gradient passes per collected batch |
| `subsampling_fraction` | `0.25` | Mini-batch fraction per optimisation step |
| `likelihood_ratio_clipping` | `0.2` | PPO clip epsilon ε |
| `entropy_regularization` | `0.01` | Entropy bonus for exploration |
| `discount` | `0.99` | Reward discount factor γ |
| `timesteps` | `200` | Maximum steps per episode |

---

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
Once configured the nanocluster composition, we can run the simulation by executing the following command:

```bash
python Deepcluster.py
```

This will initiate the agent to simulate and optimize the nanocluster configurations based on the specified parameters.

---

