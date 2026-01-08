---
title: 易班自动打卡
tags:
  - 黑科技
abbrlink: 4696
date: 2021-01-08 15:43:43
---

项目地址：[蓝奏云链接](https://gqxi.lanzous.com/iQSeok60sqf)

解压下载的源程序，

找到目录中的main.py文件，

##### 修改信息

![截图_20215019125054](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/%E6%88%AA%E5%9B%BE_20215019125054.png)

修改完成后

##### 创建虚拟环境

###### #1创建虚拟环境

```shell
python3 -m venv venv
```

###### #2安装必要依赖

```shell
pip3 install -r requirements.txt -i https://pypi.douban.com/simple
```

###### #3启动打卡

```
python3 main.py
```

###### 打卡成功

![](https://pic.imgdb.cn/item/639d832db1fccdcd363c7c64.png)

###### 这里并没有实现全自动化定点打卡

如果想这样做的话，

可以买个服务器或者电脑不关机挂着程序，

然后再设计定点运行程序。

