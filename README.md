# E-Prop SNN
### Implementing Eligibility Propagation in Spiking Neural Networks

**Status:** Active — building from foundations toward full recurrent implementation  
**Author:** Ishita, Undergraduate ECE Student, TCET Mumbai  
**Framework:** Brian2 (Python)  
**Based on:** Bellec et al. (2020), "A solution to the learning dilemma for recurrent networks of spiking neurons", Nature Communications

---

## Overview

This repository implements e-prop — eligibility propagation — a biologically 
plausible learning algorithm for recurrent spiking neural networks introduced 
by Bellec et al. in 2020. E-prop bridges the gap between biologically realistic 
local learning rules (like STDP) and the task performance achievable with 
backpropagation, using three components:

1. **Eligibility traces** — synapse-local decaying memory of recent activity
2. **Learning signal** — top-down error signal from output layer
3. **Weight update** — eligibility trace × learning signal

Unlike backpropagation through time (BPTT), e-prop is online, local in time, 
and nearly local in space — making it a serious candidate for implementation 
on neuromorphic hardware like Intel's Loihi 2.

---

## Repository Structure
eprop-snn/
├── notebooks/ ← implementation notebooks, building up from foundations
├── experiments/ ← rigorous multi-seed experimental runs
├── figures/ ← publication-quality figures
└── papers/ ← key literature informing this work


---

## Notebooks

*To be populated as implementation progresses.*

---

## Connection to Project Dopamine

This repository builds directly on the eligibility trace foundations 
established in the Project Dopamine arc (notebooks 10-12 of 
neuromorphic-experiments). The reward-modulated learning rules explored 
there connect naturally to e-prop's learning signal mechanism — e-prop 
can be seen as a generalization that replaces the simple global reward 
signal with a structured, task-specific error signal.

---

## Key Reference

Bellec, G., Scherr, F., Subramoney, A., Hajek, E., Salaj, D., Legenstein, R., 
& Maass, W. (2020). A solution to the learning dilemma for recurrent networks 
of spiking neurons. *Nature Communications*, 11, 3625.  
https://doi.org/10.1038/s41467-020-17236-y

---

## Dependencies

brian2
numpy
matplotlib
scipy
jupyter

Install: `pip install brian2 numpy matplotlib scipy jupyter`
