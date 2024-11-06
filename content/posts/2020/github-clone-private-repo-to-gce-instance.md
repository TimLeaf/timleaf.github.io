---
title: "「Terraform」作成した GCE インスタンス中で、GitHub プライベートリポジトリからソースを落とす"
date: 2020-07-05T00:00:00-09:00
slug: github-clone-private-repo-to-gce-instance
draft: false
disableRobots: true
tag:
  - Terraform
  - Compute Engine
  - GitHub
  - Bash script
  - Cloud Storage
---

## 背景

Terraform を利用して GCP などのリソースを簡単に apply・destroy できるから、必要となる時に、GCE インスタンスを作って、GitHub 上のプライベートリポジトリのソースをインスタンスで動かすという要望はありました。

Terraform バージョン:

- Terraform v0.12.28
- provider.google v3.5.0

## GitHub アカウントの SSH 秘密鍵

GitHub Docsを参照して、パスフレーズなしの SSH 秘密鍵を作ります。そして、作成した公開鍵（id_rsa.pub）は GitHub アカウントへ追加します。

秘密鍵（id_rsa）は Terraform で GCS バケットの作成とともに、バケットにアップロードします。

{{< readmore link="https://qiita.com/kyou_rai/items/ffe02998302eae720c36" >}}
