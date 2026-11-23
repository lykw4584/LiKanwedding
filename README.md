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

## 分享預覽網址（已填好）

`index.html` 最上面這兩行已經填好你們的網址，不用再改：

```html
<meta property="og:url" content="https://lykw4584.github.io/LiKanwedding/">
<meta property="og:image" content="https://lykw4584.github.io/LiKanwedding/og-image.jpg">
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
- A 面三首歌的歌詞：改 `lyrics.json`（見下方說明），不用動 index.html
- A 面相簿照片：見下方「替換相簿照片」
- 歌詞本裡每首歌的照片：見下方「替換相簿照片」的歌詞本照片表

照片準備好後，也可以直接把照片和文字交給 Claude 更新。

## 填歌詞：lyrics.json

歌詞放在獨立的 `lyrics.json`，網頁打開時會自動帶入。在 GitHub 網頁上就能改：

1. 點 `lyrics.json` → 右上角鉛筆圖示（Edit）
2. 把文字貼在 `""` 兩個引號中間：`ja` 放日文、`zh` 放中文
3. **換行請打 `\n`**（例如 `"第一行\n第二行"`），不要直接按 Enter
4. 歌詞裡如果有半形雙引號 `"`，請改成全形「」或 “ ”
5. 按 `Commit changes`，等 1～2 分鐘重新整理網頁

```json
{
  "A1": { "ja": "日文第一行\n日文第二行", "zh": "中文第一行\n中文第二行" },
  "A2": { "ja": "", "zh": "" },
  "A3": { "ja": "", "zh": "" }
}
```

留空的欄位會繼續顯示「（歌詞）」「（中文翻譯）」。
※ lyrics.json 只在 GitHub Pages 上有效；直接用手機打開 index.html 檔案預覽時不會讀取。

## 替換相簿照片（「← 左右滑動，或拖曳照片 →」那一區）

照片放在 `photos/` 資料夾，檔名固定：

| 順序 | 檔名 |
|---|---|
| 第 1 張 | `photos/gallery-1.jpg` |
| 第 2 張 | `photos/gallery-2.jpg` |
| 第 3 張 | `photos/gallery-3.jpg` |
| 第 4 張 | `photos/gallery-4.jpg` |

歌詞本裡每首歌點開後的照片也在同一個資料夾：

| 歌曲 | 檔名 |
|---|---|
| A1『戀』 | `photos/song-1.jpg` |
| A2『キセキ』 | `photos/song-2.jpg` |
| A3『Stand by me, Stand by you.』 | `photos/song-3.jpg` |

結尾配圖（TO BE CONTINUED 上方）：`photos/ending.jpg`

### 調整照片裁切位置

照片超出框的部分會被裁掉。在 index.html 搜尋照片檔名（例如 `song-3.jpg`），同一行有 `object-position:50% 95%`：
- 第二個數字是**上下**位置：0% ＝ 保留最上面、100% ＝ 保留最下面。天空太多就把數字調大
- 第一個數字是左右位置，通常維持 50%（置中）

目前設定：song-1 80%、song-2 75%、song-3 95%、ending 80%、相簿 50%

**換照片**：在 GitHub 進入 `photos` 資料夾 → `Add file` → `Upload files`，上傳**同檔名**的新照片（例如新的 `gallery-2.jpg`）就會直接覆蓋，不用動 index.html。

- 建議直式照片（2:3，例如 1000×1500），超出比例的部分會自動裁切置中
- 檔案建議壓在 300KB 以內，手機開起來比較快
- **換順序**：把檔名互換即可
- **加第 5 張以上**：在 index.html 搜尋 `gallery-4.jpg`，把那一整行複製一行貼在下面，改成 `gallery-5.jpg`，再上傳 `photos/gallery-5.jpg`
- 換完如果手機還是看到舊照片，是瀏覽器快取，重新整理或等幾分鐘即可
