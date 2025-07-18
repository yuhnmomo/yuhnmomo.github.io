# 線上書庫

這是一個輕量級的線上書庫應用程式，旨在提供一個簡潔、響應式且易於使用的平台，用於瀏覽和閱讀小說章節。它支援 Markdown 格式的章節內容，並具備年齡驗證功能，確保內容適合所有使用者。

## 功能特色

- **年齡驗證**：進入書庫前會顯示年齡確認提示，確保內容適合目標受眾。
- **書庫列表**：清晰展示所有小說，包含標題、作者和章節數量。
- **響應式設計**：介面適應不同螢幕尺寸（手機、平板、桌面）。
- **置頂章節選單**：在小說閱讀頁面，章節下拉選單固定在頂部，方便快速切換章節。
- **Markdown 支援**：小說章節內容支援 Markdown 語法，自動轉換為 HTML 顯示，讓排版更豐富。
- **內容自動調整**：載入章節內容時，會自動移除 Markdown 檔案的第一行（假定為章節標題），避免重複顯示。
- **簡潔的版面**：專注於閱讀體驗，移除多餘的視覺元素。

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
    ├── shia-pian-zhou/    <-- 第一本小說的資料夾 (英文或拼音命名)
    │   ├── ch01.md
    │   ├── ch02.md
    │   └── ...
    └── FleetingClouds/    <-- 第二本小說的資料夾 (英文或拼音命名)
        ├── ch00.md        <-- 序章 (可選)
        ├── ch01.md
        └── ...
```

### 2. 安裝與執行

建議使用 Visual Studio Code 及其 Live Server 擴充功能來本地運行和測試。

1. 安裝 Visual Studio Code (如果尚未安裝)。
2. 在 VS Code 中，點擊左側邊欄的擴充功能 (Extensions) 圖示 (Ctrl+Shift+X)，搜尋並安裝 Live Server。
3. 在 VS Code 中，點擊檔案 (File) > 開啟資料夾 (Open Folder...)，選擇您的 線上書庫專案 資料夾。
4. 在 VS Code 的檔案總管中，右鍵點擊 `mybooks.html` 檔案，選擇 Open with Live Server。

這將會在您的預設瀏覽器中開啟應用程式，您就可以開始測試了。

### 3. 更新 filelist.json

`filelist.json` 檔案用於定義書庫中的所有小說及其章節資訊。請確保其格式正確，並且 `folder` 和 `file` 屬性與您的實際資料夾和檔案名稱完全匹配。

```json
[
  {
    "title": "夢境邊界",
    "folder": "shia-pian-zhou",
    "author": "法式草莓布丁",
    "chapters": [
      { "file": "ch01.md", "title": "第1章：囚禁與奇遇" },
      { "file": "ch02.md", "title": "第2章：虛假的戀人" }
    ]
  },
  {
    "title": "過眼雲煙",
    "folder": "FleetingClouds",
    "author": "法式草莓布丁",
    "chapters": [
      { "file": "ch00.md", "title": "序章 殘神紀元" },
      { "file": "ch01.md", "title": "第1章 穿越之初" }
    ]
  }
]
```

## 如何新增小說與章節

1. **新增小說資料夾**：在 `novels/` 資料夾下，創建一個新的資料夾，建議使用英文或拼音命名（例如 `my-new-novel`）。
2. **新增章節檔案**：將您的章節內容以 Markdown (.md) 格式儲存到新創建的資料夾中（例如 `my-new-novel/ch01.md`、`my-new-novel/ch02.md`）。
3. 請確保每個 `.md` 檔案的第一行是章節標題，因為程式碼會自動移除這第一行以避免重複顯示。
4. **更新 `filelist.json`**：
   - 在 `filelist.json` 陣列的末尾，添加一個新的小說物件。
   - 填寫 `title`（小說標題）、`folder`（您在步驟 1 中創建的資料夾名稱）和 `author`。
   - 在 `chapters` 陣列中，為每個章節添加一個物件，包含 `file`（章節的檔名，如 `ch01.md`）和 `title`（章節在選單中顯示的標題）。如果需要，可以添加 `note` 屬性來顯示額外資訊。

## 版權

© 2025. All rights reserved.
