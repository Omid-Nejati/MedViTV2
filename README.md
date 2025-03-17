[![Paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2502.13693)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Omid-Nejati/MedViTV2/blob/main/Tutorials/Evaluation.ipynb)

<div align="center">
  <h1 style="font-family: Arial;">MedViT</h1>
  <h3>MedViTV2: Medical Image Classification with KAN-Integrated Transformers and Dilated Neighborhood Attention</h3>
</div>


<div align="center">
  <img src="https://github.com/Omid-Nejati/MedViT-V2/blob/main/Fig/cover.jpg" alt="figure4" width="40%" />
</div>

## Train & Test --- Prepare data
To **train or evaluate** MedViT models on **17 medical datasets**, follow this ["Evaluation"](https://github.com/Omid-Nejati/MedViTV2/blob/main/Tutorials/Evaluation.ipynb). 

⚠️ **Important:** This code also supports training **all TIMM models**.

## Visual Examples
You can find a tutorial for visualizing the Grad-CAM heatmap of MedViT in this repository ["visualize"](https://github.com/Omid-Nejati/MedViTV2/blob/main/Tutorials/Visualization.ipynb).

## 📊 Performance Overview
Below is the performance summary of MedViT on various medical imaging datasets.  
🔹 **Model weights will be available soon.**  

| **Dataset** | **Task** | **Overall Accuracy (%)** |
|:-----------:|:--------:|:-----------------------:|
| **[PAD-UFES-20](https://data.mendeley.com/datasets/zr7vgbcyr2/1)** | Multi-Class (6) | 63.6 |
| **[ISIC2018](https://challenge.isic-archive.com/data/)** | Multi-Class (7) | 77.1 |
| **[Fetal-Planes-DB](https://zenodo.org/records/3904280)** | Multi-Class (6) | 95.3 |
| **[CPN X-ray](https://data.mendeley.com/datasets/dvntn9yhd2/1)** | Multi-Class (3) | 98.2 |
| **[Kvasir](https://datasets.simula.no/kvasir/)** | Multi-Class (8) | 82.8 |
| **[ChestMNIST](https://medmnist.com/)** | Multi-Class (14) | 96.3 |
| **[PathMNIST](https://medmnist.com/)** | Multi-Class (9) | 95.9 |
| **[DermaMNIST](https://medmnist.com/)** | Multi-Class (7) | 78.1 |
| **[OCTMNIST](https://medmnist.com/)** | Multi-Class (4) | 92.7 |
| **[PneumoniaMNIST](https://medmnist.com/)** | Multi-Class (2) | 95.1 |
| **[RetinaMNIST](https://medmnist.com/)** | Multi-Class (5) | 54.7 |
| **[BreastMNIST](https://medmnist.com/)** | Multi-Class (2) | 88.2 |
| **[BloodMNIST](https://medmnist.com/)** | Multi-Class (8) | 97.9 |
| **[TissueMNIST](https://medmnist.com/)** | Multi-Class (8) | 69.9 |
| **[OrganAMNIST](https://medmnist.com/)** | Multi-Class (11) | 95.8 |
| **[OrganCMNIST](https://medmnist.com/)** | Multi-Class (11) | 93.5 |
| **[OrganSMNIST](https://medmnist.com/)** | Multi-Class (11) | 82.4 |

## License
MedViT is released under the [MIT License](LICENSE).

💖🌸 If you find my GitHub repository useful, please consider giving it a star!🌟  

## References
* [FasterKAN](https://github.com/AthanasiosDelis/faster-kan)
* [Natten](https://github.com/SHI-Labs/NATTEN)
* [MedViTV1](https://github.com/Omid-Nejati/MedViT)
  
## Citation
```bibtex
@article{manzari2025medical,
  title={Medical Image Classification with KAN-Integrated Transformers and Dilated Neighborhood Attention},
  author={Manzari, Omid Nejati and Asgariandehkordi, Hojat and Koleilat, Taha and Xiao, Yiming and Rivaz, Hassan},
  journal={arXiv preprint arXiv:2502.13693},
  year={2025}
}

@article{manzari2023medvit,
  title={MedViT: a robust vision transformer for generalized medical image classification},
  author={Manzari, Omid Nejati and Ahmadabadi, Hamid and Kashiani, Hossein and Shokouhi, Shahriar B and Ayatollahi, Ahmad},
  journal={Computers in Biology and Medicine},
  volume={157},
  pages={106791},
  year={2023},
  publisher={Elsevier}
}

```
