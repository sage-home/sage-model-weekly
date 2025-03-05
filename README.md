# SAGE Parameter Optimization

This directory contains parameter optimization tools and results for the Semi-Analytic Galaxy Evolution model using Particle Swarm Optimization (PSO). Within the output folder are plots for both Millennium and miniUchuu for the most important predictions using SAGE with the 2 different simulations.

## Overview

The code in this repository calibrates SAGE's free parameters against observational constraints using PSO. The optimization process identifies parameter sets that produce galaxy populations closely matching observed data.

## Contents

- `analysis.py`: Statistical analysis tools for evaluating model fit quality
- `common.py`: Shared utility functions
- `constraints.py`: Observational constraints implementation (SMF, BHMF, BHBM, HSMR)
- `execution.py`: SAGE execution handler for PSO
- `main.py`: Main driver script for the optimization process
- `pso.py`: Implementation of the Particle Swarm Optimization algorithm
- `space*.txt`: Parameter space definition files for different optimization scenarios
- `diagnostics.py`: Diagnostic visualization tools
- `./output`: Benchmark plots for Millennium and miniUchuu

## Calibrated Parameters

The optimization process calibrates several key SAGE parameters:

- `SfrEfficiency`: Star formation efficiency (α_SN)
- `FeedbackReheatingEpsilon`: SNe energy coupling efficiency to disk (ε_disc)
- `FeedbackEjectionEfficiency`: SNe energy coupling efficiency to halo (ε_halo)
- `ReIncorporationFactor`: Gas reincorporation efficiency (κ_reinc)
- `RadioModeEfficiency`: Radio mode AGN feedback efficiency (κ_R)
- `QuasarModeEfficiency`: Quasar mode feedback efficiency (κ_Q)
- `BlackHoleGrowthRate`: Black hole growth factor (f_BH)

## Observational Constraints

The PSO calibrates against several key observational constraints:

- Stellar Mass Function (SMF) at multiple redshifts (z=0,1,2)
- More to come ...

## Usage

The repository is organized to allow for easy execution of the PSO algorithm:

```bash
python main.py -c <config_file> -b <sage_binary> -o <output_dir> -S <space_file> -x <constraints>
```

Example scripts are provided in `run_pso.sh`.

## Output

The optimization generates several output files:

- Parameter CSV files with best-fit values
- Diagnostic plots of constraint fits
- Uncertainty analysis for parameter constraints
- Visualization of PSO particle convergence

This directory is regularly updated with newly calibrated parameter sets.
