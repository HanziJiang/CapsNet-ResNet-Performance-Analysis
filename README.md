# A Comparative Analysis of CapsNet and ResNet on Rotation Invariance
Group members: Hanzi Jiang, Yuting Shao, Weimin Huang.

Our report can be found [here](https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/A%20Comparative%20Analysis%20of%20CapsNet%20and%20ResNet%20on%20Rotation%20Invariance.pdf).

## General Idea
We investigate the performance of Capule Network (CapsNet) and Residual Neural Network (ResNet) in the presence of rotations on the [QuickDraw dataset](https://github.com/googlecreativelab/quickdraw-dataset). The models are trained and evaluated on a subset of the QuickDraw datacontaining 5 classes: triangle, square, mushroom, crown, and envelope.

__1. Example of original images in training and validation sets:__
<p align="center">
  <img  src="https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/images/train_example.jpeg">
</p>

__2. Example of images rotated by 45 degrees in test set:__
<p align="center">
  <img  src="https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/images/test_with_rotate_example.jpeg">
</p>

## Methods
To test the robustness of CapsNet to rotations, we train our two models on the padded training set. There is no rotation other than natural skewness in the original QuickDraw dataset. We then test the models on images rotated by angles, ranging from -180 to 180 degrees, with a step of step 10 degrees. There are two sets of experiments; we compare how the validation and test accuracy changes for each one.

Exp1 - Different training samples. We sample 5,000 images for each of the five categories, and randomly split them into 0.6:0.2:0.2 train:validation:test datasets. We train our CapsNet and ResNet until at least one of them converges. We also make sure that both of them have similar validation accuracy so that their test performance is comparable. Then the same experiment is performed again, except that the training set is reduced to 0.16 of its original size. This is done by randomly sampling from the original training dataset. The test and validation datasets remain the same. In this way, we reduce the amount of data the model sees during training to investigate how training sample size affects the models’ performance.

Exp2 - Different routing iterations. The same 5,000-per-category training, validation and test datasets are used. There are also two experiments. In the first one, the routing iteration is 1; in the second one, the routing iteration is 3. By comparing the validation and test accuracy, we can determine if the routing algorithm is still effective when applied to a more complex dataset.

## Getting Started
Please follow the instruction below:

__1. Run on Google Colab:__
  * Download and open [CapsNet.ipynb](https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/CapsNet.ipynb) and [ResNet.ipynb](https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/ResNet.ipynb) on Google Colab.
  * Follow the instructions on the notebook to reproduce the experiments.
  

## Results
#### Test accuracy vs. rotation angle on different training sample sizes.
<p align="center">
  <img width="460" height="300" src="https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/images/sample_size_acc.png">
</p>
For complete results, please see our [report](https://github.com/HanziJiang/CapsNet-ResNet-Performance-Analysis/blob/main/A%20Comparative%20Analysis%20of%20CapsNet%20and%20ResNet%20on%20Rotation%20Invariance.pdf).


## Acknowledgements
* Implementation of the paper [Dynamic Routing Between Capsules](https://arxiv.org/pdf/1710.09829.pdf) by Sara Sabour, Nicholas Frosst, and Geoffrey E. Hinton. Used [jindongwang/Pytorch-CapsuleNet](https://github.com/jindongwang/Pytorch-CapsuleNet) and [laubonghaudoi/CapsNet_guide_PyTorch](https://github.com/laubonghaudoi/CapsNet_guide_PyTorch) to clarify some confusions, and borrowed some code.
* [Using ResNet for MNIST in PyTorch 1.7](https://zablo.net/blog/post/pytorch-resnet-mnist-jupyter-notebook-2021/)


