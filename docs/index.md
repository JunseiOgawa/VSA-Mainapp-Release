# Virtual Snap Archive ドキュメント

VSA（Virtual Snap Archive）の使い方、セットアップ、規約、プライバシー、ライセンス情報をまとめた公開ドキュメントです。

## 規約・プライバシー・ライセンス

配布物やアプリ内の設定画面から参照する重要文書です。販売・配布ページでも以下の公開URLを明示してください。

- 利用規約（日本語）: https://junseiogawa.github.io/VSA-Mainapp-Release/ja/terms.html
- プライバシーポリシー（日本語）: https://junseiogawa.github.io/VSA-Mainapp-Release/ja/privacy.html
- Terms of Service: https://junseiogawa.github.io/VSA-Mainapp-Release/en/terms.html
- Privacy Policy: https://junseiogawa.github.io/VSA-Mainapp-Release/en/privacy.html
- ライセンス情報: https://junseiogawa.github.io/VSA-Mainapp-Release/license.html

Google OAuthの公開設定に掲載するプライバシーポリシーURLは、現行のウェブサイト版 `https://vsa-website-wine.vercel.app/ja/privacy` を使用します。

アプリ内では、**設定 > その他** から規約、プライバシーポリシー、ライセンス情報、GitHub Releases、ドキュメントトップを開けます。

## はじめに

- [インストール](./installation.md)
- [はじめに（初回セットアップ）](./guide/getting-started.md)
- [基本操作ガイド](./guide/basic-usage.md)

## サポート

- [FAQ](./faq.md)
- [トラブルシューティング](./troubleshooting.md)

## ドキュメント

### 日本語版

#### 基本操作
- [ギャラリー操作ガイド](./ja/gallery-guide.md) - 写真表示、ソート、お気に入り、ゴミ箱機能
- [ユーザー検索](./ja/person-search-guide.md) - 特定ユーザーが写っている写真検索

#### VRChat連携・カメラ制御
- [VRChat連携](./ja/vrchat-integration.md) - VRChatメタデータ取得
- [VirtualLens Controller](./ja/controller-guide.md) - カメラパラメータのリアルタイム制御
- [ゲーム側設定](./ja/game-config.md) - VRChat連携設定、タイムマシーン、サーバーステータス

#### 写真編集・共有
- [X投稿機能ガイド](./ja/x-post-guide.md) - X投稿、カメラ情報フレーム、プリセット管理
- [JXL圧縮](./ja/jxl-compression.md) - JPEG XL形式での写真圧縮

#### アカウント・クラウド連携
- [アカウントガイド](./ja/account-guide.md) - VSAアカウント管理、OAuth、X投稿状況
- [お気に入りガイド](./ja/favorites-guide.md) - お気に入り管理とクラウド保存

#### カスタマイズと設定
- [設定ガイド](./ja/settings-guide.md) - 全設定パネル詳細（外観、アニメーション、ファイル、システム、X投稿など）
- [キーボードショートカット](./ja/keyboard-shortcuts.md) - ショートカット一覧とカスタマイズ
- [セットアップウィザード](./ja/setup-wizard.md) - 初回セットアップガイド

#### サポート
- [FAQ](./ja/faq.md) - よくある質問と回答
- [トラブルシューティング](./ja/troubleshooting.md) - 問題解決ガイド

#### その他
- [利用規約](./ja/terms.md)
- [プライバシーポリシー](./ja/privacy.md)

### 英語版

#### Basic Operations
- [Gallery Guide](./en/gallery-guide.md) - Photo display, sorting, favorites, trash
- [Person Search Guide](./en/person-search-guide.md) - Search photos with specific users

#### VRChat Integration & Camera Control
- [VRChat Integration](./en/vrchat-integration.md) - VRChat metadata retrieval
- [VirtualLens Controller](./en/controller-guide.md) - Real-time camera parameter control
- [Game Config](./en/game-config.md) - VRChat integration, time machine, server status

#### Photo Editing & Sharing
- [X Posting Feature Guide](./en/x-post-guide.md) - X posting, camera info frames, preset management
- [JXL Compression](./en/jxl-compression.md) - Photo compression in JPEG XL format

#### Cloud Integration
- [Account Guide](./en/account-guide.md) - User account management
- [Favorites Guide](./en/favorites-guide.md) - Google Drive auto-upload

#### Customization & Settings
- [Settings Guide](./en/settings-guide.md) - All settings panels (appearance, animation, file, system, X post, etc.)
- [Keyboard Shortcuts](./en/keyboard-shortcuts.md) - Shortcut list and customization
- [Setup Wizard](./en/setup-wizard.md) - Initial setup guide

#### Support
- [FAQ](./en/faq.md) - Frequently asked questions
- [Troubleshooting](./en/troubleshooting.md) - Problem solving guide

#### Other
- [Terms of Service](./en/terms.md)
- [Privacy Policy](./en/privacy.md)

### チュートリアル

- [はじめに](./tutorial/getting-started.md)
- [フォルダのインポート](./tutorial/import-folder.md)

### その他

- [基本的な使い方](./basic-usage.md)
- [ライセンス情報](./license.md)

## バージョン情報

このドキュメントは **VSA v0.5.1** 以降の現行実装を基準にしています。

- 最終更新日: 2026-04-24
- 対象バージョン: v0.5.1
- 主な対応機能: ローカル写真管理、VSAアカウント、クラウド保存、X投稿、JPEG XL圧縮、VirtualLens Controller、サーバーステータス、カメラ情報フレーム

## 重要なお知らせ

- VSAの正式名称は **Virtual Snap Archive** です。旧称・無効名称をアプリ名として使用しないでください。
- VSAはVRChat Inc.、VirtualLens2、Integralおよび各権利者とは提携・承認・サポート関係にない非公式ツールです。
- ローカル基本機能は無料で利用できます。クラウド保存とX APIを利用する機能は、無料枠を超えると料金が発生する場合があります。
- VSAアカウント、クラウド保存、X投稿、Turnstile、アップデート確認、サーバーステータス表示では外部通信が発生します。
- Windows版インストーラーは未署名の場合があり、SmartScreenやセキュリティソフトの警告が出ることがあります。
- アプリ内の「ドキュメント」ボタン、または「設定 > その他」からも関連ページを開けます。
