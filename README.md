# Vite 專案 (尚未引入 BS5)

## 📌 專案簡介

- 目前僅有 **Vite + EJS**
- 預計使用 **Vite + Bootstrap 5 + EJS** 建置響應式網站
- 可快速新增共用模板 (header/footer)
- 開發時支援 Live Reload，自動刷新瀏覽器

## 🛠️ 開發環境與版本資訊

- **Node.js**: v20.18.2
- **npm**: 10.8.2

## 🖥️ 專案技術

### 🔶 前端建構工具

- **Vite** (v6.3.5) – 前端開發與打包工具
- **vite-plugin-ejs** (v1.7.0) – EJS 模板支援
- **vite-plugin-live-reload** (v3.0.2) – 開發時自動重載頁面

### 🔶 CSS / 樣式

- **Bootstrap 5** – CSS 框架
- **Sass** (v1.61.0) + **sass-loader** (v13.2.2) – SCSS 編譯

### 🔶 模板 / HTML

- **EJS** (v3.1.9) – HTML 模板引擎

#### 💠 資料夾結構

- assets # 靜態資源放置處

  - images # 圖片放置處
  - scss # SCSS 的樣式放置處

- layout # ejs 模板放置處
- pages # 頁面放置處

- JavaScript 程式碼可寫在 main.js 檔案

#### 💠 注意事項

- 已將 pages 資料夾內的 index.html 預設為首頁，建議不要任意修改 index.html 的檔案名稱
- .gitignore 檔案是用來忽略掉不該上傳到 GitHub 的檔案（例如 node_modules），請不要移除 .gitignore

#### 💠 開發模式的監聽

vite 專案執行開發模式 `npm run dev` 後即會自動監聽，不需要使用 `Live Sass Compiler` 的 `Watch SCSS` 功能

## 📝 部署 gh-pages 流程說明

### 🔶 Windows 版本

1. 在 GitHub 建立一個新的 Repository

2. 部署前請務必先將原始碼上傳到 GitHub Repository 也就是初始化 GitHub，因此通常第一步驟會在專案終端機輸入以下指令

```cmd
git init # 若已經初始化過就可以不用輸入
git add .
git commit -m 'first commit'
git branch -M main
git remote add origin [GitHub Repositories Url]
git push -u origin main // 僅限第一次輸入，往後只需要輸入 git push
```

3. 初始化完畢後，執行 `npm run deploy` 指令進行自動化部署
