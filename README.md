# A Comparative Analysis of CapsNet and ResNet on Rotation Invariance
#### Group members: Hanzi Jiang, Yuting Shao, Weimin Huang
## General Idea:
We investigate the performance of Capule Network (CapsNet) and Residual Neural Network (ResNet) in the presence of rotations on the [QuickDraw dataset](https://github.com/googlecreativelab/quickdraw-dataset). The models are trained and evaluated on a subset of the QuickDraw datacontaining 5 classes: triangle, square, mushroom, crown, and envelope.

__1. Example of original images in train and validation set:__
<p align="center">
  <img  src="https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/images/train_example.jpeg">
</p>

__2. Example of images rotated by 45 degrees in test set:__
<p align="center">
  <img  src="https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/images/test_with_rotate_example.jpeg">
</p>

## Getting Started
Please follow the instruction below:

__1. Run on Google Colab:__
  * Download and open [CapsNet.ipynb](https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/CapsNet.ipynb) and [ResNet.ipynb](https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/ResNet.ipynb) on Google Colab.
  * Follow the instructions on the notebook to reproduce the experiments.
  

## Robustness under Rotational Transformation
we compute the test accuracy of the two models on the test dataset with rotated images.

#### Test accuracy vs. rotation angle on different training sample sizes.
<p align="center">
  <img width="460" height="300" src="https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/images/sample_size_acc.png">
</p>



### Acknowledgements
* Implementation of the paper [Dynamic Routing Between Capsules](https://arxiv.org/pdf/1710.09829.pdf) by Sara Sabour, Nicholas Frosst, and Geoffrey E. Hinton. Used [jindongwang/Pytorch-CapsuleNet](https://github.com/jindongwang/Pytorch-CapsuleNet) and [laubonghaudoi/CapsNet_guide_PyTorch](https://github.com/laubonghaudoi/CapsNet_guide_PyTorch) to clarify some confusions, and borrowed some code.
* [Using ResNet for MNIST in PyTorch 1.7](https://zablo.net/blog/post/pytorch-resnet-mnist-jupyter-notebook-2021/)

