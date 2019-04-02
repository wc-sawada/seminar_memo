2019.03.06
# Meguro.css #5 @ oRo
https://megurocss.connpass.com/event/120644/

# Meguro.css #5 @ oRo
https://megurocss.connpass.com/event/120644/

# CSSだけでウェブサイトをドット化する方法
ダーシノ @bc_rikko  
https://speakerdeck.com/bcrikko/how-to-pixelize-a-website-using-only-css

https://kuroeveryday.blogspot.com/2018/10/draw-and-animate-pixel-art-using-only-css.html

# リニューアルを行う際にやったcssのルール作り
yakiniku @yakiniku040220  

Webリニューアルする理由
* SEOにかなり弱い
* 使っているPythonのサポートが今年終わる
* コードの改修が辛い

どれくらいやばかったか
* HTMLとCSSのコードが乱雑になっていること
* reset.cssが存在しない

ルール作り
* CSSののコーディングガイド作成
* 週一のレビュー会

CSSとSassのコーディングスタイルガイドを作ってみた　Qiita
https://qiita.com/manabuyasuda/items/5d83a5516051cc58a274

# styled-componentsで脱CSSModules
camcam_lemon @camcam_lemo
https://speakerdeck.com/lemon/styled-componentsdetuo-cssmodules

# CSS で MS を作る（モビルスーツ）
rry @ryamakuchi  
https://slides.com/ryamakuchi/tips-for-painting-with-css#/

パーツとして分割しやすいもの
左右対称
直線が多い

最初の目標物　ガンダムが良い！！ｗ

コーディングのポイント  
末端のdivには名前をつけない  
　nth-childで  
親要素のdivはrotate()しないこと  
borderは基本top leftしか使わない  

transform: skewY(10deg)  
transform-origin  

# create-nuxt-app で選べる現代の UI フレームワーク
いのうえたくや @inouetakuya  
https://speakerdeck.com/inouetakuya/modern-ui-frameworks
UIフレームワークのつらさ  
ちょこっとだけ変更（カスタマイズ）がしにくい  
アプリ固有のスタイルと衝突  
バージョンアップがしずらい  

Bootstrap  
　v5　脱jQuery  
Bulma  
Tachons  
Element UI  
　VueのUIコンポーネントでは最もメジャー  
iView  
Vuetify  
Tailwind CSS  

現代は問題が解決しやすくなってる

# オブジェクト指向プログラミングをSCSSで雑に(小声)紹介してみる
omiend @omiend
https://slides.com/omiend/scss/#/  

飛び込みLT
# Dark Mode
prefers-color-scheme  
https://blog.jxck.io/entries/2018-11-10/dark-mode-via-prefers-color-scheme.html

# ワークショップ
https://slides.com/yusukenakaya/try-css-3d#/try_css3d  
サイコロの法則　オモテとウラ　足すと７になる
Z軸は手前になるほどプラス、奥に行くほどマイナス

第三引数まで0か1しか入らない
transform: rotate3d(0, 0, 0, 0deg);

３Dに大切なプロパティ
transform  
perspactive  
transform-style  

transform-originは軸（中心）  

transform: 
translate  
rotate  
scale  
skew  

perspactive 遠近法
数値が大きくなるほど平面
小さいほど湾曲する
300〜500pxほどがちょうどよい

親要素にしているすもの  
transform-style:  
flat  
preserve-3d  IEではNG

transform 1234  

transeform 1+2+3+4  

rottateZ(-90deg) 反時計回り

translateZ(100px)すべてに書いてある
回転してから前進しなさい
1辺は200pxだからその半分全身

oder listをよく理解すること
