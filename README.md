# Wide ResNet Implementation with Pytorch
- Unofficial implementation of the paper *Wide Residual Networks*


## 0. Develop Environment
```
Docker Image
- pytorch/pytorch:1.8.1-cuda11.1-cudnn8-devel
```


## 1. Implementation Details
- model.py : Wide ResNet model
- train.py : train Wide ResNet
- utils.py : count correct prediction
- Wide ResNet - Cifar 10 (Single).ipynb : install library, download dataset, preprocessing, train and result
- Wide ResNet - Cifar 10 (5 Average) : average 5 runs same as paper
- Details
  * Follow CIFAR-10 train details
    * batch size 128, learning rate 0.1, nesterov momentum 0.9, weight decay 0.0005
    * learning rate schedulers on [60, 120, 160] with 0.2 learning rate drop
    * augmentation : mean/std preprocessing, pad and crop


## 2. Result Comparison on CIFAR-10
|Source|Score|Detail|
|:-:|:-:|:-|
|Paper|96.11|WideResNet with depth 28, k 10, Average 5 runs|
|Current Repo|96.27|WideResNet with depth 28, k 10, Average 5 runs|


## 3. Reference
- Wide Residual Networks [[paper]](https://arxiv.org/pdf/1605.07146.pdf) [[official code]](https://github.com/szagoruyko/wide-residual-networks)
