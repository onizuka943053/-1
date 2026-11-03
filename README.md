# NutriTrack AI 🥗⚡

智慧 TDEE 與熱量追蹤 App（純前端、資料存在本機瀏覽器）。

支援：

- AI 文字 / 照片飲食分析（**Groq** 推薦、Google Gemini）
- TDEE 計算、蛋白質目標、水分追蹤
- 常用食物、歷史趨勢圖、資料匯出匯入
- **PWA**：可安裝到手機主畫面，像原生 App 一樣使用

---

## 一、上傳到 GitHub

### 方法 A：用網頁上傳（最簡單）

1. 到 [github.com/new](https://github.com/new) 建立新 Repository  
   - Repository name 例如：`NutriTrack-AI`  
   - 選 **Public**  
   - **不要**勾選「Add a README」（我們已有檔案）
2. 建立後，點 **uploading an existing file**
3. 把本資料夾裡的所有檔案拖進去（包含 `icons` 資料夾）
4. 按 **Commit changes**

### 方法 B：用 Git 指令

```bash
cd NutriTrack-AI
git init
git add .
git commit -m "Initial commit: NutriTrack AI PWA"
git branch -M main
git remote add origin https://github.com/你的帳號/NutriTrack-AI.git
git push -u origin main
```

---

## 二、開啟 GitHub Pages（讓手機能用網址開啟）

1. 進到你的 Repo → **Settings** → 左側 **Pages**
2. **Source** 選 **Deploy from a branch**
3. Branch 選 `main`，資料夾選 `/ (root)`
4. 按 **Save**
5. 等 1～2 分鐘，會出現網址，例如：

```text
https://你的帳號.github.io/NutriTrack-AI/
```

用手機瀏覽器打開這個網址即可使用。

---

## 三、安裝成手機 App（加入主畫面）

### iPhone（Safari）

1. 用 **Safari** 打開上述網址（Chrome 在 iOS 無法完整安裝 PWA）
2. 點下方 **分享** 按鈕
3. 選 **加入主畫面**
4. 名稱可改成「NutriTrack」→ 加入

之後主畫面會有圖示，點開就是全螢幕 App 模式。

### Android（Chrome）

1. 用 **Chrome** 打開網址
2. 右上角選單 → **安裝應用程式** / **加到主畫面**
3. 確認安裝

---

## 四、第一次使用

1. 點右上角 **設定**
2. AI 引擎建議選 **Groq（免費）**
3. 到 [console.groq.com/keys](https://console.groq.com/keys) 申請免費 API Key（免綁卡）
4. 貼上 Key 後儲存
5. 即可文字或拍照分析飲食

> API Key 只存在你自己的手機瀏覽器，不會上傳到 GitHub 或任何伺服器。

---

## 五、專案結構

```text
NutriTrack-AI/
├── index.html              # 主程式（完整 App）
├── manifest.webmanifest    # PWA 設定
├── sw.js                   # Service Worker（離線快取）
├── icons/
│   ├── icon-192.png
│   ├── icon-512.png
│   └── apple-touch-icon.png
├── README.md
└── .gitignore
```

---

## 六、注意事項

- 資料（飲食紀錄、TDEE 設定）存在 **localStorage**，換瀏覽器或清除網站資料會消失；請善用「匯出備份」。
- 若更新了程式碼，重新推送到 GitHub 後，手機可能要強制重新整理，或清除該網站的快取。
- GitHub Pages 是公開網站，但 **不會** 看到你的 API Key 或飲食資料（那些只在你的裝置上）。

---

MIT License — 可自由修改與使用。
