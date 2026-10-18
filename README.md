# Smart-Closet
Smart Closet is a smart wardrobe web app featuring clothing management, automatic background removal, color analysis, personalized outfit recommendations, weather integration, and outfit previews.


# Smart Closet｜智慧穿搭助手 👕

> **Your Personal Wardrobe** — 建立自己的數位衣櫃，讓每天的穿搭更簡單。

Smart Closet 是一款以 **HTML、CSS、JavaScript** 開發的互動式智慧穿搭 Web App。使用者可上傳並管理衣物照片、編輯去背效果、整理服飾顏色，並根據場合、風格、天氣與文字需求，從自己的衣櫃中產生穿搭建議。

本專案採用**規則式推薦演算法**，並非連接生成式 AI 模型進行即時穿搭判斷。開發過程透過 AI 協助需求分析、程式實作與功能調整。

## 🌐 線上體驗

- **GitHub Pages：** [請填入部署後的網站網址]((https://github.com/Kamato-kk/Smart-Closet))
- **GitHub Repository：** [請填入專案網址](https://github.com/Kamato-kk/Smart-Closet)


## ✨ 主要功能

| 功能 | 說明 |
| --- | --- |
| 👔 數位衣櫃 | 新增、編輯、刪除衣服，並依上衣、下身、外套、鞋子分類管理 |
| 🖼️ 照片去背 | 使用瀏覽器內的影像處理移除相近色背景，可調整去背強度 |
| ✏️ 手動修圖 | 提供擦除筆刷、矩形選取、自由套索、還原、復原及重做 |
| 🎨 多色分析 | 從衣服照片推測常見顏色，並可手動調整主色、副色（最多五色） |
| 💬 文字需求 | 輸入「約會想穿休閒一點」等文字，辨識支援的場合、風格、溫度及顏色關鍵字 |
| ☀️ 天氣設定 | 手動設定溫度與天氣，或經定位授權後取得即時天氣 |
| 👗 穿搭推薦 | 依照衣物類別、色彩、風格、場合與氣溫進行規則式評分及搭配 |
| 🧍 穿搭預覽 | 顯示衣物搭配、示意人台、搭配分數與推薦理由 |
| ♡ 收藏搭配 | 收藏推薦結果，之後可查看或移除 |
| 💾 本機保存 | 使用 IndexedDB 儲存衣物及收藏資料 |

## 🚀 使用方式

1. 進入 **「我的衣櫃」**，上傳衣服照片。
2. 確認自動去背效果，必要時使用筆刷或選取工具修整。
3. 填寫名稱、分類、風格、顏色與保暖程度，按下 **「儲存衣服」**。
4. 至少新增 **一件上衣、一件下身與一雙鞋**，才能產生完整穿搭。
5. 進入 **「穿搭推薦」**，輸入穿搭需求並設定場合、風格與天氣。
6. 按下 **「產生穿搭建議」**，查看搭配預覽、評分及理由。
7. 喜歡的搭配可加入 **「我的收藏」**。

## 🛠️ 使用技術

- **HTML5：** 頁面結構與表單
- **CSS3：** 簡約視覺設計與響應式排版
- **JavaScript（Vanilla JS）：** 使用者互動、文字關鍵字解析與規則式穿搭推薦
- **Canvas API：** 圖片處理、去背、顏色分析與編輯
- **IndexedDB：** 瀏覽器本機衣物及收藏資料庫
- **Geolocation API：** 經使用者授權取得位置
- **[Open-Meteo API](https://open-meteo.com/)：** 查詢即時天氣
- **GitHub Pages：** 靜態網站部署

本專案將 HTML、CSS 與 JavaScript 整合在單一 `index.html`，不需要自行安裝套件或架設後端伺服器。

## 📁 專案結構

```text
smart-closet/
├── index.html       # 網頁主程式（含 CSS 與 JavaScript）
└── README.md        # 專案說明文件
```

## 🌍 GitHub Pages 部署

1. 在 GitHub 建立 **Public** Repository，例如 `smart-closet`。
2. 將主程式命名為 `index.html`，放在 Repository 根目錄，並上傳 `README.md`。
3. 開啟 Repository 的 **Settings → Pages**。
4. 在 **Build and deployment** 選擇 **Deploy from a branch**。
5. Branch 選擇 `main`，資料夾選擇 `/(root)`，按 **Save**。
6. 等待部署完成，開啟 GitHub Pages 提供的網址進行測試。

## 🔒 資料與使用限制

- 衣服照片在使用者的瀏覽器中處理，衣櫃與收藏資料預設儲存在該瀏覽器的 IndexedDB，不會自動同步到其他裝置。
- 自動去背採用**背景色相似度及邊緣連通區域**處理，並非 AI 語意分割；複雜背景可能需要手動修整。
- 顏色分析是像素統計推測，可能受到陰影、背景及光線影響。
- 穿搭推薦是規則式評分，結果僅供搭配參考，不代表專業造型師或生成式 AI 的判斷。
- 即時天氣需要網路、HTTPS 安全環境及定位權限；無法取得時仍可使用手動天氣設定。
- 瀏覽器清除網站資料後，已儲存的衣物及收藏可能遺失。

## 🤖 AI 協作開發

本專案以 **Vibe Coding** 方式進行，將創意轉換為可實際操作的網頁。AI 協助的工作包含：

1. **需求討論：** 確認智慧衣櫃、規則式推薦、雙模式預覽、天氣整合與簡約介面等方向。
2. **規格整理：** 將使用流程、輸入輸出、功能需求及技術限制整理成規格。
3. **程式實作：** 協助完成單一 `index.html` 中的介面、資料管理與互動邏輯。
4. **功能調整：** 針對去背、手動圖片編輯、多色分析、穿搭推薦及收藏等功能進行迭代。
5. **部署與文件：** 整理 GitHub Pages 部署方式、README 與系統規格書。



## 📚 專案資訊

**專案名稱：** Smart Closet 智慧穿搭助手  
**專案類型：** Web App／Vibe Coding 課程作品  
**開發方式：** AI 協作開發  
**語言：** 繁體中文

---

*Smart Closet — Make every outfit count.*
