# 改善依頼サンプル

次の記事をSEO改善してください。
ArticleID: A000012
URL: https://example.com/article.html
記事タイトル: 現在の記事タイトル
SEOタイトル: 現在のSEOタイトル
メタディスクリプション: 現在の説明文
メインクエリ: メインクエリ
現在値: クリック 16、表示 2946、CTR 0.5%、順位 7.2位
改善目的: 改善候補。タイトル、導入文、見出し、FAQを優先し、既存記事の良い部分は残してください。


【Search Console 上位クエリ】

1. メインクエリ
   クリック：10
   表示回数：1000
   CTR：1.0%
   平均順位：8.0

【改善優先順位】

1. SEOタイトル
2. 導入文
3. H2見出し
4. FAQ
5. 本文
6. 画像

【記事ランク】

B（成長）

【改善レベル（任意・Coreでは採用しません）】

Level 2

【変更方針】

- 既存本文は可能な限り維持
- タイトル・導入・H2・FAQを優先改善
- 広告コードは変更しない
- アフィリエイトリンクは変更しない

【現在の記事本文データ（JSON）】

```json
{
  "format": "SIMS_ARTICLE_SOURCE_V1",
  "version": "1.0",
  "truncated": false,
  "introduction": "現在の導入文",
  "sections": []
}
```

【内部リンク候補】

1. 関連記事タイトル
   URL: https://example.com/related.html
   推奨アンカーテキスト: 関連記事の内容が分かる言葉
   関連クエリ: 関連クエリ
   関連度: ★★★★★

【内部リンク利用ルール】

- 候補は参考情報です。
- 本文の流れと検索意図に合う候補だけ採用してください。
- 無理に全件使用する必要はありません。
- テキストリンクを採用する場合は、変更後の完成文へHTMLリンクを直接埋め込んでください。
- ブログカードが適切な場合は、具体的な挿入位置と完全URLを明記してください。

【標準出力】

改善サマリー、ビフォー・アフター、内部リンク評価、改善後の記事全文、SIMSフィードバックJSONの順で出力してください。改善レベルはSIMS-Coreが独自に決定してください。

【SIMSへのフィードバック出力ルール】
回答の最後に、下記仕様のJSONをコードブロックで必ず1つ出力してください。JSONの前後に説明を書いても構いませんが、JSON内にはコメントを入れないでください。

```json
{
  "format": "SIMS_FEEDBACK_V1",
  "version": "1.1",
  "article_id": "A000012",
  "article_url": "https://example.com/article.html",
  "completed_at": "YYYY-MM-DD",
  "changes": {
    "article_title": false,
    "seo_title": false,
    "description": false,
    "introduction": false,
    "headings": false,
    "faq": false,
    "internal_links": false,
    "body": false,
    "images": false
  },
  "new_values": {
    "article_title": "",
    "seo_title": "",
    "description": "",
    "main_query": "メインクエリ"
  },
  "improvement_type": "normal",
  "confidence": "high",
  "expected_effect": {"ctr": "", "clicks": ""},
  "next_action": "monitor",
  "summary": "実施した改善の要約",
  "warnings": [],
  "estimated_minutes": 20,
  "recommended_review_days": 14
}
```

変更していない項目はfalse、変更後の値がない項目は空文字にしてください。recommended_review_daysは7・14・30のいずれかにしてください。improvement_typeはminor・normal・major、confidenceはhigh・medium・low、next_actionはmonitor・remeasure・rewrite・noneのいずれかにしてください。
