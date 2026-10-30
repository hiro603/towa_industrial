# CLAUDE.md

東和精密テックのコーポレートサイト（ポートフォリオ用の架空案件）。静的 HTML + SCSS、ビルドツールなし。

## 構成

- index / service / about / works（`works/` 配下に実績詳細）/ news（お知らせ詳細）/ news-list / recruit / contact / privacy / thanks / quality（品質。2026-10-30 に Figma カンプから実装）
- `assets/scss/` → `assets/css/`（FLOCSS × BEM。規約は web-coding スキルが正）
- `_assets-src/` — 書き出し前の素材置き場

## 開発

- 開発サーバー起動は dev スキル（sass watch + live-server）
- 納品前チェックは `/qa-scan` → `/pre-deploy`

## 注意

- 実績詳細（`works/*.html`）はテンプレート複製。共通部分の修正は全ページへ波及確認
- 既知の残件: `target="_blank"` の rel="noopener" 欠落が contact / index / works 系にある（security-audit が検出済み）
- 納品していない架空案件。不具合は直してよく、ページの追加も自由
- 公開デモは `~/dev/personal/portfolio2/demo/towa`。反映時は CSS の画像パスを `../img/` に書き換え、HTML の CSS 読み込みに `?v=日付` を付ける。デモにしか無い修正があるので、HTML は差分を見てから反映する
