# 📋 LINEトーク → CSV変換

LINEのトーク履歴（`.txt`）をワンクリックでCSVに変換するWebツール。

## 使い方

1. LINEアプリからトーク履歴を `.txt` 形式でエクスポート
2. このページにドロップ or テキストエリアに貼り付け
3. 自動解析 & CSVダウンロード

## 出力カラム

| 列 | 説明 | 例 |
|---|---|---|
| `date` | 日付（和暦→西暦） | `2024-04-02` |
| `weekday` | 曜日 | `火` |
| `time` | 時刻 | `07:31` |
| `sender` | 送信者名 | `太郎` |
| `message_type` | メッセージ種別 | `text` / `photo` / `stamp` / `album` / `call` / `system` / `url` / `paypay` |
| `message` | メッセージ本文 | `こんにちは` |

## GitHub Pages でホスト

1. リポジトリの **Settings → Pages** に移動
2. **Branch** を `main`、**folder** を `/ (root)` に設定して Save
3. しばらくしたら `https://toyfer.github.io/line-to-csv/` でアクセス可能

## 技術

- 外部依存ゼロの単一HTMLファイル
- ブラウザ上で完結（サーバー不要）
- RFC 4180 準拠 CSV（BOM付きUTF-8）
- LINEエクスポート形式対応：和暦日付、複数行引用メッセージ、システムメッセージ、写真/スタンプ/アルバム/通話/PayPay/URL 種別分類
