# 貢獻指南 (Contributing to CHN Launcher)

感謝你願意為 CHN Launcher 做出貢獻！

## 參與方式

1. **譯名對照庫補齊**：歡迎在 `data/translations.json` 補充未收錄的兩岸遊戲譯名。
2. **修復 Bug / 開發新特性**：
   - Fork 本倉庫。
   - 建立特性分支：`git checkout -b feature/your-feature-name`。
   - 確保 Rust 與前端程式碼通過格式檢查（`cargo fmt` & `pnpm lint`）。
   - 提交 PR 並清晰描述修改內容。
3. **平台適配**：若欲新增支援之遊戲平台，請在 `src-tauri/src/scanner/` 下新增對應的掃描解析器。

## 提交規範 (Commit Convention)

- `feat:` 新增功能
- `fix:` 修復問題
- `style:` UI / 視覺樣式調整
- `docs:` 文件更新
- `refactor:` 重構代碼
