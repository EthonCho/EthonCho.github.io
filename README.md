# Hexo+GitHub
Hexo建置與配置檔介紹+GitHub配置

## 前置安裝
```
Hexo 指令都透過npm執行，須安裝 Node.js
```
* [Node.js](https://nodejs.org/en/) 需到官網下載安裝

## Hexo建置步驟
```
1.安裝 Hexo Git
$ npm install hexo-deployer-git --save

2.安裝 Hexo(使用 npm 來安裝 hexo) 
$ npm install hexo-cli -g

3.安裝成功後，輸入以下指令可查看版本
$ hexo version

4.初始化我們的部落格了
$ hexo init blog  
$ cd blog      
$ npm install
```
## Hexo 配置檔介紹
_config.yml 是 hexo 的預設設定檔，其設定是用 "yaml" 格式編寫。
ex: yaml 檔裡，”:”後一定要有一個空格
```
# Site
title: /標題(會顯示在網頁標題與頁首)/
subtitle: /子標題(顯示在頁首)/
description: /內容描述(給搜尋引擎看的)/
author: /作者(顯示在頁尾)/
language: /網站預設語言(台灣:zh-tw)/
timezone: /時區(預設使用你電腦的時區)/

# URL
url: /網站的網域位址/
root: /網站根目錄/
permalink: /文章目錄(預設使用 YYYY\MM\DD\文章名稱)/

# Extensions
theme: /網站的佈景主題/
       (可以到"https://hexo.io/themes/"下載喜歡的佈景放置到 theme 目錄裡)

# Deployment
deploy:
    type: /發佈型態/ 例如(git、heroku、rsync、openshift、ftpsync)
    repository: /部署位置/ 例如(git@github.com:帳號/REPO名.git)
    branch: /分支/ 例如(master、gh-pages)
    message: /部署訊息/
```
## Hexo GitHub配置
1.建置 [GitHub](https://github.com/join?return_to=https%3A%2F%2Fgithub.com%2Fnew&source=login) 帳號。

2.建置[repository](https://github.com/new)，並且定義名稱"Hexo"。

3.建立後，會有一組 http://github.com/yourname/Hexo 的產生，並修改_config.yml資訊對應輸入。
```
deploy:
  type: git
  repository: http://github.com/Ethoncho/Ethoncho.github.io.git
  branch: master
```
4.儲存文件後，部署上 GitHub
  ```
  $ hexo d -g
  ```
5.佈署成功後，就可以 https://ethoncho.github.io/ 查看是否部署成功
