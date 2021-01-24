---
title: "AWS-SAP 模試メモ - AWS Step Functions"
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
  - "AWS Step Functions"

# post type
type: "featured"
---

# AWS Step Functions
タスクとステートマシンの概念に基づく、分散アプリケーションとマイクロサービスを調整するワークフローサービスです。ワークフローには標準とExpressの2タイプが提供されています。ドメインロジックはLambda関数やAWSサービス、またはEC2やECSを使用して定義します。また、ワークフロー全体はステートマシンとして、JSONベースの言語、ASL（Amazon States Language）を使用して定義します。

## Expressワークフロー
AWS Step Functions Expressワークフローは、AWS Step Functions ワークフローの新しいワークフロータイプです。これにより、AWS のコンピューティング、データベース、メッセージングサービスを毎秒 100,000 件を超えるイベントレートでコスト効率よく調整できます。Express Workflow は、Amazon API Gateway を介した HTTP リクエスト、AWS Lambda リクエスト、AWS IoT ルールエンジンのアクション、および Amazon EventBridge の 100 件以上の AWS および SaaS イベントソースなどのイベントに応じて、自動的に開始されます。Express Workflows は、IoT データの取り込み、ストリーミングデータの処理と変換、大量のマイクロサービスオーケストレーションなどの大量のイベント処理ワークロードに適しています。

## 優先順位とBatch
タスクに優先度を作るのはStep Functions、SWF、AWS Batchのいづれでも可能です。SQSはキューに優先度をつけれます。AWS Batchはバッチ処理的なプロセスをEC2を利用して構成しますが、それをStep Functionsに組み込むことも可能です。SWFとStep Functionsとの大きな違いはワークフローの作成しやすさです。Step Functionsの方が圧倒的に容易にプロセスが構築可能であり、SWFの代替するサービスとして登場したため、Step Functionsの利用が優先されます。

## SWF との違い
AWSよりStep Functionsの利用が推奨されています。AWS Step FunctionsとSWFは基本的には同じ機能を提供してます。AWS Step FunctionsはSWFの後継サービスとして作成されているため、今後はSWFではなくAWS Step Functionsを利用することが推奨されております。しかしながら、現状ではSWFにしか対応されていない設定方式が残っているため、その場合はSWFを利用することがAWSより求められています。

プロセスにおいて介入する外部信号が必要な場合、または結果を親に返す子プロセスを起動する場合は、Amazon SWF)を使用してください。