---
title: "AWS-SAP 模試メモ - Amazon ECS"
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
  - "Amazon ECS"

# post type
type: "featured"
---

# Amazon ECS

### ECS と IAM ロール
Amazon ECS タスク実行には IAM ロールを使用します。Amazon ECS コンテナエージェントはユーザーに代わって Amazon ECS API を呼び出すため、エージェントがユーザーに属していることをサービスに伝えるために、IAM ポリシーおよびロールが必要です。この IAM ロールはタスク実行 IAM ロールと呼ばれ、様々な目的の複数のタスク実行ロールをアカウントに関連付けることができます。

例えばアプリケーションには４つの異なるタスクがある場合、各タスクは他のタスクとは異なるさまざまなAWSリソースにアクセスします。そのために必要な設定方法は、必要なアクセス許可を持つ4つの異なるIAMロールを作成し、4つのECSタスクのそれぞれにアタッチすることです。異なるタスクを実行するためには、そのタスクを定義した異なるIAMロールを準備することが必要となります。

なお、複数の異なるタスクの権限設定はタスク定義で実施するのではなく、IAMロールを分割することで実施可能です。