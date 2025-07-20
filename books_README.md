# 線上書庫

這是一個輕量級的線上書庫應用程式，旨在提供一個簡潔、響應式且易於使用的平台，用於瀏覽和閱讀小說章節。它支援 Markdown 格式的章節內容，並具備年齡驗證功能，確保內容適合所有使用者。

## 功能特色

- **年齡驗證**：不再於進入書庫前顯示全局年齡確認提示。現在，僅當嘗試閱讀在 `filelist.json` 中被標記為 R18 的章節時，才會彈出年齡確認提示。
- **書庫列表**：清晰展示所有小說，包含標題、作者和章節數量。
- **響應式設計**：介面適應不同螢幕尺寸（手機、平板、桌面）。
- **置頂章節選單**：在小說閱讀頁面，章節下拉選單固定在頂部，方便快速切換章節。
- **Markdown 支援**：小說章節內容支援 Markdown 語法，自動轉換為 HTML 顯示，讓排版更豐富。
- **內容自動調整**：載入章節內容時，會自動移除 Markdown 檔案的第一行（假定為章節標題），避免重複顯示。
- **簡潔的版面**：專注於閱讀體驗，移除多餘的視覺元素。
- **章節圖片顯示**：支援在章節內容上方顯示圖片，可設定圖片檔名、寬度和高度。

## 使用技術

- HTML5
- CSS3 (Tailwind CSS)：用於快速構建響應式和美觀的介面。
- JavaScript (Vanilla JS)：處理所有前端邏輯和 DOM 操作。
- Marked.js：一個用於將 Markdown 轉換為 HTML 的 JavaScript 函式庫。

## 如何設定與執行

### 1. 專案結構

請確保您的專案資料夾結構如下：

```
您的專案資料夾/
├── mybooks.html           <-- 主要的 HTML 檔案
├── filelist.json          <-- 小說資料的 JSON 設定檔
└── novels/                <-- 存放所有小說章節的資料夾
    ├── shia-pian-zhou/    
    │   ├── ch01.md
    │   ├── ch02.md
    │   └── img/           
    │       ├── ch01.png
    │       └── ...
    └── FleetingClouds/    
        ├── ch00.md        
        ├── ch01.md
        └── ...
```

### 2. 安裝與執行

建議使用 Visual Studio Code 及其 Live Server 擴充功能來本地運行和測試。

1. 安裝 Visual Studio Code。
2. 在 VS Code 中安裝 Live Server 擴充功能。
3. 開啟書庫專案資料夾。
4. 右鍵 `mybooks.html`，選擇 Open with Live Server。

### 3. 更新 `filelist.json`

```json
[
  {
    "title": "夢境邊界",
    "folder": "shia-pian-zhou",
    "author": "法式草莓布丁",
    "tags": "小說-奇幻-愛情-R18",
    "chapters": [
      {
        "file": "ch01.md",
        "title": "第1章：囚禁與奇遇",
        "hasChapterTitleInContent": true,
        "isR18": false,
        "img": "ch01.png",
        "imgWidth": 600,
        "imgHeight": 600
      },
      {
        "file": "ch02.md",
        "title": "第2章：虛假的戀人",
        "hasChapterTitleInContent": true,
        "isR18": false,
        "img": "ch02.png",
        "imgWidth": 600,
        "imgHeight": 600
      }
    ]
  },
  {
    "title": "過眼雲煙",
    "folder": "FleetingClouds",
    "author": "法式草莓布丁",
    "tags": "小說-古風-宮庭",
    "chapters": [
      {
        "file": "ch00.md",
        "title": "序章 殘神紀元",
        "hasChapterTitleInContent": true,
        "isR18": false
      },
      {
        "file": "ch01.md",
        "title": "第1章 穿越之初",
        "hasChapterTitleInContent": true,
        "isR18": false
      }
    ]
  }
]
```

## 如何新增小說與章節

1. **新增小說資料夾**：在 `novels/` 中建立新資料夾（英文或拼音命名）。
2. **新增章節檔案**：每章以 `.md` 格式儲存至資料夾。
3. **圖片**：章節若含圖片，請在該小說資料夾中建立 `img/` 子資料夾。
4. **更新 filelist.json**：
   - `file`：章節檔名，如 `ch01.md`
   - `title`：章節顯示名稱
   - `hasChapterTitleInContent`：是否移除第一行標題
   - `isR18`：是否為限制級章節
   - `img`、`imgWidth`、`imgHeight`：圖片檔名與尺寸

## 版權

© 2025. All rights reserved.