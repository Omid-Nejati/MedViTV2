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

**Important:** This code also supports training **all TIMM models**.

## Visual Examples
You can find a tutorial for visualizing the Grad-CAM heatmap of MedViT in this repository ["visualize"](https://github.com/Omid-Nejati/MedViTV2/blob/main/Tutorials/Visualization.ipynb).

## Usage
First, clone the repository locally:
```
git clone https://github.com/whai362/PVT.git](https://github.com/Omid-Nejati/MedViTV2.git
cd /content/MedViTV2
```
Install PyTorch 2.5
```
pip install torch==2.5.0 torchvision==0.20.0 torchaudio==2.5.0 --index-url https://download.pytorch.org/whl/cu124
```
Then, install natten 0.17.3
```
pip install natten==0.17.3+torch250cu124 -f https://shi-labs.com/natten/wheels/
```
Also, install requirements
```
pip install -r requirements.txt
```
## Training
To train MedViT-small on breastMNIST on a single gpu for 100 epochs run:
```
python main.py --model_name 'MedViT_small' --dataset 'breastmnist' --pretrained False
```

## 📊 Performance Overview
Below is the performance summary of MedViT on various medical imaging datasets.  
🔹 **Model weights will be available soon.**  

| **Dataset** | **Task** | **MedViTV2-tiny (%)** |**MedViTV2-small (%)** |**MedViTV2-base (%)** |**MedViTV2-large (%)** |
|:-----------:|:--------:|:-----------------------:|:------------------:|:---------------------:|:-----------------------:|
| **[ChestMNIST](https://medmnist.com/)** | Multi-Class (14) | 96.3 (model)| 96.4 (model)| 96.4 (model)| 96.7 (model)| 
| **[PathMNIST](https://medmnist.com/)** | Multi-Class (9) | 95.9 (model)| 96.5 (model)| 97.0 (model)| 97.7 (model)| 
| **[DermaMNIST](https://medmnist.com/)** | Multi-Class (7) | 78.1 (model)| 79.2 (model)| 80.8 (model)| 81.7 (model)|
| **[OCTMNIST](https://medmnist.com/)** | Multi-Class (4) | 92.7 (model)| 94.2 (model)| 94.4 (model)| 95.2 (model)|
| **[PneumoniaMNIST](https://medmnist.com/)** | Multi-Class (2) | 95.1 (model)| 96.5 (model)| 96.9 (model)| 97.3 (model)|
| **[RetinaMNIST](https://medmnist.com/)** | Multi-Class (5) | 54.7 (model)| 56.2 (model)| 57.5 (model)| 57.8 (model)|
| **[BreastMNIST](https://medmnist.com/)** | Multi-Class (2) | 88.2 (model)| 89.5 (model)| 90.4 (model)| 91.0 (model)|
| **[BloodMNIST](https://medmnist.com/)** | Multi-Class (8) | 97.9 (model)| 98.5 (model)| 98.5 (model)| 98.7 (model)|
| **[TissueMNIST](https://medmnist.com/)** | Multi-Class (8) | 69.9 (model)| 70.5 (model)| 71.1 (model)| 71.6 (model)|
| **[OrganAMNIST](https://medmnist.com/)** | Multi-Class (11) | 95.8 (model)| 96.6 (model)| 96.9 (model)| 97.3 (model)|
| **[OrganCMNIST](https://medmnist.com/)** | Multi-Class (11) | 93.5 (model)| 95.0 (model)| 95.3 (model)| 96.1 (model)|
| **[OrganSMNIST](https://medmnist.com/)** | Multi-Class (11) | 82.4 (model)| 83.9 (model)| 84.4 (model)| 85.1 (model)|
| **[PAD-UFES-20](https://data.mendeley.com/datasets/zr7vgbcyr2/1)** | Multi-Class (6) | 63.6 (model)| |
| **[ISIC2018](https://challenge.isic-archive.com/data/)** | Multi-Class (7) | 77.1 (model)|
| **[CPN X-ray](https://data.mendeley.com/datasets/dvntn9yhd2/1)** | Multi-Class (3) | |  95.3 (model)|
| **[Kvasir](https://datasets.simula.no/kvasir/)** | Multi-Class (8) |  |82.8 (model)| |
| **[Fetal-Planes-DB](https://zenodo.org/records/3904280)** | Multi-Class (6) | | |  95.3 (model)|

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
