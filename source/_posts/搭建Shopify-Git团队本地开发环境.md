---
title: 搭建Shopify+Git团队本地开发环境
date: 2017-11-14 20:40:19
tags: [Hexo,Shopify,Git]
comments: true
---
使用`Shopify`开发商城项目，在人少的时候可以直接在线编辑，随便没有历史但是还是能接受的，但是如果团队开发的话就必须配备`CVS`了，但是如果继续使用在线的编辑方式结合`Git`使用那成本实在太高了。如下是构建本地开发环境的步骤。
## 安装Theme工具包
如果是`*nix`用户直接使用如下命令安装：
```sh
curl -s https://raw.githubusercontent.com/Shopify/themekit/master/scripts/install | sudo python
```
或者使用`Homebrew`安装
```sh
brew tap shopify/shopify
brew install themekit
```
## 创建API并获取Key
![image](https://shopify.github.io/themekit/assets/images/shopify-local-theme-development-generate-api.gif)

## 关联theme
### 创建git仓库并clone到本地
```sh
git clone shopify-theme@gitlab.com
```
### 进入目录并关联`theme`
通过如下图片寻找`ID`，然后关联到项目
![image](https://shopify.github.io/themekit/assets/images/shopify-local-theme-development-theme-id.gif)
```
cd shopify-theme
theme configure --password=[your-password] --store=[you-store.myshopify.com] --themeid=[your-theme-id]
theme download
```

## 实时更新
运行如下命令实时同步修改的文件到远端
```
theme watch
```
这时候因为你已经关联了自己的`theme_id`，所以需要在`https://username.myshopify.com/admin/themes`页面点击`preview`实时查看自己的更新内容。如果需要修改`theme_id`等信息可以去根目录的`config.yml`文件修改。

## 团队协作
- 每一个`team member`在`Shopify`控制台创建一个属于自己的`theme`，同时在`Git`创建一个自己的开发分支。  
- 开发过程中，每一个开发人员在自己的`Git`分支开发和`Theme`版本预览。
- 开发完成之后合并`dev`分支代码在自己的`Theme`版本预览，测试没有问题，提交`Merge Request`到`dev`分支。
- 在`Shopify`控制台创建`Feature`名称的`Theme`，与`dev`分支绑定。测试没有问题点击`Publish`。
