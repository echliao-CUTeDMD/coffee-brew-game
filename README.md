# ☕ 手沖咖啡模擬器 Coffee Brew Simulator

一個純前端的手沖咖啡模擬遊戲。選豆、調參數、親手注水,最後看萃取率與風味評分。
單一 HTML 檔案,不需要建置、不需要安裝套件,支援滑鼠與手機觸控。

## 玩法

1. 選擇咖啡豆(淺焙、中焙、深焙),調整研磨度與水溫。
2. 勾選「進階模式」可自訂粉量、總注水量、悶蒸水量、悶蒸時間、注水速度。
3. 按住畫面注水,讓水壺跟著虛線水圈移動(滑鼠按住左鍵,或手指按住畫面)。
4. 先悶蒸,再繞圈注水到目標水量,等咖啡滴完。
5. 查看萃取率(理想 18–22%)、濃度 TDS、沖煮時間、注水穩定度與總分。

畫面上可切換「側面剖視」與「正視角(俯視濾杯)」兩種視角。

## 本機執行

直接用瀏覽器開啟 `index.html` 即可。也可以用任意靜態伺服器:

```bash
python3 -m http.server 8000
# 然後開啟 http://localhost:8000
```

## 部署到 GitHub Pages

專案已附上 GitHub Actions 設定(`.github/workflows/pages.yml`):

1. 把整個資料夾推上 GitHub 儲存庫的 `main` 分支。
2. 到儲存庫的 **Settings → Pages**,把 **Source** 設為 **GitHub Actions**。
3. 之後每次推送到 `main` 都會自動部署,網址為 `https://<你的帳號>.github.io/<儲存庫名稱>/`。

如果不想用 Actions,也可以在 Pages 設定選擇 **Deploy from a branch**,分支選 `main`、資料夾選 `/ (root)`。

## 檔案結構

```
.
├── index.html                 遊戲本體(HTML、CSS、JavaScript 全在這一個檔案)
├── README.md
├── LICENSE
├── .gitignore
└── .github/workflows/pages.yml
```

## 備註

- 字型使用 Google Fonts(Noto Sans TC、Noto Serif TC),離線時會改用系統字型。
- 萃取模型是為了遊戲體驗簡化過的,不代表真實的咖啡化學。

## 授權

MIT License,詳見 [LICENSE](LICENSE)。
