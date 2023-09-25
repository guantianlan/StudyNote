# ResNet——Deep Residual Learning for Image Recognition
#深度学习 

# 一、网络深度
- 网络的深度对于一个模型是十分重要的。当网络的层数增加了，网络可以进行更加复杂度特征模式的提取，所以当模型更深的时候，理论上可以取得更好的结果。
- 但事实却并非如此。实验发现，深度网络出现了退化现象，下图我们可以看出，实验结果并没有出现我们预想中，越深的网络他的效果越好，反而56层网络比20层的网络错误率要高。很明显，这不是过拟合的问题，因为56层网络在训练中的错误率同样要比20层的网络错误率要高。这是梯度消失问题。
- ResNet 提出了残差模型，在一定程度上解决了梯度消失的问题 ![[GoogleNet#^9a807f]] 

![v2-dcf5688dad675cbe8fb8be243af5e1fd_r.png](https://cdn.nlark.com/yuque/0/2022/png/33630082/1667504577951-97989602-1ea7-4359-a79c-85c988e672ce.png#averageHue=%23fcfafa&clientId=uf7179cfb-ee0a-4&from=drop&id=udaa012a5&originHeight=197&originWidth=602&originalType=binary&ratio=1&rotation=0&showTitle=false&size=36323&status=done&style=none&taskId=u7bad704d-5f30-467a-9330-c6279ad3e60&title=)
# 二、残差模型
![20190731144208639.png](https://cdn.nlark.com/yuque/0/2022/png/33630082/1667505248487-318b21f7-bd6d-4fd0-8e87-2643e4afcc4d.png#averageHue=%23f1f1f1&clientId=uecdc7be4-0123-4&from=drop&id=ub67e38d1&originHeight=463&originWidth=876&originalType=binary&ratio=1&rotation=0&showTitle=false&size=85708&status=done&style=none&taskId=ud81aef27-376f-49de-95db-c1be67ada51&title=)

- 当输入为x时，其学习到的特征应该为H(x)，但现在我不直接学得H(x)而是学得一个F(x)，这个F(x)=H(x)-x，也就是H(x)和x的残差
# 三、网络结构
![v2-7cb9c03871ab1faa7ca23199ac403bd9_720w.webp](https://cdn.nlark.com/yuque/0/2022/webp/33630082/1667507819528-9158f258-79e6-4f34-935e-f7a6fa8eaef3.webp#averageHue=%23d4d1cb&clientId=uecdc7be4-0123-4&from=drop&id=u4c9c3709&originHeight=1077&originWidth=469&originalType=binary&ratio=1&rotation=0&showTitle=false&size=55058&status=done&style=none&taskId=u7ba53d1d-d066-47e7-8e43-678866aee73&title=)

- ResNet 网络是参考了 [[VGG]] 19网络，在其基础上进行了修改，并通过短路机制加入了残差单元，如图所示。变化主要体现在 ResNet 直接使用 stride=2的卷积做下采样，并且用 global average pool 层替换了全连接层。
- 如是将通道数翻倍，如下图所示：

![20190731144535537.png](https://cdn.nlark.com/yuque/0/2022/png/33630082/1667507702804-e1a8227d-ea91-4bd2-b62b-b216b6bd523c.png#averageHue=%23dce1d1&clientId=uecdc7be4-0123-4&from=drop&id=u12e4d207&originHeight=679&originWidth=656&originalType=binary&ratio=1&rotation=0&showTitle=false&size=136802&status=done&style=none&taskId=u59585557-e472-43cb-9022-3a4006b8e72&title=)

- 由上图，我们可以清楚的看到“实线”和“虚线”两种连接方式。
- 实线的Connection部分 (第一个粉色矩形和第三个粉色矩形) 都是执行3x3x64的卷积，他们的channel个数一致，所以采用计算方式：Y = F(x) + x。
- 虚线的Connection部分 (第一个绿色矩形和第三个绿色矩形) 分别是3x3x64和3x3x128的卷积操作，他们的channel个数不同(64和128)，他们的维度也就不一样。
- 当维度不一致时（对应的是维度增加一倍），这就不能直接相加。有两种策略：（1）在输入和输出上添加一些额外的零，使得输入和输出的维度相同；（2）采用1x1的卷积进行升维，在ResNet里，输出通道翻了两倍，那么输入的高和宽通常会被减半，在进行1x1卷积的时候也会用到步幅为2。

![v2-1dfd4022d4be28392ff44c49d6b4ed94_720w.webp](https://cdn.nlark.com/yuque/0/2022/webp/33630082/1667508102373-7126ce89-1721-4630-bab3-ab939c734f7e.webp#averageHue=%23ececec&clientId=uecdc7be4-0123-4&from=drop&id=ue749f2b8&originHeight=242&originWidth=554&originalType=binary&ratio=1&rotation=0&showTitle=false&size=21910&status=done&style=none&taskId=ubd40e2ce-0d36-417f-a042-ef77981939f&title=)
# 四、两种残差单元

![v2-0892e5423616c30f69ded61111b111c0_720w.png](https://cdn.nlark.com/yuque/0/2022/png/33630082/1667508171362-ff20ec70-32eb-4ff3-bf4d-bbb8b7dfae3e.png#averageHue=%23f3f3f3&clientId=uecdc7be4-0123-4&from=drop&id=u41a96f35&originHeight=203&originWidth=566&originalType=binary&ratio=1&rotation=0&showTitle=false&size=22922&status=done&style=none&taskId=u97932d9a-59d3-4e7c-81ea-6dffa4e36a0&title=)

- 如图所示，ResNet采用了两种残差单元
- 左图对应的是浅层网络，而右图对应的是深层网络。对于短路连接，当输入和输出维度一致时，可以直接将输入加到输出上。
