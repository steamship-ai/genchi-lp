---
name: create-lp
description: Create a municipality landing page through a short, user-led interview, then implement it as a self-contained static HTML/CSS page. Use when asked to make, add, redesign, or reproduce an LP in this repository, especially when the design reference, text, or image assets must be gathered from the user.
---

# LP作成アシスタント

自治体ごとの静的LPを、必要な情報を質問で集めてから作る。推測でページの目的・素材・デザインを決めない。

## 最初に確認すること

作業前に [PROJECT.md](../../PROJECT.md) を読み、既存の `docs/` を確認する。質問は一度に詰め込まず、まず次を聞く。

> どの自治体のLPを、どのURLスラッグで作りますか？ 既存のLP（例: `docs/yokosuka/`）をベースにしますか、それとも新しいデザインにしますか？

回答に応じて、必要なものだけを続けて聞く。

- **既存デザインを流用する場合**: ベースにするフォルダと、残す要素・差し替える要素を確認する。
- **新規デザインの場合**: 目的、想定閲覧者、必要なセクション、希望する雰囲気を確認する。
- **素材**: ロゴ、写真、自治体名、掲載文、店舗情報などの提供元を確認する。既存リポジトリの素材を流用する場合も、対象を明示して了承を得る。
- **未確定事項**: 仮の文言・画像で作業してよいかを確認する。

リンク、ボタン、フォーム、JavaScriptは、ユーザーが求めない限り追加しない。必要な情報がそろうまで実装を始めない。

## 実装

1. `docs/<municipality-slug>/` を作成し、その中に `index.html`、`styles.css`、`assets/` を置く。
2. HTML/CSSとローカルアセットだけで実装する。Next.jsなどのフレームワークやビルド工程は使わない。
3. 既存ページをベースにする場合も、対象自治体フォルダへ必要なファイルを複製し、相対パスで参照する。自治体間でアセットを共有しない。
4. スマホ閲覧を最優先に、モバイルファーストで設計する。まず幅320〜430pxで余白、文字サイズ、画像比率、縦の流れを整え、PC表示はその自然な拡張として扱う。
5. スマホ幅で、画像切れ・文字の読みづらさ・横スクロールがないことを確認する。
6. 機密情報、個人情報、APIキー、非公開素材をリポジトリへ追加しない。

## 完了時

変更ファイル、公開URL（`https://steamship-ai.github.io/genchi-lp/<municipality-slug>/`）、確認結果を簡潔に伝える。`main` へのpushは `docs/` をGitHub Pagesへ反映する。
