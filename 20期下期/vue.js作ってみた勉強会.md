2019.1.23
# vue.js 作ってみた勉強会
https://igs.connpass.com/event/106398/

夏  
「jquery をやめた理由について」  
「vue に関して構文、ドキュメント、学習コスト、フレームワークの豊富さ」  
「パフォーマンスについて react と angularと比較して」  
「最近 typescript 対応した vuex を使った vue 開発」

# jQuery  
1.常にDOMを意識しなくてはならない  
2.重い  
3.構造化でない  
4.いつもjQueryに頼るとNativeのjavascript書けなくなる  

jQueryは常にDOMを意識しないといけない  
→空のtableタグを用意してDOMぶっ刺して表を動的に作成する場合とか  
→DOM大量だと死ぬ  

Vueだと  
→HTML内に書き込める＝DOM意識しなくて良い  
　データ構造になっている、いじっているのはデータのみ  

ポリマーというフレームワークがある  

# 三巨頭  
React  
Vue  
Anguler  

# vueを選んだ理由
* ドキュメントが整備
* 学習コストが低い
* 性能がいい
* Typescriptも対応
* UI　Templateが豊富

★学習コストが低い  
デフォルトのプロジェクトファイル数が他フレームワークと違い、Vueは少ない  
ReactはHTMLと混在してわかりにくい  
Angularは割とVueに似てる  

★性能  
VueとReactはバーチャルDOMだからファイルの内容変えるだけで変更される  
Angularは保存毎にリロードが走る
→実行時、開発時の性能性  

★Typescript  
* 静的型付き
* 強力な自動補完
* オブジェクト指向

# UI Framework
Quaser  
https://quasar-framework.org/  

Ant Design of Vue  
https://vuecomponent.github.io/ant-design-vue/docs/vue/introduce/  

# Vue 3.0　について
6月に発表される  
* 完全なるTypescript対応
* もっと小さいバンドルサイズ
* もっと保守しやすくなる
* 更に速くなる


***
***

帯川 「Vue開発のベストプラクティスとAtomicなコンポーネントデザインの極意 〜6ヶ月分の学びを5分で〜」  

# ベストプラクティス  
→ないｗ  Vue.js入門書を読むと良い

# Atomicなコンポーネントデザインの極意
そもそもAtomicデザインとは？  
UI設計のための方法論  

なぜ使ったのか  
→プロダクト「語学学習向けのSNS」アプリ  
　社内デザインリソースの少なさのため。  
　できればエンジニアだけで運用フェーズも完結したい。  

＜基本＞  
Atomic Designの5階層構造で設計する  

ATOMS
UIとしてそれ以上分割できない要素
ボタンとかテキストとか

Molecules
Atomsを組み合わせてできた部品
バッチ付きのものとか

Organisms  
Moleculesの組み合わせ  
画面上でそれ自体を独立して配置できる  
Sectionタグでマークアップされるもの  

Templates  
Organismsを組み合わせて作ったページ全体
コンテンツは含めない。テキストや画像はプレイスホルダ

Pages  
Templatesで作成したページにコンテンツを流し込んだもの
実際にユーザーに表示するもの

つまりレイヤー設計

1.画面のOrganismsへの分割  
大きめな粒度の画面要素をコンポーネントとして分割  
設計するときは大きい方から！  

2.Moleculesへの分割  
部品を「再利用しそうなもの」「複数回使ってるもの」のみで良い  

3.MoleculesからさらにMolecules

4.MoleculesのAtomsへの分割

# 上記をVueで実装するには？
StoryBook コンポーネントカタログツール

ディレクトリ構造  

components/  
　atoms  
　molecules  
　organisms  
　pages  

コンポーネントは自身の位置、サイズに付いて関知しない  
width float  
親のコンポーネントでサイズ、表示位置を指定する  

marginは親コンポーネントで定義する  

Vuexnogetters, actionsをpages以外で呼ばない

SlotをOrganismsのレイヤーでは使わない  

＜メリット＞
- そこそこまともな設計を機能的に導入できる
- コンポーネント設計力が上がる、洞察力がます

＜デメリット＞
- 三層のレイヤーを作る必要があるため、親から孫の値の受け渡しが面倒
- DDDと同じく小規模なAppでは必要ないかも

