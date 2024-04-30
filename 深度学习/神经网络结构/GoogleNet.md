# GoogleNet——Going deeper with convolutions
#深度学习 

# 一、Inception结构的想法来源
1. 之前的研究中有人利用多个不同尺寸的Gabor滤波器处理多尺度问题（其实这个想法是来源于灵长类动物的视觉皮质的神经科学模型），但模型层数太少，而GoogLeNet将Inception重复很多次以此实现22层的网络结构
2. 1 x 1卷积的想法来源于NiN
# 二、网络设计得更宽、更深的问题

1.  容易过拟合
2.  梯度消失
> 网络变的很深的时候，梯度将以指数形式进行[[梯度下降|梯度下降]]。梯度消失问题和梯度爆炸问题一般随着网络层数的增加会变得越来越明显。在根据损失函数计算的误差通过梯度**反向传播**的方式对深度网络权值进行更新时，得到的**梯度值接近0**或**特别大** ^9a807f
3.  计算资源有限且越大的完了过利用率未必高
# 三、整体网络结构设计
![v2-766c3f59d3791da39ad805606d6445f6_1440w.webp](https://cdn.nlark.com/yuque/0/2022/webp/33630082/1666778063310-ff430cec-2dd1-4e35-bf13-c30818f280ff.webp#averageHue=%23fbf6f4&clientId=ua8dfb534-11cc-4&from=drop&height=2050&id=GP3f2&originHeight=4096&originWidth=919&originalType=binary&ratio=1&rotation=0&showTitle=false&size=162570&status=done&style=none&taskId=u0e58220a-335d-420d-ac1b-f67b84ca368&title=&width=460)
![](https://cdn.nlark.com/yuque/0/2022/webp/33630082/1666779776781-1c40e49f-02e4-4c66-b9dc-24386c190c6d.webp#averageHue=%23eaeaea&from=url&id=S2t1Q&originHeight=758&originWidth=1440&originalType=binary&ratio=1&rotation=0&showTitle=false&status=done&style=none&title=)

# 四、什么是Inception

- 在未使用这种方式的网络里，我们一层往往只使用一种操作，比如卷积或者池化，而且卷积操作的卷积核尺寸也是固定大小的。但是，在实际情况下，在不同尺度的图片里，需要不同大小的卷积核，这样才能使性能最好。对于同一张图片，不同尺寸的卷积核的表现效果是不一样的，因为他们的感受野不同。所以，我们希望让网络自己去选择，Inception 便能够满足这样的需求，一个 Inception 模块中并列提供多种卷积核的操作，网络在训练的过程中通过调节参数自己去选择使用，同时，由于网络中都需要池化操作，所以此处也把池化层并列加入网络中。


## 1. InceptionV1
![v2-effa75269cba3c8038c49185e9e8368a_720w.jpg](https://cdn.nlark.com/yuque/0/2022/jpeg/33630082/1666777257954-532b793c-2e5b-4a8f-8168-ae8d93e08200.jpeg#averageHue=%23f3f3d8&clientId=ua8dfb534-11cc-4&from=drop&id=u535c07ad&originHeight=249&originWidth=480&originalType=binary&ratio=1&rotation=0&showTitle=false&size=19067&status=done&style=none&taskId=u9a94e480-9d28-4d05-9346-0bfe9c920e0&title=)


- 四个分支，每个分支卷积后的feature map分辨率大小是相同的，于是就可以将其堆叠起来，作为下一层的输入
- 举个例子：
- 假设上一层输出是28 x 28 x 192，
- 第一个分支卷积核是1 x 1 x 64，padding = 0，stride = 1，输出是28 x 28 x 64；
- 第二个分支卷积核是3 x 3 x 128，padding = 1，stride = 1，输出就是28 x 28 x 128；
- 第三个分支卷积核是5 x 5 x 32，padding = 2，stride = 1，输出就是28 x 28 x 32；
- 第四个分支和第二个差不多，padding = 1，stride = 1，输出是28 x 28 x 192
- （和输入一样，这也是问题所在），于是这四个分支的输出可以拼接在一起。
- 卷积公式：(_w-f+p)/s+1_


![image.png](https://cdn.nlark.com/yuque/0/2022/png/33630082/1667606439134-976f8f44-da79-40e8-86d2-e00a4d1b1720.png#averageHue=%23c58475&clientId=uf32ab3e7-c0f4-4&from=paste&height=925&id=u77a76cfb&originHeight=925&originWidth=1653&originalType=binary&ratio=1&rotation=0&showTitle=false&size=800189&status=done&style=none&taskId=u90473a0b-f43f-4dc8-9d2f-babbb7b5ecc&title=&width=1653)


## 2. InceptionV2


![80d77ee7085b4505aac57347585e14d3.png](https://cdn.nlark.com/yuque/0/2022/png/33630082/1666778164010-68d8dbc8-31bd-45c0-a75a-35bbfc39113e.png#averageHue=%23f6f3ef&clientId=ua8dfb534-11cc-4&from=drop&id=uc4ff29a6&originHeight=621&originWidth=949&originalType=binary&ratio=1&rotation=0&showTitle=false&size=62529&status=done&style=none&taskId=uf4a7f3ee-6520-405a-8cd3-c58c57a0935&title=)


- 对比上面的 V 1 版本我们可以发现，2，3，4 通道都添加了 1\*1 的[卷积层](../神经网络元素/卷积层.md)，这是为了减少参数。



![image.png](https://cdn.nlark.com/yuque/0/2022/png/33630082/1667606507643-e67dc7f7-98f8-4b3c-9c6d-32f735dc9549.png#averageHue=%23f4e2ce&clientId=uf32ab3e7-c0f4-4&from=paste&height=926&id=u89fbea64&originHeight=926&originWidth=1654&originalType=binary&ratio=1&rotation=0&showTitle=false&size=883019&status=done&style=none&taskId=u100aa310-c03c-47c7-9388-6f669853906&title=&width=1654)
## 3. 辅助分类器
### （1） 辅助分类器结构

![image.png](https://cdn.nlark.com/yuque/0/2022/png/33630082/1666779897245-c722eebd-79c7-43a8-a25c-cd3d98e41548.png#averageHue=%2393cdb0&clientId=ua8dfb534-11cc-4&from=paste&height=452&id=uaad64968&originHeight=452&originWidth=577&originalType=binary&ratio=1&rotation=0&showTitle=false&size=180872&status=done&style=none&taskId=uf7c3e258-47e5-43a5-857f-f491376952e&title=&width=577)



在训练模型时，将两个辅助分类器的损失乘以权重（论文中是0.3）加到网络的整体损失上，再进行反向传播。

### （2） 辅助分类器的两个分支有什么用呢？


- 作用一：可以把他看做inception网络中的一个小细节，它确保了即便是隐藏单元和中间层也参与了特征计算，他们也能预测图片的类别，他在inception网络中起到一种调整的效果，并且能防止网络发生过拟合。
- 作用二：给定深度相对较大的网络，有效传播梯度反向通过所有层的能力是一个问题。通过将辅助分类器添加到这些中间层，可以期望较低阶段分类器的判别力。在训练期间，它们的损失以折扣权重（辅助分类器损失的权重是 0.3）加到网络的整个损失上。


# Global Average Pooling
![image.png](https://cdn.nlark.com/yuque/0/2022/png/33630082/1666958583813-afafc68b-3193-4415-adf6-1c56ee1fcb4f.png#averageHue=%2385ad8d&clientId=u091443d4-58e6-4&from=paste&height=771&id=u1d88cff2&originHeight=771&originWidth=1651&originalType=binary&ratio=1&rotation=0&showTitle=false&size=593906&status=done&style=none&taskId=ua4cfc302-b682-458d-a016-b8bbb3d2c0a&title=&width=1651)



