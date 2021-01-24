---
title: "AWS-SAP 模試メモ - Amazon CloudFront"
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
  - "Amazon CloudFront"

# post type
type: "featured"
---

# Amazon CloudFront

### SSL証明書

独自のドメイン名と独自のSSL証明書を使用してHTTPS経由でコンテンツを配信する場合は、カスタムSSL証明書を使用することが必要です。
これにより、Webサイトは独自のドメイン名を使用するSSL接続を介したCloudFrontによりセキュリティを高めることができ、キャッシュ配信によって待ち時間が短くなり、信頼性が高まります。

AWS上でSSL証明書を利用する場合はAWS Certificate Manager（ACM）またはIAMに保存されている証明書を使用できます。
AWS Certificate Manager（ACM）に保存されたカスタムSSL証明書を使用してCloudFrontディストリビューションを作成するか、IAMに保存されたカスタムSSL証明書を使用してCloudFrontディストリビューションを作成することが必要となります。  