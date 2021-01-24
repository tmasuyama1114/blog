---
title: "AWS-SAP 模試メモ - Amazon Simple Notification Service"
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
  - "Amazon Simple Notification Service"

# post type
type: "featured"
---

# Amazon Simple Notification Service

### サブスクリプション不要時の対応
サブスクリプションが不要になった場合は、まずトピックからのサブスクリプション解除を行います。これによってマネージャー向けのサブスクリプション設定を削除することができます。SNSトピックから該当ユーザーのサブスクリプションを削除すると、ユーザーが通知を受け取ることはありません。

また、ユーザー自身で解除することも可能です。通知には、ユーザーへの通知にはユーザーが直接使用可能な購読解除URLが付与されており、このURLからユーザー自身で購読を解除する設定を操作することが可能です。