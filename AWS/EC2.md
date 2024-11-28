# EC2

## Windows PowerShell から SSH接続

## Windows VSCode ターミナルからの ssh接続
ssh ec2-user@IPアドレス -i 秘密鍵

## boto3 のインストール方法

## AWS CLIのインストール方法

## Docker のインストール方法

1. パッケージ情報を更新する
sudo yum update -y

2. Docker をインストールする
sudo amazon-linux-extras install docker -y

3. Dockerサービスを開始する
service docker start

4. ec2-user を docker グループに追加する
usermod -a -G docker ec2-user

5. Docker の動作を確認する
docker info
