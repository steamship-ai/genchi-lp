# ゲンチ LP

自治体ごとに独立した、画像とテキストのみで構成する静的LPです。GitHub Pagesで公開します。

## ページを追加する

`lp/` 配下に自治体ごとのフォルダを追加し、その中にページで使うものをすべて置きます。

```text
lp/<municipality-slug>/
├── index.html
├── styles.css
└── assets/
    └── ...
```

たとえば `lp/sample-city/` は `https://steamship-ai.github.io/genchi-lp/sample-city/` で公開されます。全体のトップページは設けません。

## 公開

`main` ブランチへのpushで、GitHub Actionsが `lp/` だけをGitHub Pagesへ公開します。
