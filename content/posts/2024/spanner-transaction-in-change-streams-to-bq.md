---
title: "BigQuery 連携クエリ・外部データセットが使う Spanner トランザクションについて"
date: 2024-11-06T00:00:00-09:00
slug: bigquery-federated-queries-external-dataset-with-spanner-transaction
draft: false
disableRobots: true
tag:
  - Spanner Transaction
  - BigQuery
  - Federated queries
  - External datasets
---

## 背景

2024年4月の[Google Cloud Next '24 Las Vegas Recap](https://cloudonair.withgoogle.com/events/gc-updates?talk=optional1-2024)で言及されて以来、10月3日に、BigQuery external dataset を使って Spanner のデータセットをリンクする機能が Public Preview になったとリリースノートで発表されました。

生成AIほどの注目を集めていないかもしれませんが、みんなの銀行のデータ基盤にとっては、嬉しいリリースになりそうです。

みんなの銀行開業に伴い、データ基盤システムが稼働開始しました。多様なデータソースから、リアルタイム、毎時、毎日といった頻度でデータ連携処理を行っています。その中で、やむを得ず、一部データについては、Spanner から BigQuery への日次連携に以下の方法を採用しました。

{{< readmore link="https://qiita.com/l-jiang-zdf/items/3bbb3902c96c26d73d15" >}}
