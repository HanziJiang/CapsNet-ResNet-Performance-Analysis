# A Comparative Analysis of CapsNet and ResNet on Rotation Invariance
#### Group members: Hanzi Jiang, Yuting Shao, Weimin Huang
## General Ideas:
We investigate the performance of CapsNet and Residual Neural Network (ResNet) in the presence of rotations on the QuickDraw dataset. 

### Getting Started
Please follow the instruction below:

__1. Run on Google Colab:__
  * Download and open [ResNet.ipynb](https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/ResNet.ipynb) and [guide_big.ipynb](https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/guide_big.ipynb) on your google drive.
  * Follow the instructions on the notebook to reproduce the experiments.
  

## Robustness under Rotational Transformation
we compute the test accuracy of the two models on the test dataset with rotated images

### Demo


### Demo



### Acknowledgements
* Implementation of the paper [Dynamic Routing Between Capsules](https://arxiv.org/pdf/1710.09829.pdf) by Sara Sabour, Nicholas Frosst, and Geoffrey E. Hinton. Used [jindongwang/Pytorch-CapsuleNet](https://github.com/jindongwang/Pytorch-CapsuleNet) and [laubonghaudoi/CapsNet_guide_PyTorch](https://github.com/laubonghaudoi/CapsNet_guide_PyTorch) to clarify some confusions, and borrowed some code.
* [Using ResNet for MNIST in PyTorch 1.7](https://zablo.net/blog/post/pytorch-resnet-mnist-jupyter-notebook-2021/)

