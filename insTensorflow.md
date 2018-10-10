# Tensorflow的安装
---

## 在windows上安装Tensorflow：https://www.tensorflow.org/install/install_windows?hl=zh-cn

1. 版本选择

    仅支持CPU的Tensorflow更容易安装

2. 安装方法：原生pip和Anaconda

3. 使用Anaconda安装Tensorflow

  打开Anaconda中的命令行

  创建名为tensorflow的conda环境

  > C:> conda create -n tensorflow pip python=3.5

  激活conda环境

  > C:>activate Tensorflow的安装

  安装仅支持CPU的版本

  > (tensorflow)C:> pip install --ignore-installed --upgrade Tensorflow的安装

  安装验证

  > import tensorflow as tf
