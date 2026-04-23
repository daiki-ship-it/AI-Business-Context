# AI事業コンテキスト（SSOT）

このリポジトリは **AI伴走プログラム**まわりの**単一情報源（SSOT）**です。  
同じ事実を複数ファイルに書かないことを原則にし、**拡大時も「どこを直すか」が迷子にならない**構成にしています。

## タスク管理と「いまの現状」（Notion ＋ このリポ）

| 何の正か | どこ |
|----------|------|
| **締切・進捗・やること一覧（編集する場所）** | [**Notion：AIローンチ進捗管理**](https://www.notion.so/AI-33e2623b5cc0803e9959f49c7f8b3a52?source=copy_link) |
| **Notion の写し（自動・読み取り専用）** | [context/notion-tasks.generated.md](context/notion-tasks.generated.md)（[同期のセットアップ](docs/NOTION_SYNC_SETUP.md)） |
| **事業コンテンツ**（商品・ICP など。人物の経歴の**事実**は [`My context`](../My%20context/career-timeline.md)） | 下記 `ssot/` |
| **Cursor / AI 向けメモ（正本ではない・ブロッカー等のみ）** | [context/current-phase.md](context/current-phase.md) |

Notion を更新すると、**GitHub Actions で `notion-tasks.generated.md` が更新される**（設定後）。Cursor では **`@context/notion-tasks.generated.md`** で最新タスク表を参照できる。

**Mac のフォルダまで自動で揃えたい:** Git は **リモート（GitHub）だけ**を更新するので、手元は **`git pull` が必要**。**Cursor でこのフォルダを開いたときに自動 `git pull`** する設定を入れてある（`.vscode/tasks.json`）。詳細と代替手段は [docs/LOCAL_AUTO_PULL.md](docs/LOCAL_AUTO_PULL.md)。

## 運用ルール（1人運用向け）

1. **事実・数値・肩書・約束の文言は、該当する `ssot/*.md` だけを編集する（例外: 下記の人物ファクト正本は `My context`）。**  
   LP・提案書・AIへのプロンプト用メモに**同文を複製しない**（参照する）。
2. **経歴と実数の正本（ワークスペース全体）は [`../My context/career-timeline.md`](../My%20context/career-timeline.md)（要約は [`../My context/context.md`](../My%20context/context.md)）。`ssot/career.md` はその参照入口にすぎない。**
3. **ICP（ペルソナ）は `ssot/persona-icp.md` のみ。** 上記正本の実話と矛盾させない。
4. **商品の週次・フローは `ssot/product-ai-accompany.md` のみ。** キャッチやゴールを変えたらここを先に直す。
5. 将来ファイルが増えても、**新規は `ssot/` 配下に置き、下の「ファイル地図」に1行追加する**（検索の入口を増やしすぎない）。
6. **タスクの締切・完了は Notion が正。** リポジトリには [context/notion-tasks.generated.md](context/notion-tasks.generated.md) が **自動同期**で追従する（手で編集しない）。[context/current-phase.md](context/current-phase.md) には **タスク一覧やフェーズの複製を書かない**（ブロッカー等の任意メモのみ）。
7. **Notion のタスクDBのメモ欄に、`ssot/*.md` の全文を貼らない。** 必要なら「→ `ssot/brand.md`」など **参照1行**にし、[context/notion-tasks.generated.md](context/notion-tasks.generated.md) の写しに二重の正を増やさない。

## ファイル地図（どこに何があるか）

| ファイル | 中身 |
|----------|------|
| [context/notion-tasks.generated.md](context/notion-tasks.generated.md) | Notion タスク表の自動スナップショット（**編集禁止**） |
| [context/current-phase.md](context/current-phase.md) | ブロッカー等の任意メモ（タスク・フェーズの複製は書かない） |
| [docs/NOTION_SYNC_SETUP.md](docs/NOTION_SYNC_SETUP.md) | Notion ↔ GitHub 自動同期のセットアップ手順 |
| [docs/LOCAL_AUTO_PULL.md](docs/LOCAL_AUTO_PULL.md) | Mac で朝に自動 `git pull` する（任意） |
| [docs/business-program-idea-current.md](docs/business-program-idea-current.md) | 外向けLPの**参照入口**（正本は `ssot/`、HTML は人間用） |
| [docs/exports-for-human/](docs/exports-for-human/) | ブラウザ用HTMLなど（`.cursorignore` でインデックス対象外にしやすい） |
| [ssot/brand.md](ssot/brand.md) | 表示名などブランド要素（**事業コンセプト本文の正本は** [ssot/business-concept.md](ssot/business-concept.md)） |
| [docs/契約書_AI業務再設計30日伴走.md](docs/契約書_AI業務再設計30日伴走.md) | 法的条項の正本 |
| [ssot/provider-contact.md](ssot/provider-contact.md) | 乙の連絡先・記入用 HTML との手順（条文の正本は上記契約書のみ） |
| [ssot/career.md](ssot/career.md) | **正本ではない** — [`My context/career-timeline.md`](../My%20context/career-timeline.md) への参照用 |
| [ssot/profile.md](ssot/profile.md) | USP・キャラ・約束（事実の重複なし） |
| [ssot/persona-icp.md](ssot/persona-icp.md) | 対象者・ペルソナ |
| [ssot/product-ai-accompany.md](ssot/product-ai-accompany.md) | AI伴走プログラム（1ヶ月）の設計 |

## よくある作業

- **プロフィールの話し方を変えたい** → `ssot/profile.md`
- **実績の数字や肩書（事実）を変えたい** → [`../My context/career-timeline.md`](../My%20context/career-timeline.md)（要約は `../My context/context.md`）。`ssot/career.md` を開いてパスを確認
- **誰に売るかを変えたい** → `ssot/persona-icp.md`
- **プログラムの週の中身を変えたい** → `ssot/product-ai-accompany.md`
- **ブランド名・事業の一文を変えたい** → `ssot/brand.md`

## 拡大するとき

- 新しい商品・プログラムが増えたら **`ssot/product-<名前>.md`** を追加する（例: `product-3month.md`）。
- チーム・協業などで境界が増えたら **`ssot/` にドメイン名のファイルを足す**だけにし、README のファイル地図に1行追加する。
