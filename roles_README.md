# AI互動式小說角色庫

這是一個用於展示AI互動式小說角色設定、後台資料以及相關客製化GPTs的網頁應用。它提供了一個直觀且美觀的介面，讓使用者可以輕鬆瀏覽和管理各種角色資訊。

## 功能特色

*   **動態載入角色資料**：從 `rolelist.json` 檔案動態載入所有角色資訊，方便管理與更新。
*   **支援 Markdown 描述**：角色描述支援 Markdown 格式，可呈現豐富的文字內容。
*   **角色圖片輪播**：使用 Swiper.js 實現圖片輪播功能，直觀展示角色視覺形象。
*   **檔案與連結整合**：提供相關檔案（如設定文件）的下載連結，以及外部資源（如客製化 GPTs）的跳轉連結。
*   **響應式設計**：採用 Tailwind CSS 構建，確保在不同裝置上都能提供良好的瀏覽體驗。

## 如何使用

1.  **克隆儲存庫**：
    ```bash
    git clone https://github.com/yuhnmomo/yuhnmomo.github.io.git
    cd yuhnmomo.github.io
    ```
2.  **開啟網頁**：
    直接在您的瀏覽器中開啟 `roles.html` 檔案即可。

    請確保 `rolelist.json` 檔案存在於專案根目錄，並且其中定義的角色描述 Markdown 檔案路徑正確。

3.  **詳細安裝說明**：
    如需更詳細的安裝與設定指引，請參閱 `instructions.html` 檔案。

## 專案結構

```
.
├── roles.html              # 角色庫主頁面
├── rolelist.json           # 角色資料清單 (JSON 格式)
├── instructions.html       # 安裝與使用說明
├── Role/                   # 角色相關資料夾
│   ├── Dream/              # 夢境邊界角色資料
│   │   ├── 夢境邊界角色設定.md
│   │   ├── 夢境邊界後台設定.md
│   │   └── img/            # 角色圖片
│   ├── Lotus/              # 逆命書角色資料
│   │   ├── 逆命書人物設定.md
│   │   ├── 逆命書後台設定.md
│   │   └── img/            # 角色圖片
│   └── ...                 # 其他角色資料夾
└── ...
```

## 使用技術

*   **HTML5**
*   **CSS3** (使用 [Tailwind CSS](https://tailwindcss.com/) 框架)
*   **JavaScript**
*   [**Markdown-it**](https://github.com/markdown-it/markdown-it) (用於解析 Markdown 內容)
*   [**Swiper.js**](https://swiperjs.com/) (用於圖片輪播)

## 貢獻

歡迎任何形式的貢獻！如果您有任何建議或發現錯誤，請隨時提交 Issue 或 Pull Request。

## 授權

本專案採用 [MIT 授權](LICENSE)。