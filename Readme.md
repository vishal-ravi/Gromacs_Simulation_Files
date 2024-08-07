

# Gromacs Simulation Files

This repository contains common simulation files for Gromacs molecular dynamics (MD) simulations. It is organized into two main directories: `protein` and `protein_ligand`. Depending on your simulation requirements, you can navigate to the appropriate directory and use the provided files for your simulations.

## Repository Structure

```
Gromacs_Simulation_Files/
├── protein/
│   ├── charmm36/
│   ├── cgenff_charmm2gmx_py3_nx2.py
│   ├── em.mdp
│   ├── ions.mdp
│   ├── md.mdp
│   ├── nvt.mdp
│   └── tip3p.gro
├── protein_ligand/
│   ├── charmm36/
│   ├── cgenff_charmm2gmx_py3_nx2.py
│   ├── em.mdp
│   ├── ions.mdp
│   ├── md.mdp
│   ├── nvt.mdp
│   └── tip3p.gro
```

### Folders and Files

#### `charmm36/`
Contains the CHARMM36 force field files required for the simulations. This directory includes parameter and topology files essential for setting up the system.

#### `cgenff_charmm2gmx_py3_nx2.py`
A Python script used to convert CHARMM force field parameters to a GROMACS-compatible format. This is particularly useful for integrating small molecules and ligands into the simulation.

#### `em.mdp`
The minimization parameter file for energy minimization steps. It contains the settings and options used to prepare the system by minimizing potential energy.

#### `ions.mdp`
The parameter file for the ion solvation step. This file is used to add ions to neutralize the system and achieve the desired ionic strength.

#### `md.mdp`
The main molecular dynamics parameter file. It contains the settings for the production MD run, where the system is simulated under the desired conditions.

#### `nvt.mdp`
The parameter file for the NVT (constant Number of particles, Volume, and Temperature) equilibration step. This step equilibrates the system temperature before the production run.

#### `tip3p.gro`
A structure file for the TIP3P water model. This file is used to solvate the system with water molecules.

## Usage Instructions

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/vishal-ravi/Gromacs_Simulation_Files.git
   ```

2. Navigate to the desired directory based on your simulation type:
   ```bash
   cd Gromacs_Simulation_Files/protein
   # or
   cd Gromacs_Simulation_Files/protein_ligand
   ```

3. Follow the standard Gromacs workflow for your simulation setup:
   - Prepare the topology and structure files.
   - Run the energy minimization using `em.mdp`.
   - Solvate the system and add ions using `ions.mdp`.
   - Perform the NVT equilibration using `nvt.mdp`.
   - Execute the production MD run using `md.mdp`.

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

