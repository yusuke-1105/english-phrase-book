# 会社の英語、まるごと1冊

ITサービス企業で働く人のための英語フレーズ帳です。入社初日のIDバッジ受け取りから、障害対応の深夜のブリッジコールまで。開発・設計・運用・提供の日常で実際に使う表現を **22章・271フレーズ** にまとめています。

**公開サイト:** https://yusuke-1105.github.io/english-phrase-book/

## 収録章

| # | 章 | # | 章 |
|---|---|---|---|
| 01 | 入社手続き・オンボーディング | 12 | 開発・エンジニアリング |
| 02 | オフィス・社内設備 | 13 | 設計・アーキテクチャ |
| 03 | 勤怠・休暇 | 14 | 運用・保守 |
| 04 | 給与・福利厚生 | 15 | 障害対応・インシデント管理 |
| 05 | メール・チャット | 16 | サービス提供・顧客対応 |
| 06 | 会議・スケジュール | 17 | セキュリティ・コンプライアンス |
| 07 | リモートワーク・オンライン会議 | 18 | テスト・品質保証 |
| 08 | 雑談・社内文化 | 19 | クラウド・データ基盤 |
| 09 | 評価・フィードバック | 20 | アイデア出し・チーム編成 |
| 10 | プロジェクト管理 | 21 | ハッカソン開発・進行管理 |
| 11 | 出張・経費 | 22 | 発表・審査 |

## 構成

```
english-phrasebook.html       ← 本体（これ1ファイルで完結。編集するのはここだけ）
icons/                        ← ファビコン・アプリアイコン一式
site.webmanifest              ← PWA / Android 用マニフェスト
browserconfig.xml             ← Windows タイル用設定
.github/workflows/deploy.yml  ← 公開用の GitHub Actions ワークフロー
```

外部依存は Google Fonts のみで、CSS も JavaScript もすべて HTML に内包しています。ローカルで確認したいときは `english-phrasebook.html` をそのままブラウザで開いてください（アイコンのパスは相対指定なので、ローカルでも正しく表示されます）。

### アイコン

| 用途 | ファイル |
|---|---|
| ブラウザのタブ（レガシー・IE 含む） | `icons/favicon.ico`（16/24/32/48/64 のマルチ解像度） |
| ブラウザのタブ（PNG） | `icons/favicon-16x16` 〜 `192x192.png` |
| iOS / iPadOS ホーム画面 | `icons/apple-touch-icon.png`（180）ほか 120 / 152 / 167 |
| macOS Safari ピン留めタブ | `icons/safari-pinned-tab.svg`（単色マスク） |
| Android / Chrome / PWA | `icons/web-app-manifest-192・512.png` |
| Android アダプティブアイコン | `icons/maskable-icon-192・512.png`（中央80%セーフゾーン対応） |
| Windows タイル | `icons/mstile-70・150・310x150・310x310.png` |
| SNS シェア（OGP / X） | `icons/og-image.jpg`（1200x630） |

アイコンを差し替えるときは元画像から `icons/` 以下を作り直し、push すれば自動で反映されます。

## 利用規約・免責事項

サイト下部に「利用規約・免責事項」セクション（折りたたみ）を掲載しています。掲載内容は無保証であること、参照・利用によって生じた損害について責任を負わないこと、および本サイト固有の注意事項（英語表現のニュアンス、対外コミュニケーション、労務・人事、セキュリティ・コンプライアンス、障害対応、機密情報の取り扱い）を明記しています。

なお本規約は一般的なひな形をもとに作成したもので、弁護士のレビューを受けたものではありません。業務での正式な公開等に用いる場合は、専門家の確認をおすすめします。

https://yusuke-1105.github.io/english-phrase-book/#terms

## 更新のしかた

1. `english-phrasebook.html` を編集する
2. `main` ブランチに push する

```bash
git add english-phrasebook.html
git commit -m "フレーズを追加"
git push
```

push すると GitHub Actions が自動で走り、`english-phrasebook.html` を `index.html` としてコピーして GitHub Pages にデプロイします。**index.html を手で更新する必要はありません。** 反映されるまでの目安は1〜2分です。

進行状況はリポジトリの **Actions** タブで確認できます。手動でデプロイしたいときは、同じタブから *Deploy to GitHub Pages* → *Run workflow* を実行してください。

## 初回セットアップ（済んでいる場合は不要）

GitHub リポジトリの **Settings → Pages → Build and deployment → Source** を **GitHub Actions** に設定します。この設定が「Deploy from a branch」のままだとワークフローがデプロイ時に失敗します。
