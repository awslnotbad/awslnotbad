---
title: Gridea静态博客教程
tags: 网站
categories: 网站
abbrlink: 30932
date: 2021-09-12 14:34:53
---

##### 前言

本文于2021.09.03在小黑盒发布：https://api.xiaoheihe.cn/v3/bbs/app/api/web/share?link_id=67733262

 先给大家简单的介绍一下吧，Gridea是一个静态博客写作客户端，相较于其他主流的静态博客，比如用hexo搭建的本站，它更简单更容易上手，只需要了解一点点Markdown的语法进行写作就可以，这就意味着哪怕是完全没有接触过这方面的人也能够在短短几分钟之内搭建一个自己的博客。
​ 那么下面就是具体操作的步骤！

##### 一、确定托管代码的平台

 Gridea是可以将博客部署到Github、Coding和自己的服务器上的。但是很明显，服务器要花钱，选择建静态博客的大部分人，还是因为不想花非刚需的钱去买主机或者服务器。而Coding新版也是要收费的，虽然也不贵而且还有六个月的试用期，但是想要用它的pages服务还需要实名认证，这也相对繁琐。因此我推荐将博客部署到github。往下的教程也是以Github为例。

##### 二、注册Github账号并创建仓库

###### 1、注册Github账号

如果你没有Github的账号，那么可以进入官网开始注册（注意一下用户名的填写，如果不使用自定义域名，用户名将会是你的Github分配给你的域名，比如你的用户名为xxx，那么你的域名会是xxx.github,io）。

```
Github官网：https://github.com 
```

###### 2、新建仓库

如图所示，点击右上角的“+”号，然后点击“New respository"即可。

![image-20210903104124892](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031041028.png)



###### 3、配置仓库

 这里推荐仓库名填写格式为：”用户名.github.io“。

 然后点击”Add a README file“，再点击”Create repository“即可。

![image-20210903111250432](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031112516.png)

###### 4、点击仓库的”Settings“，进入”pages“。

![image-20210903111403711](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031114786.png)![image-20210903111524299](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031115383.png)

 你就会看到你的域名已经正常显示出来了

![image-20210903111849347](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031118431.png)

##### 三、创建Github token

###### 1、developer settings

点击右上角头像的settings，选择菜单最下面的developer settings

![image-20210903112639601](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031126655.png)

![image-20210903112745508](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031127594.png)

###### 2、Generate new token

点击”Personal acces tokens“，再点击”Generate new token“。

![image-20210903112908952](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031129010.png)

###### 3、New personal access token

Note备注可以随便写，这里写个”Griddea“，然后选择”No expiration“，再把”repo“打上✓。

![image-20210903113217190](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031132269.png)

然后下拉页面，选择”Generate token“创建token。

![image-20210903113455025](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031134079.png)

###### 4、复制token

记得保存好，因为只显示一次，忘了又得重新申请。

![image-20210903113712997](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031137064.png)

##### 四、配置Gridea

准备工作都完成了接下来是配置Gridea。

Gridea官网： https://gridea.dev

###### 1、下载Gridea

进入官网，根据你的电脑系统下载好Gridea客户端，这里以windows为例。

![image-20210903114158437](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031141526.png)

你也可以直接在下方链接下载，因为在GIthub上下载是比较慢的。

推荐国内Gitee下载源：https://gitee.com/fehey/gridea/releases/v0.9.2

![image-20210903114657628](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031146684.png)

###### 2、配置Gridea

安装好后，打开Gridea的”远程“配置你的Github信息，然后保存，如下图。

![image-20210903123113415](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031231520.png)

然后点击左下角的检测远程链接，如果配置没问题，那就会显示远程连接成功。

如果连接失败，还请回到上述步骤自行检查。

![image-20210903123209137](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031232228.png)

###### 3、发布文章。

点击文章，点击右上角的”+“号即可。

![image-20210903120341495](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031203578.png)

编辑完成后，点击右上角保存即可。

![image-20210903120729462](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031207576.png)

###### 4、预览和同步

点击预览，本地预览后没问题即可点击”同步“推送至github。

![image-20210903120823099](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031208197.png)

当然，你还可以继续配置其他信息，比如自己的网站名字，头像，页脚，图标等等。

![image-20210903121615559](https://cdn.jsdelivr.net/gh/awslnotbad/picture@main/img/202109031216640.png)

由于篇幅原因在此不多做介绍，可以自行摸索~

###### END

