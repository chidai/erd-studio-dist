# ERD Studio 0.1.0-alpha.12

ERD Studioの公開試用版です。

## Downloads

- `ERDStudio-0.1.0-alpha.12-shared-platform-mac-arm64.pkg`
  - macOS 12以降
  - Apple Silicon（M1/M2/M3/M4/M5）
  - PKGインストーラ
- `ERDStudio-0.1.0-alpha.12-mac-x64.pkg`
  - macOS 12以降
  - Intel Mac x64
  - PKGインストーラ
- `ERDStudio-0.1.0-alpha.12-win32-x64-portable.zip`
  - Windows x64
  - インストール不要。ZIPを展開して`ERD Studio.exe`を起動

## 主な機能・改善

- PostgreSQL/MySQL等からのリバースエンジニアリングと複数スキーマ選択
- PostgreSQL TLS、AWS Session Managerポートフォワード、RDS IAM認証の接続設定
- モデル比較、整合性検査、DDL検証、CSVデータ検証
- SQLワークスペース、履歴・お気に入り、疎通確認SQL
- a5erインポートと論理設計中の特殊な物理名の安全な保存
- 大規模モデルで用語辞書パネルが停止する問題を改善
- 関連管理パネルのテーブル参照を高速化

## 検証

- TypeScript型検査: 成功
- 自動テスト: 846/846成功
- macOS共有ランタイム試験: 4/4成功
- macOSパッケージルート隔離起動: 成功
- Intel Mac版: Electron、DuckDB、Oracleのx64ロード試験成功（Rosetta上）
- Windows ZIP: 実行ファイル、内包version、DuckDB win32-x64バイナリを確認済み

## 重要な注意

このalpha版は未署名です。OSのセキュリティ警告が表示される場合があります。

重要なモデルは必ずバックアップしてください。実際の利用環境に接続する前に、権限を限定した検証用DBで接続設定を確認してください。モデル、DB認証情報、AWS認証情報をIssue等へ添付しないでください。

## SHA-256

```text
f6f1a00ec5ffed143a1863438ca39374e1694ac06da094cc3e4b37e193972d2d  ERDStudio-0.1.0-alpha.12-shared-platform-mac-arm64.pkg
039ed78073b7b8da062ca34dbfe56773f46ecf41d02493e033bc7d7256f6c9c5  ERDStudio-0.1.0-alpha.12-mac-x64.pkg
4c91d04a49b2488c4e5cc71270c4f8863fd8d86c8b8fa28e2b3d2c8df1835d1f  ERDStudio-0.1.0-alpha.12-win32-x64-portable.zip
```
