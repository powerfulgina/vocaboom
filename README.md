# Vocaboom 單字練習簿

## 開發方式

- 整個專案就是單一 index.html，直接編輯即可
- push 到 main 分支後，Netlify 會自動部署到 https://vocaboom.netlify.app/
- 開始前請先設定 git config --global user.name 和 user.email

## Firebase

- Firebase config 已內嵌在 index.html 中（專案 ID：vocabapp-3586e）
- 使用服務:Authentication(匿名登入)+ Firestore
- 運作方式:開啟網站自動匿名登入,每個裝置有專屬 userId
- 資料結構:
  - 750 個單字內容寫死在 index.html 中(Firestore 不存單字)
  - 集合 `users`:文件以 userId 命名,`words` 欄位記錄各單字的記憶進度
- 注意:進度綁定匿名帳號,清瀏覽器資料或換裝置會重新開始
- Firebase Console 權限請向 Gina 申請

## 功能狀態

- ✅ 已完成:單字閃卡、7 格記憶進度、三分類、搜尋、隱藏已熟記、雲端進度同步