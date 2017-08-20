# SURF2017
-----------------
This is a project of XJTLU 2017 Summer Undergraduate Research Fellowship, it aims at designing a generative adversarial network to implement style transfer from a style image to content image. Related literature could be viewed from [Wiki](https://github.com/LinkWoong/SURF2017/wiki)  
## 1. Overview  
-----------------
**Neural Style Transfer** is one of the cutting-edge topic in deep learning field. It aims at transfer the style of an image to content image, which could be sketch or colored. 

Our goal is to implement the neural style transfer by using [cycleGAN](https://arxiv.org/abs/1705.09966). At the same time, we also want to take one step further by using [CAN](https://arxiv.org/abs/1706.07068), which could generate image itself after a well-feed training process.

## 2. Framework   

### acGAN

Auxiliary conditional GAN network is used with **residual U-net** with two **guided decoders** on generator side. The discriminator consists of deConvNets, which minimize the difference the generated image with ground-truth.

### VGG-19 Pretrained Very Deep Network

This file is essential for the network, the download link could be viewed from [here](https://doc-0g-bk-docs.googleusercontent.com/docs/securesc/2pupit1rkqf499jf32djila3bu315tct/gf720g6apmvbsffanaqje3urb3gae67s/1499508000000/13951467387256278872/05183618345913443837/0Bz7KyqmuGsilZ2RVeVhKY0FyRmc?e=download).The VGG19 is a pretrained very deep ConvNets that could be used directly. Similar pretrained models such as Resnet, VGG16 will be tested.

### Resnet

A profound and very laconic architecture, the origin paper could be viewed [here](https://arxiv.org/abs/1512.03385)).
## 3. Some trials  
-------------------------------------------------
+ The first trial is using traditional neural style transfer.

<br>
<img src="https://raw.githubusercontent.com/LinkWoong/SURF2017/master/acGAN-Implementation/school/xjtlu.jpg" height=500 width=98% alt="Input test image"> 
<img src="https://raw.githubusercontent.com/LinkWoong/SURF2017/master/acGAN-Implementation/school/new_school.jpg" height=500 width=98% alt="Output test image">
<br>
  
+ There are more results have released by using Keras framework, please see this [link](http://stellarcoder.com/surf/anime_test_2/) created by DexHunter. The network is trained on Professor Flemming 's workstation with 4 Titan X GPUs, which cost 2 weeks to implement.
