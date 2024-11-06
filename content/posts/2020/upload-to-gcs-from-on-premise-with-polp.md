---
title: "オンプレミス環境からGCSバケットにファイルのアップロード、最小権限の設定について"
date: 2020-12-26T00:00:00-09:00
slug: upload-to-gcs-from-on-premise-with-polp
draft: false
disableRobots: true
tag:
  - Docker
  - Bash script
  - Cloud Storage
  - Principle of least privilege
---

## 背景

エンドユーザーはオンプレミス環境から GCS バケットへファイルアップロードしたいという要望がありますが、情報はこれだけで、直接に聞くのも難しかったです。
GCP プロジェクトは組織なしで作られていますが、Google Workspace を利用しているかどうか、Google アカウントを持っているかどうか、オンプレミス環境はどんな状況かなどなど、そういう要素に左右されないように、考えてみました。

## 案

GCP プロジェクトでサービスアカウントを発行し、ロールの「Storage オブジェクト作成者」を付与し、サービスアカウントキーを作成してから、エンドユーザーのオンプレミス環境の Docker コンテナからファイルアップロードすることにしました。

{{< readmore link="https://qiita.com/kyou_rai/items/1d300b48949484509199" >}}
