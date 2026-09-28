# Week 01 學習筆記：GitHub 與開發環境建立

## 本週任務

1. 建立 GitHub 帳號。
2. 安裝 Git 與 Visual Studio Code。
3. 建立名為 `115WEB_412631508` 的 Repository。
4. 在 C 槽建立 `Projects` 資料夾。
5. 將 Repository clone 到 `C:\Projects\115WEB_412631508`。

## Git 與 GitHub 的差異

| 項目 | Git | GitHub |
|---|---|---|
| 性質 | 本機的版本控制工具 | 線上的 Repository 託管與協作平台 |
| 執行位置 | 自己的電腦 | 網路服務 |
| 主要用途 | 記錄版本、比較差異、回溯 | 備份、分享、團隊協作 |
| 是否需要網路 | 基本操作不需要 | 上傳與下載需要 |

一句話記法：Git 是「管理版本的工具」，GitHub 是「放 Git 專案的線上空間」。

## 為什麼需要版本控制

只靠檔名分版本會變成這樣：

```text
index_final.html
index_final2.html
index_final_really_final.html
```

改用 Git 之後可以：

- 留下每次修改的說明與時間。
- 隨時比對前後差異，改壞了也找得回來。
- 多人同時在同一個專案上分工。
- 讓 Repository 本身就是學習歷程的紀錄。

## 實際執行的指令

確認 Git 安裝成功：

```powershell
git --version
```

建立工作資料夾並 clone：

```powershell
cd C:\
mkdir Projects
cd C:\Projects
git clone https://github.com/ianhsuHW/115WEB_412631508.git
cd C:\Projects\115WEB_412631508
code .
```

## 完成檢核

- [x] 已登入 GitHub 帳號 `ianhsuHW`。
- [x] 已建立 Repository `115WEB_412631508`。
- [x] Repository 位於自己的帳號下。
- [x] 已在 C 槽建立 `Projects` 資料夾。
- [x] 已 clone 到 `C:\Projects\115WEB_412631508`。
- [x] 已使用 VS Code 開啟該資料夾。

## 本週重點回顧

- 本週只做 Repository 建立與 clone，不做 commit 與 push。
- Repository 名稱格式為 `115web_學號`，學號必須正確替換。
- 敏感資訊（密碼、API Key、Token）絕對不放進 Repository。
