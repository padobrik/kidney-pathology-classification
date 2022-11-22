# Classification model for kidney pathology
Experimenting with the quality of classification of the kidney pathology in case of different activation functions

*Accepted to publication in "Studies in Computational Intelligence" by Springer Nature*: [Book](https://link.springer.com/chapter/10.1007/978-3-031-19032-2_37)

## Dataset
Import dataset here: `https://www.kaggle.com/datasets/nazmul0087/ct-kidney-dataset-normal-cyst-tumor-and-stone`

## Libs
- Processing and Visualization: `pandas`, `numpy`, `matplotlib`
- Neural Network Architecture: `keras`, `tensorflow`

## Results
The architecture of the neural network was based on the ReLU. To improve the quality of the classification, the activation unctions were selected: LeakyReLU, ELU, SELU and GELU. Based on the built neural network architecture, there were formed four cascades of algorithms for each of the activation functions.

Judging by the results, the most promising activation functions for the implementation of this neural network are LeakyReLU and GELU.

GELU works differently from ReLU as it weighs its inputs by their value rather than their sign when thresholding. It is known that GELU activation improves performance across almost every task in natural language processing, and computer vision. As GELU and ReLU are asymptotically equivalent to each other, it is possible to draw an analogy between them, and use GELU instead of ReLU in these applications. For GELU, the median Categorical Cross-Entropy Loss for the training set is **7.85%**, and for the validation set it is **1.87%**. For LeakyReLU it is **9.05%** and **0.49%**, respectively. For comparison, the value of the loss function for the training and validation sets with ReLU is **9.29%** and **1.89%**.

## Graphs
![](https://github.com/padobrik/kidney-pathology-classification/blob/main/graphs/functions.png)
> ReLU functions family

![](https://github.com/padobrik/kidney-pathology-classification/blob/main/graphs/evaluation.png)
> Results of experiment

## Contribution
Special thanks to:
- [Yaroslav Mikhaylik](https://github.com/HaselLoyance) for testing models
- [Alena Samarina](https://github.com/alencombo) for medical annotations
