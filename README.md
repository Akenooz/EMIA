🔍 Project Overview

Medical image analysis plays a vital role in diagnosing and treating diseases by extracting meaningful patterns from images such as X-Rays, CT scans, and MRI scans. However, human interpretation is often time-consuming and susceptible to errors. This project introduces a novel deep learning approach that harnesses Generative Adversarial Networks (GANs) and Bidirectional GANs (BiGANs) to automate the detection and classification of abnormalities—specifically bacterial and viral anomalies—in medical images.

The models are designed to learn representations of normal and anomalous medical images, reducing reliance on manual feature engineering and enhancing diagnostic accuracy.

🚀 Key Features
🧠 Deep Learning Techniques

Generative Adversarial Networks (GANs)
GANs learn to generate realistic medical images from latent vectors, improving the detection of even subtle anomalies.

Bidirectional GANs (BiGANs)
BiGANs extend GANs by jointly learning both the image generation and the inverse mapping from image to latent space—enabling improved representation learning and more precise anomaly detection.

These generative models are trained to distinguish between normal and abnormal patterns, helping identify bacterial vs. viral features and reduce diagnostic inconsistencies introduced by human reviewers.

🛠️ Architecture
🧩 Core Components
Module	Description
Data Loader	Handles loading and preprocessing medical image datasets (X-Rays, MRI, CT).
GAN Model	Standard GAN with generator and discriminator networks.
BiGAN Model	Incorporates mapping from image space to latent space, enabling better feature learning.
Anomaly Detection Logic	Uses reconstruction loss or latent representation distances to classify anomalies.
Evaluation Module	Metrics like accuracy, precision, recall on validation and test sets.
🧪 Supported Tasks

✔ Anomaly detection (binary classification — normal vs. abnormal)
✔ Anomaly categorization (Bacterial vs. Viral)
✔ Feature extraction and projection for visualization
✔ Optional: heatmaps / saliency for interpretability

📁 Repository Structure
.
├── data/
│   ├── raw/  
│   ├── processed/  
├── models/
│   ├── gan.py  
│   ├── bigan.py  
├── notebooks/
│   ├── EDA.ipynb
│   ├── Training_Visualization.ipynb
├── results/
│   ├── checkpoints/
│   ├── figures/
├── src/
│   ├── train.py  
│   ├── evaluate.py  
│   ├── utils.py  
├── README.md  
├── requirements.txt

🚀 Installation

Clone the repository

git clone https://github.com/yourusername/medical-image-analysis-gan.git
cd medical-image-analysis-gan


Create a virtual environment

python3 -m venv venv
source venv/bin/activate


Install dependencies

pip install -r requirements.txt

📈 Usage
🧪 Train a Model
python src/train.py \
  --model gan \
  --dataset ./data/processed \
  --epochs 150 \
  --batch_size 32


Replace gan with bigan to use the BiGAN architecture.

🧾 Evaluate Performance
python src/evaluate.py \
  --model bigan \
  --checkpoint ./results/checkpoints/bigan.pth


Results will be output as:

Confusion matrices

ROC curves

Classification reports

🧠 Citation

If you use this project in your research, please cite:

@article{EmpoweringMedicalImageAnalysis2024,
  author = {Vatsal Kumar Sharma and Aryan Jakhar and Aaroh Vats and Gurwinder Singh},
  title = {Empowering Medical Image Analysis: Unveiling Anomalies Through GANs and BiGAN’s Models},
  year = {2024},
  note = {Research article},
}


Note: actual publication info may differ if a DOI appears when the paper is formally published.

🧩 Acknowledgments

Thanks to the authors for advancing the field of medical image analysis with innovative use of generative deep learning models. This work contributes toward reducing reliance on manual radiological interpretation and improving automated clinical decision support.

❤️ Contributions

All contributions are welcome—just open a Pull Request!
