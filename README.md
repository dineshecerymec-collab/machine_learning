# Understanding Contrastive Learning: How Neural Networks Learn Representations Without Labels

## Overview
This project investigates how neural networks can learn meaningful feature representations without using labelled data. It focuses on contrastive learning, a self-supervised approach that trains models by distinguishing between similar and dissimilar samples.

The study analyses training behaviour, feature space structure, and downstream classification performance using the CIFAR-10 dataset.

---

## Objectives
- Explain the limitations of supervised learning in requiring labelled data  
- Demonstrate how contrastive learning constructs representations using similarity  
- Analyse training behaviour through contrastive loss  
- Evaluate learned representations using embedding visualisation and linear classification  

---

## Methodology

### Dataset
The experiments use the CIFAR-10 dataset, consisting of 60,000 colour images across 10 classes.

### Model
The model consists of:
- an encoder (ResNet-18) to extract features  
- a projection head (MLP) for contrastive training  

### Training
- Contrastive learning using InfoNCE loss  
- Batch size: 256  
- Learning rate: 0.001  
- Number of epochs: 10  

### Evaluation
A linear classifier is trained on frozen features to evaluate representation quality.

---

## Results

### Contrastive Training Loss

| Epoch | Loss |
|------:|-----:|
| 1 | 4.8965 |
| 2 | 4.6004 |
| 3 | 4.5352 |
| 4 | 4.5025 |
| 5 | 4.4836 |
| 6 | 4.4689 |
| 7 | 4.4564 |
| 8 | 4.4461 |
| 9 | 4.4373 |
| 10 | 4.4304 |

The loss decreases steadily, indicating improved alignment of positive pairs and separation of negative samples.

---

### Linear Evaluation Performance

| Method | Accuracy |
|-------|---------:|
| Linear Classifier on Learned Features | 0.5890 |

The learned representations achieve moderate classification performance, demonstrating that meaningful features are learned without supervision.


## Installation

Clone the repository: 
cd contrastive-learning-tutorial  

Install dependencies:

pip install -r requirements.txt  

---

## Usage

Run the notebook:

jupyter notebook  

Open:

Dinesh_24174065.ipynb  

Run all cells to reproduce results and figures.

---

## Requirements

- Python 3.x  
- PyTorch  
- torchvision  
- numpy  
- matplotlib  
- scikit-learn  

---

## Accessibility

The project incorporates accessibility considerations:
- figures include descriptive captions and alt-text  
- colour schemes are chosen for readability  
- content is structured with clear headings  
- results are presented in clear tables  

---

## References

- Chen, T. et al. (2020). A Simple Framework for Contrastive Learning of Visual Representations  
- He, K. et al. (2020). Momentum Contrast for Unsupervised Visual Representation Learning  
- Oord, A. et al. (2018). Representation Learning with Contrastive Predictive Coding  
- Goodfellow, I. et al. (2016). Deep Learning  

---

## License

This project is licensed under the MIT License.

---
