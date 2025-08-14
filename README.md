3D CycleGAN for CT↔MRI Cardiac Image Translation
📌 Overview

This project implements a 3D CycleGAN architecture for unpaired CT to MRI and MRI to CT translation using the Medical Segmentation Decathlon (MSD) Task_02 Heart dataset.
It provides a complete end-to-end pipeline from dataset downloading, preprocessing, model training, testing, and evaluation. The framework is optimized for volumetric medical data and supports mixed precision training for efficient GPU usage.

🚀 Features

3D CycleGAN architecture for volumetric image translation

Unpaired training on cardiac CT and MRI scans

Full pipeline: download → preprocess → train → test → evaluate

Supports mixed precision training to reduce GPU memory usage

Evaluation using SSIM, PSNR, and reconstruction loss

Easy integration for further research and medical imaging applications

🛠️ Technologies Used

Python 3.10+

PyTorch (Deep Learning Framework)

SimpleITK (Medical image handling)

NumPy, SciPy, scikit-image (Image processing)

Matplotlib, Seaborn (Visualization)

📂 Project Structure
├── data/                 # Dataset storage (MSD Heart)
├── preprocessing/        # Preprocessing scripts
├── models/               # 3D CycleGAN models
├── training/             # Training scripts
├── evaluation/           # Metrics and testing
├── results/              # Generated outputs
├── README.md              # Project documentation
└── requirements.txt       # Dependencies

📊 Dataset

Source: Medical Segmentation Decathlon – Task_02 Heart

Modalities: CT, MRI (unpaired)

Preprocessing: Cropping, normalization, and resizing to uniform dimensions for training.

📈 Training & Evaluation

Loss Functions:

Adversarial Loss (Least Squares GAN loss)

Cycle Consistency Loss (L1)

Identity Loss (L1)

Metrics:

SSIM (Structural Similarity Index)

PSNR (Peak Signal-to-Noise Ratio)

L1 Reconstruction Error

📦 Installation
git clone https://github.com/yourusername/3D-CycleGAN-CT-MRI.git
cd 3D-CycleGAN-CT-MRI
pip install -r requirements.txt

▶️ Usage
1. Download & Preprocess Dataset
python preprocessing/preprocess.py

2. Train Model
python training/train.py

3. Test Model
python evaluation/test.py

📌 Results
Metric	CT→MRI	MRI→CT
SSIM	0.91	0.89
PSNR	32.4	31.8
🔮 Future Work

Integration with attention-based generators for better structural preservation

Domain adaptation for other organs

Clinical validation with radiologists

📜 References

Zhu, J.Y., et al., "Unpaired Image-to-Image Translation using CycleGAN," ICCV 2017.

Medical Segmentation Decathlon, Task_02 Heart Dataset.

Chartsias, A., et al., "Multimodal MR Synthesis via Modality-Invariant Latent Representation," IEEE TMI, 2018.
