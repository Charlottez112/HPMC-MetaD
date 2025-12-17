## Code for paper: Exploring Entropy Landscapes using Hard Particle Metadynamics

In paper, *Exploring Entropy Landscapes using Hard Particle Metadynamics*, we introduce a new algorithm that integrates the Hard Particle Monte Carlo scheme with Metadynamics, which we term "HPMC-MetaD".

To perform HPMC-MetaD simulations, we implemented the algorithm as a [HOOMD-blue](https://hoomd-blue.readthedocs.io/en/v5.4.0/) custom updater, and we provide a minimal example in this repository:

`simulation.ipynb` - HPMC-MetaD simulation of N = 50 $S_2$ particles (see paper for shape definition).

`colvar.py` – Implementation of several commonly used order parameters, used in `hpmetad.py`. Modify this file to include custom collective variables.

`hpmetad.py` – Implementation of the HPMC-MetaD algorithm.

`restart.ipynb` - Restart and continue the HPMC-MetaD simulation.

`analysis.ipynb` - Analyze the simulation data for, e.g., checking the acceptance rate, collective variable/bia potential vs time, and plotting the free energy profile.

In the `larger_system_data` directory, we also provide a simulation trajectory with N = 500 $S_2$ particles (run 5 as labeled in the Supplementary Material). The rest of the simulation data for our paper can be provided upon request.
