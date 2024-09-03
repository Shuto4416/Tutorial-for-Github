# GitHubの使い方

---

## 【目次】

- [GitHubとは](#GitHubとは)

- [GitHubを使い始める前に知っておきたい知識](#GitHubを使い始める前に知っておきたい知識)

- [VSCodeでGitHubを使ってみよう](#VSCodeでGitHubを使ってみよう)
  
  - [1.既存のリポジトリを導入](#1既存のリポジトリを導入)
  
  - [2.ブランチを切ろう](#2ブランチを切ろう)
  
  - [3.ファイルを作成して変更点を反映させよう](#3ファイルを作成して変更点を反映させよう)
  
  - [4.pull requestを送ろう](#4pull-requestを送ろう)

## 【GitHubとは】

GitHubという言葉を分解すると、git（ギット）のhub（ハブ）。日本語で「拠点」の「集まり」と訳すことができます。

GitHub上では、エンジニア各々が公開用のプログラムをアップして自分以外のエンジニアに共有したり、その後、履歴を残しながら更新したり、自分以外のエンジニアも修正を加えることが可能です。

## 【GitHubを使い始める前に知っておきたい知識】

書くと長いのでこれらのサイトを参考にしてください

[GitHubの使い方を画像つきで徹底解説！初心者でもすぐ使える | 侍エンジニアブログ](https://www.sejuku.net/blog/73468)  

[【入門】VSCodeとGitHubの連携手順・使い方をわかりやすく解説 - カゴヤのサーバー研究室](https://www.kagoya.jp/howto/rentalserver/webtrend/vscode/)

## 【VSCodeでGitHubを使ってみよう】

### 1.既存のリポジトリを導入

まずVSCodeで適当なフォルダを開き、そのフォルダにリポジトリをクローンします。

ここではファイル名をTutorial-for-Github-Testとしていますが、名前はなんでもいいです。

![スクリーンショット (141)](https://github.com/user-attachments/assets/96665de1-40e3-4827-bca0-7ded8af5e4b6)
GitHub 上から「Code」のリンクをコピー  
`HTTPS`か`SSH`かを注意して、

`SSH`をコピーしてください

![スクリーンショット (143)](https://github.com/user-attachments/assets/ecf8db88-2f95-4351-8bdb-0f2171ebab1a)
VSCodeのターミナルで以下のコマンドを実行

```
$ git clone [コピーしたリンク]
```

![スクリーンショット (146)](https://github.com/user-attachments/assets/c1e95c4e-5228-47e9-919f-d1ab82b3fb77)
### 2.ブランチを切ろう

まずは今いるブランチの確認をしましょう

```git
// ブランチの確認
$ git branch
```

そうすると以下のように出力されると思います

```git
* main
```

今いるブランチは皆の作業結果をまとめる場所となるので下手に触るとまずいです

なので新しくブランチを作成し、そこに移動しましょう

```git
// ブランチを作成&移動
$ git switch -c [ブランチ名]
```

名前はわかりやすくGitHubのアカウント名にしておきましょう

再び今いるブランチを確認すると

```git
* [作成したブランチ名]
```

これが最初に出てきたら成功です

### 3.ファイルを作成して変更点を反映させよう

リポジトリの中のself-introductionsフォルダの中に`[GitHubのアカウント名].txt`を作成し、自己紹介を書いてみましょう

書き終わったら変更をステージしてリポジトリに変更を反映させる準備を行います

![Stage](https://github.com/user-attachments/assets/56ed15d2-6590-4620-9307-75b5fd3fc515)
画像の通り + マークを押すだけです

ステージされている変更の項目に自己紹介のファイルが追加されます

次にコミット前に今回の変更点について記載します

そうしないと進捗がわかりづらいですからね

![Message](https://github.com/user-attachments/assets/88bc1c9b-1396-4c36-9c33-37c5e5151b0f)
これも赤枠で囲んでる部分に入力するだけです

今回の場合だと「自己紹介文を書いたファイルを追加した」とかですね

![Commit](https://github.com/user-attachments/assets/e9327eda-5f39-4a76-afe5-efa17e4271ea)

あとは赤枠の部分を押せばコミットは完了です

### 3.リモートリポジトリに変更を反映させよう

早速リモートリポジトリに変更を反映させる前にプルを行います

以下のコマンドをVSCodeのtターミナルで実行しましょう

```git
git pull origin develop
```

これによりリモートリポジトリの最新の状態を取得できます

`Already up to date.`と出た場合は最新であるという意味になります

![Branch](https://github.com/user-attachments/assets/f79b42d7-fce8-4064-8a50-a6e0671512f4)
ここまで来たら`Branchの発行`を押してリモートリポジトリに変更を反映させます

### 4.pull requestを送ろう

変更はBranchには反映されましたが、Developのにはまだ反映されていません

他の人の作業結果とマージ(つまり合体)させる必要があります

しかし、他の人と作業結果が被るとバグが起きてしまう可能性があるので合体する前に`pull request`というものを送ってマージしても大丈夫か確認してもらいます

![Pull_Req_1](https://github.com/user-attachments/assets/4da98754-e0d7-4103-9c6f-2091a96e7112)
pull requestを送りたいリポジトリを開き、`pull request`を作るためのボタンを押します

![Pull_Req_2](https://github.com/user-attachments/assets/b1bcb6a5-cc87-487b-8081-fa5cb0d93698)
あとは作業内容を書いて`Create pull request`を押して作業終了です

お疲れさまでした




