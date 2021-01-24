---
title: "AWS-SAP 模試メモ - AWS Direct Connect"
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
  - "AWS Direct Connect"

# post type
type: "featured"
---

# AWS Direct Connect

## Link Aggregation Group
Link Aggregation Control Protocol (LACP) を使用して、1 つの AWS Direct Connect エンドポイントに複数の接続を集約し、それらを 1 つのマネージド型接続として扱うことを可能にする論理インターフェイスです。既存の接続から LAG を作成するには、それらの接続は同じ AWS デバイス上にあり、同じ帯域幅を使用する必要があります。接続を削除することにより、元の LAG で使用できる接続の最小数の設定を下回る場合、既存の LAG から接続を移行することはできません。 また、LAGは最大4つの接続が許可されます。

LAG は既存の専用接続から作成できます。または、新しい専用接続をプロビジョニングすることもできます。LAG を作成したら、この LAG に既存の接続 (スタンドアロンであるか、別の LAG の一部であるかを問わず) を関連付けることができます。

以下のルールが適用されます。

- すべての接続は専用接続でなければならず、ポート速度が 1 Gbps または 10 Gbps であることが必要です。
- LAG のすべての接続では、同じ帯域幅を使用する必要があります。
- LAG では最大 4 個の接続を行うことができます。LAG の各接続はリージョンの全体的な接続制限の対象になります。
- LAG のすべての接続は、同じ AWS Direct Connect エンドポイントで終了する必要があります。

