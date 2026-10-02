# 台股盤後分析網站

此專案是可部署到 GitHub Pages 的靜態網站。頁面會從臺灣證券交易所 OpenAPI 讀取最新類股指數資料；開啟時載入，且頁面保持開啟時每 5 分鐘更新。

## 發布方式

1. 將本資料夾中的檔案推送到 GitHub 儲存庫的 `main` 分支。
2. 在儲存庫 Settings → Pages 將 Build and deployment 設為 GitHub Actions。
3. 推送後由 `.github/workflows/pages.yml` 自動部署，完成後網址會顯示在 Pages 設定頁。

網站只顯示證交所目前提供的最新交易日資料；休市時會沿用最近可取得的交易日。瀏覽器需要能連線至 `openapi.twse.com.tw`。
