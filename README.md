# Forest Escape 森林露營放鬆空間

第一版作業作品。網站程式只有 `index.html` 一個檔案，CSS、JavaScript、程序化模型、紋理及合成環境音皆寫在檔案內。Three.js r180 由 CDN 載入；YouTube 播放器依使用者操作連線，因此需要網路。

## 開啟方式

建議先上傳 GitHub Pages，再用 Chrome 或 Edge 等支援 WebGPU／WebGL 2 的瀏覽器開啟。直接雙擊 HTML 可能遇到本機檔案來源、模組或 YouTube 來源辨識限制。

若電腦已安裝 Python，可在放置 `index.html` 的資料夾開啟終端機，執行：

```sh
python -m http.server 8000
```

然後在瀏覽器開啟 `http://localhost:8000`。Windows 若找不到 `python`，可改用 `py -m http.server 8000`。此方式只是本機預覽，不會公開網站。

## GitHub Pages 上傳步驟

1. 登入 GitHub，新增儲存庫，名稱例如 `forest-escape`。一般免費帳號可建立 Public 儲存庫供 Pages 使用。
2. 點 **Add file → Upload files**，將 `index.html` 上傳到儲存庫根目錄。不要只上傳 ZIP，也不要多包一層資料夾。
3. 點 **Commit changes** 儲存。
4. 到 **Settings → Pages**，在 **Build and deployment** 的 **Source** 選擇 **Deploy from a branch**。
5. 將 **Branch** 設為 `main`、資料夾設為 `/ (root)`，按 **Save**。
6. 等待部署完成。網站網址通常為 `https://你的帳號.github.io/forest-escape/`，以 GitHub Pages 顯示的實際網址為準。
7. 在自己的電腦測試一次，再用無痕視窗或另一台電腦開啟。作業可附上儲存庫網址、網站網址與規格書。

若網站回傳 404，先確認檔名是小寫 `index.html`、放置位置與 Pages 發布來源一致，再查看 GitHub 的 Actions／Pages 部署狀態。若畫面載入失敗，確認網路能連線至 `cdn.jsdelivr.net` 或 `unpkg.com`，並開啟瀏覽器硬體加速。

## 操作

| 操作 | 方法 |
| --- | --- |
| 開始體驗 | 等待初始化完成，點「進入森林」 |
| 觀看方向 | 拖曳場景；雙擊可嘗試鎖定滑鼠，Esc 退出 |
| 移動 | W／A／S／D 或方向鍵；Shift 加速 |
| 觸控 | 滑動場景轉向，使用左下方向鍵移動 |
| 回到指定位置 | 營火旁、帳篷前、森林小徑 |
| 介面 | 收合面板；H 或「沉浸模式」切換介面 |
| 自然環境音 | 分別調整風聲、營火與蟲鳴；0% 關閉該音源 |
| 音樂 | 貼上 YouTube／YouTube Music 的影片或清單網址，載入後在播放器按播放 |
| 靜音 | 自然聲音面板的「全部靜音」同時靜音環境音與已載入音樂 |

## 功能與限制

- WebGPU 優先；初始化後顯示實際後端，不支援時由 Three.js 嘗試 WebGL 2。
- 提供午後、黃昏、夜晚三種光線；這是預設切換，沒有連續日夜循環。
- 3D 模型與紋理為程式產生，環境音為即時合成，並非實景掃描或自然錄音。
- 移動限制於營地附近，具有地面高度跟隨、樹幹及主要營地物件的簡化碰撞；不是完整物理模擬。
- 載入 YouTube 後，播放器在獨立浮動視窗持續可見。關閉播放器會移除影片並停止播放。
- 不提供 YouTube Music 帳號登入、私人歌單匯入或付費訂閱功能。私人清單、動態 Mix、年齡／地區限制或禁止嵌入的內容可能無法播放。
- 載入音樂可能向 YouTube 傳送網站來源及播放相關資料；網站本身沒有後端、不建立帳號、不儲存個人資料。
- 自然音在頁面切到背景時暫停。YouTube 由官方播放器及瀏覽器決定背景播放行為。
- 桌面操作為主要驗收情境；手機有基本觸控控制，仍需實機確認效能及畫面排版。
- 已完成 JavaScript 語法、HTML 結構及無瀏覽器環境下可執行的邏輯檢查；尚未完成實際瀏覽器的 WebGPU／WebGL 畫面、音效、YouTube 與 FPS 驗收。請依規格書驗收表完成交作業前檢查。

## 素材與技術

網站中的地形、樹木、帳篷、椅子、營火、燈具及紋理由程式生成，沒有使用第三方照片或錄音。Three.js 使用 MIT 授權；透過 CDN 載入的發行檔保留其授權聲明。YouTube 影片由官方播放器提供，依各內容權利與平台條件播放。

- Three.js r180：https://github.com/mrdoob/three.js/tree/r180
- WebGPURenderer：https://threejs.org/docs/pages/WebGPURenderer.html
- YouTube IFrame API：https://developers.google.com/youtube/iframe_api_reference
- GitHub Pages：https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

版本：1.0　日期：2026 年 10 月 19 日
