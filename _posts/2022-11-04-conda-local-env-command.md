---
layout: post
title:  "Conda本地环境常用命令"
date:   2022-11-04 22:30:00
categories: coding4fun
tags: [python, anaconda]
---



查看conda命令帮助信息:
```shell
conda -h
```

安装numpy:
```shell
conda install numpy
```

创建、删除一个虚拟环境：
```shell
conda create --name python36  python=3.6
conda activate python36 
conda deactivate 
conda remove -n python36 --all (删除某个虚拟环境)
conda env remove  -n python36 (删除某个环境的所有包)
```

查看所有安装环境
```shell
conda info -e
```


查看某个指定环境的已安装包:
```shell
conda list -n python36
```

指定环境安装、删除package（如果不用-n指定环境名称，则被安装在当前活跃环境）:
```shell
conda install -n python36 numpy
conda remove -n python36 numpy
```

更新conda，更新anaconda
```shell
conda update conda
conda update anaconda
```

更新Python，假设当前python环境是3.6.1而最新版本是3.6.2，那么就会升级到3.6.2
```shell
conda update python
```

更新、删除package
```shell
conda update -n python36 numpy
conda update matplotlib
conda remove matplotlib
```


查看已安装的包
```shell
conda list 
```


进入对应的conda环境，然后使用pip install安装
```shell
conda activate python36
pip install tensorflow==1.14.0

```
直接用conda命令安装
```shell
conda install -n python36 tensorflow==1.14.0
```

另一种方法会快很多，安装时还可以指定镜像源，比如清华园镜像源，这个是更新比较快的源
```shell
pip install keras -i https://pypi.tuna.tsinghua.edu.cn/simple
```

