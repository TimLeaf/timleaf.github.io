---
title: "BigQueryロードする前の文字コード変換"
date: 2021-11-15T00:00:00-09:00
slug: convert-encoding-before-bq-load
draft: false
tag:
  - BigQuery
  - Cloud Functions
  - Cloud Run
  - Eventarc
  - Character code
---

# 背景
Cloud Storage(GCS)からCSVデータをBigQueryに読み込む際は、様々な注意点がありますが、文字コードはそのひとつです。 公式ドキュメントには、下記の文言が含まれています。

> BigQuery に読み込む CSV データは UTF-8 でエンコードされている必要があります。 ISO-8859-1(Latin-1)の場合は--encodingで明記する必要はあります。 [Cloud Storage からの CSV データの読み込み](https://cloud.google.com/bigquery/docs/loading-data-cloud-storage-csv#encoding)

ということで、Shift_JISやEUC-JPなどが多用されているため、BigQueryにロードする前に、UTF-8へ変換しなければなりません。

ここではiconvコマンドを用いて、Shift_JIS(CP932)をUTF-8へ変換をCloud Functions、Cloud Runで試みます。

> Shift_JIS のバリエーションについて、[Shift_JIS 系文字一覧イメージと SJIS・MS932・CP943・SJIS2004 の違い](https://tools.m-bsys.com/ex/sjis.php)を参照してください。

{{< readmore link="https://dryaki.gicloud.co.jp/articles/convert-encoding-before-bq-load" >}}