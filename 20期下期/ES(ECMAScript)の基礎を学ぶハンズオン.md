2018.11.26
# 【初心者向け】JavaScriptの次のステップ、ES(ECMAScript)の基礎を学ぶハンズオン

https://js-builders.connpass.com/event/105770/

# 【初心者向け】JavaScriptの次のステップ、ES(ECMAScript)の基礎を学ぶハンズオン

## ECMAScriptについて
JSを標準化させた仕様の言語

ES2018(9)が最新  
ES4はトラブルによってリリースはしていない  
ES6がメジャー  

毎年6月ごろリリース  

ES2017  
Async functions  

2018は最近なのもあり、あまり使われてない

***

変数  
配列  
データ型  
関数とスコープ  

## var 変数
var　で定義しても  
null 定義はされているけどからのデータ  
undefined 定義されていない  

## データ型
★プリミティブ型  
数  
文字列  
ブール  
null  
undefined  

★オブジェクト型  
オブジェクト  
関数  


## 配列
Array  
new式はあまり使われてない  
多次元配列、連想配列  
連想配列はDicと呼ばれがち

## 関数とスコープについて
関数内でvarをつけるとローカル変数になるため、関数外で呼ぶとエラーになる。


# ECMAScript
let も再宣言できない

forEach  
ES5で追加された、配列の中で存在する要素だけ。オブジェクトだと使えない  

map  
ループ処理というより新しい配列を作成すると認識したほうがよい  
戻り値がある  

filter  
必要な条件のものだけ抽出するループ処理

forEachとmapのちがい  
mapは新しい配列を作っているため、戻り値がある  
forEachは指定した配列をただ回すだけ  


# 関数にデフォルト値について
Rest　paramerters  
スプレッド演算子  

# テンプレート文字列
インジェクション攻撃を避けることができる  
${} エクスプレッション  

# モジュール構文
１つのモジュールは１つのファイルに対応  
非同期なので必要とされるまでは実行されない  

頭に　export つけるだけで関数モジュール化  
外部読み込みは import 
エイリアスもつけられる
```
inport { add2 as my Func } from "./script"
```

export default

# Class構文
従来のクラス宣言に比べてシンプルになった
extends
super(親クラス呼び出し)

# 非同期関数
Promise
ES2015(ES6)で追加
非同期処理の成功時、失敗時の処理を明示的にかける
async await
ES2017で追加された
Orimiseno処理完了まで待つ

