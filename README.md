# todo_app
## todo管理 by rails &amp; vue.js
- railsとvueの連携の動きの勉強のために作成
- https://github.com/mkhairi/materialize-sass を参考につくりました。個人的勉強

### どうやって連携しているか
- webpackでrailsと連携をとっている
→どうやって? yarnで依存関係をつくっている？

### vueのコンパイル
- vueはコンパイルが必要
```
bin/webpack
```
- 都度、上記コードを実行するのは面倒→変更を検知して自動コンパイルしてくれるgemを活用

```
gem 'foreman'
```
- bin/server, Procfile.devを作成し、自動コンパイルの設定

## APIによる、Vueとの通信
- controller内にapiフォルダを切ってapiを作成,伴ってrouteも作る

- viewのjsonファイル作成。views直下にapiフォルダ,controller同名のフォルダ作成する

- seedで初期データをつくった後、curlでAPI確認

## railsとvueの連携
- viewsにvueを置く →componentで置くtagをつくっておく(置き場所の管理)
- packs/componentsにvueファイルを作成　→　ここでcomponentされるファイルを生成

- routingはvue-router

## API通信　←ここメイン
- v:onclick ：イメージを作る　ボタンがおされたときにこのメソッドを呼ぶなど
- v-model :双方向バインディング

