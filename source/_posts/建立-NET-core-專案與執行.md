---
title: 建立 .NET core 專案與執行
date: 2021-12-09 01:49:18
tags:
- dotnet
---

## 建立專案
到要建立專案的資料夾下，執行 `dotnet new console` 建立專案
- `console` 表明建立 **主控台** 應用程式，可以替換成其他 [專案模板](https://docs.microsoft.com/zh-tw/dotnet/core/tools/dotnet-new)

### 建立 .gitignore 檔案
- 到 [core/.gitignore at main · dotnet/core](https://github.com/dotnet/core/blob/main/.gitignore) 下載 .gitignore 檔案

## 執行
執行 `dotnet run`

## 參考資料
- [core/.gitignore at main · dotnet/core](https://github.com/dotnet/core/blob/main/.gitignore)
    - .NET Core 專案適用的 .gitignore 檔案
- [dotnet new 命令 - .NET CLI | Microsoft Docs](https://docs.microsoft.com/zh-tw/dotnet/core/tools/dotnet-new)
    - .NET Core 可使用的專案模板