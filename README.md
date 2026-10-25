# 放大鏡 PWA

檔案全部放同一層，上傳到 GitHub Pages 的任一資料夾即可（例如 `magnifier/`）。

- index.html — 主程式（相機 / 圖片 / 文字三種模式）
- manifest.json — PWA 設定
- sw.js — 離線快取（改版時把 CACHE 名稱 v1 → v2）
- icon-*.png — 圖示

iOS：用 Safari 開啟 → 分享 → 加入主畫面。相機需 HTTPS，LINE 內建瀏覽器可能無法開相機。

## 唸給我聽（v2）
- 朗讀：POST arcar `/tts`（台灣腔），失敗自動改用手機內建語音
- 看字／翻譯：POST arcar `/v1/messages`（Claude 視覺，model 在 index.html 的 AI_MODEL 常數）
- 端點寫在 index.html 搜尋 `var API=` 即可修改
