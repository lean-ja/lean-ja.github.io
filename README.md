# README

lean ja のウェブサイトです．

## 開発方法

ローカルにプレビューする方法を書きます.

**STEP1** このサイトは Rust 製の静的サイトジェネレータである，Zola を用いています．まず[インストール手順](https://www.getzola.org/documentation/getting-started/installation/)に従って Zola をインストールします．

**STEP2** このリポジトリを clone します．下記コマンドを実行してください．

```bash
git clone --recursive https://github.com/lean-ja/website.git
```

`--recursive` フラグは，含まれている　git submodule も同時に clone するために必要です．このリポジトリは，Zola の [juice テーマ](https://juice.huhu.io/)を submodule 経由で利用しています．

**STEP3** `zola serve` を実行し，`Web server is available at ...` とあるところをクリックします．
