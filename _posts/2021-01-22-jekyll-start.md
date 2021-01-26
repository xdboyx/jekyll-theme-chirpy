---
title: 使用 jekyll 在github上做筆記
date: 2021-01-22 14:00:00 +0800
categories: [jekyll]
tags: [jekyll]
pin: true
---

原本程式筆記是記在Notion上面，不過看到蠻多人在gitgub page上分享筆記

覺得如果自己的筆記也能幫助其他有需要的人，感覺也是蠻不錯。

>[Notion](https://www.notion.so/) 在2020年5月之後，block 就可以無限制的使用

於是在google大神的幫助之下。

發現我們可以使用 **jekyll** 在github上作筆記。。

## [jekyll 官網](https://jekyllrb.com/) 

我們可以看到 DOCS 的 Quick start 的頁面

有需要先安裝 Ruby 相關檔案的說明
![](https://drive.google.com/uc?id=1Km2n-cKRpLvW-IQF4pyRxrwZTtstMD-B)

點開 [Requirements 看裡面的內容](https://jekyllrb.com/docs/installation/#requirements)

由於我是Windows系統的
![](https://drive.google.com/uc?id=1oQ_PNIzVEmM-G_RkAwDhGUHpWxZrqpXy)

[點 Windows](https://jekyllrb.com/docs/installation/windows/)

## Install Ruby
在 [Jekyll on Windows](https://jekyllrb.com/docs/installation/windows/) 頁面可以看到詳細教學。

大致上的步驟:

1. [Install Ruby](https://rubyinstaller.org/downloads/)
   ![](https://drive.google.com/uc?id=1XeTSA6ooF7bu8Jk2JkFbswj4k2IeJYHV)
   右上方有說如果不知道要安裝哪個版本就裝推薦的版本
   
   點 **I accept this License**，我使用他預設的安裝 按下一步安裝
2. Start Command Prompt with Ruby

   安裝完後，應用程式會多個 Start Command Prompt with Ruby
   ![](https://drive.google.com/uc?id=1jgtlTQk32VXkSREhYpJbpGfyTMgr2Aep){: width="400"}


## Install jekyll
接下來可以按照 官網上 [Quick start](https://jekyllrb.com/docs/) 上的順序安裝 jekyll 和 new Jekyll site 

在command 指令上輸入 安裝指令 

Install the jekyll and bundler `gems`.
```terminal
gem install jekyll bundler
```
Create a new Jekyll site at ./myblog
```terminal
jekyll new myblog
```
Change into your new directory.
```terminal
cd myblog
```
Build the site and make it available on a local server.
```terminal
bundle exec jekyll serve
```

Browse to http://localhost:4000

## [jekyll themes](http://jekyllthemes.org/)
可以使用別人已經寫好的外觀，不過在使用前還是要先看一下read。看一下使用的規則