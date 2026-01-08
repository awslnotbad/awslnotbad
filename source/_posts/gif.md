---
title: B站如何更换动态头像
tags: 哔哩哔哩
abbrlink: 30932
date: 2020-06-27 15:49:53
---

首先准备一个180*180大小的GIF图片。
然后通过 `https://www.upyun.com/webp` 上传保存好webp格式。
将下面的代码复制到浏览器书签里面

```
javascript:void (()=>{var a=document.createElement("input");a.type="file";a.onchange=function(){if(a.files.length>0){var b=new FormData();b.append("dopost","save");b.append("Displayrank","10000");b.append("face",a.files[0]);var c=new XMLHttpRequest();c.withCredentials=!!1;c.open("POST","https://api.bilibili.com/x/member/web/face/update?csrf="+document.cookie.match(/bili_jct=(.+?);/)[1]);c.onload=function(){var d=c.response;try{d=JSON.parse(d);switch(d.code){case 0:alert("更新成功，刷新页面即可");break;case 40012:alert("头像格式错误");break;case 40013:alert("头像大小不能超过2M");break;default:alert("未知返回"+c.response);console.error(c.response, c);break}}catch(e){console.error(e, c, d);alert("解析返回数据时出现错误，具体看console")}};c.onerror=function(e){console.error(e,c);alert("请求出现错误，具体看console");};c.send(b)}else{alert("请选择一个文件")}};a.click();})()
```

然后打开B站更换头像的网页，点击书签，选择转好的webp格式图片，然后点击提交，上传成功，刷新网页即可查看效果。

![](https://pic.imgdb.cn/item/5f4fbc31160a154a67fe6108.gif)

目前此方法已失效[doge]

