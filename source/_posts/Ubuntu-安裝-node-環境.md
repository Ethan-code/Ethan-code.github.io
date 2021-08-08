---
title: Ubuntu 安裝 node 環境
date: 2021-08-08 12:56:41
tags:
- ubuntu
- nodejs
---

Ubuntu 下安裝選擇透過 nvm 來安裝，可以提供多個 node 環境，方便開發環境不同進行切換。

## 安裝 nvm

參考 [nvm github 網站](https://github.com/nvm-sh/nvm#install--update-script) 安裝方式

1. 使用 `crul` 或者 `wget` 取得安裝的 shell script，這次我選擇使用 wget

  ```shell
  wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
  ```

1. 安裝後的 script 會在 `~/.nvm/` 資料夾下，執行該資料夾下的 `install.sh` 進行 nvm 安裝

  ```shell
  sh ~/.nvm/install.sh
  ```

1. 用 `nvm -v` 確定是否安裝完成，確認安裝完後便可以使用 nvm 了

## 安裝 nodejs

完成安裝 nvm 以後，只是安裝完了 node 環境的 **管理器**，實際上還沒安裝任何 node 環境，透過 `nvm install <version>` 的指令來安裝指定版本的 node 環境

1. 可以先使用 `nvm list-remote` 查看目前有哪些版本的 node 環境，目前我想要安裝的是最新版的 LTS 環境，是 `v14.17.4`
1. 透過 nvm 定義的 `'lts/*'` 安裝最新版的 LTS node 環境

  ```shell
  nvm install 'lts/*'
  ```

1. 安裝完成後，透過 `-v` 可以查看當前安裝版本，確認是否安裝完成

  ```shell
  node -v
  ```

## 參考資料
[nvm-sh/nvm: Node Version Manager - POSIX-compliant bash script to manage multiple active node.js versions](https://github.com/nvm-sh/nvm)
