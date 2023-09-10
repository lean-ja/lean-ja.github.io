# README

lean ja のウェブサイトです．

## 開発方法

ローカルにプレビューする方法を書きます.

* このサイトは Rust 製の静的サイトジェネレータである，Zola を用いています．まず[インストール手順](https://www.getzola.org/documentation/getting-started/installation/)に従って Zola をインストールします．

* このリポジトリを clone します

```bash
git clone https://github.com/lean-ja/website.git
cd website
```

* Zola の juice テーマを gitsubmodule を用いてインストールするために，`git submodule update --init` を実行します．

* `zola serve` を実行し，`Web server is available at ...` とあるところをクリックします．