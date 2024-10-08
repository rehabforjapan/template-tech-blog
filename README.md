# template-tech-blog

このテンプレートリポジトリを使って、各自のリポジトリを作成してください。

## 0.準備

[Zenn CLIの導入手順](https://zenn.dev/zenn/articles/install-zenn-cli#zenn-cli%E3%81%AE%E5%B0%8E%E5%85%A5%E6%89%8B%E9%A0%86)

### Node.jsのインストール

[Node.jsのインストール](https://nodejs.org/ja/download/)
[参考記事(Mac)](https://qiita.com/blue_fish/items/7440df68734f3d5ce772)

### Zenn CLIの導入

```shell
npm init --yes # プロジェクトをデフォルト設定で初期化
npm install zenn-cli # zenn-cliを導入
```

### 初回設定

```shell
npx zenn init
```

### (Zenn CLIのアップデート)

```shell
npm install zenn-cli@latest
```

## 1.記事作成

[Zenn CLIで記事・本を管理する方法](https://zenn.dev/zenn/articles/zenn-cli-guide)

```shell
# npx zenn new:article
npx zenn new:article --slug 記事のスラッグ --title タイトル --type idea --emoji ✨
```

### 画像挿入

`images/{slug}/{***}` に画像を配置して、記事内で以下のように記述する。
[GitHubリポジトリ連携で画像をアップロードする方法](https://zenn.dev/zenn/articles/deploy-github-images)

```markdown
![画像の説明](/images/{slug}/{***})
```

## 2.記事のプレビュー

```shell
npx zenn preview
```

## 3.記事を公開する

Front Matterで
`published: true`
を指定することで公開される

## 4.記事をRehabのPublicationに追加する

Front Matterで
`publication_name: "rehabforjapan"` を指定することで、RehabのPublicationに追加される

## 4.PRレビュー

レビューを受ける

### レビュアーとなる人

- チーム/グループの誰かがレビューする
  - マネージャが促していく
  - それでもレビューアがいない場合は、マネージャーかTechBlog有志メンバーが見る
- 最終チェック： CTO
  - コンプラチェック程度
