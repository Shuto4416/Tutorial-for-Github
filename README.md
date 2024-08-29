# GitHubの使い方

---

## 【目次】

- [GitHubとは](#【GitHubとは】)

- [GitHubを使い始める前に知っておきたい知識](#【GitHubを使い始める前に知っておきたい知識】)

- [VSCodeでGitHubを使ってみよう](#【VSCodeでGitHubを使ってみよう】)

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

![スクリーンショット (141).png](https://github.com/user-attachments/assets/96665de1-40e3-4827-bca0-7ded8af5e4b6)

GitHub 上から「Code」のリンクをコピー  
`HTTPS`か`SSH`かを注意

![スクリーンショット (143)](https://github.com/user-attachments/assets/ecf8db88-2f95-4351-8bdb-0f2171ebab1a)

VSCodeのターミナルで以下のコマンドを実行

```
$ git clone [コピーしたリンク]
```

![スクリーンショット (146)](https://github.com/user-attachments/assets/c1e95c4e-5228-47e9-919f-d1ab82b3fb77)
