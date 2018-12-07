# EasyDeepLearning

## Pytorch

### 1.基本概念

* iteration（迭代）：也叫training step，每次迭代更新一次网络结构的参数，即**一次**训练数据forward+backward后更新参数的过程

* batch（批）：指把数据集分成多少份

* batch-size（批尺寸）：一次迭代所使用的样本量

  * 深度机器学习中的batch的大小对学习效果有何影响？ - 知乎
    https://www.zhihu.com/question/32673260

* epoch（周期）：一个epoch是指把所有训练数据完整地过一遍，这个过程包括**所有**训练数据forward+backward后更新参数的过程

  > * 如果有1,000条数据，可能数据集太大了，全部跑完再调参很慢，我们可以把这些数据分成10份，每一份100条
  >
  > * batch = 10
  >
  >   batch_size = 100
  >
  > * 每次跑完一个batch都要更新参数，这个过程叫iteration
  >
  > * epoch是指跑完这10个batch，也就是10个iteration的这个过程，记住：在一个 epoch 中，batch 数和迭代数是相等的
  >
  > * 怎么调参数：Epoch vs Batch Size vs Iterations – Towards Data Science
  >   https://towardsdatascience.com/epoch-vs-iterations-vs-batch-size-4dfb9c7ce9c9

### 2.图像分类有三种训练方式：

* Scrach：构建一个新的模型并从头开始训练。

* Bottleneck：在已经训练好的模型基础上，修改模型的最后的全连接层，并重新训练全连接层。

* Finetune：在已经训练好的模型基础上，修改模型的最后的全连接层，并重新训练全连接层同时微调模型的卷积层。

