---
title: OneManager
tags: 网盘
date: 2021-04-30 12:41:38
---

实现目的：利用onemanager托管到Glitch（免费）可实现挂载多个网盘，通过网站直接去访问网盘的文件,可以实现直链下载，网页在线观看视频等功能。

目前支持的网盘有：onedrive/onedriveCN、阿里云盘、谷歌云等。

项目地址：https://github.com/qkqpttgf/OneManager-php

我的网盘：https://yun.awslnotbad.cn/

下面是具体的步骤：



一、以github账号登陆Glitch

Glitch官网： https://glitch.com/

登陆方式选择github账号登陆

<img src="https://pic.imgdb.cn/item/639edec3b1fccdcd36705a8d.jpg" alt="image-20220430171546539" style="zoom:50%;" />

二、新建项目

1、登陆后，点击右上角的 “New project” 创建项目。

<img src="https://pic.imgdb.cn/item/639edf3cb1fccdcd367134c7.jpg" alt="image-20220430171725438" style="zoom:50%;" />

2、创建方式选择从github中导入，点击 “Import from GitHub”。

添加链接  https://github.com/qkqpttgf/OneManager-php

点击确定。

<img src="https://pic.imgdb.cn/item/639edf50b1fccdcd36714d77.jpg" alt="image-20220430171808146" style="zoom:67%;" />

<img src="https://pic.imgdb.cn/item/639edf6cb1fccdcd36716fbc.jpg" alt="image-20220430171917654" style="zoom: 67%;" />



3、等待项目构建完成

这是完成后的截图

<img src="https://pic.imgdb.cn/item/639edf85b1fccdcd36719308.jpg" alt="image-20220430172122470" style="zoom:67%;" />

4、点击页面下方的PREVIER-Preview in a new window，在新窗打开预览

预览的这个链接就是你的网盘链接

<img src="https://pic.imgdb.cn/item/639edfc0b1fccdcd3671e03c.jpg" alt="image-20220430172244316" style="zoom:67%;" />





<img src="https://pic.imgdb.cn/item/639edfdab1fccdcd36720400.jpg" alt="image-20220430183028348" style="zoom:67%;" />

5、配置网盘

以阿里云盘为例，点击开始安装程序

<img src="https://pic.imgdb.cn/item/639edff0b1fccdcd3672219a.jpg" alt="image-20220430172412147" style="zoom:50%;" />

语言选择简体中文。

<img src="https://pic.imgdb.cn/item/639ee006b1fccdcd36724ce2.jpg" alt="image-20220430172446744" style="zoom:50%;" />

<img src="https://pic.imgdb.cn/item/639ee018b1fccdcd36726642.jpg" alt="image-20220430172519060" style="zoom:50%;" />

管理密码很重要，请牢记。

<img src="https://pic.imgdb.cn/item/639ee02bb1fccdcd36728258.jpg" alt="image-20220430172559907" style="zoom:50%;" />

<img src="https://pic.imgdb.cn/item/639ee03db1fccdcd36729d11.jpg" alt="image-20220430172638040" style="zoom:50%;" />

然后登录，点击管理-设置。

选择你所需要添加的网盘，点击添加盘

<img src="https://pic.imgdb.cn/item/639ee067b1fccdcd3672da16.jpg" alt="image-20220430172918336" style="zoom: 67%;" />

填写任意名称

<img src="https://pic.imgdb.cn/item/639ee092b1fccdcd36732380.jpg" alt="image-20220430173057862" style="zoom:67%;" />



这时，需要添加你的网盘refresh token

<img src="https://pic.imgdb.cn/item/639ee0a3b1fccdcd36733c70.jpg" alt="image-20220430175129526" style="zoom:67%;" />

获取refresh_token方式如下

<img src="https://pic.imgdb.cn/item/639ee0b8b1fccdcd367357f0.jpg" alt="image-20220430175027187" style="zoom: 50%;" />



复制填入token,然后确认

根据自己的需求，选择空间，这里选择普通空间

<img src="https://pic.imgdb.cn/item/639ee0cdb1fccdcd367379eb.jpg" alt="image-20220430175216549" style="zoom:50%;" />

至此，利用onemanager挂载一个网盘已经完成。

后续还可以在设置中配置相关的内容，达到美化的效果

<img src="https://pic.imgdb.cn/item/639ee0e1b1fccdcd36739a13.jpg" alt="image-20220430183721608" style="zoom:67%;" />

以下为我搭建好的网盘，设置了主题，动态/随机背景，评论，引入一言，添加多个网盘等。

<img src="https://pic.imgdb.cn/item/639ee0f5b1fccdcd3673bd3d.jpg" alt="image-20220430181019466" style="zoom:67%;" />



<img src="https://pic.imgdb.cn/item/639ee10cb1fccdcd3673e20a.jpg" alt="image-20220430180802238" style="zoom:67%;" />

赶紧去试试吧！
