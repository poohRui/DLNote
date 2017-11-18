# 基于Virtualenv安装

> 其他安装方法和具体安装细节参考[官方文档](http://www.tensorfly.cn/tfdoc/get_started/os_setup.html)，文章的安装步骤基于Mac OS系统，建议在Virtualenv环境下安装，其实就是新建了一个干净的python环境，可以减少不必要的错误

## 环境配置

* python3.5

* 与python版本对应的pip

* virtualenv

  用`pip`安装`virtualenv`

  ```
  sudo pip3 install --upgrade virtualenv 
  ```

  建立一个全新的 virtualenv 环境（一定要注意python版本）

  ````
  virtualenv --system-site-packages -p python3 ~/tensorflow
  ````

  激活virtualenv

  ```
  source bin/activate  # 如果使用 bash
  ```

* TensorFlow

  在 virtualenv 内, 安装 TensorFlow

  ```
  (tensorflow)$ sudo pip install --upgrade tensorflow
  ```

  检验

  ```
  在virtualenv下使用import tensorflow检验，不报错即可。
  ```

## 前方有坑

* python版本一定要对应

* 在安装TensorFlow时，如果使用pip总出现`Read timed out`超时错误，建议去google搜索对应的`tensorflow`的`.whl`文件，下载下来，直接使用

  ```
  (tensorflow)$ sudo pip install --upgrade XXX.whl
  ```

  安装即可，速度有很大提升。