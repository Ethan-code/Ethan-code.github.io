---
title: Kubuntu 安裝 Go 環境
date: 2021-12-21 20:44:38
tags:
- go
- kubuntu
---

## 步驟
1. 安裝 Go 的執行環境，到官網下載頁面下載 tar.gz 檔（此次版本為 go1.17.5.linux-amd64.tar.gz）
1. 解壓縮到 `/usr/local/go` 路徑下

  ```bash
  ## 移除原有 go 資料夾
  rm -rf /usr/local/go

  ## 解壓縮到 /usr/local 下，因為有建立資料夾的問題，加上 sudo 給權限
  sudo tar -C /usr/local -xzf go1.17.5.linux-amd64.tar.gz
  ```

1. 加入 go 指令到 PATH 內

  ```bash
  export PATH=$PATH:/usr/local/go/bin
  ```

1. 執行 `go version` 確認安裝沒問題

## 參考資料
- [Download and install - go.dev](https://go.dev/doc/install)
