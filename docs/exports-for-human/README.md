# 人間向けエクスポート（HTML など）

**このフォルダのファイルは消さない。** ブラウザで開く・相手に渡す・印刷するためのものです。

| 種類 | AI が読むときの正本（Markdown） |
|------|----------------------------------|
| 外向けLPの文章・構成 | [`../business-program-idea-current.md`](../business-program-idea-current.md) → そこから `ssot/` へ |
| 外向けLPの PDF（印刷・送付用） | このフォルダの `business-program-idea-current.pdf`（中身は上記と整合させる） |
| 契約の条文 | [`../契約書_AI業務再設計30日伴走.md`](../契約書_AI業務再設計30日伴走.md) |
| 記入用HTML | このフォルダ内の `.html`（手続きは [`../../ssot/provider-contact.md`](../../ssot/provider-contact.md)） |

リポジトリ直下の `.cursorignore` にこのフォルダが書いてあるため、**Cursor が自動で読み込む範囲から外れやすい**です。AI に見せたいときは `@docs/exports-for-human/ファイル名` のように明示してください。
