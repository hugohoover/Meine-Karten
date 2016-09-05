---
layout: post
title: "dagbok, jekyll och github"
date: 2016-09-06 00:57:10
image: '/assets/img/'
description: '過去的一天很不好，我甚至感覺自己有躁鬱症或者抑鬱症了，閱讀沒有動力，做什麼事情都會被打斷。兒子的情緒也很差。我的耐心似乎都用盡了。'
main-class: 'dagbok'
color:
tags:
- jekyll
- github
categories:
twitter_text:
introduction: '強迫自己記日記，我感覺有點像描述Howard Hughes的那種情況了。'
---

## 在日記類別用藍色標籤是不是有點不妥
因為blue也有憂鬱的意思，好像有點不吉利。
當然說到吉利，我還是秉承了中國人的傳統 -- 封建迷信。
不過說到封建，很多人並不了解真實的意思：封疆建藩。
這又是另一話題了。

不過，既然有這種心理陰影，我還是準備換一個討彩的顏色。
紅色帶有危險的意思；
黃色代表示警；
黑色又太陰鬱；
粉色娘砲；
深綠色又是台獨支持者的顏色。

糾結總歸是有理由的。

## jekyll och github-page
由於疏忽，我沒有在gitignore中加入忽略`node_modules`，於是在`git push`的時候需要推送很多不必要的文件。
我嘗試了中止，但是重新開始的時候依然繼續之前的操作。
這個時候就尷尬了。

我在想，按照手冊來進行或許才是最靠譜的：

`git push`
-> `modifying gitignore`
-> `git rm`
-> `git push (again)`


