---
title: "AWS-SAP 模試メモ - Elastic Load Balancing"
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
  - "Elastic Load Balancing"

# post type
type: "featured"
---

# Elastic Load Balancing

## CLB

### ルーティングの分散
Classic Load Balancer では、Cookie を使用して、特定の Amazon EC2 インスタンスにユーザーセッションを接続する機能をサポートしています。ユーザーがアプリケーションにアクセスし続ける限り、トラフィックは同じインスタンスにルーティングされます。セッションをインスタンスにマッピングするために使用されるAWSELBという名前のCookieを作成して、スティッキーセッションを実行します。

デフォルトでは、Classic Load Balancerは最小の負荷で登録されたインスタンスに各リクエストを個別にルーティングします。ただし、スティッキーセッション機能を使用して、ロードバランサーがユーザーのセッションを特定のインスタンスにバインドできます。これにより、セッション中のユーザーからのすべてのリクエストが同じインスタンスに送信されます。