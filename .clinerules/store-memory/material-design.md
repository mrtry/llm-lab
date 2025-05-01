# Material Design

このプロジェクトでは、デザインガイドラインとしてMaterial Design Guidelineをベースにしています。
そのため、SpacingやUXについての考え方は、Material Design Guidelineに記載があることに則ることを開発者に求めています。
ここに記載されている値と一致しない値を利用しているときは、修正することを検討してください。

- https://m2.material.io/design/introduction
- https://m3.material.io/

## Spacing

- margin/padding、Textなどについてのsize/spacing managementに関するrule
- `StyleSheet.create()` `StyleType<T>` `ViewProps` `TextProps` `ImageProps` などがルールの対象になります

https://m2.material.io/design/layout/spacing-methods.html#baseline-grid:~:text=Responsive%20layout%20grid-,Spacing%20methods,-Component%20behavior

| 項目                  | 内容                                                                 |
|-----------------------|----------------------------------------------------------------------|
| **グリッド単位**       | **4dp を最小単位**とするベースライングリッド                         |
| **テキストの行間**     | `line-height` は必ず **4dp の倍数**に設定                             |
| **テキストの配置**     | **テキストのベースライン**を 4dp グリッドに揃える                     |
| **UI要素の高さ**       | コンポーネントの高さも **4dp の倍数**になるように設計                 |
| **上下スペーシング**   | 要素間の余白（マージン・パディング）も **4dp の倍数**に揃える          |
| **多行テキスト**       | 各行のベースラインがグリッドに合うように `line-height` を調整する      |

## Icon

ComponentにIconと含まれるもの、Image Componentでwidth/heightが同値(つまり正方形のUI)などがこのルールの対象になります

https://m2.material.io/design/iconography/system-icons.html#grid-and-keyline-shape

- 基本的にサイズは `20dp x 20dp` である
- PropsにonXxxPressのようなnaming ruleが含まれている場合、Touchable Componentに記載されているruleが適用されている必要がある
- 隣接するcomponentから、最低2dp離れるように `padding: 2` などが設定されている必要がある


## Touchable Component

ユーザーがタッチ可能なComponentについてのルールです
対象となるComponentは、PropsにonXxxPressのようなnaming ruleで実装されています
該当するComponentでは、以下の要件を満たしていることが重要です

### Touch target size  

ユーザーが指で操作するモバイルアプリにおいて、誤操作を防ぎ操作性を確保するために、十分なタッチ領域が必要です。  
Material Design では、視覚的なサイズに関わらず、タッチ可能な領域を **最低 48dp × 48dp** に保つことが推奨されています。  
視覚的に小さな要素（アイコンボタンなど）でも、透明なパディングでタッチ領域を補うことが推奨されます。

https://m3.material.io/foundations/designing/structure#b421e522-35a6-47cd-bfc6-bf94cbacf7bb

### Target spacing  

隣接する操作可能な要素の間隔は、ユーザーの誤操作を防ぐために重要です。  
ターゲット間の **最小スペースは 8dp** 以上が推奨されており、より快適な操作性を確保するには **16dp** 以上のスペースが理想的です。

https://m3.material.io/foundations/designing/structure#1057f862-b8f1-42a1-9239-7077b8763a48