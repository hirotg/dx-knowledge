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

- README の役割
共同作業者が最初に目にするのがREADMEファイル 
良いREADMEファイルには必要な情報が網羅されている 

- READMEファイルの基本構成
プロジェクトのタイトル 
概要(プロジェクトの目的や背景)
使い方
運用ルール

- READMEファイルのベストプラクティス
簡潔に書く
見やすいフォーマットを使う
定期的に更新する

# .gitignore


# ブランチ保護

# GitHubブランチ

- main
- feature/xxx
- develop/xxx   開発環境・テスト環境用ブランチ
- bugfix/xxx    バグ修正用ブランチ
- release       リリース用ブランチ
- hotfix/xxx    リリースされたものに対する修正ブランチ

# Git Flow と GitHub Flow

## Git Flow の特長


## GitHub Flow の特長
素早い対応が可能
構成がGit Flowよりもシンプル
自動デプロイ前提のため人的ミスを減らせる
常にデプロイ可能



# テクニック

## コミットの粒度を小さくする
- 理由
トレーサビリティの向上
リバートのしやすさ
コードレビューの効率化
コンフリクトの解消に便利

- 1コミットに一つの変更内容
一つのコミットで、複数の変更(例えば、バグの修正と機能の追加) をしない


# 参考情報

## オンライン教育
-udemy	3分動画でしっかり学ぶGit/GitHub入門

## 書籍
