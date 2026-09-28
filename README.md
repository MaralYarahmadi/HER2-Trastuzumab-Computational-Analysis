# HER2-Trastuzumab-Computational-Analysis
In silico analysis of the HER2- trastuzumab interface and alanine-scanong mutations
# Computational Analysis of the HER2–Trastuzumab Protein–Protein Interface

## Overview

This project investigates the molecular interface between human epidermal growth factor receptor 2 (HER2) and the therapeutic monoclonal antibody trastuzumab using a reproducible in silico structural biology workflow.

The analysis begins with structural characterization of the experimentally determined HER2–trastuzumab complex, followed by residue-level interface analysis, hotspot screening, alanine-scanning mutations, structural refinement, and computational estimation of mutation-dependent changes in binding energetics.

The project is designed as a reproducible computational workflow in which raw structural data, interaction reports, mutant structures, analysis notes, and computational results are maintained separately.

---

## Biological System

**Protein complex:** HER2–trastuzumab  
**Reference structure:** PDB ID 1N8Z

### Chains

- **HER2:** Chain C
- **Trastuzumab:** Chains A and B

The structural complex is analyzed at the protein–protein interface formed between HER2 and the antibody.

---

## Project Objectives

The main objectives are to:

1. Characterize the HER2–trastuzumab binding interface at the residue and atom levels.
2. Identify residues that contribute substantially to the observed interface.
3. Characterize hydrogen bonds and non-bonded atomic contacts at the interface.
4. Screen selected interface residues using independent alanine substitutions.
5. Compare WT and mutant interaction networks.
6. Evaluate structural changes associated with selected mutations.
7. Refine WT and mutant structures using a consistent computational protocol.
8. Estimate mutation-dependent changes in protein–protein binding energetics using Rosetta-based methods.
9. Maintain a reproducible record of the computational workflow and intermediate results.

---

## Initial WT Interface Analysis

The wild-type HER2–trastuzumab complex was initially analyzed using UCSF ChimeraX.

The initial interface analysis identified:

- **6 hydrogen bonds**
- **76 atom–atom contacts**

The raw interaction reports are preserved in the `data/` directory.

---

## Interface Residue Screening

Residues were selected for further investigation based on their observed participation in hydrogen bonding and/or multiple atomic contacts at the HER2–trastuzumab interface.

Initial candidate residues included:

- D560
- K569
- F573
- K593
- Q602

These residues were selected for an initial alanine-scanning analysis.

The selected mutations are evaluated independently rather than as cumulative or multiple-site mutations.

---

## Alanine-Scanning Analysis

The initial mutant panel consists of:

| Mutation | HER2 residue |
|----------|--------------|
| D560A | Asp560 → Ala |
| K569A | Lys569 → Ala |
| F573A | Phe573 → Ala |
| K593A | Lys593 → Ala |
| Q602A | Gln602 → Ala |

Alanine scanning is used here as a structural and energetic probing strategy to investigate the contribution of individual interface residues.

A decrease in the number of contacts or hydrogen bonds is not interpreted by itself as a quantitative measure of binding affinity. Binding-energy calculations are performed separately.

---

## Current Interaction Results

The currently available WT and mutant interaction counts are summarized below.

| Structure | H-bonds | Contacts | Δ H-bonds vs WT | Δ Contacts vs WT |
|----------|--------:|---------:|----------------:|-----------------:|
| WT | 6 | 76 | — | — |
| K569A | 5 | 74 | -1 | -2 |
| F573A | 6 | 67 | 0 | -9 |
| K593A | 5 | 63 | -1 | -13 |
| Q602A | 4 | 59 | -2 | -17 |
| D560A | 5 | 72 | -1 | -4 |

These values represent structural interaction counts and are not, by themselves, equivalent to binding free energies.

Detailed atom-level interaction comparisons will be performed using the raw ChimeraX reports.

---

## Computational Workflow

The planned workflow is:

```text
Experimental structure (PDB 1N8Z)
                │
                ▼
       WT interface analysis
                │
                ▼
      Interface residue screening
                │
                ▼
       Alanine-scanning panel
                │
                ▼
       WT / mutant comparison
                │
                ▼
      Structure preparation
                │
                ▼
       Structural refinement
                │
                ▼
       Interface energy analysis
                │
                ▼
        ΔΔG binding analysis
                │
                ▼
        Comparative interpretation
