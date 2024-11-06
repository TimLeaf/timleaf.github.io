---
title: "Google Cloud Composer で Bigquery にロード時 「Error: Bad character (ASCII 0) encountered.」の回避策"
date: 2020-02-25T00:00:00-09:00
slug: avoid-ascii-0-error-cloud-composer
draft: false
disableRobots: true
tag:
  - Cloud Composer
  - BigQuery
  - Airflow
  - Bash script
  - Null character
---

## 背景

GoogleCloudStorageToBigQueryOperator を使った csv ファイルを Bigquery にロードする処理で、下記のエラーが発生しました。

> 「Error while reading data, error message: Error detected while parsing row starting at position: XXX. Error: Bad character (ASCII 0) encountered.」

## 回避策

調べたところ、取込 csv ファイルに「[ヌル文字 - Wikipedia](https://ja.wikipedia.org/wiki/%E3%83%8C%E3%83%AB%E6%96%87%E5%AD%97)」が混入しました。

{{< readmore link="https://qiita.com/kyou_rai/items/6c3bc3ca2bf6c9371b59" >}}
