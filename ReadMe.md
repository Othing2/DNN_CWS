# 基于深度学习的中文分词

使用TensorFlow实现基于深度学习的中文分词

本项目使用`python3`编写，没有支持`python2`的计划。


## 使用方法

### 准备

1. 安装tensorflow：
```python
pip install tensorflow
```

2. clone本项目至本地

### 开始使用

在本项目文件夹下创建一个文件，在里面添加如下代码并运行：

```python
from seg_dnn import SegDNN
import constant

cws = SegDNN(constant.VOCAB_SIZE,50,constant.DNN_SKIP_WINDOW)
print(cws.seg('我爱北京天安门')[0])
```

详细示例可见文件`test.py`

## 相关代码文件说明

* `seg_dnn.py`: 使用（感知机式）神经网络进行中文分词
* `prepare_data.py`: 预处理语料库，包括msr和pku
* `init.py`: 用于生成进行训练和测试的数据的脚本文件

## 参考论文：

* [deep learning for chinese word segmentation and pos tagging](www.aclweb.org/anthology/D13-1061) （已完全实现）
* [Max-Margin Tensor Neural Network for Chinese Word Segmentation](www.aclweb.org/anthology/P14-1028) （正在实现）

## Todo List

-[ ] 支持`pip`