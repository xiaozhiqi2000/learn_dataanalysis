# 今天主要内容
1. [Anaconda]()

参考：
[官网地址](https://www.anaconda.com) 

[anaconda安装](https://www.zhihu.com/question/58033789})

[anaconda下载页面](https://www.anaconda.com/distribution/)


## 一、Anaconda 概述
### 1.Anaconda是什么？
Anaconda在英文中是“蟒蛇”，麻辣鸡（Nicki Minaj妮琪·米娜）有首歌就叫《Anaconda》，表示像蟒蛇一样性感妖娆的身体。

Anaconda 解决了官方 PYthon的两大痛点：
- 提供了包管理功能，Windows平台安装第三方包经常失败的场景得以解决
- 第二：提供环境管理的功能，功能类似Virtualenv，解决了多版本Python并存、切换的问题

### 2.为什么需要Anaconda
- 1）Anaconda 附带了一大批常用数据科学包，它附带了 conda、Python 和 150 多个科学包及其依赖项。因此你可以立即开始处理数据。
- 2）管理包Anaconda 是在 conda（一个包管理器和环境管理器）上发展出来的。在数据分析中，你会用到很多第三方的包，而conda（包管理器）可以很好的帮助你在计算机上安装和管理这些包，包括安装、卸载和更新包。
- 3）管理环境为什么需要管理环境呢？比如你在A项目中用了 Python 2，而新的项目B老大要求使用Python 3，而同时安装两个Python版本可能会造成许多混乱和错误。这时候 conda就可以帮助你为不同的项目建立不同的运行环境。还有很多项目使用的包版本不同，比如不同的pandas版本，不可能同时安装两个 Numpy 版本，你要做的应该是，为每个 Numpy 版本创建一个环境，然后项目的对应环境中工作。这时候conda就可以帮你做到。

### 3. 如何安装Anaconda？

如果你是windows 10系统，注意在安装Anaconda软件的时候，右击安装软件→选择以管理员的身份运行。

如果安装后，在Anaconda Prompt中都无法使用Conda命令，解决方法在这里：
https://zhuanlan.zhihu.com/p/34337889

```
conda list
conda upgrade --all
conda install pandas numpy  
conda install numpy=1.10
conda remove pandas3
conda upgrade numpy
conda search numpy
```

### 4.如何管理环境？
#### 安装nb_conda用于notebook自动关联nb_conda的环境
```
conda install nb_conda
```
#### conda 可以为你不同的项目建立不同的运行环境。
```
conda create -n env_name package_names

conda create -n py3 pandas
conda create -n py36 python=3.6.3
```
- env_name 是设置环境的名称
- -n 是指该命令后面的env_name是你要创建环境的名称
- package_names 是你要安装在创建环境中的包名称。

#### 进入环境
```
activeate env_name
```
#### 离开环境
```
deactivate
```
### 5.进入jupyter notebook
```
jupyter notebook
```
#### jupyter notebook 快捷键
```
a 向前插入cell
b 向后插入cell
x 删除cell
m cell切换成mardown
y 切换成code
tab 自动补全
shift+enter 执行cell
shift+tab 弹出帮助文档
```
#### 指令
```
%run 执行外部的源文件 %run test.py
%time   计算他右边的代码的运行时长
%%time  计算代码块的执行时间
```
