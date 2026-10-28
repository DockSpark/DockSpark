# DockSpark

[English](README.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Español](README.es.md)

DockSpark は、macOS の Dock から直接ブラウザのプロファイルを切り替えられるアプリです。対応ブラウザのアイコンにポインタを合わせ、使いたいプロファイルを選択するだけで切り替えられます。ブラウザのプロファイルメニューを開く必要はありません。

[最新バージョンをダウンロード](https://github.com/DockSpark/DockSpark/releases/latest)
· [公式サイト](https://dockspark.app)
· [変更履歴（英語）](CHANGELOG.md)
· [問題を報告](https://github.com/DockSpark/DockSpark/issues)

## 機能

- ブラウザの Dock アイコンに表示されるポップオーバーからプロファイルを切り替え
- macOS ネイティブアプリでブラウザのプロファイルを管理
- 名前や色をカスタマイズして、プロファイルを簡単に識別
- Dock のホバーメニューに表示する名前付きプロファイルを選択
- DockSpark Free を利用、または Pro でブラウザ数とプロファイル数の制限を解除
- メニューバーと Dock のアイコンを表示・非表示に設定
- アプリ内でアップデートを確認
- 「ヘルプ」メニューからドキュメントを開いたり、所定の形式でフィードバックを送信
- 英語、簡体字中国語、繁体字中国語、日本語、韓国語、ドイツ語、フランス語、スペイン語に対応
- Dock アイコンのサイズに合わせてポップオーバーを拡大・縮小（Dock の拡大表示にも対応）
- 「一般」設定で匿名の利用状況分析を無効化可能

## 動作環境

- macOS 14.0 以降
- Apple シリコンまたは Intel 搭載 Mac
- 対応ブラウザを Dock に追加しておくこと

### 対応ブラウザ

| ブラウザ | Dock からのプロファイル切り替え |
| --- | --- |
| Safari | 対応 |
| Firefox | 対応 |
| Google Chrome | 対応 |
| Chromium | 対応 |
| Microsoft Edge | 対応 |
| Brave Browser | 対応 |
| Vivaldi | 対応 |
| Opera | 対応 |
| Opera GX | 対応 |
| Arc | 対応 |

Safari、Google Chrome、Firefox は、インストールされている場合、デフォルトで有効になります。Free プランでは、有効にできるブラウザは 1 つ、名前付きプロファイルはブラウザごとに 3 つまでです。プライベートブラウズやシークレットモードの項目は、このプロファイル数に含まれません。Pro ではこれらの制限が解除されます。ほかのインストール済みブラウザは、アプリ一覧から追加できます。

## インストール

### Homebrew

```sh
brew trust --cask dockspark/tap/dockspark && \
  brew install --cask dockspark/tap/dockspark
```

### 手動ダウンロード

1. [最新リリース](https://github.com/DockSpark/DockSpark/releases/latest)を開きます。
2. `DockSpark-0.5.0.dmg` をダウンロードします。GitHub が自動生成したソースコードのアーカイブはダウンロードしないでください。
3. ディスクイメージを開き、`DockSpark.app` を「アプリケーション」フォルダにドラッグします。
4. DockSpark を起動し、要求された macOS の権限を許可します。

手動インストール用に `DockSpark-0.5.0.zip` も用意されています。

DockSpark は Developer ID 証明書で署名されており、Apple の公証を受けています。

## 権限

DockSpark は、プロファイルの切り替えに必要なシステム権限のみを要求します。

- **アクセシビリティ**：Dock 内の対応ブラウザアイコンに対するポインタ操作を検出します。
- **オートメーション**：選択したブラウザにプロファイルの切り替えを要求します。
- **フルディスクアクセス**：任意です。Chromium と Firefox のプロファイルメタデータの検出にのみ使用します。

これらの権限は、**システム設定 > プライバシーとセキュリティ**でいつでも確認・取り消しできます。

## 使い方

1. 対応ブラウザを Dock に追加します。
2. DockSpark でブラウザとプロファイルを設定します。
3. ブラウザの Dock アイコンにポインタを合わせます。
4. ポップオーバーからプロファイルを選択します。

## AI アシスタント用スキル

[DockSpark スキル](skills/dockspark/SKILL.md)は、AI アシスタントが DockSpark の用途や活用場面を説明し、インストールや日常的な使い方を案内し、公式ドキュメントを探し、よくある問題を解決するのに役立ちます。スキルのバージョン **0.5.0** はアプリのバージョンに対応しており、同梱のガイドは DockSpark 0.5.0 に基づいて確認済みです。アシスタントはあなたの言語で回答します。

[Skills CLI](https://github.com/vercel-labs/skills) でインストールします（Node.js が必要です。現在の動作要件は CLI のドキュメントをご覧ください）。

```sh
npx skills add DockSpark/DockSpark --skill dockspark
```

指示に従って AI アシスタントを選択してください。デフォルトでは現在のプロジェクトにインストールされます。グローバルにインストールする場合は `-g` を追加します。上記の GitHub コマンドを使うには、スキルがこのリポジトリで公開されている必要があります。ローカルのチェックアウトからは、次のコマンドを使います。

```sh
npx skills add . --skill dockspark
```

[Codex に手動でインストール](https://developers.openai.com/codex/skills/)する場合は、`references/` と `agents/` を含む `skills/dockspark` ディレクトリ全体を、`~/.agents/skills/dockspark` またはプロジェクト内の `.agents/skills/dockspark` にコピーしてください。ほかのアシスタントでは、スキルの保存先が異なる場合があります。スキルが表示されない場合は、アシスタントのスキルを再読み込みするか、新しいセッションを開始してください。

プロンプトの例：

- `$dockspark を使って、DockSpark でできることを説明してください。`
- `$dockspark を使って、Chrome のプロファイル設定を手伝ってください。`
- `$dockspark を使って、Dock アイコンにポインタを合わせても何も起こらない原因を調べてください。`

英語やほかの言語でも質問できます。スキルは使い方を案内するものです。アプリを使用するには、DockSpark を別途インストールしてください。アプリの新バージョンをリリースする際は、スキルのガイドと公式リンクを確認し、スキルのバージョンと確認対象のアプリバージョンを併せて更新してください。

## スクリーンショット

![DockSpark のプロファイル管理ウインドウ](Assets/img_dockspark.jpg)

> DockSpark のインターフェースを示すスクリーンショットです。バージョン 0.5.0 は、Safari、Firefox、Chrome、および上表に記載されたその他の Chromium ベースのブラウザで、Dock からのプロファイル切り替えに対応しています。

## アップデート

DockSpark は Sparkle を使ってアプリ内アップデートを提供します。[リリースページ](https://github.com/DockSpark/DockSpark/releases)から手動でダウンロードすることもできます。

## リリースファイルの整合性

SHA-256 チェックサムは次のとおりです。

```text
DockSpark-0.5.0.dmg  90c0f9369d67eb33e6939b1cac008ec70277f7c176c0f2a1aa0e50fb08e85eff
DockSpark-0.5.0.zip  1d7eb10b9ce7736f2a1e5f1fd790eebb399675fadb95702a6032f329f65db129
```

ダウンロード後、次のコマンドで確認できます。

```sh
shasum -a 256 DockSpark-0.5.0.dmg DockSpark-0.5.0.zip
```

## フィードバック

不具合の報告や改善の提案には [GitHub Issues](https://github.com/DockSpark/DockSpark/issues) をご利用ください。不具合を報告する際は、macOS のバージョン、ブラウザのバージョン、再現手順を記載してください。

このリポジトリには DockSpark の公開リリース資料が含まれています。アプリのソースコードは含まれていません。
