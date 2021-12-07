---
title: 比較 window.matchMedia 與 resize 事件差異
date: 2021-12-08 01:04:19
tags:
- javascript
---

近日認識到 `window.matchMedia` 這個函式，方便在不同寬度下呼叫 callback，想到以往會使用 resize 事件來完成在特定寬度時觸發事件，想知道兩者在實際運用上有何不同

## 筆記
- resize 會在每次變更寬度時觸發，可能會造成效能問題。如果我們只想關注特定寬度事件，用 `window.matchMedia` 會是更好的選擇
- `window.matchMedia` 也可以不設定 eventListener 直接使用

## 參考資料
- [Why you should use window.matchMedia when checking for window resizes in Javascript - Web dev etc - my software development blog](https://webdevetc.com/blog/matchmedia-events-for-window-resizes/)
    - 幾乎說明了 resize 與 matchMedia 的差異，感覺我可以把他整篇文章翻譯就好XD
- [css - What's the most reliable way to integrate javascript with media queries? - Stack Overflow](https://stackoverflow.com/a/29133907)
    - 提到了使用 resize 要使用節流方案來避免防抖動，以前在使用 resize 時的確有遇到此情境

---

## Todo
- [ ] 將敘述完整、讓看文章的人可以了解差異
- [ ] 加上程式範例
- [ ] 補上 matchMedia 可以使用的格式