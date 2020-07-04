---
title: hexo使用
date: 2020-07-05 01:33:04
tags:
---
# 初识Hexo

##### 创建我们的博客文件夹

```
Hexo init 文件夹
```

**安装发布工具**

```
npm install hexo-deployer-git --save
```

这个命令需要在博客文件夹内安装,所以如果你创建了新的博客文件夹,需要重新安装

**修改配置文件**

```
theme: landscape

deploy:

  type: git

  repository: 你的GitHub仓库地址

  branch: master
```

注意地址也使用git开头的SSH地址

**Hexo 提交**

Hexo的提交也分为三个命令：

```
hexo clean
这条命令的用途是清除缓存，能让新发布的博客能快速生效
hexo generate
这条命令的作用是生成新的静态文件,可以简写为 hexo g
hexo deploy
这条命令的作用是把生成的文件部署到我们的博客上，发布后，我们就可以看到我们的博客变成了这样：
```

**修改主题**

首先我们下载新的主题，一般来说这是一个git仓库，比如next的下载我们可以在博客根目录使用：

```
git clone https://github.com/iissnan/hexo-theme-next themes/next
这里https://github.com/iissnan/hexo-theme-next是该主题的仓库地址
```

themes/next 表示下载到根目录中的themes文件夹下，下载为next文件夹，注意前面有个空格和仓库地址分隔哦

出错：git设置问题


#  git分支及git ignore

### 分支(brancgh)的简单命令

**创建分支**

```
git branch dev
```

**切换到新的分支**

```
git checkout dev
```

 通常我们会把这两条命令合并使用 

```
git checkout -b dev
```

###  分支的应用 & git ignore 

**查看我们的gitignore文件**

> 用于排除不要提交的文件

```
.DS_Store
Thumbs.db
db.json
*.log
node_modules/
public/
.deploy*/
```

###  提交到新分支 

```
git init
    
git remote -v
    
git remote add origin git@github.com:zh767/zh767.github.io.git
    
git checkout -b dev
创建并切换dev分支
```

**提交三部曲**

```
git add -A
git commit -m "全部提交"
git push
```

