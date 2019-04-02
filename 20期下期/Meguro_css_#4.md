2018.11.09
# Meguro.css
https://megurocss.connpass.com/event/103713/

# 雑誌風レイアウトをCSSnGridLayoutでリファクタリング
フレックスをGridに  
HTML構成は適したマークアップ変更  
霊圧とと無関係な部分は変更しない  
RWD  

IE11でのバグ  
・grid itemに直接したpadding/marginがおかしくなる  
・grid containerに対するalign-item、 grid itemに対するalign-selfが適用されない  
・@mediaのなかでgrid-areaを@forで書き出すとIEのprefixが付与されない  

感想
コードは読みやすくなる
アスキーアート組はIE11でも対応できる
RWDならモバイルファーストで組むほうが楽

# CSSフレームワークを自作してみた話
UNITS  
→カードとかメイン、テーマに合わせてテンプレートがある  
　コンポーネントベースのCSSフレームワーク  
　日本語の表示に最適化 etc  
属性セレクタの便利さに気づいた！

UNY  
→SCSS採用  
　remを採用

UNIM  
レイアウト用、テーマ用、カラー用  
日本語での表示に特化

mono.css  
jpn.css

# CSSとShadowDOM
ShadowDOM  
記述を内包的にできる！  

reset.cssどうなるの？  
→ShadowDOMごとに読み込む必要ある

all: initial;  
all: unset;

CSSCustomPropaty  
::part,::them提案中

# outline: none;
思考停止してoutline: none;にするのはやめよう！  
キーボード操作ができなくなる  
アクセシビリティ的に良くない  
:forcus-visible  
what-input polifilみないな

buttonタグまたはrolで対応して！

# 平成最後に作る本気のMarqueeタグ
Marqueeタグでゲームを作りたい

CSS JS

remarquee

animationend
animation iterate

# word-wrap周りのベスト・プラクティスを考えた
