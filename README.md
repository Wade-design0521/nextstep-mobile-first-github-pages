# 下一步｜解題練習室（Mobile-First）

手機版優先的繁體中文網頁 App，將「提示階梯」與「個人解題日誌」整合在一起。採用原生 HTML、CSS、JavaScript，不需建置工具，適合直接部署到 GitHub Pages。

## 功能

- 手機優先介面：觸控尺寸、底部導覽、單欄流程與安全區留白。
- 桌面響應式介面：寬螢幕自動切換為側邊導覽與雙欄解題版面。
- 提示階梯：理解問題、拆解步驟、思考原因、選擇方法、檢查結果與反思。
- 個人解題日誌：儲存、搜尋、篩選、查看與刪除紀錄。
- 備份與還原：可將日誌匯出成 JSON 並從備份匯入。
- PWA 基礎支援：manifest 與 service worker，部署到 HTTPS 網站後可從支援的瀏覽器加入主畫面；快取部分網站檔案供離線開啟。
- 本機資料儲存：日誌存在使用者自己的瀏覽器，不會自動上傳至伺服器。

## GitHub Pages 部署

1. 在 GitHub 建立一個 **Public** repository，例如 `nextstep-solver`。
2. 將本資料夾內的所有檔案上傳至 repository 根目錄（`index.html`、`manifest.webmanifest`、`sw.js`、`icon.svg`、`icon-192.png`、`icon-512.png`、`apple-touch-icon.png`、`README.md`、`.nojekyll`）。
3. 前往 repository 的 **Settings → Pages**。
4. Source 選 `Deploy from a branch`；Branch 選 `main`，目錄選 `/(root)`，按 `Save`。
5. 等部署完成後，Pages 會提供公開網址，通常為 `https://你的帳號.github.io/nextstep-solver/`。
6. 使用手機瀏覽該網址測試。若要加到主畫面，使用瀏覽器的「加入主畫面」或「安裝應用程式」功能（依裝置與瀏覽器而異）。

## 資料與隱私限制

- 這是無後端的靜態 App。每位訪客的日誌存在自己的瀏覽器 `localStorage`，其他訪客不能直接看到。
- 清除瀏覽器網站資料或更換裝置可能造成紀錄遺失；可使用日誌頁面的 JSON 匯出／匯入功能備份與搬移。
- 目前沒有帳號、雲端同步、多裝置同步或多人共用資料庫。
- 避免在紀錄中輸入密碼、身分證號等敏感資料。

## 本機預覽

可直接用現代瀏覽器開啟 `index.html`。PWA 安裝與離線快取功能需透過 HTTPS 網站（例如 GitHub Pages）或 localhost 才會啟用。
