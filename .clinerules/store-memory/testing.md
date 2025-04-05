# Testing

## About

- テストコードについての計画/実装についてのRule

## テスト計画について

以下の手順で、実行するテストについてパターン列挙する

- テスト対象の入出力関係を調べる
- 同値分割をする
- 境界値分析をする
- Pairwise Testingする

## テスト実装方法について

## hooksとcomponentについて

- `@testing-library/react-native` を使ってcomponentやhooksのrenderingをする
- componentのassertionは、`@testing-library/react-native` で実装されているmatcherを使う ([docs](https://callstack.github.io/react-native-testing-library/docs/api/jest-matchers))

| 関数名                               | 利用用途                                                                                                                                     |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `toBeOnTheScreen()`                  | 要素が画面上に存在するかを検証します。                                                                                                        |
| `toHaveTextContent(text, options?)`  | 要素が指定したテキストコンテンツを持つかを検証します。`text`には文字列または正規表現を指定できます。                                          |
| `toContainElement(element)`          | 親要素が指定した子要素を含んでいるかを検証します。                                                                                            |
| `toBeEmptyElement()`                 | 要素が子要素やテキストコンテンツを持たないことを検証します。                                                                                  |
| `toHaveDisplayValue(value, options?)`| `TextInput`要素が指定した表示値を持つかを検証します。`value`には文字列または正規表現を指定できます。                                           |
| `toHaveAccessibilityValue(value)`    | 要素のアクセシビリティ値が指定した値であるかを検証します。`value`は`min`、`max`、`now`、`text`のプロパティを持つオブジェクトで指定します。     |
| `toBeEnabled()` / `toBeDisabled()`   | 要素が有効または無効であるかを検証します。                                                                                                   |
| `toBeSelected()`                     | 要素が選択されているかを検証します。                                                                                                         |
| `toBeChecked()` / `toBePartiallyChecked()` | 要素がチェックされているか、または部分的にチェックされているかを検証します。                                                                |
| `toHaveProp(propName, propValue?)`   | 要素が指定したプロパティを持ち、オプションでその値も検証します。                                                                              |
| `toHaveStyle(style)`                 | 要素が指定したスタイルを適用しているかを検証します。                                                                                         |
| `toHaveAccessibilityState(state)`    | 要素のアクセシビリティステートが指定した状態であるかを検証します。`state`は`disabled`、`selected`、`checked`、`busy`、`expanded`のプロパティを持つオブジェクトで指定します。 |
| `toHaveAccessibleName(name, options?)` | 要素が指定したアクセシブルな名前を持つかを検証します。`name`には文字列または正規表現を指定できます。                                           |