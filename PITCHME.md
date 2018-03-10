# いまからはじめるAnsible 第2回
## @hiyoko_taisa
---
# 前回のおさらい
---
## Infrastructure as Code とは
- ダイナミックなインフラに対応するための考え方
- 自動構成ツールを使ってコードでインフラを管理
---
## Ansible とは
- Red Hatとコミュニティで開発している自動構成ツール
- YAML形式のPlaybookでインフラを定義する
- Module
  -> Ansibleが使用するコマンド群
- Inventory
  -> Ansibleが管理するノード一覧
- Role
  -> Playbookを細分化したもの
---
# 本日の内容
---
## おしながき
- より発展的なPlaybookの書き方
- デモ(Wordpressのインストール)
- Dynamic Inventory
- デモ(AWS EC2のインベントリ取得)
---
## Playbookをそれっぽく書くコツ
- 変数を外部で定義する
- with_itemsをうまく使う
- べき等性を意識する
- Simple is best
---
## Wordpressのセットアップを考える
### 必要と思われる作業
- 本体と関連パッケージのインストール
- 自動起動設定
- tcp:80のinbound/outbound許可
- 設定ファイルの編集
- コンテンツの配置
---
## インストール作業
- packageモジュールを使う(yumモジュールでもいい)

## Role化する
---
## 設定ファイルはJinja2テンプレートを活用
