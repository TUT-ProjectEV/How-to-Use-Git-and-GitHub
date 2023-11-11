# Git GitHub Tutorial 1

## About
- Git, GitHubの基本的な使い方を学ぶチュートリアル
- ここでは簡単化のため、チームアカウントではなく個人アカウントのみで行う
- チーム開発向けチュートリアルは別途用意
- Gitのインストールと初期設定 [^1] 、GitHubアカウントの作成 [^2] まで完了しているものとする

## リモートリポジトリ作成
1. [GitHub](https://github.com/) から自分のアカウントにサインインし、 `Create repository` をクリック
![Screenshot of Dashboard](/images/create-repository-1.png)
2. `Repository name` に任意のリポジトリ名を入力
- 半角で入力
- その他にも設定項目があるが、今は一旦デフォルトで進める
![Screenshot of Create a new repository](/images/create-repository-2.png)
3. `Create repository` をクリック
![Screenshot of Create a new repository, finish fill in Repository name](/images/create-repository-3.png)
4. リポジトリの作成完了

## ローカルリポジトリ作成
- ここでは先ほど作成したリモートリポジトリをクローンすることで簡単化
1. コマンドプロンプトを起動し、ローカルリポジトリを作成したいディレクトリに移動
- ex) デスクトップに作成したい場合
```
cd Desktop
```
2. 先ほど作成したリモートリポジトリをローカルにクローン [^3]
- もしhttps通信でクローン出来ない人はSSH接続の設定 [^1] を行ってください
#### https通信でのクローン
```
git clone https://github.com/"Username"/"Repository name".git
```
#### SSHでのクローン
```
git clone git@github.com:"Username"/"Repository name".git
```
- クローンすると、空のリポジトリをクローンしたよと警告が出るが、無視でOK
```
warning: You appear to have cloned an empty repository.
```
3. クローンしたローカルリポジトリに移動
```
cd "Repository name"
```
4. コマンドプロンプトはそのままにしておく

## ローカルリポジトリにコミット
1. エクスプローラーを開き、クローンしたリポジトリを確認
2. そのフォルダ内で右クリックし、 `新規作成>テキストドキュメント` をクリック
![Screenshot of Folder](/images/commit-rocal-repository-1.png)
3. 任意の名前を入力して、ファイル作成
4. メモ帳でそのファイルを開き、適当な文を入力
![Screenshot of Memo editor](/images/commit-rocal-repository-2.png)
5. 保存して終了
6. コマンドプロンプトに戻り、インデックスへ作成したファイルを追加する [^3]
```
git add "File name you created".txt
```
7. インデックスに追加したファイルをローカルリポジトリにコミット
- ここの "" は必要なので注意
- `File name` は適当に置き換えてください [^4]
```
git commit -m "add File name"
```
- 変更履歴を確認するコマンド
```
git log
```

## リモートリポジトリにプッシュ
- ローカルリポジトリの変更内容をリモートリポジトリに反映させる
1. リモートリポジトリにプッシュ
```
git push origin main
```
- ここでもしパスワードなど聞かれた場合、SSH接続の設定 [^1] を行ってください [^5]
2. 最初にリモートリポジトリを作成したときのwebページを確認
3. 自分がローカルリポジトリで変更した内容が反映されていればチュートリアル完了

## Well done!
- お疲れ様でした
- GitやGitHubには他にもソフト開発やチームでの開発を支援する機能がたくさん備わっているので、気になる人は調べてみてください
- わからないことはDiscordなど用いて聞いても構いませんが、このリポジトリの `Discussions` に投げてみても良いかもしれません

[^1]: [Gitのインストールと初期設定手順](./Git-settings/)
[^2]: [GitHubアカウントの作成手順](./GitHub-creating-account/)
[^3]: "" の部分は各自読み替え ("" は不要)
[^4]: `-m` はコミットメッセージを入力するオプションであり、コミットメッセージは履歴情報を詳細に記録するのに役立つ
[^5]: ここで要求されるパスワードはアカウントにサインインするときのものとは異なるため (どうしてもSSH接続の設定をしたくない人は個人アクセストークンを作成してください)
