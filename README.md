# longqc image file for chinese
LongQC 是一个用于三代测序数据质控的软件。作者在其[github](https://github.com/yfukasawa/LongQC)上提供了两种安装方法：conda安装和docker image安装。但是无论哪种安装方式都有问题
  1. conda安装时会有一个[特定的bug](https://github.com/yfukasawa/LongQC/issues/37)，导致软件不可用。
  2. docker安装会因为docker源和conda libmamba-solver 依赖问题导致安装失败

# 我修改了作者提供的docker image file 解决了docker安装的问题，2024年12月在ubuntu 20.04LTS 上测试可以通过docker安装运行
下载这个dockerfile，然后使用以下命令安装：
> docker build -t longqc .
