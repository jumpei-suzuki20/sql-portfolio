# 鈴木潤平のポートフォリオ

## 整形外科混雑分析

### 背景・目的
整形外科クリニックにおける混雑時間帯、主訴別リハビリ時間、年齢層ごとの来院傾向をSQLとTableauで分析し、
待ち時間短縮や人員配置の最適化、患者サービス向上の具体的施策のヒントを得ることを目的としました。

### 仮説
- 月曜・土曜午前中に来院が集中して混雑が発生している
- 高齢患者の来院比率が高く、特に腰・膝の疾患で高齢患者の来院件数が多い
- 主訴によってリハビリ時間に大きな差がある

### 分析結果
- **ヒートマップ（曜日・時間帯別受付件数）**
  月曜・土曜の9〜11時台に来院件数のピークが集中し、混雑時間帯と一致

- **主訴別 平均リハビリ時間と来院件数**
  平均リハビリ時間は主訴間で大きな差はなかったものの、肘・膝・首の順に来院件数が多く、負担集中リスクが示唆された

- **主訴別 来院患者の年齢層構成比**
  全疾患で高齢患者の割合が高く、特に肘・膝・首の順に高齢患者の来院件数が多かった

### 提案
- 月曜・土曜午前中のシフト強化、受付体制の見直し
- 高齢患者向けの優先受付枠や動線の工夫
- 来院件数が多くリハビリ負担の大きい主訴に応じた専門担当者配置、時間帯別体制強化

### SQLファイル
- 曜日・時間帯別混雑分析:(https://console.cloud.google.com/bigquery?sq=548316000047:ab9484a99f3c4a1f967c74975720ee85)
- - [曜日・時間帯別混雑分析結果（CSVファイル）](https://github.com/jumpei-suzuki20/sql-portfolio#:~:text=5%20minutes%20ago-,%E6%9B%9C%E6%97%A5%E3%83%BB%E6%99%82%E9%96%93%E5%B8%AF%E5%88%A5%E6%B7%B7%E9%9B%91%E5%88%86%E6%9E%90.csv,-Add%20files%20via)
- 主訴別リハビリ時間・年齢層傾向分析：(https://console.cloud.google.com/bigquery?sq=548316000047:9c261e3374be4233a1b88e8f0027e1d5)
- 主訴別 来院患者の年齢層構成比:(https://console.cloud.google.com/bigquery?sq=548316000047:c28ad27aee59457fa1d843eeed82e25b)

### 可視化例
#### ヒートマップ（曜日×時間帯の来院件数）
- [ヒートマップダッシュボードを見る（曜日×時間帯の来院件数）](https://public.tableau.com/views/_17505907730690/1_1?:language=ja-JP&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


#### 主訴別 平均リハビリ時間と来院件数
- [主訴別 平均リハビリ時間と来院件数ダッシュボードを見る](https://public.tableau.com/views/_17505908189580/2_1?:language=ja-JP&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


#### 主訴別 来院患者の年齢層構成比
- [主訴別 来院患者の年齢層構成比ダッシュボードを見る](https://public.tableau.com/views/_17505909176350/7?:language=ja-JP&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


orthopedic-congestion-analysis/
├── README.md  （GitHub 用の内容入り）
├── sql/
│   ├── congestion_analysis.sql
│   └── symptom_analysis.sql
├── dashboards/
│   ├── congestion_heatmap.png （ダミー）
│   ├── symptom_bar_chart.png （ダミー）
│   └── age_group_bar_chart.png （ダミー）
└── report/
