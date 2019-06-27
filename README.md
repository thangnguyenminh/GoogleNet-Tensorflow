# GoogLeNet-TensorFlow
TensorFlow implementation of GoogLeNet.

## Introduction
Focus on the structure of the project, The current code can be properly trained. Next I will continue to improve the readability of the code and the structure of the project will also improve the accuracy of the GoogLeNet network training.

## To-Do
This repository will use object-oriented programming as much as possible to make the machine learning code structure clearer. So far I have implemented data loader and processing configuration classes and implemented Inception v1 network class. In addition, the current code can be visualized using tensorboard.

- [x] data loader
- [x] config file
- [x] base network class
- [x] inception v1 network class
- [ ] inception v2 network class
- [ ] inception v3 network class
- [ ] inception v4 network class
- [x] tensorboard
- [ ] trainer
- [ ] better log
- [ ] improve the accuracy

## Usage

### Data
This repository will support data in a variety of formats.
Up to now it supports 102flowers dataset.

##### 102flowers
In order to ensure the correct training, please organize the structure of the data as follows.
```
data
├── flowers102
│   ├── imagelabels.csv
│   └── jpg
└── imagenet_models
    └── googlenet.npy

```
You can download the dataset from [here](http://www.robots.ox.ac.uk/~vgg/data/flowers/102/index.html).

### Training
All configuration of data and training can be modified in the file. Use the more readable yaml file format as the configuration file. 

For more details, please refer to `experiments/configs/inception_v1.yml`

Simply run this script:
```bash
python ./training.py
```
Recommend using python virtual environment to train.

### Reference
> Szegedy, C., Liu, W., Jia, Y., Sermanet, P., Reed, S., Anguelov, D., et al. (2014, September 17). Going Deeper with Convolutions. arXiv.org.

> Nilsback, M-E. and Zisserman, A.
> Automated flower classification over a large number of classes

### Images
#### example of data
|![](http://ww1.sinaimg.cn/thumbnail/006rfyOZgy1fpcpn6to9ij30ii0dwq54.jpg)|![](http://ww1.sinaimg.cn/thumbnail/006rfyOZgy1fpcpn6usntj30ij0dwgnp.jpg)|![](http://ww1.sinaimg.cn/thumbnail/006rfyOZgy1fpcppf8u16j30ku0dwq4y.jpg)|
|---|---|---|
#### loss and accuracy
![](http://ww1.sinaimg.cn/mw690/006rfyOZgy1fpcp7bei91j313k0f2775.jpg)
#### graph
Please note that the current Tensorboard shows Graph has been beautified, but it is implemented in other ways. Because of the lower version of TensorFlow, using variable_scope when loading pre-trained weights will result in duplicate variable_scope being created. If you need to beautify Graph, please select a version of `tensorflow >=1.5.0` and use `uxiliary_name_scope=False`

![](http://ww1.sinaimg.cn/mw690/006rfyOZgy1fpcp7f9av7j316n3zh4qp.jpg)
### Release
v0.1.1
# GoogleNet-Tensorflow
# GoogleNet-Tensorflow
