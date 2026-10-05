# Week 03 學習筆記：HTML 網頁基礎

## 本週流程

```text
建立 index.html
   ↓
撰寫 HTML 文件結構
   ↓
加入文字、連結、圖片與清單
   ↓
加入表格與語意化區塊
   ↓
在瀏覽器檢查結果
   ↓
git add → git commit → git push
```

## 本週成果

```text
Week03
├── index.html     首頁：自我介紹、興趣清單、步驟、課程進度表
├── about.html     關於我：基本資料表、興趣詳細介紹
├── images
│   └── profile.jpg
└── README.md
```

## HTML、CSS、JavaScript 的分工

| 技術 | 角色 | 例子 |
|---|---|---|
| HTML | 結構與內容 | 標題、段落、圖片、表格 |
| CSS | 外觀與版面 | 顏色、字型、間距 |
| JavaScript | 行為與互動 | 按鈕事件、表單檢查 |

## 基本觀念

- **元素**：開始標籤 + 內容 + 結束標籤，例如 `<p>段落</p>`。
- **空元素**：沒有結束標籤，例如 `<img>`、`<meta>`。
- **屬性**：寫在開始標籤裡，格式是 `name="value"`，例如 `href`、`src`、`alt`。
- **巢狀結構**：元素可以包在其他元素裡，但要按順序正確關閉。

## 文件基本結構

| 元素 | 用途 |
|---|---|
| `<!DOCTYPE html>` | 宣告為 HTML5 文件 |
| `<html lang="zh-Hant">` | 根元素，標示繁體中文 |
| `<head>` | 編碼、標題等設定，不會顯示在頁面 |
| `<meta charset="UTF-8">` | 避免中文亂碼 |
| `<meta name="viewport" ...>` | 手機正確縮放 |
| `<title>` | 瀏覽器分頁標題 |
| `<body>` | 頁面上看得到的內容 |

## 常用元素整理

| 元素 | 用途 |
|---|---|
| `h1`～`h6` | 標題層級，一頁一個 `h1`，不跳層 |
| `p` | 段落 |
| `strong` / `em` | 重要內容／語氣強調 |
| `a href` | 連結；外部連結加 `target="_blank" rel="noreferrer"` |
| `img src alt` | 圖片，`alt` 寫替代文字 |
| `ul` / `ol` / `li` | 無序清單／有序清單／清單項目 |
| `table` `caption` `thead` `tbody` `tr` `th` `td` | 表格結構 |
| `div` / `span` | 沒有語意的區塊／行內容器 |

## 語意化元素

| 元素 | 用途 | 本週頁面中的使用 |
|---|---|---|
| `header` | 頁首 | 網站標題與導覽 |
| `nav` | 導覽連結 | 首頁、關於我、外部連結 |
| `main` | 主要內容 | 每頁一個 |
| `section` | 有標題的區段 | 自我介紹、興趣、課程進度 |
| `footer` | 頁尾 | 版權宣告 |

能用語意化元素就不要全部用 `div`，對搜尋引擎、螢幕閱讀器和維護都比較好。

## 表格的 scope

- `thead` 裡的欄標題用 `<th scope="col">`（index.html 的課程進度表）。
- 每列開頭的列標題用 `<th scope="row">`（about.html 的基本資料表）。

## 檢查方式

1. 存檔後用瀏覽器開啟 `index.html`，重新整理。
2. 點過所有連結，確認首頁與關於我可以互相連回。
3. 按 `F12` 開啟開發者工具，在 Elements 看結構、在 Console 看錯誤。
4. 圖片破圖時，先檢查 `src` 路徑與檔名大小寫。

## Git 紀錄

```powershell
git status
git add Week03/
git commit -m "Add Week 3 HTML personal introduction pages"
git log --oneline
git push
```

## 完成檢核

- [x] 已建立結構完整的 `index.html`。
- [x] 已正確使用 `h1`、`h2` 與段落。
- [x] 已加入外部連結與本機頁面連結。
- [x] 已加入具有 `alt` 的圖片。
- [x] 已加入無序清單與有序清單。
- [x] 已建立具有表頭與資料列的表格。
- [x] 已使用語意化元素組織頁面。
- [x] 已建立 `about.html` 並完成頁面互連。
- [x] 已在瀏覽器檢查頁面與所有連結。
- [x] 已建立 Git commit 並 push 到 GitHub。

## 下週預告

Week 4 使用 CSS 美化頁面：顏色、字型、間距、版面與響應式設計。
