---
title: "AWS-SAP 模試メモ - Amazon API Gateway"
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
  - "Amazon API Gateway"

# post type
type: "featured"
---

# Amazon API Gateway

## Lambda オーソライザー
Lambda オーソライザーは、Lambda 関数を使用して API へのアクセスを制御する API Gateway の機能です。 Lambda オーソライザーは、OAuth や SAML などのベアラートークン認可戦略を使用する、または発信者 ID を判断するためにリクエストパラメータを使用するカスタム認証スキームを実装する場合に利用します。クライアントが API のメソッドの 1 つにリクエストを送信すると、API Gateway は Lambda オーソライザーを呼び出します。これは発信者 ID を入力として受け取り、IAM ポリシーを出力として返します。 Lambda オーソライザーには 2 種類あります。 

#### トークンベース
TOKEN オーソライザーとも呼ばれます。
JSON ウェブトークン (JWT) や OAuth トークンなどのベアラートークンで発信者 ID を受け取ります。

#### リクエストパラメータベース
REQUEST オーソライザーとも呼ばれます。
ヘッダー、クエリ文字列パラメータ、stageVariables、および $context 変数の組み合わせで、発信者 ID を受け取ります。 


## Lambda 統合

#### Lambda プロキシ統合
Amazon API Gateway Lambda プロキシ統合は、単一の API メソッドのセットアップで API を構築するシンプル、強力、高速なメカニズムです。Lambda プロキシ統合は、クライアントが単一の Lambda 関数をバックエンドで呼び出すことを可能にします。この関数は、他の Lambda 関数の呼び出しを含め、他の AWS のサービスのさまざまなリソースや機能にアクセスします。

API Gateway は Lambda プロキシ統合では、クライアントとバックエンド Lambda 関数間に介入しないため、クライアントと統合された Lambda 関数は、API の既存の 統合セットアップを損なうことなく、相互の変更に適応できます。これを有効にするには、クライアントはバックエンド Lambda 関数が制定したアプリケーションプロトコルに従う必要があります。したがって、Lambdaプロキシ統合が、シナリオに示されている説明と一致します。HTTPSを介して、クライアントからの着信要求をバックエンドLambda関数への入力値として渡すシンプルな統合方式を実装する際はLambda プロキシ統合で実現することになります。

#### Lambda 非プロキシ統合
Lambda 非プロキシ統合では、プロキシ統合のセットアップ手順に加えて、受信リクエストデータがどのように統合リクエストにマッピングされるか、統合レスポンスデータの結果がメソッドレスポンスにどのようにマッピングされるかを指定する統合方式となります。この統合方式では、API Gatewayを利用してLambdaを呼び出す際に、HTTPリクエストに含まれている情報を連携するために、別途Mapping Templateを作成して、HTTPヘッダーなどをeventオブジェクトに設定する必要があます。Lambda 非プロキシ統合はより複雑なマッピングを定義したい場合に利用することになります。