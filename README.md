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
- [congestion_analysis.sql](./sql/congestion_analysis.sql)：曜日・時間帯別混雑分析
- [symptom_analysis.sql](./sql/symptom_analysis.sql)：主訴別リハビリ時間・年齢層傾向分析

### 可視化例
#### ヒートマップ（曜日×時間帯の来院件数）
![ヒートマップ](https://github.com/user-attachments/assets/4713e5a1-f668-442e-8ce2-1f824688d4d4)

#### 主訴別 平均リハビリ時間と来院件数
![主訴別リハビリ](https://github.com/user-attachments/assets/d6ebab98-7d5d-4a43-b5aa-7c433cb5ca8a)

#### 主訴別 来院患者の年齢層構成比
![主訴別年齢層]([./dashboards/age_group_bar_chart.png](https://public.tableau.com/views/_17505909176350/7?:language=ja-JP&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link))


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
