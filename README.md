# 鈴木潤平のポートフォリオ

## 整形外科混雑分析

### 背景・目的
整形外科クリニックにおける混雑時間帯、主訴別リハビリ時間、年齢層ごとの来院傾向をSQLとTableauで分析し、
待ち時間短縮や人員配置の最適化、患者サービス向上の具体的施策のヒントを得ることを目的としました。

### 仮説
- 月曜・土曜午前中に来院が集中して混雑が発生している。
- 高齢患者の来院比率が高く、特に腰・膝の疾患で高齢患者の来院件数が多い。
- 主訴によってリハビリ時間に大きな差がある。

### 分析結果
- **ヒートマップ（曜日・時間帯別受付件数）**
  ：月曜・土曜の9〜11時台に来院件数のピークが集中し、混雑時間帯と一致。

- **主訴別 来院患者の年齢層構成比**
  ：全疾患で高齢患者の割合が高く、特に肘・膝・首の順に高齢患者の来院件数が多かった。

- **主訴別 平均リハビリ時間と来院件数**
  ：平均リハビリ時間は主訴間で大きな差はなかったものの、肘・膝・首の順に来院件数が多く、負担集中リスクが示唆された。


### 提案と期待される結果

- **月曜・土曜午前中のシフトを強化し、受付体制を見直す**  
  混雑ピーク時に人員を増員し、受付手順を簡略化する。問診票を事前配布し、診察券・保険証確認をチェックリスト化することで、受付処理を迅速化する。  
  *これにより、待機時間を短縮し、患者のストレスを軽減する。*

- **来院時間の分散を目的とした簡易予約と受付番号発行システムを導入する**  
  窓口・電話での予約受付や番号順受付を実施し、来院時間の集中を防ぐ。  
  *これにより、待合室の混雑を解消し、受付業務を効率化する。*

- **高齢患者向けに優先受付枠を設け、院内動線を最適化する**  
  優先受付時間帯を設定し、誘導サインやスタッフの積極的な声かけ対応を徹底する。  
  *これにより、高齢患者の混乱を防ぎ、安全でスムーズな案内を実現する。*

- **リハビリ負担の大きい主訴に応じて専門担当者を配置し、時間帯別体制を強化する**  
  データに基づく主訴別・時間帯別の担当配置を行い、リハビリ待機時間を短縮する。  
  *これにより、リハビリの品質を安定させ、作業の偏りを防止する。*

- **混雑状況やリハビリデータを定期的に分析し、体制を継続的に見直す**  
  月次・四半期ごとにデータを振り返り、人員配置や業務フローを改善する。  
  *これにより、状況変化に柔軟に対応し、無駄を削減して業務効率を高める。*


### SQLファイル
- [曜日・時間帯別混雑分析](https://console.cloud.google.com/bigquery?sq=548316000047:ab9484a99f3c4a1f967c74975720ee85)
- [曜日・時間帯別混雑分析結果（CSVファイル）](https://github.com/jumpei-suzuki20/sql-portfolio/blob/main/%E6%9B%9C%E6%97%A5%E3%83%BB%E6%99%82%E9%96%93%E5%B8%AF%E5%88%A5%E6%B7%B7%E9%9B%91%E5%88%86%E6%9E%90.csv)

- [主訴別 平均リハビリ時間と来院件数分析](https://console.cloud.google.com/bigquery?sq=548316000047:64a3913600c04c70b725197159545067)
- [主訴別 平均リハビリ時間と来院件数分析結果（CSVファイル）](https://github.com/jumpei-suzuki20/sql-portfolio/blob/main/%E4%B8%BB%E8%A8%B4%E5%88%A5%20%E5%B9%B3%E5%9D%87%E3%83%AA%E3%83%8F%E3%83%92%E3%82%99%E3%83%AA%E6%99%82%E9%96%93%E3%81%A8%E6%9D%A5%E9%99%A2%E4%BB%B6%E6%95%B0%E5%88%86%E6%9E%90%E7%B5%90%E6%9E%9C.csv)

- [主訴別 来院患者の年齢層構成比](https://console.cloud.google.com/bigquery?sq=548316000047:c28ad27aee59457fa1d843eeed82e25b)
- [主訴別 来院患者の年齢層構成比分析結果（CSVファイル）](https://github.com/jumpei-suzuki20/sql-portfolio/blob/main/%E4%B8%BB%E8%A8%B4%E5%88%A5%20%E6%9D%A5%E9%99%A2%E6%82%A3%E8%80%85%E3%81%AE%E5%B9%B4%E9%BD%A2%E5%B1%A4%E6%A7%8B%E6%88%90%E6%AF%94%E7%B5%90%E6%9E%9C.csv)

### 可視化例
#### ヒートマップ（曜日×時間帯の来院件数）
- [ヒートマップダッシュボードを見る（曜日×時間帯の来院件数）](https://public.tableau.com/views/_17505907730690/1_1?:language=ja-JP&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


#### 主訴別 平均リハビリ時間と来院件数
- [主訴別 平均リハビリ時間と来院件数ダッシュボードを見る](https://public.tableau.com/views/_17505908189580/2_1?:language=ja-JP&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


#### 主訴別 来院患者の年齢層構成比
- [主訴別 来院患者の年齢層構成比ダッシュボードを見る](https://public.tableau.com/views/_17505909176350/7?:language=ja-JP&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

### フォルダ構造
```
orthopedic-congestion-analysis/
├── README.md
├── sql/
│   ├── https://console.cloud.google.com/bigquery?sq=548316000047:ab9484a99f3c4a1f967c74975720ee85
│   ├── https://console.cloud.google.com/bigquery?sq=548316000047:64a3913600c04c70b725197159545067
│   └── https://console.cloud.google.com/bigquery?sq=548316000047:c28ad27aee59457fa1d843eeed82e25b
├── report/
│   ├── https://github.com/jumpei-suzuki20/sql-portfolio/blob/main/%E6%9B%9C%E6%97%A5%E3%83%BB%E6%99%82%E9%96%93%E5%B8%AF%E5%88%A5%E6%B7%B7%E9%9B%91%E5%88%86%E6%9E%90.csv
│   ├── https://github.com/jumpei-suzuki20/sql-portfolio/blob/main/%E4%B8%BB%E8%A8%B4%E5%88%A5%20%E5%B9%B3%E5%9D%87%E3%83%AA%E3%83%8F%E3%83%92%E3%82%99%E3%83%AA%E6%99%82%E9%96%93%E3%81%A8%E6%9D%A5%E9%99%A2%E4%BB%B6%E6%95%B0%E5%88%86%E6%9E%90%E7%B5%90%E6%9E%9C.csv
│   └── https://github.com/jumpei-suzuki20/sql-portfolio/blob/main/%E4%B8%BB%E8%A8%B4%E5%88%A5%20%E6%9D%A5%E9%99%A2%E6%82%A3%E8%80%85%E3%81%AE%E5%B9%B4%E9%BD%A2%E5%B1%A4%E6%A7%8B%E6%88%90%E6%AF%94%E7%B5%90%E6%9E%9C.csv
├── dashboards/
│   ├── https://public.tableau.com/views/_17505907730690/1_1?:language=ja-JP&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
│   ├── https://public.tableau.com/views/_17505908189580/2_1?:language=ja-JP&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
│   └── https://public.tableau.com/views/_17505909176350/7?:language=ja-JP&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
```

