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

- **主訴別 平均リハビリ時間と来院件数**
  ：平均リハビリ時間は主訴間で大きな差はなかったものの、肘・膝・首の順に来院件数が多く、負担集中リスクが示唆された。

- **主訴別 来院患者の年齢層構成比**
  ：全疾患で高齢患者の割合が高く、特に肘・膝・首の順に高齢患者の来院件数が多かった。

### 提案
- 月曜・土曜午前中のシフト強化、受付体制の見直し。
- 高齢患者向けの優先受付枠や動線の工夫。
- 来院件数が多くリハビリ負担の大きい主訴に応じた専門担当者配置、時間帯別体制強化。

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
│   ├── congestion_analysis.sql
│   ├── symptom_rehab_analysis.sql
│   └── symptom_agegroup_analysis.sql
├── report/
│   ├── congestion_analysis_result.csv
│   ├── symptom_rehab_analysis_result.csv
│   └── symptom_agegroup_analysis_result.csv
├── dashboards/
│   ├── congestion_heatmap.png
│   ├── symptom_bar_chart.png
│   └── age_group_bar_chart.png
```

