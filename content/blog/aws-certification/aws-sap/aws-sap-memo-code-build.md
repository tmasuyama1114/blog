---
title: "AWS-SAP 模試メモ - AWS CodeBuild"
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
  - "AWS CodeBuild"

# post type
type: "featured"
---

# AWS CodeBuild

### シナリオ例

毎週定期的にビルドを実行するようにCodeBuildをスケジュールして、このスケジュールされたビルドに使用される定数をCodeBuildに渡す設定方法があります。  
例えば、毎晩午後8時にCodeBuildプロジェクトビルドをスケジュールするルールを作成するには以下のような手順を実施します。

1. https://console.aws.amazon.com/cloudwatch/ でCloudWatchコンソールを開きます。 
2. ナビゲーションペインで、[イベント]、[ルールの作成]を選択します。 
3. イベントソースの場合は次の手順を実行します。  　
  - a. スケジュールを選択します。     
  - Cron式を選択し、式として次を指定します：「0 20 ? * MON-FRI *」
    - 「0 20 ? * MON-FRI *」を細かく指定することで定期タスクを設定することが可能です。 
4. [ターゲット]で、[ターゲットの追加]、[CodeBuildプロジェクト]を選択します。 
5. プロジェクトARNには、ビルドプロジェクトのARNを入力します。 　
  - ここに実行したいタスクのCodeBuildプロジェクトARNを設定します。 
6. パラメーターをCodeBuildに渡すオプションのステップを追加して、デフォルトをオーバーライドします。 CodeBuildをターゲットとして設定する場合、これは必要ありません。パラメーターを渡すには、入力の構成、定数（JSONテキスト）を選択します。[定数（JSONテキスト）]の下のボックスに次を入力して、これらのスケジュールされたビルドのタイムアウトオーバーライドを30分に設定します。 
7. CloudWatch Eventsは、ビルドプロジェクトの実行に必要なIAMロールを作成できます。 
8. 詳細設定を選択します
9. [ルールの定義]で、ルールの名前と説明を入力します。
10. ルールの作成を選択します。