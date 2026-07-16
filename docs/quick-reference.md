# Quick Reference

- 手順へ貼る：`01_Project_Instructions/CLAUDE_PROJECT_INSTRUCTIONS.md`
- コンテキストへ追加：`02_Project_Knowledge/*.md`
- 毎回貼る：SIMS-Blog-Managerの改善依頼文
- Blog-Managerへ戻す：回答末尾のSIMS_FEEDBACK_V1 JSON
- 旧Engineファイル：登録不要


## 内部リンク

- テキストリンク：変更後のHTMLをそのままコピー
- ブログカード：指定位置へ完全URLを貼付
- 候補は全件使用不要
- 不自然なリンクは追加しない


## R4要点

- 記事ランク：Blog-Managerが提供
- 改善レベル：Coreが決定
- 標準出力：サマリー→Before/After→内部リンク評価→全文→JSON
- Feedback JSONに記事全文は入れない
- Claude Knowledgeは8ファイル


## R5出力品質ルール

- Before／Afterのコードブロック内には、コピー対象以外のラベルを入れません。
- 改善後の記事全文は導入文から文末の内部リンク・ブログカードまで含みます。
- ブログカードは完全URLを完成記事の指定位置へ反映します。
