# Cording

## About

- コーディングする上で遵守してほしいルール

## Rules

- 3項演算子はnestさせない
- 引数やpropertyで関数名に `onXxx` と指定されているとき、それに代入する関数名は命名規則として `handleXxx` を使うこと
- 関数をファイル内部で定義する時、exportしているものを上部、exportしていないものを下部になるようにsortしてあること
  - exportしているものは上部/そうでないものは下部にするだけで、辞書的なsortはしなくていい
  - `React.memo()` しているものについては、先にexportしていないComponentを定義し、後に `React.memo()` したものを公開しても良いことにする
