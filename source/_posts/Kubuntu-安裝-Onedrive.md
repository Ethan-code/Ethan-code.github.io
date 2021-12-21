---
title: Kubuntu-安裝-Onedrive
date: 2021-12-20 11:47:57
tags:
- kubuntu
---

## 環境
- Kubuntu 20.04

## 步驟
- 更新 `/etc/apt/source.list` 檔案，添加以下文字

  ```bash
  # Onedrive
  deb https://download.opensuse.org/repositories/home:/npreining:/debian-ubuntu-onedrive/xUbuntu_20.04/ ./
  ```

- 下載 release key

  ```bash
  # Onedrive
  wget https://download.opensuse.org/repositories/home:/npreining:/debian-ubuntu-onedrive/xUbuntu_20.04/Release.key
  ```

- 加入到 apt key repository
  - 可以使用 `apt-key list` 檢查是否加入成功

  ```bash
  # Onedrive
  sudo apt-key add ./Release.key
  ```

- 更新 apt package cache

  ```bash
  sudo apt-get update
  ```

- 安裝 Onedrive

  ```bash
  sudo apt install onedrive
  ```

## 指令
- `onedrive --synchronize`: 同步資料
  - 預設同步資料夾會在 `~/Onedrive/` 目錄下
  - 會將當前狀態同步到線上（原以為只是單純下載，同步時才發現把檔案給刪掉了...）

## 參考資料
- [onedrive/ubuntu-package-install.md at master · abraunegg/onedrive](https://github.com/abraunegg/onedrive/blob/master/docs/ubuntu-package-install.md#distribution-ubuntu-2004)
- [onedrive/USAGE.md at master · abraunegg/onedrive](https://github.com/abraunegg/onedrive/blob/master/docs/USAGE.md#using-the-client)
