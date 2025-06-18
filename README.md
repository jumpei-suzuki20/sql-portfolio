# 鈴木潤平のポートフォリオ

## 整形外科混雑分析

### 背景・目的
整形外科クリニックの混雑時間帯や主訴別リハビリ時間の傾向をSQLとTableauで分析し、  
待ち時間短縮や人員配置の最適化のヒントを得ることを目的としました。

### 仮説
- 月曜・土曜午前中に来院が集中して混雑が発生している
- 土曜は高齢患者の来院比率が高い
- 主訴によってリハビリ時間に大きな差がある

### 分析結果
- **ヒートマップ**：月曜・土曜の10-11時台で来院件数・待ち時間がピーク
- **主訴別平均リハビリ時間**：肩・腰のリハビリが長時間傾向
- **土曜年齢層別棒グラフ**：65歳以上が全体の約8割

### 提案
- 混雑時間帯のスタッフ増員・シフト調整
- 高齢患者向け優先受付枠の導入
- 主訴別にリハビリ担当者の配置見直し

### SQLファイル
- [congestion_analysis.sql](./sql/congestion_analysis.sql)：曜日・時間帯別混雑分析
- [symptom_analysis.sql](./sql/symptom_analysis.sql)：主訴別リハビリ時間・傾向分析

### 可視化例
#### ヒートマップ（曜日×時間帯の来院件数・平均待ち時間）
![ヒートマップ](./dashboards/congestion_heatmap.png)

#### 主訴別 平均リハビリ時間
![主訴別リハビリ](./dashboards/symptom_bar_chart.png)

#### 土曜日 年齢層別 来院件数
![土曜年齢層](./dashboards/age_group_bar_chart.png)

### 構成

├── README.md
├── sql/
│ ├── congestion_analysis.sql
│ └── symptom_analysis.sql
├── dashboards/
│ ├── congestion_heatmap.png
│ ├── symptom_bar_chart.png
│ └── age_group_bar_chart.png
└── report/
