---
title: blog小白搭建手册--hexo
category: 前端
tags: hexo
---

![小白搭建手册](/img/01.jpg)

**前言：** 博主进行多方检索对比，发现目前博客平台有很多主要分为：社区类，个人类。

社区类主要有：CSDN，博客园，简书，码云这些托管平台，它们关注可以让笔者更好的关注与文章内容，但是这类平台具有对于文章内容进行限制并且会在个人页面上加上植入的各类广告，对于像博主这样的强逼症者，必须要让自己的页面保持简洁啦！:smiley:

所以更偏向于个人类博客：像WordPress,Zbolg，GitHub托管，像WordPress,Zbolg这类平台页面风格比较小清新，相对其他博客平台比较唯美，但是它们的搭建不仅需要耗费时间精力还必须耗费金钱去购买域名与服务器，还有定期维护，单就一个个人博客而言有过之而不及，综合以上考虑选择一款简洁，免费的平台，本文选择hexo主题，还有其他主题next，可自行搜索下载。





##### 1.0 主题 Hexo

[^_^]:  [snippet](https://github.com/shenliyang/hexo-theme-snippet#hexo-theme-snippet)

- [Hiero](https://github.com/iTimeTraveler/hexo-theme-hiero#hiero)
- [JSimple](https://github.com/tangkunyin/hexo-theme-jsimple#jsimple)
- [BlueLake](https://github.com/chaooo/hexo-theme-BlueLake#bluelake)



##### 1.1 Hexo搭建步骤

- 安装Git
- 安装Node.js
- 安装Hexo
- GitHub创建个人仓库
- 生成SSH添加到GitHub
- 对hexo进行页面设计排版
- 将hexo部署到GitHub
- 设置个人域名
- 发布





##### 2.0 安装Git

```cmake
git --version                         ##检查版本
```



##### 3.0 安装Nodejs

- 直接使用Git Bash执行命令



##### 4.0 安装Hexo

```cmake
npm install -g hexo-cli              ##安装hexo
```

- Step 1: 先在电脑盘符进行创建`your_name.github.io `  文件夹

- Step 2: 在终端切换到 `your_name.github.io` 所在文件夹路径

- Step 3: 由于默认的NPM镜像过慢，把源替换成淘宝的镜像，在终端执行命令

  ```cmake
  npm config set registry "https://registry.npm.taobao.org"   ##该切换是暂时的
  ```

- Step 4: 根据Hexo进行一键式建站

  ```cmake
  hexo init
  npm install
  ```

  `you_name.github.io` 会生成如下目录

  ```tex
  .
  ├── _config.yml  ##网站大部分配置信息
  ├── package.json ##插件信息
  ├── scaffolds  ##模板文件夹
  ├── source  
  |   └── _posts  ##用户提交的模板文件
  └── themes  ##主题文件夹
  ```

- Step 5：根据Hexo的官方文档进行下载hexo主题

  ```cmake
  hexo server                    ##开启hexo服务,输入localhost:4000可看到生成的博客
  ```



##### 5.0 GitHub创建个人仓库

​      **5.1：Creating a repository**

​              登录GitHub账户并创建一个名为`your_name.github.io` 的repository，==your_name==为你的账户名。

​     **5.2：Setting up Git**

​             告诉Git是谁提交的文件，及提交地址执行下列代码 

```cmake
git config --global user.name "your name"                   ##your name是自己取的名字
git config --global user.email "your email address"         ##是自己的邮箱
```

​            GitHub允许多人向一个Repo提交

​    **5.3：Authenticating with GitHub from Git**

​          根据GitHub的官方文档 [Generating a new SSH key](https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key) 执行下列代码

```cmake
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"       ##your_email@example.com是GitHub注册邮箱
```

​          然后进行下一步下一步。

5.4：将SSH key添加到ssh-agent









