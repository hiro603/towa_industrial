# CLAUDE.md

トーワ工業のコーポレートサイト（クライアント案件）。静的 HTML + SCSS、ビルドツールなし。

## 構成

- index / service / quality / works（`works/` 配下に実績詳細）/ news / recruit / contact / privacy / thanks
- `assets/scss/` → `assets/css/`（FLOCSS × BEM。規約は web-coding スキルが正）
- `_assets-src/` — 書き出し前の素材置き場

## 開発

- 開発サーバー起動は dev スキル（sass watch + live-server）
- 納品前チェックは `/qa-scan` → `/pre-deploy`

## 注意

- 実績詳細（`works/*.html`）はテンプレート複製。共通部分の修正は全ページへ波及確認
- 既知の残件: `target="_blank"` の rel="noopener" 欠落が contact / index / works 系にある（security-audit が検出済み）
- 納品済み案件。追加要望はまず scope-negotiation スキルでスコープ判定
