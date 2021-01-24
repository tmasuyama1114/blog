---
title: "AWS-SAP 模試メモ - Amazon Simple Queue Service"
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
  - "Amazon Simple Queue Service"

# post type
type: "featured"
---

# Amazon Simple Queue Service

### キューの種類
例えばオークションの買い手と売り手からのトランザクションが、受け取った順序どおりに処理される必要があるとき、SQSに対してFIFOなどのメッセージ処理機能を組み合わせることが有効です。

また、メッセージグループIDはFIFO配信を支援する機能です。これによって、 同じメッセージグループに属するメッセージは、常にメッセージグループに対して厳密な順序で1つずつ処理されます。

### 可視性タイムアウト
可視性タイムアウトは、この設定時間内に他のコンシューマーが同じメッセージを受信したり処理したりすることはできません。  
※これはメッセージの重複排除などで利用される機能であり、メッセージ順序を保証するものではありません。

### メッセージ重複排除ID
メッセージが重複して処理されるのを防ぐ方法