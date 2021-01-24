---
title: "AWS-SAP 模試メモ - Amazon EFS"
date: 2021-01-24T12:14:47+09:00
draft: false

# post thumb
# image: "images/xxxxx.jpg"

# meta description
description: "AWS-SAP の模擬試験を受けての復習メモ"

# taxonomies
categories:
  - "AWS-SAP"
tags:
  - "AWS"
  - "SAP"
  - "ソリューションアーキテクトプロフェッショナル"
  - "Amazon EFS"

# post type
type: "featured"
---

# Amazon EFS
Amazon EFSは、Amazon EC2 で使用するためのシンプルでスケーラブルなファイルストレージを提供します。Amazon EFS を使用すると、ストレージ容量は弾力的で、ファイルの追加や削除に応じて自動的に拡張および縮小されるため、アプリケーションは必要なときに必要なストレージを確保できます。マウントヘルパーユーティリティであるamazon-efs-utils パッケージは、Amazon EFS ツールのオープンソースのコレクションです。amazon-efs-utils は追加コストなしで使用でき、 https://github.com/aws/efs-utilsで、GitHub からこれらのツールをダウンロードできます。amazon-efs-utils パッケージは、Amazon Linux パッケージリポジトリで利用でき、他の Linux ディストリビューションのパッケージをビルドおよびインストールできます。

### EFSのマウントヘルパー
Amazon EFS ファイルシステムを作成するには、マネジメントコンソールの設定画面の「VPC] でEFSボリューム向けにインスタンスがあるVPCにマウントターゲットを設定します。 

コンソールまたは実行コードによって、EFSファイルシステムIDをEFS APIから取得して、EC2インスタンスからのアクセスの際に設定することが求められます。EFSファイルシステムIDを利用してEC2 インスタンスを起動し、EFS ファイルシステムをマウントします。 

マウントヘルパーユーティリティのamazon-efs-utils パッケージには、マウントヘルパーおよび Amazon EFS の転送時のデータ暗号化の実行を簡単にするツールが用意されています。マウントヘルパーユーティリティを利用した際に、暗号化オプション「-o tls」を追加することが可能です。   