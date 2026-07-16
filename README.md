# SIMS-Core

SIMS-Coreは、SIMS-Blog-Managerまたは利用者から渡されたSEO改善依頼を、ClaudeなどのAIで実行するためのProductionパッケージです。

## 現在のリリース

Production Claude Package R4 Standard Output & Improvement Authority（UAT Ready）

## 現行インターフェース

- 入力：`SIMS_REQUEST_TEXT_V2`（自然文形式、V1後方互換）
- 出力：`SIMS_FEEDBACK_V1` version `1.1`（回答末尾のJSON）

SIMS-Blog-Manager側をJSON入力へ変更する必要はありません。

## Claudeへの登録

`distribution/SIMS-Core-Claude-Upload/`だけを使用します。

1. `01_Project_Instructions/CLAUDE_PROJECT_INSTRUCTIONS.md`をClaude Projectの「手順」へ貼り付ける。
2. `02_Project_Knowledge/`の8ファイルを「コンテキスト」へ登録する。
3. SIMS-Blog-Managerの改善依頼文をClaudeへ貼り付ける。

詳細は`docs/setup-guide.md`を参照してください。

## 開発資産

- `product/contracts/`：正式な入出力契約
- `claude/`：Claude向け原本
- `tests/`：実記事UAT
- `tools/validate_feedback.py`：Feedback JSON検証
- `distribution/`：利用者向けClaude登録パッケージ


## Product 5.2連携

Search Console上位クエリ、改善優先順位、記事ランク、変更方針、本文JSON、内部リンク候補を受け取り、ビフォー・アフター＋理由で改善します。採用したテキストリンクはアフター完成文へHTMLで直接埋め込み、ブログカードは具体的な挿入位置と完全URLを出力します。


## 標準出力

1. 改善サマリー（Coreが決定した改善レベルと理由を含む）
2. ビフォー・アフター
3. 内部リンク評価
4. 改善後の記事全文（コピペ用）
5. SIMS_FEEDBACK_V1 JSON

記事ランクはSIMS-Blog-Managerが提供し、改善レベルはSIMS-Coreが独自に決定します。Feedback JSONへ記事全文は含めません。
