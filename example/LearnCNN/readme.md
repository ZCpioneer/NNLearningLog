### 注意
**包间调用出错请参考网上资料解决**

### cifar_10_cnn
数据：`NNLearningLog\famousData\cifar-10-batches-py`
cifar_10_cnn的数据是图片，它的工作就是将图片分类成10类。
数据的获取方式和上面的几个例程一样。

### imdbCNN
ImdbCNN中的数据是有关于评论的数据，来自于`NNLearningLog/famousData/imdb.npz`

虽然imdb数据是时间序列，但它用CNN网络来训练可以达到80%的准确率。
不过，如果把优化器从Adam换成sgd，网络会没有学习能力，只有50%的准确率。

### mnist_transfer_cnn
mnistCNN中的数据来自于`NNLearningLog/famousData/mnist.npz`。
迁移学习
1. 用MNIST的0-4训练网络，准确率99.8%
2. 用上一步网络+fine-tune全连接层训练5-9，准确率99.2%

### mnistCNN
mnistCNN中的数据来自于`NNLearningLog/famousData/mnist.npz`。

### vanGogh
图像风格转移，通过图片A的内容和图片B的风格产生一个新的图片C。
比如，我们可以让一个普通的图片加上梵高的作品风格，生成一个新的艺术作品。
这个技术的关键在于构建损失函数，损失函数包括三部分：
1. total variation loss 表示图片C中像素的连续性；
2. style loss
3. content loss
参考论文：[A Neural Algorithm of Artistic Style](http://arxiv.org/abs/1508.06576)