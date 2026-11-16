# 與你同甘，共赴蔚來

李昆蔚 & 甘育甄 的線上婚禮邀請函
2027.03.28（日）11:30・高雄翰品酒店 3F 雲廳

以錄音帶為主題：A 面是我們的過去，B 面邀請你一起錄下未來。

---

## 檔案說明

| 檔案 | 用途 |
|---|---|
| `index.html` | 邀請函本體（字型以外全部內嵌，單一檔案即可運作） |
| `og-image.jpg` | 在 LINE / FB 分享連結時顯示的預覽圖（1200×630） |
| `.nojekyll` | 讓 GitHub Pages 直接原樣發佈，不經過 Jekyll 處理 |
| `README.md` | 這份說明 |

## 上傳與開啟 GitHub Pages

1. 在 GitHub 建立一個新的 **Public** repository，例如 `wedding`。
2. 把這個資料夾裡的所有檔案上傳到 repository 根目錄
   （網頁上傳：`Add file` → `Upload files`，把檔案拖進去後按 `Commit changes`）。
   - `.nojekyll` 是隱藏檔，如果電腦看不到也沒關係，少了它網站一樣能運作。
3. 進入 repository 的 `Settings` → `Pages`：
   - Source 選 `Deploy from a branch`
   - Branch 選 `main`、資料夾選 `/ (root)`，按 `Save`
4. 等 1～2 分鐘，網址會是：
   `https://<你的帳號>.github.io/<repository 名稱>/`

## 上線後要改的一個地方：分享預覽網址

打開 `index.html`，在最上面找到這兩行，把 `YOUR-NAME` 和 `YOUR-REPO` 換成你的帳號和 repository 名稱：

```html
<meta property="og:url" content="https://YOUR-NAME.github.io/YOUR-REPO/">
<meta property="og:image" content="https://YOUR-NAME.github.io/YOUR-REPO/og-image.jpg">
```

改完後，在 LINE 貼上連結就會出現酒紅桌巾＋錄音帶的預覽圖。
（LINE 會快取預覽，如果改完還是舊的，過一陣子再試，或在網址後面加 `?v=2`。）

## 分享建議

- **LINE 分享時**，在網址後面加上 `?openExternalBrowser=1`，LINE 會直接用手機瀏覽器開啟，動畫和版面最完整：
  `https://<你的帳號>.github.io/<repository 名稱>/?openExternalBrowser=1`
- **Wix**：可以在 Wix 頁面放一個按鈕連到上面的網址；或用「嵌入程式碼 → 嵌入網站」貼上網址嵌入。

## 小機關

- **預覽倒數彩蛋**：連點主視覺的「甘蔚」印章 5 下，上方會出現預覽提示，點提示可依序預覽：
  就是今天 → NOW PLAYING → 今天錄好了 → 婚後第 10 天 → 第 520 天 → 第 1314 天 → 回到現在。
- 彩蛋階段依時間自動切換：
  - 3/28 以前：倒數到 11:30
  - 3/28 00:00 起：「就是今天」＋導航按鈕
  - 3/28 11:30 起：「正在播放中」
  - 3/28 15:00 起：「B 面的第一首，今天錄好了」，回覆按鈕換成「謝謝你來」
  - 3/29 起：「B 面已經錄了 N 天」

## 之後要補的內容（在 index.html 裡搜尋即可找到）

- 回覆截止日期：搜尋 `○ 月 ○ 日`
- A 面三首歌的故事內文：搜尋 `（待補：`
- 照片：搜尋 `class="ph"`（目前是斜線底的佔位框）

照片準備好後，也可以直接把照片和文字交給 Claude 更新。
