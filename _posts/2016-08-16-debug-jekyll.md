---
layout: post
title: Debugging i Jekyll
image: '/assets/img/'
description: '解決方案的來源是Stack Overflow。'
main-class: 'Notizen'
tags:
- jekyll
categories: 'jekyll'
introduction: '見招拆招是我現在採用的方法，其目的是迅速積累經驗。'
---

## 初始，在MBP上的OS X环境下进行尝试

出現了`WARN: Unresolved specs during Gem::Specification.reset:`，於是到[stack overflow](http://stackoverflow.com/questions/17936340/unresolved-specs-during-gemspecification-reset)上找答案。

運行了這些命令，

    gem cleanup rouge
    gem cleanup jekyll-watch
    gem cleanup listen
    gem cleanup ffi
    bundle install

It works on my MBP.

## 但是当我转向MBA上的macOS Sierra beta之后
`WARN: Unresolved specs during Gem::Specification.reset:`出现在`listen`上，而且之前的方法不起作用了。
于是采用了: `bundle clean --force`



