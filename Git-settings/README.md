# Git Install and Settings

## About
- Gitのインストール方法と初期設定について解説

## Install
### Windowsの場合
1. [Git公式サイトのダウンロードページ](https://git-scm.com/downloads) にてインストーラをダウンロード
2. ダウンロードしたインストーラをクリック
3. `このアプリがデバイスに変更を加えることを許可しますか？` と聞かれたら `はい` をクリック
4. ライセンスに同意し進める
5. 特に変更する必要のあるところはないので、デフォルトのまま `Next` で進める
6. `Install` が出てきたらクリックして、完了したら `Finish`
7. 検索バーで「コマンドプロンプト」と検索し起動
8. 以下のコマンドを実行
```
git --version
```
9. Gitのバージョンが表示されればインストール成功の合図

## Settings
- 先にGitHubアカウントを作成し、そのユーザーネーム/メールアドレスを使用することを推奨 [^1]
1. ユーザーネームの設定 [^2]
```
git config --global user.name "User Name"
```
2. ユーザーメールアドレスの設定 [^2]
```
git config --global user.email "User@email.com"
```
3. 設定項目の確認
```
git config -l
```
4. 設定したユーザーネーム/メールアドレスが確認できれば完了

## SSH接続の設定 (任意)
- ここはGitHubアカウント作成済みであることが前提
1. コマンドプロンプトを起動
2. 公開鍵・秘密鍵の発行
```
ssh-keygen -t rsa
```
3. 特に設定が必要なければEnter連打
4. 公開鍵の表示 [^2]
```
type /c/Users/"ユーザー名"/.ssh/id_rsa.pub
```
5. `ssh-rsa...` から始まる箇所をコピーしておく
6. [GitHub](https://github.co.jp/) にアクセスし、サインイン
7. 画面右上のアカウントのアイコンをクリックし、 `Settings` をクリック
8. `SSH and GPG keys` をクリック
9. `New SSH key` をクリック
10. `Title` に今自分が使用しているPCの名前を入力
- なんでもよい
- 自分がその `Title` を見てどのPCを言っているのかわかるようなものにすることを推奨
11. `Key` に先ほどコピーした `ssh-rsa...` から始まる箇所をペースト
12. `Add SSH key` をクリック
13. コマンドプロンプトに戻り、以下のコマンドを実行
```
ssh -T git@github.com
```
14. 以下のような表示がでれば成功 [^2]
```
Hi "Username"! You've successfully authenticated, but GitHub does not provide shell access.
```

[^1]: [GitHubアカウント作成手順](./GitHub-creating-account/)
[^2]: "" の部分は各自読み替え ("" は不要)