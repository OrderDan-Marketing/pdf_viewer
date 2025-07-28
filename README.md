# 📖 PDF 線上閱讀器

一個基於 PDF.js 的線上 PDF 閱讀器，支援 URL 參數直接跳轉到指定頁面，完美適合文件分享和協作。

## ✨ 功能特色

- 📄 **線上 PDF 閱讀**：無需下載，直接在瀏覽器中閱讀 PDF
- 🔗 **URL 頁籤參數**：支援 `?url=PDF網址&page=頁碼` 直接跳轉
- 📱 **響應式設計**：支援手機、平板、桌面等各種裝置
- ⚡ **快速載入**：基於 PDF.js，載入速度快
- 🎯 **多種縮放**：50%-200% 縮放選項，適應不同閱讀需求
- 📋 **分享功能**：一鍵產生帶頁碼的分享連結
- 🔧 **無需安裝**：純網頁應用，開箱即用

## 🚀 線上體驗

**網址：** `https://your-app.zeabur.app/`

### 快速測試
```
# 基本使用
https://your-app.zeabur.app/

# 開啟第5頁
https://your-app.zeabur.app/?url=PDF網址&page=5

# 開啟第3頁並放大150%
https://your-app.zeabur.app/?url=PDF網址&page=3&scale=150
```

## 📋 使用方法

### 1. 上傳 PDF 檔案
將您的 PDF 檔案上傳到以下任一平台：
- GitHub Pages
- Google Drive（設定為公開分享）
- Dropbox（公開連結）
- 您的網站伺服器

### 2. 產生閱讀連結
使用以下格式建立分享連結：
```
https://your-app.zeabur.app/?url=[PDF網址]&page=[頁碼]&scale=[縮放比例]
```

### 3. 參數說明
| 參數 | 必填 | 說明 | 範例 |
|------|------|------|------|
| `url` | ✅ | PDF 檔案的網址 | `https://example.com/doc.pdf` |
| `page` | ❌ | 跳轉到指定頁面 | `5` |
| `scale` | ❌ | 縮放比例（百分比） | `150` |

## 💡 使用範例

### 基本分享
```html
<!-- 分享整份文件 -->
https://your-app.zeabur.app/?url=https://example.com/manual.pdf

<!-- 分享特定章節（第10頁） -->
https://your-app.zeabur.app/?url=https://example.com/manual.pdf&page=10
```

### 教學應用
```html
<!-- 課程講義第一章 -->
https://your-app.zeabur.app/?url=https://school.edu/course1.pdf&page=1

<!-- 作業說明第3頁 -->
https://your-app.zeabur.app/?url=https://school.edu/homework.pdf&page=3&scale=125
```

### 商業用途
```html
<!-- 產品手冊重點頁面 -->
https://your-app.zeabur.app/?url=https://company.com/product.pdf&page=15

<!-- 合約條款特定條文 -->
https://your-app.zeabur.app/?url=https://company.com/contract.pdf&page=8&scale=200
```

## 🛠️ 技術規格

### 前端技術
- **PDF.js**: Mozilla 開發的 PDF 渲染引擎
- **HTML5 + CSS3**: 響應式用戶界面
- **JavaScript ES6**: 現代瀏覽器支援

### 瀏覽器支援
- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+
- 📱 iOS Safari 12+
- 📱 Chrome Mobile 60+

### PDF 格式支援
- ✅ 標準 PDF 文件
- ✅ 加密 PDF（需要密碼）
- ✅ 多頁 PDF
- ✅ 高解析度 PDF
- ❌ 不支援互動式表單填寫

## 🔧 部署方式

### 本專案部署於 Zeabur
1. Fork 此倉庫
2. 連接到 [Zeabur](https://zeabur.com)
3. 選擇靜態網站部署
4. 自動獲得 HTTPS 網址

### 其他部署選項
- **Vercel**: 拖拽部署
- **Netlify**: GitHub 自動同步
- **GitHub Pages**: 免費靜態託管
- **自有伺服器**: 上傳 HTML 檔案即可

## 📁 PDF 檔案託管建議

### 免費選項
1. **GitHub Pages**
   ```
   https://username.github.io/pdf-files/document.pdf
   ```

2. **Google Drive**
   - 上傳 PDF → 右鍵分享 → 複製連結
   - 將連結格式改為：`https://drive.google.com/uc?id=FILE_ID`

3. **Dropbox**
   - 上傳 PDF → 建立分享連結
   - 將連結結尾的 `?dl=0` 改為 `?dl=1`

### 付費選項
- **AWS S3**: 高穩定性
- **Cloudflare R2**: 價格優惠
- **自有伺服器**: 完全控制

## ⚠️ 注意事項

### 安全性
- PDF 檔案必須支援 CORS（跨來源資源共享）
- 建議不要分享包含敏感資訊的 PDF
- 使用 HTTPS 連結確保安全傳輸

### 效能
- 大型 PDF 檔案（>50MB）載入時間較長
- 建議壓縮 PDF 以提升載入速度
- 行動裝置上建議使用較小的 PDF 檔案

### 限制
- 無法編輯 PDF 內容
- 不支援 PDF 表單填寫
- 依賴網路連線

## 🆘 常見問題

### Q: PDF 無法載入怎麼辦？
**A:** 檢查以下項目：
1. PDF 網址是否正確且可存取
2. PDF 檔案是否支援 CORS
3. 網路連線是否正常
4. PDF 檔案是否過大

### Q: 如何分享私人 PDF？
**A:** 
1. 上傳到支援公開分享的平台
2. 設定分享權限為「任何人皆可檢視」
3. 複製公開連結使用

### Q: 手機上使用體驗如何？
**A:** 
- 支援觸控操作
- 自動適應螢幕大小
- 建議使用較小的 PDF 檔案

### Q: 可以自訂外觀嗎？
**A:** 
- 可以修改 CSS 樣式
- 支援深色/淺色主題切換
- 可調整字體和按鈕大小

## 🤝 貢獻

歡迎提交 Issue 和 Pull Request！

### 開發環境
```bash
# 克隆專案
git clone https://github.com/yourusername/pdf-viewer.git

# 本地預覽（需要 HTTP 伺服器）
python -m http.server 8000
# 或
npx serve .
```

## 📄 授權

本專案基於 [MIT License](LICENSE) 開源授權。

## 🙏 致謝

- [PDF.js](https://mozilla.github.io/pdf.js/) - Mozilla PDF 渲染引擎
- [Zeabur](https://zeabur.com) - 部署平台

---

## 📞 聯絡方式

如有問題或建議，歡迎透過以下方式聯絡：
- 📧 Email: dan@orderdan-ai-marketing.com

---

**⭐ 如果這個專案對您有幫助，請給我們一個 Star！**
