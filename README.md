# 6-Month Debut Album

靜態音樂播放器，可使用 GitHub Pages 發布，並將公開 HTTPS 網址寫入 NFC 標籤。

公開網頁：https://suu03.github.io/6-month-debut-album/

## 檔案結構

```text
index.html              網頁、樣式與播放器
site.webmanifest        主畫面名稱與圖示設定
apple-touch-icon.png    iPhone 主畫面圖示
assets/
  images/               封面與藝人 logo
  icons/                分頁與網站應用程式圖示
music/                  六首音檔
```

`apple-touch-icon.png` 保留在根目錄，讓 Apple 裝置可依標準檔名尋找圖示。

## 發布

1. 將 `index.html`、`site.webmanifest`、`apple-touch-icon.png`、`assets/`、`music/` 與 `.nojekyll` 上傳至 GitHub repository 的 `main` 分支。
2. 在 repository 的 **Settings → Pages**，選擇 **Deploy from a branch**。
3. 選擇 **main** 分支與 **/(root)**，按 **Save**。
4. 等待部署完成，使用 Pages 顯示的公開網址，並確認手機可播放所有歌曲。

## NFC

在支援 NFC 寫入的手機上，使用 NFC 寫入工具新增 **URL / URI** 記錄，填入部署完成的 HTTPS 網址，再寫入 NFC 標籤。

使用另一支手機感應標籤並開啟網頁，點選播放按鈕。手機瀏覽器通常需要使用者點擊才允許播放音樂。

日後在同一個 repository 更新網頁，保持 Pages 網址不變，便不需要重新寫入 NFC。
