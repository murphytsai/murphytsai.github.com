---
layout: post
title: "發佈 octopress 文章四部曲"
date: 2013-03-28 18:04
comments: true
categories: 
---

* $ rake new_post["文章標題"]

####撰寫文章內容
* 編輯 source/_posts/time-title.markdown 

####產生網頁相關資料
* $ rake generate 

####發佈文章
* $ rake deploy
