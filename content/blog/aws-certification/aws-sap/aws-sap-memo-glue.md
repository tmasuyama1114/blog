---
title: "AWS-SAP 模試メモ - AWS Glue"
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
  - "AWS Glue"

# post type
type: "featured"
---

# AWS Glue
フルマネージドなETL（Extract、Transform、Load）サービスです。RDSやS3といったデータソースをクロールしてデータカタログを構築、次にETL処理をジョブとしてトリガ登録（スケジュール／連結／オンデマンド）することで処理を実行できます。

## スケジュールジョブの実行
AWS Glueは大量のデータセットを効果的に処理でき、コーディング要件をほとんど、または全く必要とせずに変換を処理できる完全なサーバーレスETLフレームワークであり、インポートファイルの処理に利用することができます。 AWS Glueのインポートが完了すると、AWS Batchプロセスをトリガーできます。これにより、インポートされたデータに基づいてルートスケジューリングジョブを呼び出すことができます。 