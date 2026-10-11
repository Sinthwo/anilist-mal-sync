# Obsidian Anime Sync

**言語：** [English](README.md) | [Français](README.fr.md) | [Deutsch](README.de.md) | 日本語

> **個人的なメモ：** 現在、フランス語と日本語を勉強しています。

**Obsidian、AniList、MyAnimeList を連携させる、Python ベースの同期プロジェクトです。**

> **開発状況：** 現在はプロジェクトのひな形のみです。アプリケーションの処理はまだ実装されていません。

## 目標

Obsidian 内の Markdown でアニメのライブラリを管理し、将来的には各サービスの API を使って、視聴状況、視聴済み話数、評価、その他の対応する項目を AniList と MyAnimeList の間で同期できるようにします。

## 実装予定の機能

- AniList と MyAnimeList から Obsidian ノートへの初回インポート
- 競合検出とプレビューモードを備えた、3 つのツール間の同期
- アニメのメタデータ、カバー画像、Markdown テンプレート
- ローカルの SQLite に保存する同期状態のスナップショットとバックアップ
- ターミナルコマンド、統計、Obsidian ダッシュボード
- ユニットテスト、統合テスト、エンドツーエンドテスト

## リポジトリの構成

| パス | 予定している役割 |
| --- | --- |
| `src/anime_sync/providers/` | AniList と MyAnimeList の API クライアント |
| `src/anime_sync/obsidian/` | Obsidian 保管庫の読み書きとノートの生成 |
| `src/anime_sync/sync/` | データの照合と競合の処理 |
| `src/anime_sync/storage/` | ローカルの同期状態とキャッシュ |
| `src/anime_sync/metadata/` | アニメのメタデータの補完 |
| `src/anime_sync/statistics/` | 集計処理 |
| `src/anime_sync/automation/` | 定期的な同期とファイルの監視 |
| `templates/obsidian/` | 今後作成する Markdown テンプレート |
| `tests/` | 自動テスト |
| `docs/` | プロジェクトのドキュメント |

## はじめに

現在のリポジトリには、**空の実装用ファイル**が置かれています。アプリケーションはまだ実行できません。まず設定と API 認証を実装し、次に読み取り専用のインポートを実装したうえで、安全な双方向同期を追加する予定です。

## セキュリティ

API トークン、OAuth のシークレット、ローカルのデータベース、個人の Obsidian 保管庫をコミットしないでください。`.env` はローカルで使用し、外部サービスへの書き込みを有効にする前に、ドライランで変更内容を確認してください。

## 使用予定の技術

Python · GraphQL · REST · SQLite · Obsidian Markdown · OAuth2

## ロードマップ

1. 基盤と設定
2. AniList と MyAnimeList の認証、および API への読み取り専用アクセス
3. Obsidian 用 Markdown のインポートとエクスポート
4. 識別情報に基づく項目の対応付けと移行
5. 競合を考慮した同期
6. ダッシュボードと自動化

## ドキュメント

以下のページは仮のページで、本文はまだ作成されていません。各ページには翻訳へのリンクがあります。

- [アーキテクチャ](docs/ja/architecture.ja.md)
- [認証](docs/ja/authentication.ja.md)
- [CLI リファレンス](docs/ja/cli-reference.ja.md)
- [設定](docs/ja/configuration.ja.md)
- [競合の解決](docs/ja/conflict-resolution.ja.md)
- [データベーススキーマ](docs/ja/database-schema.ja.md)
- [インストール](docs/ja/installation.ja.md)
- [Obsidian との連携](docs/ja/obsidian-integration.ja.md)
- [同期アルゴリズム](docs/ja/sync-algorithm.ja.md)
- [トラブルシューティング](docs/ja/troubleshooting.ja.md)

## ライセンス
