# Codex HTML 簡報

這個專案已初始化為 HTML / Reveal.js 簡報工作區，並包含一份公開簡報：

- `index.html`: HTML is the new Markdown? AI Agent 輸出格式之爭

已套用的懶人包：

- GitHub: https://github.com/mathruffian-dot/claude-html-slide-builder
- Codex skill 管理位置: `C:\Users\SC-ENGINEER\.codex\skills\html-slide-builder`
- Claude Code 相容位置: `C:\Users\SC-ENGINEER\.claude\skills\html-slide-builder`
- Codex 端已整合 SOIL portable HTML 子模式，可在需要單檔可攜 HTML、Chart.js、可排序表格、決策樹或 SOIL 教學節奏時使用。
- 目前這份簡報使用 Reveal.js / GitHub Pages 模式，已加入文字雲、投票、VIZ 滑桿、功能標記頁與背景素材。

目前狀態：

- Python / Pillow 可用
- GitHub CLI 可用
- Firebase 使用懶人包預設示範專案 `teacherstudy-109ef`
- Draw Skill 尚未安裝
- `OPENAI_API_KEY` 尚未設定
- 因 Draw Skill / OpenAI API key 尚未設定，這版背景先用本專案可控 SVG 視覺素材替代 AI 生圖。

使用方式：

在 Codex / Claude Code 中提供教材、講稿或大綱，要求轉成 HTML 互動簡報或 Reveal.js 簡報。

本專案的 `index.html` 可直接用瀏覽器開啟，也可透過 GitHub Pages 發布。

## 本次試做踩坑

- `html-slide-builder` 的 `[BG]`、`[ICON]`、`[INTERACT:*]`、`[VIZ]` 是生成時的內部功能標記，不應直接顯示在觀眾看到的標題或標籤中。若需要保留語意，改放在 `data-feature`、註解或 README。
- `[VIZ]` 滑桿頁不要只把兩組抽象文字互相裁切；應使用同一份內容的「前」與「後」做清楚對照，例如 Markdown 原稿 vs HTML 渲染結果，並確認 0%、50%、100% 都能讀懂。
- icon 頁要確認圖示本身有出現，標題不應靠 `[ICON]` 這種文字提醒來說明功能。
- 發布前至少檢查可見標題是否還殘留中括號功能標記：`<h1>`、`<h2>`、`.tag` 這類觀眾會看到的位置都要掃過。
- 若瀏覽器驗證因環境或額度中斷，不能視為完成；需要標明「已寫入但尚未完成實機截圖驗證」，等可執行時再補驗。
