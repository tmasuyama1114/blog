---
title: "AWS-SAP 模試メモ - AWS Systems Manager"
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
  - "AWS Systems Manager"

# post type
type: "featured"
---

# AWS Systems Manager

## ステートマネージャー
安全でスケーラブルな設定管理サービスであり、Amazon EC2 およびハイブリッドインフラストラクチャを、定義された状態に保つプロセスを自動化します。シェルスクリプトによって、午前0:00にCE2インスタンスからS3バケットにログを取得する設定が可能です。 

## Patch Manager
セキュリティ関連のアップデートと他のタイプのアップデートの両方でマネージドインスタンスにパッチを適用するプロセスを自動化します。スクリプトまたはコマンドを実行するツールではありません。 

## セッションマネージャー
セッションマネージャーは、安全で監査可能なインスタンス管理を提供するサービスであり、スクリプトまたはコマンドを実行するツールではありません。

## 