# 直笛音高挑戰 V4｜雲端曲目庫

## 檔案結構

- `index.html`：遊戲網站
- `songs.json`：曲目清單
- `songs/`：MusicXML 樂譜資料夾

## 發布到 GitHub Pages

1. 建立 GitHub repository。
2. 將本資料夾內的所有檔案與資料夾上傳到 repository 根目錄。
3. 在 GitHub repository 進入 `Settings → Pages`。
4. Source 選擇 `Deploy from a branch`。
5. Branch 選擇 `main`，資料夾選擇 `/root`，儲存。
6. 等待 GitHub Pages 產生網址後，以該網址開啟。

雲端曲目庫使用 `fetch()` 讀取 `songs.json` 和 MusicXML，因此直接雙擊
`index.html` 時，部分瀏覽器會阻擋曲目庫。直接開檔仍可使用「老師測試模式」
自行上傳 MusicXML。

## 新增歌曲

1. 從 MuseScore 匯出「已解壓縮（*.musicxml）」。
2. 將檔案放進 `songs/` 資料夾，檔名建議使用英文字母、數字與連字號。
3. 在 `songs.json` 增加一筆資料，例如：

```json
{
  "id": "little-star",
  "title": "小星星",
  "file": "songs/little-star.musicxml",
  "grade": "三年級",
  "semester": "上學期",
  "category": "基礎練習",
  "difficulty": 2,
  "defaultBpm": 72,
  "tags": ["4/4", "do-sol-la"],
  "description": "基礎音高與穩定拍練習。",
  "enabled": true
}
```

4. 提交變更。學生重新整理網站後即可看到新歌曲。

將 `"enabled"` 改成 `false`，可以暫時從學生曲目庫隱藏歌曲。
