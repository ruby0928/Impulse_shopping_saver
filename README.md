# 💸 購物慾望與股票換算器 (Shopping Impulse Saver)

這是發想自一篇threads貼文的理財輔助工具。透過將消費金額即時換算為等值的台股標的（如台積電、0050），並計算其五年後的複利價值，幫助使用者在衝動購物前重新評估金錢的「機會成本」。

---

## 🚀 技術亮點

### 1. 即時金融數據串接 (Real-time API)
* 透過 **FinMind API** 串接台股即時數據，確保換算基礎符合當前市場行情。
* **智能日期判定：** 內建邏輯自動判斷台股開收盤時間與週末，若當日數據尚未更新，將自動抓取前一交易日之收盤價，確保系統不因非交易日而中斷。

### 2. 前端效能與資源優化 (Performance Optimization)
* **LocalStorage 持久化快取：** 實作瀏覽器端快取機制，將抓取到的股價暫存一小時。
* **減少冗餘請求：** 透過快取機制，有效節省 API 配額，並顯著提升使用者在重複查詢時的反應速度（秒出結果）。

### 3. 機會成本視覺化 (Opportunity Cost Calculation)
* **五年複利模擬：** 內建複利公式計算功能，以年化報酬率 5% 為基準，展示該筆消費若投入市場五年後的預期價值。
* **數字格式化：** 使用 `toLocaleString()` 實作千分位符號，提升財務數據的閱讀專業感。

### 4. 響應式 UI 設計 (Modern UI/UX)
* 使用 **Tailwind CSS** 建構輕量化、現代化的響應式介面，適配手機與電腦操作。

---

## 🛠 使用技術

- **Frontend:** HTML5, JavaScript (ES6+), Tailwind CSS
- **API:** [FinMind Data](https://finmindtrade.com/)
- **Storage:** Browser LocalStorage
- **Deployment:** GitHub Pages

---

## 📈 未來優化方向

本專案預計於未來加入以下功能：
- **Server-side Caching:** 導入 GitHub Actions 定時執行腳本，實現後端層級的快取，徹底解決多使用者環境下的 API 配額限制。
- **數據視覺化：** 引入 Chart.js，以圖表形式呈現「消費 vs 投資」的成長曲線對比。

