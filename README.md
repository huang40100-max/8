# SLOWDAY COFFEE — React + AI 協作開發

這是 **SLOWDAY COFFEE 品牌概念網站**。採用 React、Vite、Tailwind CSS v4、Motion、Lucide Icons。

## 啟動方式

請使用 Node.js 20.19+ 或 22.12+。

```bash
npm install
npm run dev
```

在終端機顯示的本機網址開啟網站，通常是 http://localhost:5173。

## 正式建置

```bash
npm run build
npm run preview
```

## 功能

- 響應式導覽列 / 手機漢堡選單
- 品牌 Hero / Intro
- 菜單分類篩選（`src/data/menu.js` 可維護菜單）
- Gallery 圖片燈箱（鍵盤 Escape、左右鍵支援）
- Google Maps 嵌入預留位置（`src/data/site.js`）
- 課堂展示用預約表單，包含必填驗證、日期時間驗證、摘要回饋
- 全站 375 / 768 / 1024 / 1440 px 響應式配置

## 正式店家資料與地圖

網站目前是**概念／課堂展示**，沒有實際店址。請在 `src/data/site.js` 設定 `address`、`phone`、`hours`、`mapsUrl`、`mapsEmbedUrl`。未設定時顯示佔位文字，**不會捏造地址**。Google Maps 嵌入連結應從真實 Google Maps 分享／嵌入功能取得。

## 訂位流程注意

`BookingForm` 只在瀏覽器內檢查資料並顯示摘要，不會傳送資料到伺服器、寄送 Email、建立訂位或永久儲存。介面有明確展示說明。若未來要改成真正可訂位，需另外串接提供可用時段、持久化、衝突檢查及確認通知的 API／第三方服務。

## 圖片與版權

網站使用 Unsplash 遠端示意圖片，需連網方能載入。正式商業發布前，請換成授權明確、符合真實店家商品與空間的圖片，並檢查對應使用條款。

## Vercel 部署

1. 在 GitHub 新增 repository，將專案上傳（不要上傳 node_modules）。
2. 前往 Vercel，選 `Add New → Project`，匯入 repository。
3. Framework Preset 選 Vite；Build Command 為 `npm run build`；Output Directory 為 `dist`。
4. Deploy 即可取得公開網址。

注意：公開網址不代表網站是真實營業的咖啡廳，請保留展示說明。
