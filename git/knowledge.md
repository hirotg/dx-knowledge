# Git

# コミット
コミットは、git commit -m "コミットメッセージ"   の 1行コミットを利用する
コミットメッセージには、理由を記載する

# ブランチ

- git branch
ブランチを確認する



- git branch -v
各ブランチの最新のコミットメッセージを表示する

- git merge ブランチ
現在のブランチに、ブランチをマージする

- git branch --merges
現在のブランチに、マージされたブランチを表示する

- git branch --no-merged
現在のブランチに、マージされていないブランチを表示する


- git branch ブランチ
ブランチを新規作成する

- git checkout ブランチ
ブランチへ切り替える

- git checkout -b ブランチ
新しいブランチを作成し、切り替える

- git branch -m ブランチ
現在のブランチの名称を変更する

# SSH

## SSHキーを生成する
````
ssh-keygen -t ed25519 -C "メールアドレス"
````

## SSH公開鍵を GitHub へ登録する
- 右上アイコンを選択
- [Settings]を選択
- 左メニュー [SSH and GPG Keys]を選択
- 公開鍵を登録する

## config の作成
- ./config ファイルを作成する

````
Host github.com
    HostName github.com
    IdentityFile ~/.ssh/id_ed25519_github
    User git
````

## SSH接続確認
````
ssh -T git@github.com
````

