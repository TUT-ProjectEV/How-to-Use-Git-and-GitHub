# Git GitHub Tutorial 2

## About
- チーム開発のチュートリアル
- チームアカウント(Organization)へのアクセス、アプローチの仕方
- チームのリポジトリでの作業の流れ

## Description
- Gitのインストールと初期設定 [^1] 、GitHubアカウントの作成 [^2] まで完了しているものとする
- チュートリアルでやること
    - 各班の自己紹介リポジトリ (作成済み) に自分の自己紹介を追加
    - 自分の名前のディレクトリを作成し、その下に 'README.md' ファイルを置く

## Organizationへの参加
- チームのアカウントをGitHubでは 'Organization' として扱う
- `Organization` のリポジトリにアクセスし、開発を行っていくには `Organization` の管理者に招待してもらい、参加する必要がある
1. [TUT-ProjectEV](https://github.com/TUT-ProjectEV) の管理者にユーザーネームを伝え、招待してもらう
2. 自身のGitHubアカウントに設定したメールアドレス宛に招待メールが届くので、 `Join @TUT-ProjectEV` をクリック
![Screenshot of invite email](images/join-organization-1.png)
3. webページに飛ばされるので、 'Join 東京工科大学 ProjectEV' をクリック
4. 参加完了

## GitHubを使用したチーム開発におけるルール
- [Project EV rules](https://github.com/TUT-ProjectEV/.github-private/tree/develop/profile) 参照

## リモートリポジトリ作成
- 自己紹介リポジトリは作成済みなので、ここはスキップでOK
    - 今後の使い方の参考までに書いておく
1. [TUT-ProjectEV](https://github.com/TUT-ProjectEV) へアクセス
2. 画面上部 `Repositories` タブをクリック
![Screenshot of team page](images/creating-remote-repository-1.png)
3. 画面右上 `New repository` をクリック
![Screenshot of team repositories page](images/creating-remote-repository-2.png)
4. `Repository template` を `No template` から `TUT-ProjectEV/repository-temp` へ変更
5. `Include all branches` にチェックを入れる
6. `Repository name` を入力
7. `Private` から `Public` に変更
> [!WARNING]
> 企業の部外秘の情報など含まれる場合は 'Private' のままにしておくこと
8. `Create repository` をクリックしてリポジトリ作成完了
![Screenshot of create a new repository](images/creating-remote-repository-3.png)

## リモートリポジトリをローカルにクローン

## 自分の作業ブランチ作成

## ローカルリポジトリにコミット

## リモートリポジトリにプッシュ

## プルリクエスト作成

## プルリクエスト承認

## Well done!

[^1]: [Gitのインストールと初期設定手順](./../Git-settings/)
[^2]: [GitHubアカウント作成手順](./../GitHub-creating-account/)