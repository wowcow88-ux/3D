# 3D Studio C5P — 第一版 v0.1.0

免費、手機／Android 平板／Mac／Windows 皆可使用的 3D 模型編輯 Web App。針對 Flashforge Creator 5 Pro 的 256 × 256 × 256 mm 平台設計。

## 使用方式

1. 將 `index.html` 與 `vercel.json` 上傳到 **GitHub 儲存庫根目錄**。
2. Vercel → Add New → Project → Import 此 GitHub Repo。
3. Framework Preset 選 **Other**，Root Directory 設 `./`，Build Command 留空，Output Directory 使用 `.`。
4. 點 Deploy。之後每次更新 GitHub 的 `main` 分支，Vercel 便會重新部署。
5. 進入網頁後直接操作。匯出 STL，接著使用 **Flash Studio Desktop** 選擇 Creator 5 Pro 對應噴嘴與線材設定進行切片、傳輸及列印。

> 如果儲存庫只有 `index.html` 一個檔案，也可以部署（Vercel 請選 Other 並設定 root）。`vercel.json` 只是協助固定部署設定。

## 已有功能
- Apple 風格的簡約介面、膠囊按鈕，支援觸控、滑鼠與手寫筆。
- 匯入 STL、OBJ、GLB、SVG（SVG 必須包含封閉向量路徑）。
- 新增圓角底座、方塊、球、圓柱、圓錐、圓環。
- 畫出平面閉合輪廓並拉伸成 3D。
- 360 度檢視、頂視/正視/側視、物件點選、拖曳移動／旋轉／縮放、輸入毫米尺寸。
- 物件複製、刪除、變更顏色、顯示與隱藏、回到平台、復原／重做。
- 匯出 STL 供切片；匯出 GLB 保存幾何、顏色與場景組成；下載 PNG 預覽。
- 使用 IndexedDB 自動儲存於目前裝置，**不會自動跨裝置同步**。

## 尚未實作
- 任意頂點雕塑、完整網格修補、布林挖孔、真正的 AI 圖片轉 3D、3MF 專案檔匯入、實體模擬和自動切片。
- C5P 列印機器連線與一鍵列印（依需求特意延後）。

## 重要提醒
- 第一次開啟需要網路連線載入 Three.js（採 `three@0.173.0` 的 jsDelivr CDN）。
- STL 不包含顏色、材料和切片參數。請用 Flash Studio 設定印表機、噴頭、層高、材料及支撐。
- GLB 依據匯入來源與模型細節可能非常大，建議定期備份到檔案，不要只依賴瀏覽器自動儲存。
- 不同來源的 GLB/OBJ 可能使用 Y-up 坐標，匯入後如果角度不符，請使用旋轉欄位調整。
- 60 MB 的單檔上傳限制是為了減少手機／平板卡頓，大型網格可能仍超出裝置效能。

## 技術
純靜態 HTML + CSS + JavaScript ES Modules，Three.js 與官方 Addons。無後端、不需要 Supabase、API 金鑰或付費 AI。

## 版本
v0.1.0 — 第一版可操作 MVP。
