# 次世代ランタイム x フロントエンドの将来性
## Deno Update: 最近のフロントエンド向け機能の紹介
hinosawaさん @kt3k
「Denoってサーバーは良いが、フロントは厳しいよね」
最近は改善されてるよ

フロントで使える型、リント、フォーマッタ

Reactで使うと型エラーが起こるが、色々設定したらＯＫ
jsx import source types and npm packages
ts-types
deno.json
import map
で綺麗に書ける

Deno内で自動化しようという流れがある。

### Denoの型と環境
DenoはデフォルトでDeno環境でinfer
だが、deno.jsonを変えるとプロジェクト全体に影響しちゃう
If front and back are on the same repo, it wasnt easy to make it work correctly

deno2.4 made it possible to make different deno.json files
use
deno upgrade --canary
to get the latest version

### Deno lint
An extremely fast linter made with Rust

rules of hooks

lint for react
use recommended react

Deno 2.2 Custome Lint Rules

### Formatters
Deno 1.46 CSS HTML formatters
deno fmt
command to format css html files


## LINEスキマニのフロントエンド開発にDenoを採用した理由
## Honoをフロントエンドで使う3つのやり方
## 次世代ランタイム×フロントエンドの将来性（パネルディスカッション ）
