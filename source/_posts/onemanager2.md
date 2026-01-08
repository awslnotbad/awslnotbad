---
title: OneManager美化
tags: 网盘
date: 2021-08-28 12:41:38an
---

## 源仓库

https://github.com/qkqpttgf/OneManager-php

我的网盘：https://yun.awslnotbad.cn/

## 设置/美化

#### adminloginpage

自定义登录地址，设置后就会隐藏登录按钮(有些主题本来就没有登录按钮)，登录时需要手动在网盘地址后加上?你设置的值进行登录。
比如设置为cloud，那么你只能通过http://xxx.com/xxx?cloud地址来登录 。

#### background

填入一个 图片/api 的url地址
https://film.magenchun.cn/bing.php (每日必应)
https://api.ixiaowai.cn/api/api.php (二次元动漫)
http://www.dmoe.cc/random.php（二次元随机图）
https://api.ixiaowai.cn/mcapi/mcapi.php （menhera酱）
https://api.ixiaowai.cn/gqapi/gqapi.php （a风景）
https://acg.yanwz.cn/wallpaper/api.php（二次元随机图）

#### customCss

```
#自定义ccs，例如隐藏语言栏

<style>.changelanguage{display:none}</style>
```

#### customScript

```
#设置自定义js，会作用于所有页面。
#例如如设置http重定向到https：

<script type="text/javascript">
    var targetProtocol = "https:";
    if (window.location.protocol != targetProtocol)
        window.location.href = targetProtocol + window.location.href.substring(window.location.protocol.length);
</script>
```

#### disableChangeTheme

设置为1后游客将不显示右下角的主题切换功能

#### disableShowThumb

设置为1后将不显示缩略图的按钮和功能，对于云函数用户来说，建议设为1来关闭该功能，因为该功能可能点一下就是一分钱

#### hideFunctionalityFile

设置为1后，游客浏览网盘时就会看不到read.md，head.md，head.ofm，foo.omf这些文件

##### 设置顶部和底部说明文字

在需要展示顶部说明的目录下新建一个head.md文件，在文件里写入说明内容即可，这是一个markdown文件，可以使用markdown语言进行书写。
底部说明说明文字对应的是readme.md文件，规则与顶部文字一样。

##### 利用head.omf设置一言

head.omf作用和head.md一样，区别是他不支持markdonw语言，但是支持html语言，可以写入html、css、js内容

```
<p id="hitokoto">:D 获取中...</p>
<script>
    fetch('https://v1.hitokoto.cn')
        .then(response => response.json())
        .then(data => {
            const hitokoto = document.getElementById('hitokoto')
            hitokoto.innerText = data.hitokoto
        })
        .catch(console.error)
</script>
```

##### 利用foot.omf设置Valine评论

使用Valine需要先注册LeanCloud并实名认证，然后新建应用获取AppID和Key，不过这个实名认证比较繁琐

```
<script src='//unpkg.com/valine/dist/Valine.min.js'></script>
<div id="vcomments"></div>
<script>
    new Valine({
        el: '#vcomments',
        appId: '你获取的AppID',
        appKey: '你获取的AppKey'
    })
</script>
```

#### passfile

设置密码文件名，比如这里设置为password.txt，那么在某一个目录下新建一个password.txt文件，其中写入密码，这样任何人在浏览这个网盘目录时都需要输入相应密码后才能访问

#### domain_path

当绑定多个域名时，可以使不同域名打开时访问不同目录。当然如果你只有一个域名也可以用，通过这种方式可以使当前域名访问一个指定子目录，和后面的public_path起到一样的作用。
下面是两个域名的设置方法，中间用|隔开，如果有多个域名只设置一个域名时，未设置的域名好像也会只访问该目录，要访问根目录dirname设置为/。

```
domain1.com:/dir1name|domain2.com:/dir2name
```

#### downloadencrypt

设置为1时启用该功能，这样在设置了密码的目录下的文件虽然无法在网页端浏览，但可以通过具体的文件链接进行下载

#### public_path

设置该盘的显示的根目录，默认为/，换个说法就是可以显示指定的文件夹，默认显示全部。
比如我们只想将网盘下的public文件夹内容作为网盘，可以设置为/public/。
有了这个功能，即使只有一个onedrive账号，我们也可以通过重复绑定同一个账号来生成多盘，然后每个盘的public_path设置为不同的路径，这样可以将一个盘的功能分开。
例如有一种特殊情况是我既想让游客上传文件，又想让游客看见上传后的文件目录，目前就只能通过这种方法将该目录设置到两个盘，一个盘作上传，一个盘作目录展示。

### 进阶设置

#### 设置网站ico图标

将favicon.ico图片放在网盘根目录下，and新版的html主题只需要在绑定的第一个盘下面设置就行了

```
#当然我们也可以在customCss或customScript中进行全局设置

<link rel="icon" href="https://www.google.com/favicon.ico" type="image/x-icon">
```

#### 利用index.html设置自定义页面

如果一个目录下有名为index.html的文件，则直接显示该文件，可以利用这个功能设置一个自定义页面或者用于隐藏一个特定页面，相当于部署了一个静态页面



