---
title: "AWS-SAP 模試メモ - AWS Serverless Application Repository"
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
  - "AWS Serverless Application Repository"

# post type
type: "featured"
---

# AWS Serverless Application Repository
AWS Serverless Application Repository は、サーバーレスアプリケーション用のマネージド型リポジトリです。チーム、組織、開発者個人が、再利用可能なアプリケーションを保存して共有できます。また、強力な新しい方法でサーバーレスアーキテクチャを簡単に組み立ててデプロイすることもできます。Serverless Application Repository を使用すると、ソースコードのクローンを作成したり、ソースコードをビルドしてパッケージ化したり、デプロイする前に AWS に発行したりする必要はありません。代わりに、サーバーレスアーキテクチャで Serverless Application Repository からあらかじめ構築されたアプリケーションを使用できます。

## Serverless Application Model (SAM)
AWS サーバーレスアプリケーションモデル (SAM）は、サーバーレスアプリケーション構築用のオープンソースフレームワークです。迅速に記述可能な構文で関数、API、データベース、イベントソースマッピングを表現できます。リソースごとにわずか数行で、任意のアプリケーションを定義して YAML を使用してモデリングできます。デプロイ中、SAM が SAM 構文を AWS CloudFormation 構文に変換および拡張することで、サーバーレスアプリケーションの構築を高速化することができます。SAMサーバーレスアプリケーションはCloudFormationテンプレートで定義され、CloudFormationスタックとしてデプロイされます。 AWS SAMテンプレートはCloudFormationテンプレートと見なすことができますが、AWS SAM独自の特別なリソースがあります。

#### AWS :: Serverless :: Api
HTTPS エンドポイントを介して呼び出すことのできる Amazon API Gateway リソースとメソッドのコレクションを作成します。

#### AWS::Serverless::Function
関数、AWS Lambda (AWS Identity and Access Management) 実行ロール、および関数をトリガーするイベントソースマッピングを作成します。IAM

#### AWS::Serverless::SimpleTable
1 つの属性プライマリキーを使用して DynamoDB テーブルを作成します。プライマリキーを介してデータにアクセスする必要がある場合に便利です。