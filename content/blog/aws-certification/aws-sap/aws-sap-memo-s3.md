---
title: "AWS-SAP 模試メモ - Amazon S3"
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
  - "Amazon S3"

# post type
type: "featured"
---

# Amazon S3

## CLIオプション
AWS CLIを利用してS3の大きな項目リストを返すコマンドを実施する場合、3 つのオプションを利用することができます。それらを利用して、AWS CLI がサービスの API を呼び出してリストを生成するときに出力に含まれる項目の数を制御できます。 デフォルトでは、AWS CLI は 1,000 のページサイズを使用して、利用可能な全ての項目を取得します。

#### --max-items
AWS CLI 出力で一度に含める項目を少なくするには、--max-items オプションを使用します。AWS CLI はサービスとのページ区切りを処理しますが、指定した時点での項目数のみを出力します。 

#### --page-size
--page-size オプションを使用して、AWS CLI が AWS のサービスの**1 回の呼び出しで要求する項目数を少なくする**ことができます。その場合でも、CLI は完全なリストを取得しますが、多数のサービス API コールをバックグラウンドで実行し、1 回の呼び出しで取得する項目数が少なくなります。このため、個々の呼び出しがタイムアウトにならずに成功する可能性が高くなります。ページサイズを変更しても、出力には影響しません。出力を生成するために必要な API 呼び出しの数が変わるだけです。