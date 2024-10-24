# GitHub ノウハウ

# SSHカギ設定

## SSH鍵設定

- SSH鍵を生成する
ssh-keygen -t ed25519 -C "メールアドレス"

- GitHubへ公開鍵を登録する
GitHub 右上プロフィールアイコン Settings を選択
SSH and GPG Keys に、 ***.pub の内容を貼り付け



## ssh configの設定

.ssh/config   へ以下を追加する

Host github.com
	HostName github.com
	IdentityFile C:\Users\hirot/.ssh/id_ed25519_github
	User git


## 接続確認
ssh -T git@github.com


# README


# ブランチ保護

# GitHubブランチ

- main
- feature/xxx
- develop/xxx   開発環境・テスト環境用ブランチ
- bugfix/xxx    バグ修正用ブランチ
- release       リリース用ブランチ
- hotfix/xxx    リリースされたものに対する修正ブランチ

