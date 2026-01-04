# ULTra

This repository provides a *Jupyter notebook* (`ULTra_demo.ipynb`) that demonstrates key ideas from:

**ULTra: Unveiling Latent Token Interpretability in Transformer-Based Understanding and Segmentation**  
(arXiv:2411.12589)

## What this notebook demonstrates
1) **ULTra interpretability (core methodology)**  
   We compute **latent token explanation maps** in a transformer-based vision encoder (CLIP ViT).  
   This corresponds to the paper’s overall interpretability methodology (token-level explanation maps at a chosen layer).

2) **Unsupervised semantic segmentation (Section 4.1)**  
   Following *Section 4.1*, we treat explanation maps as token-wise “concept” signals and perform **unsupervised segmentation** by grouping token maps (clustering) and assigning each pixel to the most dominant clustered concept.

> Note: this repo is intentionally minimal (single-image demo).

## Notebook pipeline (high level)
- Load CLIP ViT + preprocess image
- Compute **token explanation maps** at a selected layer (interpretability)
- Aggregate/group token maps via clustering (Section 4.1)
- Produce a segmentation mask by assigning pixels to the strongest clustered concept

If you use this code, please cite:
```bibtex
@article{hosseini2024ultra,
  title={ULTra: Unveiling Latent Token Interpretability in Transformer-Based Understanding and Segmentation},
  author={Hosseini, Hesam and Mighan, Ghazal Hosseini and Afzali, Amirabbas and Amini, Sajjad and Houmansadr, Amir},
  journal={arXiv preprint arXiv:2411.12589},
  year={2024}
}
```

## Acknowledgements
- We use the CLIP implementation and utilities from Chefer et al.’s repository:
  https://github.com/hila-chefer/Transformer-MM-Explainability
- CLIP model: OpenAI CLIP.




