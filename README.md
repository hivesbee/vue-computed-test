# vue-computed-test

## 背景
Vue のコンポーネントで関数を返したら全評価し直しに本当になっちゃうのか気になったのでテスト

## 結果
全評価し直しでした

## 小言
リスト系のスタイルを当てたり外したりするときによく使ってたのでちょい悲しい

## 対策
`ListItem.vue` みたいにリストアイテム専用のコンポーネントを作り、props で受け取った単一のデータを computed するのが良さそうですかね…  
コンポーネントの分解をサボってはいけない（戒め）
