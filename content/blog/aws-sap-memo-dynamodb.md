---
title: "AWS-SAP 模試メモ - Amazon DynamoDB"
date: 2021-01-24T12:15:47+09:00
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
  - "Amazon DynamoDB"

# post type
type: "featured"
---

# Amazon DynamoDB

### リージョン間でのレプリケーション

DynamoDBテーブルのリージョン間でのレプリケーションを実施するのは簡単で、DynamoDBテーブルにおいてストリームを有効化する。その上でグローバルテーブルを作成して、別リージョン間でデータを共有することで別リージョンにレプリケーションを実施することができます。