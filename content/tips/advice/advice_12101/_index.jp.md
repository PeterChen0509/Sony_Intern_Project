---
title: "データの行数を減らしましょう"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
weight: 4
draft: false
# metaタグのパラメータ
meta:
  description: "予測分析ツールPrediction Oneが提案する精度改善のための改善ヒントについて説明するページです。"
# クラウド・デスクトップ限定ページの場合は片方のみtrueにする
visible:
  is_cloud_only: false
  is_desktop_only: false
# 検索でヒットする文字列の指定
keywords:
  ["ヒント","改善ヒント","tips","精度改善"]
toc: true
---

### 説明
精度は高いのに、予測モデルの作成に時間がかかる場合は、学習用データから一部の行を削除しましょう。
時系列予測モードで予測モデルの作成を行う場合は古いデータを削除しましょう。それ以外の予測モデルを作成する場合はランダムに削除しましょう。
学習用データの行数が十分に多い場合、データの行数をある程度減らしても、予測モデルの精度はあまり変わらないことが多く、予測モデルの作成時間も削減することができます。

![](../img/t_slide12.png)

### 関連資料

- {{% a_in "./../../../terminology/imbalance/" "データの偏り・不均衡なデータ" %}}

