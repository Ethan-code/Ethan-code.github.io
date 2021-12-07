---
title: Ubuntu 新增螢幕截圖快捷鍵
date: 2021-12-08 02:05:14
tags:
- ubuntu
- screenshot
---

## 起因
在製作文章或者溝通時，常常會有截圖需要，只知道可以透過 PrintScreen 的按鍵去擷取整個畫面，想要有擷取部份畫面的功能

## 解決方式
Gnome 內建就有指令，如果要方便使用，可以透過設定鍵盤快捷鍵的功能來啟動指令

```shell
# 在 Ubuntu 20.04 不起作用
gnome-screenshot -ac

# 將上述指令改為以下指令可以正常運作
sh -c "gnome-screenshot -acf /tmp/test && cat /tmp/test | xclip -i -selection clipboard -target image/png"
```

- `a` 代表區塊 (area) 擷取
- `c` 代表將擷取的圖片傳送到剪貼簿中

目前鍵盤快捷鍵設定與 garena 的截圖相同，使用 `Ctrl` + `Alt` + `A` 啟動指令

## 參考資料
- [Ubuntu Shortcut for Partial Screenshot to Clipboard | by Destan Sarpkaya | Medium](https://medium.com/@dorukdestan/ubuntu-shortcut-for-partial-screenshot-to-clipboard-3a4018e8d3dd)
- [GNOME Screenshot can't copy to clipboard in Ubuntu 18.04 - Ask Ubuntu](https://askubuntu.com/questions/1196914/gnome-screenshot-cant-copy-to-clipboard-in-ubuntu-18-04)