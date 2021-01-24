---
title: "AWS-SAP 模試メモ - AWS OpsWorks"
date: 2021-01-24T14:10:47+09:00
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
  - "AWS OpsWorks"

# post type
type: "featured"
---

# AWS OpsWorks

## ライフサイクルイベント
AWS OpsWorks Stacks の各 Layer には、5 つの一連のライフサイクルイベントがあり、それぞれのイベントに、その Layer に固有の一連のレシピが関連付けられます。
レイヤーのインスタンスでイベントが発生すると、一連の適切なレシピが AWS OpsWorks スタックによって自動的に実行されます。

#### Setup
このイベントは、開始されたインスタンスの起動が終了した後で発生します。Setup スタックコマンドを使用して、Setup イベントを手動でトリガーすることもできます。対応するレイヤーに基づいてインスタンスをセットアップするレシピが AWS OpsWorks Stacks によって実行されます。たとえば、そのインスタンスが Rails アプリケーションサーバー Layer に従属している場合、Apache、Ruby Enterprise Edition、Passenger、Ruby on Rails が、Setup レシピによってインストールされます。

#### Configure
このイベントは、以下のいずれかが発生したときに、スタックのすべてのインスタンスで発生します。

- インスタンスがオンライン状態に移行したか、オンライン状態から移行した。
- Elastic IP アドレスをインスタンスに関連付けたか、インスタンスから Elastic IP アドレスの関連付けを解除した。
- Elastic Load Balancing ロードバランサーを Layer にアタッチしたか、Layer からデタッチした。

#### Deploy
このイベントは、Deploy コマンドを実行したときに発生します。通常、一連のアプリケーションサーバーインスタンスにアプリケーションをデプロイする目的でこのコマンドが実行されます。アプリケーションとその関連ファイルをリポジトリから Layer のインスタンスにデプロイするレシピがインスタンスによって実行されます。たとえば、Rails Application Server インスタンスの場合、Deploy レシピは、指定された Ruby アプリケーションをチェックアウトし、Phusion Passenger に対して、それを再ロードするように伝えます。Deploy を他のインスタンスで実行することもできます。たとえば、新しくデプロイされたアプリケーションに応じてそのインスタンスの設定を更新することができます。

#### Undeploy
このイベントは、アプリケーションを削除したとき、つまり、Undeploy コマンドを実行して、一連のアプリケーションサーバーインスタンスからアプリケーションを削除したときに発生します。指定したインスタンスによってレシピが実行され、すべてのアプリケーションバージョンが削除されて、必要なクリーンアップ処理が実行されます。

#### Shutdown
このイベントは、インスタンスをシャットダウンするよう AWS OpsWorks スタックに指示した後、関連する Amazon EC2 インスタンスが実際に終了する前に発生します。サービスのシャットダウンなど、各種クリーンアップタスクを行うレシピが AWS OpsWorks スタックによって実行されます。

Elastic Load Balancing ロードバランサーを Layer にアタッチし、Connection Draining のサポートを有効にした場合、AWS OpsWorks スタックは Connection Draining が完了するまで待機した後、Shutdown イベントをトリガーします。

Shutdown イベントをトリガーした後、AWS OpsWorks スタックは Shutdown レシピがタスクを実行するために指定された時間だけ待機してから、Amazon EC2 インスタンスを停止または終了します。デフォルトの Shutdown タイムアウト値は 120 秒です。Shutdown レシピでさらに時間が必要な場合は、Layer 設定を編集してタイムアウト値を変更できます。インスタンス Shutdown の詳細については、「インスタンスの停止」を参照してください。