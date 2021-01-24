---
title: "AWS-SAP 模試メモ - AWS Single Sign-On"
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
  - "AWS Single Sing-On"

# post type
type: "featured"
---

# AWS Single Sign-On

### 既存ユーザーIDEAをAWS外で管理している場合
AWS アカウントに IAM ユーザーを作成する代わりに、IAM ID プロバイダーを利用できます。ID プロバイダー (IdP) を使用すると、AWS の外部のユーザー ID を管理して、これらの外部ユーザー ID にアカウント内の AWS リソースに対するアクセス許可を与えることができます。

また、フェデレーションにより、AWSクラウドリソースへのアクセスを一元管理できます。フェデレーションでは、シングルサインオン（SSO）を使用して、社内ディレクトリの認証情報を使用してAWSアカウントにアクセスできます。フェデレーションは、セキュリティアサーションマークアップ言語2.0（SAML）などのオープンスタンダードを使用して、IDプロバイダー（IdP）とアプリケーションの間でIDおよびセキュリティ情報を交換します。