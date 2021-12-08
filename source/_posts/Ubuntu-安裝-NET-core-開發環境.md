---
title: Ubuntu 安裝 .NET core 開發環境
date: 2021-12-09 00:59:27
tags:
- dotnet
- ubuntu
---

## 安裝
### 加入 package repository 與 signing key
執行以下指令加入

```shell
wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb
```

### 安裝 SDK

```shell
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y dotnet-sdk-6.0
```


### 安裝 runtime
ASP.NET Core Runtime 提供那些不包含 runtime 的 .NET 應用程式一個執行環境

如果有安裝 SDK 就不用安裝對應的 runtime

> 這次已安裝 SDK，不安裝 runtime，故不對安裝過程多做說明

## 檢查安裝成功
執行 `dotnet --list-sdks` 與 `dotnet --list-runtimes` 查看安裝版本

## 參考資料
- [Install .NET on Ubuntu - .NET | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/core/install/linux-ubuntu#2004-)
- [Check installed .NET versions on Windows, Linux, and macOS - .NET | Microsoft Docs](https://docs.microsoft.com/en-us/dotnet/core/install/how-to-detect-installed-versions?pivots=os-windows)