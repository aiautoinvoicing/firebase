永久免费！零成本部署Firebase谷歌云主机，附带CDN和SSL证书
2025-06-18 07:30·海阳顶端
Firebase 是谷歌提供的一个一站式云端开发平台，专门帮助开发者快速构建和运营 App 或网站。简单讲，就是几条命令，就可以搭建一个网站或APP。


图1

部署过程步骤如下（前提你要能打开Google网站）：

一、
https://console.firebase.google.com/注册，并建立一个项目。

如下图2所示，我已经建立了一个lily110的项目。这个步骤很简单。


图2

二、本机安装 Node.js（含 npm）。

打开浏览器访问：https://nodejs.org/。
点击下载 LTS安装包（推荐稳定性较好）。
安装完成后，打开 命令提示符（CMD） 或 PowerShell，验证是否安装成功：
node -v
npm -v



图3

三、安装 Firebase CLI 工具

继续在 CMD 或 PowerShell 执行在命令行下执行：

npm install -g firebase-tools
装好之后查看版本：

firebase --version



图4

四、开始部署

1、命令行下登陆控制台：firebase login --no-localhost。它会在命令行下出现一个网址，让你访问后得到验证码。浏览器打开网址，复制验证码填写到命令行下。验证码是很长的那一串。要注意不是图5的，是图6的。




图6


图6

2、初始化项目，命令行执行：firebase init hosting。它会自动在当前目录建立一个public文件夹，里边有一个index.html文件。你可以修改这个index.html文件内容，也可以在同目录下增加文件。

3、部署项目，命令行执行：firebase deploy --only hosting。部署完毕之后，会自动给你一个网址。


图8

在部署整个项目，需要你能够访问Google。部署完毕就不需要了。像我的网址是https://lily110.web.app/，不需要代理就能打开了。我这个网址有兴趣你可以看下，就写了一句话。

你以后只需要在public文件夹里放文件或编辑文件就可以，更新时执行firebase deploy --only hosting一条命令就可以了。