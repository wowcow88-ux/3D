# 3D Studio v0.1.1 — 主畫面 App 圖示版本

本版本保留上一版 3D 建模功能，新增黑灰白 Logo 及 iPhone / Android 桌面 App 圖示設定。沒有增加一鍵列印或付費服務。

## 用 GitHub + Vercel 部署

請**解壓縮後**，把這個資料夾裡全部檔案放到你的 GitHub 儲存庫**根目錄**（跟 index.html 同一層），若已有 index.html、vercel.json，選擇覆蓋舊版。不要只上傳 ZIP，也不要放進額外子資料夾。

index.html
manifest.webmanifest
icon-180.png
icon-192.png
icon-512.png
icon-1024.png
icon-maskable-512.png
favicon-32.png
vercel.json
README.md

Vercel 若已連線 GitHub main，推送後就會自動部署，無須改設定。這是 PWA 外觀設定，不含 service worker，因為 Three.js 等依賴網路 CDN，暫不保證離線可用。

## iPhone

1. 使用 Safari 進入部署好的網址。
2. 點分享 → 加入主畫面。
3. 開啟「打開為網頁 App」(若有選項)。
4. 設定名稱「3D Studio」→ 加入。
5. 若先前已加到主畫面但仍顯示舊圖示，請移除舊主畫面圖示後重新加入（不會刪除 Vercel 網站）。

## Android

Chrome 打開網站 → ⋮ → 加到主畫面 / 安裝應用程式。

## 注意

* 目前建模工作仍預設 Flashforge C5P 平台尺寸；新的 Logo 不限定品牌，但多機型切換將是後續功能。
* 專案本機儲存跟瀏覽器／網域有關；更換網域或移除原網站前，先從程式匯出 GLB 備份。
* 這是可以加入桌面的網頁 App，不是原生 iOS / Android App，是否可離線使用需另做開發。
