---
title: "AWS-SAP 模試メモ - AWS CloudFormation"
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
  - "AWS CloudFormation"

# post type
type: "featured"
---

# AWS CloudFront

### パラメータ設定方法
AWS::Lambda::Functionを利用して、Lambda 関数のデプロイパッケージをCloudFormationで参照します。すべてのランタイムに対して、Amazon S3 内のオブジェクトの場所を指定できます。

※Lambda関数コードをコードレポジトリーに保存し、CloudFormationのAWS :: Lambda :: Functionにおいて参照するといった設定方法はありません

また、Node.js および Python 関数の場合で依存関係がない限りテンプレートにインラインで関数コードを指定できます。