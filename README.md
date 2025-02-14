# SAFE: Self Supervised Learning for Intrusion Detection Systems
This repository contains implementation for the framework described in the following paper: https://arxiv.org/abs/2502.07119  

Our self-supervised learning intrusion detection framework consists of 4 modules:  

**1. Feature Selection**: Features are ranked in accordance to the absolute value sum of each feature's loadings. A parameter *k* can be set such that the top *k* features are kept.  
**2. Vector to Image Matrix Mapping**: The kept feature vectors are then converted to image matrices by applying t-SNE to obtain each feature's $$\mathbb{R}^2$$ cordinates. These coordinates then allow us to map each feature from the vector into an image matrix, where every entry contains a geometric relationship with another.  
**3. Masked Autoencoder (MAE) Training**: A masked autoencoder is employed to then learn the latent features of our now converted image dataset.  
**4. Feature Extraction and Novelty Detection**: Using the encoder head of our trained MAE, we then extract the latent features from our image dataset and fit a novelty detector to classify threats.  

<img width="1194" alt="SAFE-Framework" src="https://github.com/user-attachments/assets/d2a98202-b2be-45fd-b434-042035341b68" />  

# Citation  
If you use this methodology in your work, please cite our paper:  
```  
@misc{li2025safeselfsupervisedanomalydetection,
      title={SAFE: Self-Supervised Anomaly Detection Framework for Intrusion Detection}, 
      author={Elvin Li and Zhengli Shang and Onat Gungor and Tajana Rosing},
      year={2025},
      eprint={2502.07119},
      archivePrefix={arXiv},
      primaryClass={cs.CR},
      url={https://arxiv.org/abs/2502.07119}, 
}
```  
