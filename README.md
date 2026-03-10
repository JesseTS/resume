# 求職履歷專案

整理履歷內容、供求職網站使用，並有一份網頁版客製履歷。

## Project rules（專案規則）

- **履歷內容以 `content/resume.md` 為唯一來源。**
- 所有履歷相關的資料變更都必須**先**更新 `content/resume.md`，再以該檔案為參考同步至 `web/`（網頁版）。
- 若內容不一致，以 `content/resume.md` 為準。

## 資料夾結構

```
Resume/
├── content/
│   └── resume.md      ← 履歷主檔：在這裡填寫／整理內容，再複製到 104、CakeResume、LinkedIn 等
├── web/
│   ├── index.html     ← 網頁版履歷
│   └── styles.css     ← 網頁版樣式
└── README.md
```

## 使用方式

### 1. 整理履歷內容（求職網站用）

- 編輯 **`content/resume.md`**
- 依區塊填入：基本資料、工作經驗、學歷、技能、專案等
- 應徵時從這裡複製對應段落到各求職網站（104、CakeResume、LinkedIn、Yourator 等）

### 2. 網頁版履歷

- 用瀏覽器開啟 **`web/index.html`** 即可預覽
- 若要修改顯示內容：**先**在 `content/resume.md` 更新，再依主檔同步到 `web/index.html`
- 列印成 PDF：在瀏覽器按「列印」→ 選擇「另存為 PDF」，即可得到一份 PDF 履歷

### 3. 本地預覽（可選）

若想用本地伺服器看網頁版（避免部分瀏覽器對 file:// 的限制）：

```bash
cd web
# 若已安裝 Python 3
python3 -m http.server 8000
# 或若已安裝 Node.js 且已安裝 npx
npx serve .
```

再在瀏覽器打開 `http://localhost:8000`。

## 建議流程

1. 先在 **`content/resume.md`** 把經歷、學歷、技能寫完整  
2. 再依同一份內容更新 **`web/index.html`**，讓網頁版與主檔一致  
3. 應徵時從 **resume.md** 複製到各求職網站  
4. 需要時從網頁版列印 PDF 或分享連結（若之後部署到 GitHub Pages 等）
