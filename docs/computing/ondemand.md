## What is OnDemand?:

OnDemand is an online GUI for launching Jupyter notebooks (avoiding the need to use SLURM in terminal). 

If you are not on a Rutgers network, you will need to use the VPN! See here for more details: https://sites.google.com/view/cluster-user-guide/amarel

## Getting started with OnDemand for launching Jupyter notebooks

1.	Navigate to https://ondemand.hpc.rutgers.edu/

    a. Login using your netid 

2.	Click on 'Interactive Apps' and 'Personal Jupyter':

    a. Number of hours: can go up to 3 days on the main partition, 14 days on our lab partition

    b. Number of cores: we have 64 cores on our lab partition. If you need to use more than ~16, switch to the main partition to not slow down other lab users. 

    c. Gigabytes of memory: we have 240 GB RAM on our lab partition. Don't use it all up! Typically you won't need more than 32 GB RAM at most - if you do, please revisit the efficiency of your workflow. 

    d. Partition: specify the partition. 

        1. Our lab partition is: `p_sq140_1`

    e. Reservation: keep empty

    f. Slurm feature: keep empty

    g. conda path: specify path to your local miniconda install: e.g. `/home/sq140/miniconda3/`
    
    h. conda environment: specify environment name
