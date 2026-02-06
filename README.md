# iGEM Plastics Modelling 🧬♻️

This repository contains **molecular modelling and simulation files for common plastic polymers** developed as part of the **iGEM 2024 – REC Chennai** project.

The models are designed to support **computational analysis of plastic–biological interactions**, aiding our efforts to understand and engineer **plastic degradation mechanisms**.

🌐 Project Wiki:  
https://2024.igem.wiki/rec-chennai/model

---

## 📦 Polymers Included

The repository currently contains simulation setups for:

- **Polyethylene (PE)**
- **Polypropylene (PP)**
- **Polystyrene (PS)**

Each polymer includes structures and simulation input files for different molecular dynamics stages.

---

## 📁 File Description

### Structure Files (`.gro`)
- `minPE.gro`, `minPP.gro`, `minPS.gro`  
  → Energy-minimized structures

- `meltPP.gro`, `meltPS.gro`  
  → Melted polymer configurations

- `productionPE.gro`, `productionPP.gro`, `productionPS.gro`  
  → Final production-ready structures

---

### Simulation Parameters (`.mdp`)
- `min*.mdp`  
  → Energy minimization parameters

- `pre_NpT-*.mdp`  
  → Pre-equilibration under NPT ensemble

---

### Topology Files (`.top`)
- `topologyPE.top`
- `topologyPP.top`
- `topologyPS.top`

These define bonded and non-bonded interactions required for running simulations in **GROMACS**.

---

## 🧪 Simulation Software

- **Molecular Dynamics Engine:** GROMACS  
- **Force Field:** Coarse-grained polymer models (Martini-compatible)

> ⚠️ Ensure correct force-field files are present in your GROMACS installation before running simulations.

---

## 🚀 How to Use

1. Clone the repository:
   ```bash
    git clone https://github.com/lokaaaaaaa/iGEM-plastics-modelling.git
   cd iGEM-plastics-modelling

Run energy minimization:

gmx grompp -f minPE.mdp -c minPE.gro -p topologyPE.top -o em.tpr
gmx mdrun -deffnm em
   git clone https://github.com/lokaaaaaaa/iGEM-plastics-modelling.git
   cd iGEM-plastics-modelling
