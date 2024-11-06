---
title: "BeyondCorp Enterprise用いて、GCPへアクセスは会社所有デバイスのみに制限"
date: 2021-11-19T00:00:00-09:00
slug: device-restriction-by-beyondcorp
draft: false
disableRobots: true
tag:
  - BeyondCorp Enterprise
  - Access Context Manager
  - Endpoint Verification
  - VPC Service Controls
---

## BeyondCorp Enterprise とは

Googleはゼロトラストを社内で長年に取り込んで、2021年初にそのソリューションとして、「BeyondCorp Enterprise」のサービスを一般提供しました。 BeyondCorp Enterpriseは、以下４つのGoogle Cloudサービスの組み合わせて、セキュリティの向上につながるソリューションです。

- Identity-Aware Proxy（IAP）によるGCPリソースの保護
  - App Engine、Compute Engine、Kubernetes Engine、オンプレミス環境で動くアプリケーションの保護
  - VMインスタンスへのSSH、RDP接続の保護
- アクセスルールを定義するため、Access Context Manager（ACM）でアクセスレベルの作成
- Identity and Access Management（IAM）条件の適用
  - ACMで作成したアクセスレベルをIAM条件に適用
- Google Chrome拡張機能のEndpoint Verificationによるデバイス情報の収集


{{< readmore link="https://dryaki.gicloud.co.jp/articles/device-restriction-by-beyondcorp" >}}
