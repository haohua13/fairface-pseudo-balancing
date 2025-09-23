
# Fairness Without Labels: Pseudo-Balancing for Bias Mitigation in Face Gender Classification  

Official implementation of the paper:  
**Fairness Without Labels: Pseudo-Balancing for Bias Mitigation in Face Gender Classification**  

Accepted at **ICCV 2025 – 2nd Workshop on Fairness and Ethics towards Transparent AI: Facing the Challenge through Model Debiasing (FAILED)**.  
- **Authors:** Haohua Dong, Ana Manzano Rodríguez, Camille Guinaudeau, Shin’ichi Satoh  
- **Preprint:** [HAL Archive](https://hal.science/hal-05210445)  
---
## Datasets & Model
We conduct comprehensive experiments using:  
- [FairFace dataset](https://github.com/joojs/fairface)  
- [All-Age-Faces dataset (AAF)](https://github.com/JingchunCheng/All-Age-Faces-Dataset)  

<div align="center">
  <img src="https://github.com/user-attachments/assets/199b565b-812e-445e-8523-f884758d6f24" alt="all-age-faces-dataset" width="20%"/>
  <img src="https://github.com/user-attachments/assets/cddab897-482d-40c3-a6af-84294743948b" alt="fair-face-dataset" width="20%"/>
</div>

We use a ResNet18-based CNN, pre-trained on the [Kaggle gender classification dataset](https://github.com/ndb796/Face-Gender-Classification-PyTorch). The pretrained model's weights are found in classification_model.pth

---

## Folders
### `AAF-Dataset-Pseudo-Labeling-DANN/`
Experiments using **AAF as training data** and **FairFace as test data** with pseudo-labeling and DANN techniques.
### `FairFace-Controlled-Bias-Experiments/`
Experiments using **FairFace as training data** (with different racial/gender biases) and **AAF as test data**.  
### `FairFace-Dataset-Pseudo-Labeling/`
Initial pseudo-labeling and iterative self-training experiments with **FixMatch** and **FlexMatch** using **FairFace as training data** and **AAF as test data**.  
### `Unsupervised-Domain/`
Domain adaptation experiments with **DANN**, **CoRaL**, and **Maximum Mean Discrepancy (MMD) Loss**.  
### `Bias-Visualization/`
Visualization scripts for model performance analysis and bias exploration.  
---

## Citation
If you find this work useful, please cite our paper:

```bibtex
@inproceedings{dong2025:hal-05210445,
  TITLE = {{Fairness Without Labels: Pseudo-Balancing for Bias Mitigation in Face Gender Classification}},
  AUTHOR = {Dong, Haohua and Manzano Rodr{\'i}guez, Ana and Guinaudeau, Camille and Satoh, Shin'Ichi},
  URL = {https://hal.science/hal-05210445},
  BOOKTITLE = {{Second workshop on Fairness and ethics towards transparent AI: facing the chalLEnge through model Debiasing (FAILED) at the 2025 International Conference on Computer Vision}},
  YEAR = {2025}
}
