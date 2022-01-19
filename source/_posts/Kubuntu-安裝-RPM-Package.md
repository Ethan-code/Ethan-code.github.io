---
title: Kubuntu 安裝 RPM Package
date: 2022-01-19 22:12:53
tags:
- kubuntu
- rpm
---

1. 安裝 `alien` 套件：`sudo apt install alien`
2. 使用 alien 將 **rpm** package 轉換成 **deb** 格式
  - 範例：將 slack 的 rpm 檔案轉換成 deb 格式 `sudo alien slack-4.23.0-0.1.fc21.x86_64.rpm`
3. 成功後會跳出 deb 檔案產生訊息
  - 範例：`slack_4.23.0-1.1_amd64.deb generated`

## 參考資料
- [Install RPM packages on Ubuntu | Linuxize](https://linuxize.com/post/install-rpm-packages-on-ubuntu/)
