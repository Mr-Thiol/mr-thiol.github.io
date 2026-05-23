---
title: "Chemformer Retrosynthesis Demo"
layout: "page"
url: "/chemformer/"
summary: "Interactive retrosynthesis app powered by Chemformer"
hidemeta: true
---

This module supports:

- Input SMILES
- 2D molecular rendering
- 3D molecular rendering
- Data-driven success probability estimation
- Chemformer one-step retrosynthesis with beam outputs

{{< retrosyn src="/retro/chemformer-widget.html" >}}

---

## References

1. Irwin, R.; Dimitriadis, S.; He, J.; Bjerrum, E. J. Chemformer: A Pre-Trained Transformer for Computational Chemistry. *Mach. Learn.: Sci. Technol.* **2022**, *3* (1), 015022. [https://doi.org/10.1088/2632-2153/ac3ffb](https://doi.org/10.1088/2632-2153/ac3ffb)

**Open-source repositories:**

- [MolecularAI/Chemformer](https://github.com/MolecularAI/Chemformer) — Pre-trained BART transformer for retrosynthesis
- [MolecularAI/pysmilesutils](https://github.com/MolecularAI/pysmilesutils) — SMILES tokenization & utilities

