# 次世代ランタイム x フロントエンドの将来性
## Deno Update: 最近のフロントエンド向け機能の紹介
https://x.com/kt3k/status/1891435044947837246?s=46
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
kazushikonosuさん@kazushikonosu
### なぜDenoを採用したか
LINEスキマニでは技術選定ミニマムなソリューションが多い。(依存しない)
ロックインされる。技術トレンドに乗れない。
最近のトレンドhono、ミニマムなライブラリが好まれることが多い
Nextjs→Vite
サーバーっでNodejs以外を検討するのが楽になった

Nodejs環境構築、だるくね？
tsconfig.jsonやts-node
Linter

Denoは
Web標準に準拠する
future-proof
「できないこと」が多いのはいいこと

### 活用法
Nodejsの互換として使ってない
package.jsonなしでdeno.json使ってる  
フロントエンドはDeno上で実行してる  

Deno(バック)とPackage(フロント)でフロントとバックの依存関係をわけられて、認知
expressとReactが同列にある意味とは…？←意味ない
### 振り返り
フロント開発環境のセットアップがシンプルになった  
tsの設定をDenoに任せられた  
コードのランタイムとして魅力的な
## Honoをフロントエンドで使う3つのやり方
yusuke wadaさん

フロント「ユーザーが触れる領域」  
Honoは元々バック用に作られた  

### Hono自体がフロントを提供
SSR  
c.setRenderer c.renderでrenderの形を指定できる(テンプレ化)

1つのHonoプロジェクトでSPAとAPIが作れる

### Honoの上にフロントを載せる
フロントをmiddlewareにすると簡単に載せられる。
### フロントの中でHonoを使う
## 次世代ランタイム×フロントエンドの将来性（パネルディスカッション ）
