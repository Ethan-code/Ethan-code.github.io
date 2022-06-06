---
title: Kubuntu-安裝-IntelliJ
date: 2022-06-06 21:15:57
tags:
- kubuntu
- intellij
---

(未完成)

## 環境
- Kubuntu 22.04

## 步驟
1. 到 IntelliJ 官網下載 `<tarball>.tar.gz` 安裝檔
1. 使用 `sudo tar -xzf <ideaIU>.tar.gz -C /opt` 解壓縮成資料夾
  - `/opt` 路徑一般是用來放第三方軟體預設安裝位置
1. 到 `/opt/<ideaIU>/bin/` 目錄下，執行 `sh idea.sh`
1. 建立桌面捷徑，在 Welcome 畫面上點擊齒輪，並點擊 `Create Desktop Entry`

  {% asset_img intellij_create_desktop_entry.png %}

## 參考資料
- [Install IntelliJ IDEA | IntelliJ IDEA](https://www.jetbrains.com/help/idea/installation-guide.html#standalone)
- [tar 指令的常用語法 | Vixual](http://www.vixual.net/blog/archives/127)
  - 了解 tar 指令參數涵義
