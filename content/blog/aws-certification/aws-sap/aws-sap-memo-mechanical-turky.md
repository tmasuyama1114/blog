---
title: "AWS-SAP 模試メモ - Amazon Mechanical Turk"
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
  - "Amazon Mechanical Turk"

# post type
type: "featured"
---

# Amazon Mechanical Turk
Amazon Mechanical Turk は、人間にリクエストすることによって、サービス依頼者（以後、「依頼者」）に、疑似人工知能を直接依頼者のアプリケーションに統合するサービスを提供します。依頼者は、Amazon Mechanical Turk ウェブユーザーインターフェイスまたはウェブサービス API を使用して Amazon Mechanical Turk ウェブサイトにタスクを提出し、完了したタスクを承認し、回答をアプリケーションに組み込みます。ウェブサービス API を使用している時のこのやり取りはリモートプロシージャコールとたいへん良く似ています。アプリケーションがリクエストを送信し、サービスが結果を返すというかたちです。現実的には、人間の作業者（今後「作業者」と言及します）のネットワークがウェブサイトにアクセスし、タスクを検索し、完了し、仕事に対する報酬を受けることで、この疑似人工知能は機能しています。

## 通知
Amazon Mechanical Turkは、特定のタスクタイプについて、ワーカーが割り当てを受け入れ、放棄、返却、または送信したとき、タスクが「レビュー可能」になったとき、またはタスクが期限切れになったときに通知メッセージを送信できます。その際にはAmazon Simple Queue Service（Amazon SQS）キューまたはAmazon Simple Notification Service（Amazon SNS）トピックに通知を送信できます。