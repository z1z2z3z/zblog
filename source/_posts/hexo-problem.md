---
layout: post
title: hexo部署遇到的问题
date: 2023-12-05 17:49:21
tags:
 - 问题
categories: 其他 
---
## 起因
  将之前的hexo文件移动到别的电脑上，然后运行`hexo`命令发现报错。
## 原因及解决
  是因为别的电脑没有安装对应版本的`hexo-cli`导致。因为我移到的电脑之前没有安装`hexo-cli`，当运行`npm i -g hexo-cli`命令时便会安装最新版，由此造成了版本问题。此时只需要安装正确版本或者删除`node_modules`文件和`package-lock.json`文件，更改package.json文件并重新安装对应的依赖