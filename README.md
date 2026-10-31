# SPCCPS P6 AI × Swift Vibe Coding — 瀏覽器示範

小學六年級「AI × Swift Vibe Coding」五課 App 的網頁版。SwiftUI 不能在瀏覽器執行，所以每一課用**一個 HTML 檔**示範完成品的用法。

這些是課堂練習的瀏覽器替身，不是學校的正式系統。沒有電話、電郵或其他聯絡資料。

## 打開方式

不用安裝，也不用建置。

1. 雙擊 `index.html`，或雙擊任一課的 HTML。
2. 用 Chrome 或 Safari 的「開啟檔案」也可以。
3. 若想用本機伺服器（同一部電腦）：

```bash
python3 -m http.server 43123
```

然後打開 [http://127.0.0.1:43123/](http://127.0.0.1:43123/)。

上傳 Google Drive 時，用根目錄這些單檔即可。每個檔案都自包含，不靠其他檔案。

| 課 | 檔案 |
| --- | --- |
| 第一課 2048 | `SPCCPS_P6_L1_2048_demo.html` |
| 第二課 計算機 | `SPCCPS_P6_L2_Calculator_demo.html` |
| 第三課 九巴到站 | `SPCCPS_P6_L3_KMB_demo.html` |
| 第四課 學習計劃 | `SPCCPS_P6_L4_StudyPlanner_demo.html` |
| 第五課 植物辨識 | `SPCCPS_P6_L5_PlantID_demo.html` |

## 每一課在示範甚麼

- **2048**：方向鍵或手指滑動、分數、最高分、新遊戲。達成 2048 可以繼續。
- **計算機**：加、減、乘、除。先乘除，後加減。`12 + 7 × 2` 是 26，不是 38。除以 0 會顯示「不能除以 0」。畫面上分開輸入、處理、輸出。
- **九巴到站**：選路線 → 方向 → 車站 → 分鐘。少於 3 分鐘用紅色，快到顯示「即將到站」，沒有班次顯示「暫時沒有班次」。可看示範 JSON、每 30 秒更新、儲存最愛。**全部是寫死的示範數據，這個網頁不會連上 data.etabus.gov.hk。**
- **學習計劃**：功課（按截止日期排序，逾期變紅，今天不算逾期）、星期一至五時間表、25 分鐘專注 / 5 分鐘休息。功課和時間表存在瀏覽器的 localStorage。
- **植物辨識**：揀相或用示範相片。顯示中文名稱、百分比信心度、前三名、Google 搜尋。貓、書包、手會顯示「認不到」。信心度不足顯示「不確定」。**不是 Create ML，也不會呼叫付費 API。** 日記存在這部瀏覽器。

## 清除這部瀏覽器記住的資料

示範會把少量資料存在 localStorage：

- `spccps-p6-l1-2048-best`
- `spccps-p6-l3-kmb-fav`
- `spccps-p6-l4-study-planner-v1`
- `spccps-p6-l5-plant-diary-v1`

在瀏覽器清除這個網站的網站資料，就會回到最初的示範狀態。

## 發佈

目標是公開的 GitHub repo：`antluun/vibe-coding-template`。

若這個草稿還沒推上 GitHub，在已登入 `gh` 的電腦執行：

```bash
gh repo create antluun/vibe-coding-template --public --source=. --remote=github --push
```
