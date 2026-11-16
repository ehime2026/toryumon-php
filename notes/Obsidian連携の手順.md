# Obsidian連携の手順

パソコン側でやる作業です。最初の1回だけ必要です。
[[ようこそ]] に戻る。

## しくみ

```
Claude  ⇄  GitHub (toryumon-php)  ⇄  あなたのパソコンのObsidian
```

GitHubを「共有の置き場」にして、ClaudeとObsidianの両方がそこを見ます。

## 手順1：プルリクエストを取り込む

1. Claudeが案内したプルリクエストのページを開く。
2. 緑色の「Merge pull request」ボタンを押す。
3. 続けて「Confirm merge」を押す。

これでノートが `main`（本体）に入ります。

## 手順2：リポジトリをパソコンにダウンロードする

1. [GitHub Desktop](https://desktop.github.com/) をインストールする。
2. GitHubのアカウントでサインインする。
3. メニューの「File」→「Clone repository」を選ぶ。
4. 一覧から `ehime2026/toryumon-php` を選び、「Clone」を押す。
5. 保存先のフォルダの場所を覚えておく（例：ドキュメント/GitHub/toryumon-php）。

## 手順3：Obsidianで開く

1. Obsidianを起動する。
2. 左下の保管庫アイコン →「フォルダを保管庫として開く」を選ぶ。
3. 手順2でダウンロードした `toryumon-php` フォルダを選ぶ。
4. 左の一覧に `notes` フォルダが出て、「ようこそ」が開ければ成功。

## 手順4：自動で同期されるようにする

1. Obsidianの「設定」→「コミュニティプラグイン」を開く。
2. 「コミュニティプラグインを有効化」を押す。
3. 「閲覧」を押して `Git` を検索し、「Git」（作者：Vinzent）をインストールして有効化する。
4. 「設定」→「Git」を開き、次の2つに数字を入れる。
   - Auto commit-and-sync interval (minutes)：`10`
   - Auto pull interval (minutes)：`10`

これで10分ごとに、あなたのノートがGitHubへ送られ、Claudeのノートが届きます。

うまく動かない場合は、パソコンにGit本体が必要なことがあります。
[Gitの公式サイト](https://git-scm.com/downloads) からインストールして、Obsidianを再起動してください。

## 覚えておくこと

- **Claudeが書いたノート**は、プルリクエストを「Merge」した後にObsidianへ届きます。
- **今までのノート**は自動では移りません。使いたいものは `notes` フォルダにコピーしてください。
- **公開範囲**：このリポジトリが「Public」の場合、ノートは誰でも読めます。個人的な内容を書く前に、GitHubのリポジトリ設定で「Private」になっているか確認してください。
- **スマホ**：この方法はパソコン向けです。スマホのObsidianでは同期の設定が別に必要です。
