# Getting Started with Conda

## Before getting started

1. Request an Amarel account: https://oarc.rutgers.edu/amarel-cluster-access-request/
2. Remind Salman to request you be added to the lab partition

## Getting started with Conda for environment maintenance

1. Install miniconda in your home directory

2. Run the following commands in terminal (replace `[netid]` with your actual netid):

```bash
/cache/home/[netid]/miniconda3/bin/conda init
/cache/home/[netid]/miniconda3/bin/conda config --set auto_activate_base true
source ~/.bashrc
```

3. Now you will use this local miniconda to install your conda environments!

## Using installed environments as a kernel in Jupyter

When you install a conda environment, it is not automatically visible in Jupyter. 

### Method 1: Manual kernel registration

1. Activate your conda environment: `conda activate [env_name]`
2. Install ipykernel **inside your environment**:
   ```bash
   pip install ipykernel
   ```
3. Register the kernel (replace `[env_name]` with your environment's name and optionally `[display_name]` with a friendly name):
   ```bash
   python -m ipykernel install --user --name [env_name] --display-name "[display_name]"
   ```

### Method 2: Automatic detection with nb_conda_kernels

Install `nb_conda_kernels` in your **base environment** (where Jupyter is running):
```bash
conda install -c conda-forge nb_conda_kernels
```

**Note**: With `nb_conda_kernels`, you still need to install `ipykernel` in each conda environment you want to use. The package automatically detects and registers environments that have `ipykernel` installed.

---

[Back to Computing](README.md)