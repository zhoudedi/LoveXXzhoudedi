# LoveXXzhoudedi

## 插件简介

LoveXXzhoudedi是一款Typecho邮件通知类插件这个插件专门为了Typecho主题：【[Brave—勇敢爱💕](https://blog.zwying.com/archives/59.html)】设计，支持SMTP、Send Cloud、阿里云邮件推送三种邮件通知方式。
在用户发布祝福时回复感谢，祝福审核通过后告知用户、还有用户忘记密码邮箱通知对不同场景进行对用户的不同邮件通知。


## 体验插件地址【[点击跳转](https://www.lvxin.xn--6qq986b3xl/)】效果图:
###  1. 用户发布祝福后收到的邮件效果图：

>![用户发布祝福后收到的邮件](https://images.gitee.com/uploads/images/2021/0522/182705_83aa88f6_8758841.jpeg "IMG_20210522_181250.jpg")
###  2. 用户祝福审核通过后收到的邮件效果图：

>![用户祝福审核通过后收到的邮件](https://images.gitee.com/uploads/images/2021/0522/182738_c5705375_8758841.jpeg "IMG_20210522_181348.jpg")
###  3. 用户祝福被回复后收到的邮件效果图：

>![用户祝福被回复后收到的邮件](https://images.gitee.com/uploads/images/2021/0522/182902_67c40f3c_8758841.jpeg "IMG_20210522_182130.jpg")
###  4. 用户登入页点击忘记后收到的邮件效果图：

>![用户登入页点击忘记后收到的邮件](https://images.gitee.com/uploads/images/2021/0522/182922_b7dae14a_8758841.jpeg "IMG_20210522_181447.jpg")
## 安装方法

> 1. 至[LoveXXzhoudedi](https://gitee.com/LinkXiaoZhou/LoveXXzhoudedi)中下载最新版本插件；
> 2. 将下载的压缩包进行解压并上传至`Typecho`插件目录中，注意目录名称更改为`LoveXXzhoudedi`；
> 3. 后台激活插件；
> 4. 根据自己的实际情况选择邮件发送接口方式；
> 5. 根据所选的邮件发送接口，配置相应接口参数。

## 自定义模板说明

插件共有三个模板，保存在插件`theme`目录下，分别为：

> 1. approved.html：祝福审核通过通知模板。
> 2. author.html：用户祝福通知用户收到祝福模板。
> 3. reply.html：祝福回复通知被回复者模板。

三个模板使用变量作为内容替换，您只需在自己的模板中增加相应的模板变量即可，模板变量列表如下：

### approved.html

> 1. {blogUrl}：博客地址
> 2. {blogName}：博客名称
> 3. {author}：祝福者名称
> 4. {permalink}：文章链接
> 5. {title}：文章标题
> 6. {text}：祝福内容

### author.html

author.html内变量与approved.html内变量一致。

### reply.html

> 1. {blogUrl}：博客地址
> 2. {blogName}：博客名称
> 3. {author}：被回复者名称
> 4. {permalink}：文章链接
> 5. {title}：文章标题
> 6. {text}：被回复者祝福内容
> 7. {replyAuthor}：回复者名称
> 8. {replyText}：回复内容

## 更新日志

### 2021.05.21

> 1. 新增异步回调邮件发送模式，仅在Typecho版本大于1.1/17.10.30时使用
> 2. 新增配置验证模式，Send Cloud验证API USER及API KEY正确性，SMTP验证登录正确性，阿里云仅验证是否填写
> 3. 与LoveKKForget插件合并，可自由开启
> 4. 去除新版本检测功能，请使用[[TeStore](http://www.yzmb.me/archives/net/testore-for-typecho)]进行版本检测

**修复**
> 用户发布祝福后会收到邮件给用户而不在是发给作者，这样起到邮箱通知提示用户方便用户想起自己博客，降低被遗忘。

### 2021.05.20
> 本插件由[[lovexiaozhou](https://gitee.com/LinkXiaoZhou/lovexiaozhou)]美化更改而得[[LoveXXzhoudedi](https://gitee.com/LinkXiaoZhou/LoveXXzhoudedi)]

> 增加用户发布祝福、祝福审核通过、祝福被回复、忘记密码功能（用户发布祝福、祝福审核通过、祝福被回复、提交忘记密码后会自动发送邮件通知用户）
