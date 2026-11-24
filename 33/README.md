# 柚日子｜麻豆文旦農創品牌網站

這是純靜態網站，使用原生 HTML、CSS、JavaScript 製作。**不需要 Node.js、npm、框架或建置步驟**，可以直接用瀏覽器開啟 `index.html` 預覽，也可部署至 GitHub Pages 或 Render Static Site。

## 專案結構

```text
├── index.html       # 網站頁面內容
├── src/
│   ├── style.css    # 品牌視覺、響應式樣式
│   └── app.js       # 商品篩選、購物袋與互動表單
├── render.yaml      # Render 靜態網站 Blueprint
└── README.md
```

## 功能

- 品牌首頁、麻豆四季與風土故事
- 商品分類、詳情、購物袋數量調整、移除、金額試算與模擬結帳
- 挑柚與辭水知識、認養果樹編號查詢
- 柚子帽投稿與老欉 VIP 預約互動表單
- 企業詢價、果園位置地圖連結
- 手機與桌面響應式版面

表單和結帳目前僅為瀏覽器內的互動示範，資料不會傳送或保存。正式營運時可再串接後端、郵件、訂單及金流服務。

## 直接預覽

在檔案管理員中雙擊 `index.html`，或在瀏覽器選擇「開啟檔案」。也可以將 `index.html`、`src/` 一起放在任何靜態網站主機。請保留資料夾結構，否則 CSS 與 JavaScript 相對路徑會失效。

## Render 部署

1. 將專案推送到 GitHub Repository。
2. Render 選 **New → Blueprint** 並連接此 Repository；或選 **New → Static Site**。
3. 手動建立時，Build Command 可留空，Publish Directory 設為 `.`（專案根目錄）。無需 Start Command 或環境變數。
4. 建立服務後，使用 Render 提供的網址瀏覽網站。更新 GitHub 分支後 Render 會重新部署。

`render.yaml` 使用不安裝套件的空操作 Build Command，並將專案根目錄直接發布。若 Render Dashboard 允許 Build Command 留空，也可留空。

## GitHub 推送

先在 GitHub 建立空 Repository，然後於專案目錄使用已安裝的 Git：

```bash
git init
git add .
git commit -m "建立柚日子麻豆文旦品牌網站"
git branch -M main
git remote add origin https://github.com/你的帳號/你的repo.git
git push -u origin main
```

## 圖片與品牌素材

目前主要情境使用 CSS 插畫、Emoji 及文字，無需下載圖片即可顯示。若要換成實拍圖，可建立 `images/` 資料夾，在 HTML 使用 `images/檔名.webp`。社群投稿照片上線前，請先取得投稿者刊登同意。

網站使用 Google Fonts 作為字體增強；沒有網路時會回退至系統字體。若需完全離線，可移除 `src/style.css` 第一行的 Google Fonts `@import`。

歷史年代、地方地名、產銷履歷及風味描述正式商用前，請依可佐證資料與在地工作者核對。
