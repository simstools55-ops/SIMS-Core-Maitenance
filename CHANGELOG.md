# Changelog

## 0.4.2-production-preview - 2026-07-16

- Reorganized Claude Project Instructions into execution, quality, output, and feedback rules.
- Made the current request the Single Source of Truth over prior conversation history.
- Required complete execution without confirmation when sufficient input is present.
- Prevented repeated requests from being stopped as already processed.
- Consolidated the final-output lock and Japanese deliverable rules.
- Synchronized the source and Claude upload distribution copies.

## 0.4.1-production-preview

- Removed Before/After labels and annotations from copy-ready code blocks.
- Added mandatory Completed Article QA.
- Required complete article output to begin with the introduction and include all sections through the closing links.
- Required adopted and existing blog cards to remain in the completed article unless explicitly removed or replaced.
- Added warnings when an existing blog-card URL cannot be reconstructed from the input.


## 0.4.0-production-preview - 2026-07-16

- 記事ランクはSIMS-Blog-Manager、改善レベルはSIMS-Coreという責務分離を正式化
- 依頼文中の改善レベル指定を採用せず、Coreが独自判定するルールを追加
- Level 1〜5の改善レベルとLevel 5再構築ルールを追加
- 標準出力を改善サマリー、ビフォー・アフター、内部リンク評価、改善後全文、Feedback JSONの5部構成へ固定
- Before/Afterを独立コードブロック化し、タイトル類をtext形式へ統一
- HTML内部リンクに加えてMarkdown版の出力を追加
- 改善後の記事全文を必須化し、Feedback JSONへ全文を含めない仕様を明記
- Claude Knowledgeを8ファイル構成へ更新

## 0.3.0-production-preview - 2026-07-15

- SIMS_REQUEST_TEXT_V2を追加し、Product 5.2依頼文へ対応
- Search Console上位20クエリ、改善優先順位、記事ランク、変更方針に対応
- Internal Link Optimization Knowledgeを追加
- 採用テキストリンクをアフター完成文へHTMLで直接埋め込む仕様を追加
- ブログカードの挿入位置、記事タイトル、完全URLの出力を必須化
- 内部リンクの採用・保留・不採用評価とUAT項目を追加
- Claude登録用distributionを7 Knowledge構成へ更新

## 0.2.0-production-preview - 2026-07-14

- Claude Project InstructionsをProduction品質へ拡張
- Knowledge 6ファイルの改善判断・執筆・QAルールを具体化
- SIMS_FEEDBACK_V1の変更フラグ対応表を追加
- 実記事UATガイドとチェックリストを追加
- Feedback JSON検証スクリプトを追加
- Claude登録用distributionを再生成

## 0.1.0-production-preview

- Production Architecture R1
- SIMS_REQUEST_TEXT_V1とSIMS_FEEDBACK_V1 v1.1を正式化
