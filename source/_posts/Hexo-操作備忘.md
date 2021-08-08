---
title: Hexo 操作備忘
date: 2021-08-08 14:01:03
tags:
- hexo
---

## 起因
紀錄有關 Hexo 的操作方式，避免之後忘記。因為可能很久才會更新一次XD。

## 備忘
1. 新增文章，使用 `hexo new "article title"`，可以使用中文名稱，檔名也會是中文的
1. 初始化 Hexo 需要安裝全域的 `hexo-cli`，才可以使用例如 `hexo new "article"` 新增文章的指令，安裝腳本如下

  ```shell
  npm install -g hexo-cli
  ```

1. 目前的 Hexo 網站是以 Github + Travis CI 進行部屬
