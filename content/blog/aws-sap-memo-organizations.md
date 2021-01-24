---
title: "AWS-SAP 模試メモ - AWS Organizations"
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
  - "AWS Organizations"

# post type
type: "featured"
---

# AWS Organizations

## 環境の一元管理
AWS でのワークロードを拡大しスケールするときに、AWS Organizations は環境の一元管理に役立ちます。Organizations があれば、請求の一元管理や、アクセス、コンプライアンス、セキュリティの制御、AWS アカウント間でのリソースの共有ができます。AWS Organizations を使用すると、一括請求 (コンソリデーティッドビリング) を使用して、組織内のすべての AWS アカウントに対して単一の支払い方法を設定できます。また、IAMでクロスアカウントアクセスを有効化して、IT管理部門で個別のAWSアカウントを管理できるようにすることが可能です。 

## よくある勘違い
 
- マスターアカウントからメンバーアカウントへのクロスアカウントアクセスを有効化するという機能はありません。 
- AWS OrganizationsのメンバーアカウントをIT管理部門の管理者に設定するのではなく、マスターアカウントとして登録して、個別のアカウントのリソース利用とコスト管理を制御できるようにします。   