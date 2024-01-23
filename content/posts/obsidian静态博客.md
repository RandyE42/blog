---
title: Obsidian+Hugo+Cloudflare Pages搭建静态博客
date: 2023-12-12T17:24:18+08:00
draft: false
layout: posts
tags:
  - obsidian
  - hugo
  - 静态博客
---

今年开始使用obsidian做知识库管理和笔记，也重新开始写博客。于是想要也用obsidian来写，那么同样支持markdown格式的静态博客方案就非常适合了。

整个方案的流程如下：
1. obsidian 创建文章并写作。
2. 利用 obsidian-git 插件将文件自动同步到 github。
3. cloudflare 自动拉取 github 仓库，并自动构建为 hugo 项目。
搭建记录如下：
<!--more-->

### 安装Hugo

macos下安装hugo：
```sh
brew install hugo #使用homebrew命令安装
```

新建博客站点目录：
```
hugo new site _path/to/blog
```

新建hugo站点后需要先设置主题才可预览
```
cd _path/to/blog
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
echo "theme = 'ananke'" >> hugo.toml
hugo server
```
主题可以任意选择自己喜欢的下载到theme目录即可


### 使用Obsidian进行写作
Obsidian新建仓库，选择打开刚刚建立的Hugo本地仓库目录

![](39d40c81ff5af31505db50a3ee0fe563_MD5.jpeg)
![](39d40c81ff5af31505db50a3ee0fe563_MD5.jpeg)


### 同步Github仓库



## Cloudflare Pages自动构建静态博客
