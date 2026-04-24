# ライセンス情報

最終更新日: 2026年4月24日

## VSAについて

VSA（Virtual Snap Archive）は、写真の整理、検索、メタデータ管理、JPEG XL圧縮、任意のクラウド保存、任意のX投稿を行うためのデスクトップアプリケーションです。

VSA本体のソースコード、名称、ロゴ、独自UI、独自ドキュメントの権利は運営者または正当な権利者に帰属します。VSA本体は、別途明示された範囲を除き、オープンソースソフトウェアとして提供されるものではありません。

## サードパーティライブラリ

VSAは、npmパッケージおよびRust crateを含む複数のサードパーティソフトウェアを利用しています。主な依存関係とライセンス種別は以下のとおりです。

| 分類 | 主なライブラリ | 主なライセンス |
| --- | --- | --- |
| フロントエンド | React, React DOM, React Router, i18next, TanStack Table/Virtual, Radix UI, Tailwind CSS, Sonner, Tabler Icons | MIT / ISC / Apache-2.0等 |
| デスクトップ基盤 | Tauri, Tauri plugins | MIT / Apache-2.0 |
| Rust基盤 | serde, tokio, reqwest, rusqlite, tracing, notify, axum, keyring, image, png, uuid等 | MIT / Apache-2.0 / BSD系等 |
| 画像処理 | image, png, jxl-oxide, zune-jpegxl, imageproc, ab_glyph | MIT / Apache-2.0 / BSD系等 |
| Web/解析系の推移依存 | cssparser, selectors等 | MPL-2.0等 |

確認時点では、主要なランタイム依存にGPL/AGPLのみで配布義務が発生する依存は確認していません。ただし、依存関係はアップデートにより変化するため、リリースごとに `package-lock.json` と `Cargo.lock` を基準に再確認します。

## 注意が必要なライセンス

- MPL-2.0の依存が一部含まれます。通常の動的/静的利用自体は可能ですが、対象ライブラリ自体を改変して配布する場合はMPL-2.0の条件に従う必要があります。
- 一部の依存は複数ライセンスから選択できる形で提供されています。配布時は許容されるライセンス条件を選択して扱います。
- npm依存には、ライセンス表記がpackage metadataに存在しないが、同梱LICENSEでMIT等が確認できるものがあります。

## 配布時の対応方針

リリース配布物には、以下のいずれかの形でサードパーティ通知を同梱します。

1. `THIRD-PARTY-NOTICES.txt` として、npm/Rust依存の名称、バージョン、ライセンス、著作権表示、ライセンステキスト参照をまとめる
2. アプリ内ドキュメントの本ページから、同等の通知ファイルへリンクする

## 第三者名称について

VRChat、VirtualLens2、Integral、X、Google、Cloudflare、Supabase、GitHub等の名称は、それぞれの権利者に帰属します。VSAは、VRChat Inc.、VirtualLens2、Integralおよび各権利者とは提携・承認・サポート関係にない非公式ツールです。

## お問い合わせ

ライセンスに関するお問い合わせは、以下までご連絡ください。

virtualsnaparchive@gmail.com
