# README

lean ja のウェブサイトです．

## 開発方法

ローカルにプレビューする方法を書きます.

* このサイトは Rust 製の静的サイトジェネレータである，Zola を用いています．まず[インストール手順](https://www.getzola.org/documentation/getting-started/installation/)に従って Zola をインストールします．

* このリポジトリをして，Zola の juice テーマを gitsubmodule を用いてインストールします．

```bash
git clone https://github.com/lean-ja/website.git
cd website
git pull --recurse-submodules
```

* `zola serve` を実行し，`Web server is available at ...` とあるところをクリックします．