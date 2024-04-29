# Docusaurus Website

このリポジトリは、Docusaurus（v1.14.7）を使用して構築されたウェブサイトのソースコードを管理しています。

## 必要条件

- Node.js（v14以上）
- npm（v6以上）

## インストール

1. リポジトリをクローンします。
   git clone https://github.com/your-username/your-repo.git

2. プロジェクトディレクトリに移動します。
   cd your-repo

3. 依存関係をインストールします。
   cd website
   npm install

## ローカルでの開発

1. `website`ディレクトリに移動します。
   cd website

2. ローカル開発サーバーを起動します。
   cd website
   npm run start

3. ブラウザで`http://localhost:3000`を開き、サイトを確認します。

## ビルド

1. 静的ファイルを生成します。
   cd website
   npm run build

   生成された静的ファイルは、`website/build/docusaurus`ディレクトリに出力されます。

## デプロイ

このプロジェクトは、GitHub Pagesを使用してデプロイされます。以下の手順に従ってデプロイを行います。

1. `main`ブランチに変更をコミットし、プッシュします。

2. 以下のコマンドを実行して、静的ファイルを生成します。
   cd website
   npm run build
   cd ..

3. `gh-pages`ブランチに切り替えます。
   git checkout gh-pages

4. `gh-pages`ブランチのファイルを全て削除します。
   git rm -rf .

5. `website/build/docusaurus`ディレクトリの内容を`gh-pages`ブランチのルートディレクトリに移動します。
   mv website/build/docusaurus/* .

6. 不要になった`website/build/docusaurus`ディレクトリを削除します。
   rm -rf website/build/docusaurus

7. 変更されたファイルをステージングします。
   git add .

8. ステージングされたファイルをコミットします。
    git commit -m "Update GitHub Pages"
9. `gh-pages`ブランチをリモートリポジトリにプッシュします。
    git push origin gh-pages
 
    以上の手順を実行すると、GitHub Pagesを使用してサイトがデプロイされます。
    Github pages 側の設定はよしなに

## ドキュメントの編集

ドキュメントは、`docs`ディレクトリ内のMarkdownファイルで管理されています。必要に応じて、既存のファイルを編集するか、新しいファイルを追加してください。

## サイト設定

サイトの設定は、`website/siteConfig.js`ファイルで管理されています。サイトのタイトル、タグライン、ヘッダーリンクなどを変更する場合は、このファイルを編集してください。
