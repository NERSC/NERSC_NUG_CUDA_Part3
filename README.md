![NERSC Logo](NERSClogo087.png)

# NERSC NUG Community Call: CUDA C/C++ on Perlmutter (Part 3)

#### Welcome to the repository for the NERSC User Group (NUG) Community Call,"A Birds-Eye View of Using Cuda C/C++ on Perlmutter (Part 3)"
#### This session was presented on October 30, 2025, by Dr. Charles Lively III, Dr. Lipi Gupta, Dr. Helen He on behalf of NERSC Core Training Team and User Engagement Group

This repository contains all the hands-on materials, including the presentation slides and the Jupyter Notebooks used for the demonstration.

## About This Training

This training series is designed to take NERSC users from zero to writing, compiling, and running simple CUDA C++ programs on Perlmutter. This session (Part 3) focuses on the most critical concepts for performance: **memory optimization**.

**Learning Objectives:**
* Understand the CUDA execution model (Kernels, Grids, Blocks, Threads).
* Learn the difference between Host (CPU) and Device (GPU) memory.
* Write and compile your first kernels using `nvcc`.
* Identify global memory as a performance bottleneck.
* Implement a **tiled** matrix multiplication kernel using **shared memory** (`__shared__`).
* Use `__syncthreads()` to manage thread synchronization and prevent race conditions.

##  Repository Contents

* **`NUG_Community_Call_Oct302025.pdf`**: The main presentation slides, covering the core concepts of CUDA memory hierarchy, tiling algorithms, and barrier synchronization
* **`NERSC_NUG_CUDA_Part3_1.ipynb`**: **Notebook 1: CUDA Fundamentals**. A hands-on introduction to writing, compiling, and running kernels.
    * Verifying the GPU environment (`nvidia-smi`).
    * "Hello, World!" in CUDA C++.
    * Host vs. Device memory (`cudaMalloc`, `cudaMemcpy`).
    * A simple, data-parallel kernel: Vector Addition.
* **`NERSC_NUG_CUDA_Part3_2.ipynb`**: **Notebook 2: Kernel Optimization**. A deep dive into fixing performance bottlenecks using shared memory.
    * **Baseline:** A *naive* matrix multiplication kernel to see the global memory bottleneck.
    * **Optimized:** A *tiled* matrix multiplication kernel using `__shared__` memory for data reuse.
    * **Synchronization:** A demo that shows *why* `__syncthreads()` is essential by running a "broken" kernel that produces garbage data.
* **`NERSClogo087.png`**: NERSC logo used in the notebooks.

## How to Use These Materials

These notebooks are designed to be run directly on Perlmutter via the NERSC JupyterHub.


## Resources & Further Reading

* **NERSC User Docs:** [Running Jobs on Perlmutter](https://docs.nersc.gov/jobs/) 
* **NERSC Training:** [Upcoming and Past Events](https://www.nersc.gov/users/training/events/)
* **NUG Slack:** [Join the NERSC Users Slack](https://www.nersc.gov/users/user-news/join-the-nersc-users-slack-sponsored-by-nug-today)
* **NVIDIA Docs:** [CUDA C++ Programming Guide](https://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html)
