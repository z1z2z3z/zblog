---
layout: post
title: git-used
date: 2023-12-05 19:28:20
tags:
 - git
categories: git 
---
1. 创建远程仓库
  
  - 创建文件夹 ``` mkdir test cd test ```
    
  - 然后创建仓库 ```git --bare init```
    
  - 然后本地创建文件夹 ```git init ``` 随便在文件夹里创建个文件(`Readme.md`)
    
  - 本地`git add .` `git commit -m 'first'`
    
  - 连接远程 `git remote add origin(名字,一般为origin) (url)ssh:test@ip/home/.../test`
    
  - 拉取远程`git pull origin`
    
  - 把刚才本地仓库同步给远程仓库`git push origin master`（主支）
    
    2. 创建远程分支（分支名为`dev`）
    
    - 本地创建并跳转分支 `git checkout -b dev`相当于`git branch dev 和 git checkout dev`
    - 关联远程分支 `git push -u origin dev`相当于`git push origin dev 和 git branch --set-upstream origin dev`
2. 一些基本操作
  
  - 查看所有远程和本地分支`git branch` -a
  - 删除分支`git branch -D dev`
  - 创建本地分支`git branch dev`
  - 分支跳转`git checkout dev`
  - 查看当前分支状态`git status`
  - 查看提交次数`git commit .`
  - ............. [参考链接](https://juejin.cn/post/6844903586120335367)

```bash
# 切换到目标分支
git checkout master

# 合并 feature 分支到 master
git merge feature

# 合并并指定合并提交消息
git merge -m "Merge feature branch" feature

# Fast-Forward 合并
git merge --ff-only feature
```