---
layout: post
title:  "MATLAB deeplearning toolbox"
date:   2019-09-11 9:39:42
categories: 工具箱
tags: MATLAB DeepLearning
---

* content
{:toc}

MATLAB深度学习工具箱汇总。






Matlab一直以来都有着神经网络工具箱，而从2016的版本开始，提供深度神经网络的相关工具。而到现如今2017的版本，功能更加完善，因此本人在此总结Matlab 2017所包含的深度学习的功能。

如今版本的Matlab已经包含的如下功能：

Ø  [利用自己的数据微调训练好的网络（迁移学习）](https://ww2.mathworks.cn/help/deeplearning/ug/deep-learning-in-matlab.html#bvmv5y4)

Ø  获取已经训练好的神经网络

 [包含Alexnet、VGG16、VGG19](https://ww2.mathworks.cn/help/deeplearning/ug/pretrained-convolutional-neural-networks.html)

Ø  提供了方便的窗口式的神经网络工具箱

[Neural Newwork Time Series Tool](https://ww2.mathworks.cn/help/deeplearning/gs/neural-network-time-series-prediction-and-modeling.html)神经网络时间序列工具，可训练RNN

[Neural Pattern Recognition app](https://ww2.mathworks.cn/help/deeplearning/gs/classify-patterns-with-a-neural-network.html) 神经网络特征识别工具

[Neural Fitting app](https://ww2.mathworks.cn/help/deeplearning/function-approximation-and-nonlinear-regression.html) 神经网络拟合工具

[Nerual Clustering app](https://ww2.mathworks.cn/help/deeplearning/gs/cluster-data-with-a-self-organizing-map.html) 神经网络聚类工具

Ø  使用深度神经网络进行[分类](https://ww2.mathworks.cn/help/deeplearning/examples/create-simple-deep-learning-network-for-classification.html)或[回归](https://ww2.mathworks.cn/help/deeplearning/examples/train-a-convolutional-neural-network-for-regression.html)

Ø  [使用超过内存大小的数据集来训练网络](https://ww2.mathworks.cn/help/deeplearning/ref/trainnetwork.html#bu6sn60-2)

Ø  [训练用于目标检测的神经网络](https://ww2.mathworks.cn/help/deeplearning/ref/trainnetwork.html#bu6sn60-2)

Ø  [特征网络可视化](https://ww2.mathworks.cn/help/deeplearning/examples/visualize-activations-of-a-convolutional-neural-network.html)

Ø  [在个人电脑或者云端使用CPU、GPU、多个GPU加速训练](https://ww2.mathworks.cn/help/deeplearning/ug/deep-learning-in-matlab.html#bvmt9z2)

当前版本GPU计算性能高于2.0的都使用GPU加速

Ø  提供了经典的神经网络应用例子与教程（附代码）

例如，MNIST手写体识别，[Deep Dream](https://ww2.mathworks.cn/help/deeplearning/examples/deep-dream-images-using-alexnet.html)、[Fast-RCNN](https://ww2.mathworks.cn/help/vision/examples/object-detection-using-faster-r-cnn-deep-learning.html?searchHighlight=CNN&s_tid=doc_srchtitle)物体检测等

Ø  提供了官方的Caffe接口

载入[Caffe模型](https://ww2.mathworks.cn/help/deeplearning/ref/importcaffenetwork.html)、[层](https://ww2.mathworks.cn/help/deeplearning/ref/importcaffelayers.html)等

Ø  提供了一系列预处理工具

[自动修改训练集图片文件名](https://ww2.mathworks.cn/help/vision/ug/label-images-for-classification-model-training.html)等

Ø  [提供了神经网络控制系统工具箱](https://ww2.mathworks.cn/help/deeplearning/neural-network-control-systems.html)


————————————————
版权声明：本文为CSDN博主「文宇肃然」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/wenyusuran/article/details/81327987

