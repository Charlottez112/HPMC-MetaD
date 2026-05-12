## Code for paper: Exploring Entropy Landscapes Using Hard Particle Monte Carlo Metadynamics

In paper, *[Exploring Entropy Landscapes Using Hard Particle Monte Carlo Metadynamics](https://www.pnas.org/doi/10.1073/pnas.2537764123)*, we introduce a new algorithm that integrates the Hard Particle Monte Carlo scheme with Metadynamics, which we term "HPMC-MetaD".

To perform HPMC-MetaD simulations, we implemented the algorithm as a [HOOMD-blue](https://hoomd-blue.readthedocs.io/en/v5.4.0/) custom updater, and we provide a minimal example in this repository:

`simulation.ipynb` - HPMC-MetaD simulation of N = 50 $S_2$ particles (see paper for shape definition).

`colvar.py` – Implementation of several commonly used order parameters, used in `hpmetad.py`. Modify this file to include custom collective variables.

`hpmetad.py` – Implementation of the HPMC-MetaD algorithm.

`restart.ipynb` - Restart and continue the HPMC-MetaD simulation.

`analysis.ipynb` - Analyze the simulation data for, e.g., checking the acceptance rate, collective variable/bia potential vs time, and plotting the free energy profile.

In the `larger_system_data` directory, we also provide a simulation trajectory with N = 500 $S_2$ particles (run 5 as labeled in the Supplementary Material). The rest of the simulation data for our paper can be provided upon request.

If you have any questions, feel free to reach out to: zshiqi[at]umich.edu

If you find this repository helpful, please consider citing our paper: 

C.S. Zhao, S.-T. Tsai, & S.C. Glotzer, Exploring entropy landscapes using hard particle Monte Carlo metadynamics, Proc. Natl. Acad. Sci. U.S.A. 123 (20) e2537764123, https://doi.org/10.1073/pnas.2537764123 (2026).
