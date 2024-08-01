# MineSweeper Build
## 1. 規則介紹
在自訂範圍的地圖內進行探索，若該地面為地雷則遊戲結束，若非地雷則根據周遭地雷數是否為```0```而連續探索，直到找出所有地雷位置獲得勝利。
## 2. 程式碼介紹
### MineSweeperGrid
用來儲存和查找地圖資訊
1. Reset：根據指定範圍重製地圖
2. BuryMine：根據指定數量再隨機位置埋藏地雷，並回傳所有地雷位置
3. Detected：偵查指定位置是否為地雷，```-1```為地雷，```0~8```為周遭地雷數量
### MineSweeperQuery
用來儲存和查找地圖及地圖資訊及探索狀態
1. AllMine：當前地圖所有地雷的位置
2. Size：當前地圖範圍
3. MineCount：當前地圖地雷數量
4. Detected：紀錄指定位置當次探索已偵查
5. IsDetected：檢查指定位置當次探索是否偵查
6. GetDetected：取得並清除所有檢查位置並回傳所有為空地的位置
7. SetMine：紀錄所有地雷位置
### MineSweeperModel
執行遊戲動作及檢查遊戲狀態
1. Start：指定地圖範圍及地雷數量並開始遊戲
2. Detected：指定位置開始探索，回傳```false```為採種地雷遊戲失敗，```true```為找到空地，繼續遊戲
### Timer
遊戲計時器
1. Interval：計時間隔
2. Enable：計時狀態
3. Start：開始計時
4. Stop：停止計時
## 3. 使用資源
圖片資源：https://opengameart.org/content/minesweeper-tile-set
