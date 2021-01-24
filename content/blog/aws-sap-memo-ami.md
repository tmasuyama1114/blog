---
title: "AWS-SAP 模試メモ - AMI"
date: 2021-01-24T12:16:47+09:00
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
  - "AMI"

# post type
type: "featured"
---

# CloudFront

### インスタンスストアにバックアップされたLinux AMI作成
インスタンスストアにバックアップされたLinux AMIを作成するには、既存のインスタンスストアにバックアップされたLinux AMIから起動したインスタンスを利用します。

ニーズに合わせてインスタンスをカスタマイズしたら、ボリュームをバンドルし、これらのカスタマイズで新しいインスタンスを起動するために使用できる新しいAMIを登録します。
インスタンスストアボリュームのAMI作成プロセスは、Amazon EBS-backed AMIとは異なり、**コンソール画面から実行できません**。
ec2-bundle-volやec2-upload-bundleなどのAMIツールが必要です。