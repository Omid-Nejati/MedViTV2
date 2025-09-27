[![Paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2502.13693)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Omid-Nejati/MedViTV2/blob/main/Tutorials/Evaluation.ipynb)

<div align="center">
  <h1 style="font-family: Arial;">MedViT</h1>
  <h3>MedViTV2: Medical Image Classification with KAN-Integrated Transformers and Dilated Neighborhood Attention</h3>
</div>


<div align="center">
  <img src="https://github.com/Omid-Nejati/MedViT-V2/blob/main/Fig/cover.jpg" alt="figure4" width="40%" />
</div>

## 🔥 News 
- **[2025.08.27]** We have released the pre-trained weights.
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
🔹 **Model weights are available now.**  

| **Dataset** | **Task** | **MedViTV2-tiny (%)** |**MedViTV2-small (%)** |**MedViTV2-base (%)** |**MedViTV2-large (%)** |
|:-----------:|:--------:|:-----------------------:|:------------------:|:---------------------:|:-----------------------:|
| **[ChestMNIST](https://medmnist.com/)** | Multi-Class (14) | 96.3 ([model](https://drive.google.com/file/d/1j7HVQZ66_nbLuHepiYDfNJZURcJyyH66/view?usp=drive_link))| 96.4 ([model](https://drive.google.com/file/d/1TFtUYEqckZsa0oF7hlh5ixD9mLRXAEYv/view?usp=drive_link))| 96.4 ([model](https://drive.google.com/file/d/1biyIHSd6V4aSIz0rlhxj3OzQXql-8WzT/view?usp=drive_link))| 96.7 ([model](https://drive.google.com/file/d/1ecn2TZNGt0L3FXkaNgMqkFuU3bvh0YWr/view?usp=sharing))| 
| **[PathMNIST](https://medmnist.com/)** | Multi-Class (9) | 95.9 ([model](https://drive.google.com/file/d/1bD3fxpxzlbP3SuC8EDV3oZuBYhs5XpOl/view?usp=drive_link))| 96.5 ([model](https://drive.google.com/file/d/1Q09QdkwSLtb-au_3ip7vYzxo_VKvOyby/view?usp=drive_link))| 97.0 ([model](https://drive.google.com/file/d/1WazBW35P2sD3nnnSkuC9cjQAMH-PAICi/view?usp=drive_link))| 97.7 ([model](https://drive.google.com/file/d/1imY08j2tiBEsQAN_Du9-Ve1AdUeBmiVU/view?usp=sharing))| 
| **[DermaMNIST](https://medmnist.com/)** | Multi-Class (7) | 78.1 ([model](https://drive.google.com/file/d/1kFsxcB0L6S_WiEayDdyFoviXw8QInT71/view?usp=drive_link))| 79.2 ([model](https://drive.google.com/file/d/1b3MC7O-AeMaUeOwhcUE0NcKfInJeRMAL/view?usp=drive_link))| 80.8 ([model](https://drive.google.com/file/d/11nsf8LeQc_yZAwozXUul8jgYvLzKjeed/view?usp=drive_link))| 81.7 ([model](https://drive.google.com/file/d/1j-39VrzQII8Rgsi8htUNCrIiWJWx1LFM/view?usp=sharing))|
| **[OCTMNIST](https://medmnist.com/)** | Multi-Class (4) | 92.7 ([model](https://drive.google.com/file/d/1hNoTKG9R4QLqgeT77CVBM2WJ0Qgtgzfv/view?usp=drive_link))| 94.2 ([model](https://drive.google.com/file/d/1LyDzhY3dyutYp-Z1-uxCTpKEHwHTDPQ1/view?usp=drive_link))| 94.4 ([model](https://drive.google.com/file/d/1g7rStUsAqiXLKpt1QSULbzNSgG_madW0/view?usp=drive_link))| 95.2 ([model](https://drive.google.com/file/d/14pWK-8dXX9tw9LiCRuOlVJ_njg9JXrGR/view?usp=sharing))|
| **[PneumoniaMNIST](https://medmnist.com/)** | Multi-Class (2) | 95.1 ([model](https://drive.google.com/file/d/1EJmHGtmYqNhNlnEKpcKMUBieOaZbGFXg/view?usp=drive_link))| 96.5 ([model](https://drive.google.com/file/d/1z-NpuR-U4irhfHV5pF6w2Da5kvfdNsoE/view?usp=drive_link))| 96.9 ([model](https://drive.google.com/file/d/19IRSskO1TtVwCMzIs6NsKtVqec2aqEeb/view?usp=drive_link))| 97.3 ([model](https://drive.google.com/file/d/1oYzejaGw7UuYMXibzeP922kEgW3hio7A/view?usp=sharing))|
| **[RetinaMNIST](https://medmnist.com/)** | Multi-Class (5) | 54.7 ([model](https://drive.google.com/file/d/1rZd94-OoSZwJam8PcX53gNPPc-4FK4z-/view?usp=drive_link))| 56.2 ([model](https://drive.google.com/file/d/1gKl5LV05kUxJcR39NZckklBItND3l5tB/view?usp=drive_link))| 57.5 ([model](https://drive.google.com/file/d/1so0GEW1i6yUMc5kN5pHxqz-rf_7uagRU/view?usp=drive_link))| 57.8 ([model](https://drive.google.com/file/d/1bCwYBSsINop_JpZFDK29zsICJxRl3D0l/view?usp=sharing))|
| **[BreastMNIST](https://medmnist.com/)** | Multi-Class (2) | 88.2 ([model](https://drive.google.com/file/d/1vJAKCWTZIU3Q5gdY4Zu4k9RCzlwV1ZlY/view?usp=drive_link))| 89.5 ([model](https://drive.google.com/file/d/1VL8-ZJ1KhCZY0CELyfaP6gHZCfqRRhkf/view?usp=drive_link))| 90.4 ([model](https://drive.google.com/file/d/1tE3WEHappzok1Ax-lXTL9lvYamHEmSjM/view?usp=sharing))| 91.0 ([model](https://drive.google.com/file/d/1_e11jiGdy03fDokWqIq-uLQePSLuX4RZ/view?usp=drive_link))|
| **[BloodMNIST](https://medmnist.com/)** | Multi-Class (8) | 97.9 ([model](https://drive.google.com/file/d/1v5-TyJTY14ZA4A5_3SYvfszSO_YGbBUQ/view?usp=drive_link))| 98.5 ([model](https://drive.google.com/file/d/1gn96VohPPlqsN_98ZNUwcFTNZ3wahBOt/view?usp=drive_link))| 98.5 ([model](https://drive.google.com/file/d/1gn96VohPPlqsN_98ZNUwcFTNZ3wahBOt/view?usp=sharing))| 98.7 ([model](https://drive.google.com/file/d/1NSNDOWuOOruGX3NSbEzh8N1_WqXjuwKj/view?usp=drive_link))|
| **[TissueMNIST](https://medmnist.com/)** | Multi-Class (8) | 69.9 ([model](https://drive.google.com/file/d/1n3hcdWLDU3v7YmenHXrFV91Qu6-lCAMO/view?usp=drive_link))| 70.5 ([model](https://drive.google.com/file/d/1xZ8w-ZSJnP0CLUkyPwz982Ua9LSE6Fv8/view?usp=drive_link))| 71.1 ([model](https://drive.google.com/file/d/1fdCAKKxVKFSyC6rgXdxy46J39CormgLM/view?usp=drive_link))| 71.6 ([model](https://drive.google.com/file/d/1Fgi-JSiyw6qKhI1HiJ_O8-tZACrXeH_C/view?usp=sharing))|
| **[OrganAMNIST](https://medmnist.com/)** | Multi-Class (11) | 95.8 ([model](https://drive.google.com/file/d/18lAPYy4RfwWSd3lpYhfKOSIcuAILRlOr/view?usp=drive_link))| 96.6 ([model](https://drive.google.com/file/d/1yOkNU3-WC1zBf_uPligWHmUpxUrsuZ1U/view?usp=drive_link))| 96.9 ([model](https://drive.google.com/file/d/1xFtcQMnkfgEmWtaWYNgqBFM5jvw9G3RU/view?usp=drive_link))| 97.3 ([model](https://drive.google.com/file/d/1D9XIKdJmbUbvzrKXCzXxF4nXK6RJuDfh/view?usp=sharing))|
| **[OrganCMNIST](https://medmnist.com/)** | Multi-Class (11) | 93.5 ([model](https://drive.google.com/file/d/1Rs_yH-iL2m7SXJ4X0Cyu22QQJCWp7N_a/view?usp=drive_link))| 95.0 ([model](https://drive.google.com/file/d/1d0nhYmsUVzMKul5F7pY2Tpu6eEsQd3g0/view?usp=drive_link))| 95.3 ([model](https://drive.google.com/file/d/1Qk43YyXdJrcO9OFJc1aY-E6VPefcoCih/view?usp=drive_link))| 96.1 ([model](https://drive.google.com/file/d/1jpPTbcy0ztZxo9XshfU_J0TiRV26RwFC/view?usp=sharing))|
| **[OrganSMNIST](https://medmnist.com/)** | Multi-Class (11) | 82.4 ([model](https://drive.google.com/file/d/17yvqiBt57QUQJNxpQSL-ddke-pBEytxo/view?usp=drive_link))| 83.9 ([model](https://drive.google.com/file/d/1bq_g2EstVUCo5Heb_ulRV4pL67WHIFJ1/view?usp=drive_link))| 84.4 ([model](https://drive.google.com/file/d/10NGAdpeo5hj2rqtpyAl80jGKqdmMshtv/view?usp=drive_link))| 85.1 ([model](https://drive.google.com/file/d/1kWdjz_WxCmfSM3uSIs40bYKtgt7jYyFF/view?usp=sharing))|
| **[PAD-UFES-20](https://data.mendeley.com/datasets/zr7vgbcyr2/1)** | Multi-Class (6) | 63.6 ([model](https://drive.google.com/file/d/1geL0CJoAUlR6smifzU-K9JOPUsJjrcOf/view?usp=drive_link))| |
| **[ISIC2018](https://challenge.isic-archive.com/data/)** | Multi-Class (7) | 77.1 ([model](https://drive.google.com/file/d/170V8I-Ghmvl8kj-BtGuTkC1u9LfTC6Nx/view?usp=drive_link))|
| **[CPN X-ray](https://data.mendeley.com/datasets/dvntn9yhd2/1)** | Multi-Class (3) | |  95.3 ([model](https://drive.google.com/file/d/1S3prrvtcBeNAeiGjtxlwsNYP45S4Y-_3/view?usp=drive_link))|
| **[Kvasir](https://datasets.simula.no/kvasir/)** | Multi-Class (8) |  |82.8 ([model](https://drive.google.com/file/d/1T5OSt9ngHLx3er3KPNGtKTiKsfk14tsD/view?usp=drive_link))| |
| **[Fetal-Planes-DB](https://zenodo.org/records/3904280)** | Multi-Class (6) | | |  95.3 ([model](https://drive.google.com/file/d/16bWPHWGQxvq_ynVYnRRfhANNMNlFx9O1/view?usp=drive_link))|

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
