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
  - 如果沒有全域安裝會有找不到 hexo 的狀況，可以加上 `npx` 執行
1. 初始化 Hexo 需要安裝全域的 `hexo-cli`，才可以使用例如 `hexo new "article"` 新增文章的指令，安裝腳本如下

  ```shell
  npm install -g hexo-cli
  ```

1. 目前的 Hexo 網站是以 Github + Travis CI 進行部屬

---

## Hexo 透過 Asset Folders 設定添加圖檔
1. 開啟 `_config.yml` 檔案，找到 `post_asset_folder` 屬性，預設為 `false`，將屬性值改為 `true` 啟用 Asset Folders
1. 開啟設定後，透過 `hexo new` 的指令會自動建立一個與 post 名稱相同的資料夾，將圖檔擺放在其中就可以引用
  - 如果是已經建立的 post 也可以透過建立同名的資料夾來使用圖片
1. 在 `.md` 檔案中透過 hexo 的特殊語法 `{% asset_img <image_name.png> %}` 引用圖片

## 參考資料
- [Asset Folders | Hexo](https://hexo.io/docs/asset-folders.html)
- [Asset Folders | Hexo - Static Site Generator | Tutorial 9 - YouTube](https://www.youtube.com/watch?v=feIDVQ2tz0o)

---

## 在本地使用 `hexo server` 首頁出不來，訊息：WARN No layout: index.html?
- 原因是因為主題設定沒有設定好
- 此次是因為本地沒有拉取 next theme 的 repository，所以在執行時會找不到主題顯示，透過 `git clone https://gitlab.com/hexo-theme-next/hexo-theme-next themes/next` 取得相關的 code 以後便可正常顯示
