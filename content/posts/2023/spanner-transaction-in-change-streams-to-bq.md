---
title: "Spanner Change Streams to BigQuery: Spannerトランザクション処理はどう連携されるか？"
date: 2023-03-02T00:00:00-09:00
slug: spanner-transaction-in-change-streams-to-bq
draft: false
disableRobots: true
tag:
  - Spanner Change Streams
  - Spanner Transaction
  - BigQuery
  - Dataflow
---

## 背景

2022年5月28日にCloud Spanner Change Streamsが[GA](https://cloud.google.com/blog/products/spanner/change-streams-for-cloud-spanner-now-generally-available?hl=en)化してから、ヘビーなSpannerユーザーの私たちにとしては、とてもとても黙っているわけにはいきません。が、時の流れが早い...世の中には、サービスイメージをつかむための[記事](https://medium.com/google-cloud/change-streams-in-cloud-spanner-replication-to-bigquery-61b20b78118a)とCloud Skills Boostの[ラボ](https://www.cloudskillsboost.google/catalog_lab/5725)がすでに存在しております。そのため、この記事は少し深いところ（Spannerトランザクション処理）を探ってみたいと思います。これからChange Streamsを検証してみたい方に少しでも役立てばいいなと思います。

{{< readmore link="https://qiita.com/l-jiang-zdf/items/0051c5f11e4e8aa39604" >}}
