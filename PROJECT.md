# ゲンチ LP プロジェクトガイド

## 目的

自治体ごとに、画像とテキストだけで構成する簡易的な静的LPを管理・公開するリポジトリです。GitHub Pagesで公開します。

## 構成

```text
lp/
└── <municipality-slug>/
    ├── index.html
    ├── styles.css
    └── assets/
        └── ...
```

- 自治体ページは `lp/<municipality-slug>/` に置く。
- 1自治体のHTML・CSS・画像などは、その自治体フォルダ内で完結させる。
- ページごとにデザインが異なってよい。共通コンポーネントや共通CSSは前提にしない。
- リポジトリ直下のトップページは作らない。

## 実装方針

- ビルド不要のHTML/CSS/ローカルアセットのみを使う。
- 外部リンク、ボタン、フォーム、JavaScriptは、依頼がない限り追加しない。
- レスポンシブ表示と日本語表示を確認する。
- 新しいページには、意味のある英小文字・ハイフン区切りのスラッグを使う。
- APIキー、トークン、パスワード、個人情報、非公開の画像・資料などの機密情報は、このリポジトリ内に置かない。

## 公開

- GitHub Pagesには `lp/` ディレクトリだけを公開する。公開はGitHub Actionsで行う。
- `lp/sample-city/` の公開URLは `https://steamship-ai.github.io/genchi-lp/sample-city/`。
- GitHub Freeの組織では、Pages公開用リポジトリをPublicにする。
