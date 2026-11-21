# Modelling and Visualisation in Physics
**MPhys Course Checkpoints** · University of Edinburgh

> Python simulations of statistical physics, cellular automata and partial differential equations on lattices, using Monte Carlo methods and iterative numerical solvers accelerated with Numba, with live animations and measurement modes for each model.

## Background

Many physical systems are made up of huge numbers of simple interacting parts. Even when the rules for each part are simple, they can produce rich collective behaviour such as phase transitions, self-organising patterns, epidemics and phase separation. These behaviours can rarely be solved analytically, so we study them by simulating the system on a lattice and measuring how it evolves.

This course builds a set of such simulations from scratch. It covers stochastic Monte Carlo models like the Ising model and the SIRS epidemic model, deterministic cellular automata like Conway's Game of Life, and numerical solutions of partial differential equations such as the Cahn-Hilliard and Poisson equations. Each simulation can be watched as a live animation or run in a measurement mode that sweeps parameters, records observables and produces plots.

## Repository Structure

```
modelling_and_visualisation/
│
├── checkpoint1/
│   └── ising_model/              # Ising model with Glauber and Kawasaki dynamics
│
├── checkpoint2/
│   ├── game_of_life/             # Conway's Game of Life
│   └── sirs/                     # SIRS epidemic model
│       └── exams/                # Past exam paper practice
│
├── checkpoint3/
│   ├── cahn_hilliard_equation/   # Cahn-Hilliard phase separation
│   └── poissons_equation/        # Poisson's equation for electric and magnetic fields
│
├── .gitignore
└── README.md
```

Each simulation folder contains:

```
simulation/
├── simulation.py                 # Simulation script
├── README.md                     # Arguments and command line examples
└── outputs/
    ├── datafiles/                # Raw measurement data (.txt)
    └── plots/                    # Saved figures (.png)
```

## Getting Started

### Prerequisites

- Python 3.8+

### Installation

```bash
# Clone the repository
git clone https://github.com/grxcetait/modelling_and_visualisation.git
cd modelling_and_visualisation

# Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate        # macOS/Linux
# venv\Scripts\activate         # Windows

# Install dependencies
pip install numpy scipy matplotlib numba
```

### Running the Simulations

Each simulation is run from the terminal with command line arguments. For example:

```bash
cd checkpoint1/ising_model
python ising_model.py -d g -T 2.0
```

> **Note:** Every script has an animation mode and a measurement mode. The README in each simulation folder lists all available arguments, their defaults and example commands.

## Simulations

| Checkpoint | Simulation | Techniques |
|---|---|---|
| 1 | Ising Model | Metropolis Monte Carlo, Glauber and Kawasaki dynamics, bootstrap errors on specific heat |
| 2 | Game of Life | Cellular automata, equilibration time distributions, glider velocity |
| 2 | SIRS Model | Stochastic lattice epidemics, phase diagrams, variance, vaccination / herd immunity |
| 3 | Cahn-Hilliard Equation | Finite difference methods, phase separation, free energy density |
| 3 | Poisson's Equation | Jacobi, Gauss-Seidel and successive over-relaxation (SOR), electric and magnetic fields |

## Acknowledgements

This coursework was completed as part of the Modelling and Visualisation in Physics course at the University of Edinburgh.
