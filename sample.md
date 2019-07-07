name: inverse
layout: true
class: center, middle, inverse
---
# ゴリゴリッと簡単なホームページを作成しよう
Yuki Morimatsu

---
layout:false
## profile

* Yuki Morimatsu (森松 祐樹) (41歳)

* ３年前に中途入社。だから上田君より後輩。

* だけどフリーのエンジニア(協力会社社員)としても勤務していたので、NESでは10年以上働いています

* 普段の仕事
    * サービスの開発・運用・保守
    * 黒瀬G案件のSI(プログラム中心)
    * 別PJの製造支援や技術課題解決支援

* 趣味
    * 食べること
    * プログラム

* 将来の夢
    * キャンプしながらプログラムをするユーチューバーになること

---
layout:false
## agenda

1. Visual Studio Code とは
1. Visual Studio Code インストール
1. Visual Studio Code プラグインとは
1. Visual Studio Code プラグイン Live Server インストール
1. HTMLとは
1. HTMLの簡単な構文
1. HTMLの確認方法
1. CSSとは
1. CSSの簡単な構文
1. Java Scriptとは
1. Java Scriptの簡単な構文

---
layout:false
## Visual Studio Code とは
* 軽量のテキストエディタ
  
だけど、
  
* HTMLを書いて表示したり
* プログラムを書いて実行したり
  
すことがができる
  
* スタートアップ系企業やWEB系企業のエンジニアは絶対に使っている、今一番~~ナウい(死語)~~イケてる開発環境

---
layout:false
## Visual Studio Code インストール

1. 以下のURLにアクセスします
    * [https://code.visualstudio.com/](https://code.visualstudio.com/)

1. あとはその場で説明します。

---
layout:false
## Visual Studio Code プラグインとは
####Visual Studio Codeは素のままだと普通のテキストエディタでしかありません。
そんなエディタに、特別な機能を追加するのが**プラグイン**になります

### 有名なプラグイン
* HTML Snippets

* HTML CSS Support

* Live Server

その他、数えきれないくらい沢山のプラグインがあるので、手当たり次第、入れて試してみよー

---
layout:false
## プラグイン インストール

その場で説明します。  
まずは、**Visual Studio Code**を起動しましょう。


---
layout:false
## HTMLとは
#### Hyper Text Markup Language（ハイパーテキスト マークアップ ランゲージ)
* ハイパーテキストを記述するためのマークアップ言語の1つ
* ウエブベージを記述するのに一番使われている
* リンクや画像等のマルチメディアを埋め込むハイパーテキストとしての機能、見出しや段落といったドキュメントの抽象構造、フォントや文字色の指定などの見た目の指定、などといった機能がある。

~~ほえ〜、私も初めて知ったー。マルチメディアとかハイパーテキストって今どき聞かんなぁ。。~~
---
layout:false
## HTMLの簡単な構文
mario.html
```
<html>
    <head>
        <meta charset="utf-8">
        <title>まりおのページ</title> 
    </head>
    <body> 
        <h1>マリオだ〜い好き♥</h1>
        <img src="mario_64.png">
    </body>
</html>
```

---
layout:false
## HTMLの確認方法

まずは、適当にHTMLを書いてみましょう。   
その後に説明します。

```
<html>
    <head>
        <meta charset="utf-8">
        <title>まりおのページ</title> 
    </head>
    <body> 
        <h1>マリオだ〜い好き♥</h1>
        <img src="mario_64.png">
    </body>
</html>
```


---
layout:false
## CSSとは
####Cascading Style Sheets（カスケーディング・スタイル・シート、カスケード・スタイル・シート)
* HTML や XML の要素をどのように修飾（表示）するかを定義するW3Cによる仕様の一つ。
* 文書の構造と体裁を分離させるという理念を実現する

構造と体裁を分離しない例) mario_style.html
```
<html>
    <head>
        <meta charset="utf-8">
        <title>まりおのページ</title> 
    </head>
    <body style="color: #000000;
                 background-color:
                 yellow;font-size:
                 x-large;font-weight: bold;"> 
        <h1>マリオだ〜い好き♥</h1>
        <img src="mario_64.png">
    </body>
</html>
```

---
layout:false
## CSSの簡単な構文

mario.css
```
body {
    color: #000000;
    background-color: yellow;
    font-size: x-large;
    font-weight: bold;
}
```

mario_css.html
```
<html>
    <head>
        <meta charset="utf-8">
        <title>まりおのページ</title> 
        <link rel="stylesheet" href="mario.css">
    </head>
    <body>
        <h1>マリオだ〜い好き♥</h1>
        <img src="mario_64.png">
    </body>
</html>
```

---
layout:false
## Java Scriptとは
#### ウェブブラウザ上で動作し、動的なウェブサイト構築やリッチインターネットアプリケーションの開発に用いられるスクリプト言語
* Javaと名前が似ているが、全く異なるプログラミング言語
* 昔はHTMLに動きを与えるために利用されていたが、近年がサーバー側の処理、スマホアプリ開発など幅広く利用されている。
* 極論をいえば、HTML,Java Script,目新しいアイデアさえできれば、独立して会社を興すことも可能
---
layout:false
## Java Scriptの簡単な構文
mario_js.html
```
<html>
    <head>
        <meta charset="utf-8">
        <title>まりおのページ</title> 
        <link rel="stylesheet" href="mario.css">
    </head>
    <body>
        <h1>マリオだ〜い好き♥</h1>
        <img id="mario_img" src="mario_64.png">
        <button onclick="rotateMario()">回転</button>
        <script>
            var d=0;
            function rotateMario(){
                d = d + 90;
                document.getElementById('mario_img').style.transform = "rotate("+d+"deg)";
            }
        </script>
    </body>
</html>

```

---
layout:false
## あとは時間までページをつくりましょー
