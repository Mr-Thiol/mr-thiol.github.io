---
title: "Chemformer Retrosynthesis Demo"
layout: "page"
url: "/chemformer/"
summary: "Interactive retrosynthesis app powered by Chemformer"
hidemeta: true
---

## About This Demo

This is an interactive one-step retrosynthesis tool built as part of the *AI for Chemistry* (AI4Chem) course assignment (HW4). Given a target molecule in SMILES notation, the model predicts plausible sets of reactants that could be used to synthesize it.

### What is retrosynthesis?

Retrosynthesis is the process of working backwards from a target molecule to identify simpler precursors. Traditionally performed by expert chemists, it can now be assisted by sequence-to-sequence deep learning models trained on large reaction databases.

### How it works

1. **Input**: Paste a SMILES string, or click one of the 10 curated example molecules.
2. **Preview**: The backend generates a 2D depiction and an RDKit 3D conformer via ETKDG.
3. **Beam search**: Chemformer (a BART-based transformer) decodes up to *N* reactant SMILES in parallel beams. A confidence estimate is derived from the beam score distribution.
4. **Output**: Each predicted reactant set is rendered in 2D and 3D for inspection.

The backend runs as a Hugging Face Space (FastAPI) using the fine-tuned USPTO-50K checkpoint released by MolecularAI.

### Features

- 2D molecular rendering (SmilesDrawer 2.0)
- 3D conformer rendering (3Dmol.js)
- Data-driven success probability estimation
- Beam search retrosynthesis with 1–10 parallel outputs
- 10 curated example drug molecules

{{< retrosyn src="/retro/chemformer-widget.html" >}}

---

## References

1. Irwin, R.; Dimitriadis, S.; He, J.; Bjerrum, E. J. Chemformer: A Pre-Trained Transformer for Computational Chemistry. *Mach. Learn.: Sci. Technol.* **2022**, *3* (1), 015022. [https://doi.org/10.1088/2632-2153/ac3ffb](https://doi.org/10.1088/2632-2153/ac3ffb)

**Open-source repositories:**

- [MolecularAI/Chemformer](https://github.com/MolecularAI/Chemformer) — Pre-trained BART transformer for retrosynthesis
- [MolecularAI/pysmilesutils](https://github.com/MolecularAI/pysmilesutils) — SMILES tokenization & utilities

---

## Acknowledgements

This demo was developed as Homework 4 for the *AI for Chemistry* course. The full-stack implementation (FastAPI backend, Vue 3 frontend, Hugo integration) was built with the assistance of **GitHub Copilot** powered by **Claude Sonnet 4.6**. The fine-tuned Chemformer model and training data are credited to the MolecularAI team at AstraZeneca.

