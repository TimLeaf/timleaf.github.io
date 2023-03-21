---
title: "DataflowカスタムコンテナでDBSCANクラスタリングを実行してみた"
date: 2022-01-24T00:00:00-09:00
slug: run-dbscan-in-dataflow-custom-container
draft: false
disableRobots: true
tag:
  - Dataflow
  - Docker
  - DBSCAN
---

# 背景

> Dataflow now supports [custom containers](https://cloud.google.com/dataflow/docs/guides/using-custom-containers) in GA.
> ※ このカスタム コンテナ機能は、Python で一般提供が開始されました。Java ではプレビューで利用できます。

になってから、もうすぐ半年が経ちます。一方、初心者にやさしいBigQuery MLのクラスタリングはK平均法（k-means）のみサポートしています。DBSCANはk-meansより優れるように[見え](https://scikit-learn.org/stable/auto_examples/cluster/plot_cluster_comparison.html#sphx-glr-auto-examples-cluster-plot-cluster-comparison-py)ますので、Dataflowカスタムコンテナで回してみることにしました。

# 準備
[Dataflow でのカスタム コンテナの使用](https://cloud.google.com/dataflow/docs/guides/using-custom-containers#python)には詳しい内容がありますから、Apache Beam SDK (>2.30.0)とDockerインストールの説明は割愛させていただきます。

{{< readmore link="https://dryaki.gicloud.co.jp/articles/run-dbscan-in-dataflow-custom-container" >}}