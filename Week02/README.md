# Week 02 學習筆記：Git 基礎與版本控制

## 本週流程

```text
修改檔案
   ↓
git status   查看哪些檔案有變動
   ↓
git diff     查看實際改了哪幾行
   ↓
git add      放進暫存區
   ↓
git commit   建立本機版本紀錄
   ↓
git log      查看提交歷史
   ↓
git push     同步到 GitHub
```

## Git 的四個位置

| 位置 | 意義 | 進入此處的指令 |
|---|---|---|
| 工作目錄 Working Directory | 目前正在編輯的檔案 | 直接編輯並存檔 |
| 暫存區 Staging Area | 下一次 commit 要記錄的修改 | `git add` |
| 本機 Repository | 已經 commit 的版本歷史 | `git commit` |
| 遠端 Repository | GitHub 上的備份與協作位置 | `git push` |

`git pull` 方向相反，是把遠端的最新內容拉回本機。

## 設定使用者資訊

```powershell
git config --global user.name "你的姓名"
git config --global user.email "你的 GitHub 電子郵件"
```

查看目前設定：

```powershell
git config --global user.name
git config --global user.email
```

這組資訊只會寫進 commit 紀錄，和 GitHub 登入密碼無關。

## 常用指令整理

| 指令 | 用途 |
|---|---|
| `git status` | 查看目前檔案狀態 |
| `git diff` | 查看尚未 add 的修改 |
| `git diff --staged` | 查看已經 add 的修改 |
| `git add 檔名` | 將指定檔案加入暫存區 |
| `git add .` | 將目前資料夾的修改全部加入暫存區 |
| `git commit -m "訊息"` | 建立一筆版本紀錄 |
| `git log` | 查看完整提交歷史 |
| `git log --oneline` | 以精簡格式查看歷史 |
| `git push` | 推送本機 commit 到 GitHub |
| `git pull` | 取得並整合 GitHub 的最新內容 |
| `git restore --staged 檔名` | 把檔案移出暫存區（不會刪修改） |
| `git commit --amend -m "訊息"` | 修改最近一筆尚未 push 的 commit 訊息 |

## .gitignore

`.gitignore` 列出 Git 不應該追蹤的檔案。本 Repository 根目錄的 `.gitignore` 內容：

```gitignore
node_modules/
.env
*.log
```

不該提交的東西：

- 密碼、API Key、Token 等敏感資訊。
- `.env` 環境設定檔。
- `node_modules/` 這類可以用 `npm install` 重新產生的資料夾。
- 編輯器或作業系統的暫存檔。

`.gitignore` 檔案本身要提交，這樣其他人 clone 下來才有同一套規則。

## 本週建立的 commit

```text
Initial commit
Add Week 1 environment setup notes
Update README for Week 2
Add Git practice note
Add .gitignore for node_modules, env files and logs
```

## 常見問題筆記

| 訊息 | 原因與處理 |
|---|---|
| `Author identity unknown` | 還沒設定 user.name／user.email，設定後重新 commit |
| `nothing to commit, working tree clean` | 沒有未提交的修改，確認檔案是否已存檔 |
| `git diff` 沒有輸出 | 修改可能已經 `git add`，改用 `git diff --staged` |
| `src refspec main does not match any` | 本機還沒有任何 commit，先 commit 再 push |

## 完成檢核

- [x] 已設定 Git 使用者姓名與電子郵件。
- [x] 已修改 README.md 並儲存。
- [x] 會使用 `git status` 查看狀態。
- [x] 會使用 `git diff` 查看差異。
- [x] 已使用 `git add` 加入暫存區。
- [x] 已建立至少兩筆 commit。
- [x] 會使用 `git log --oneline` 查看歷史。
- [x] 已使用 `git push` 推送到 GitHub。
- [x] 已理解 `git pull` 的用途。
- [x] 已建立 `.gitignore`。

## 下週預告

Week 3 開始 HTML，建立 `index.html`，學習文件結構、標題、段落、連結、圖片、清單、表格與區塊元素。
