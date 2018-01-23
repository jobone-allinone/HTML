# HTML Part2 タグ編

## 目次
- 試しに作ってみよう
- よく使うタグを覚えよう

## よく使うタグを覚えよう

## 見出し
h1~h6 (headline or heading) ブロック要素
h1：1番大きな見出し、タイトルなどに使う ※使用頻度は1ページに1回程度
h2：2番目に大きな見出し、大見出しなどに使う
h3：3番目に大きな見出し、小見出しなどに使う ※必ずh2の中で使うこと
※h4以降はあまり使う機会は少ない

## 見出しコード例
```html
<h1>SMAPが解散！？</h1>
<p>コンテンツコンテンツ</p>
<h2>メンバー間の亀裂が原因</h2>
    <h3>木村と香取の不仲説</h3>
    <p>コンテンツコンテンツ</p>
    <h3>中居はどっち派閥か</h3>
    <p>コンテンツコンテンツ</p>
<h2>香取と草彅が発端か</h2>
    <h3>解散の原因</h3>
    <p>コンテンツコンテンツ</p>
    <h3>年内解散の理由</h3>
    <p>コンテンツコンテンツ</p>
```

## 段落
p (paragraph) ブロック要素
pタグに近いものに`<br>`があります。

`<br>`は改行です。
ですが、`<br>`は極力使用しないでください。
改行はpを使いましょう。

## 段落②
`<br>`はスマホ画面が崩れやすい！
PC画面
![PC画面](https://user-images.githubusercontent.com/35711528/35255665-7581c972-0033-11e8-9fe1-49806af5edcb.gif)
スマホ画面
![スマホ画面](image-tag-2.gif)

## 段落③
改行は`<p>`を使いましょう
PC画面
![PC画面](image-tag-3.gif)
スマホ画面
![スマホ画面](image-tag-4.gif)

## リスト
順序がないリスト
ul (unordered list) ブロック要素

順序があるリスト
ol (ordered list) ブロック要素

リスト内容
li (list item) ブロック要素

## リスト②　順序がないリスト
HTMLコード
```html
<h2>好きな食べ物</h2> HTML
<ul>
    <li>ハンバーグ</li>
    <li>カレーライス</li>
　　<li>ラーメン</li>
</ul>
```
ブラウザ上
<h2>好きな食べ物</h2>
<ul>
    <li>ハンバーグ</li>
    <li>カレーライス</li>
    <li>ラーメン</li>
</ul>

## リスト③　順序があるリスト
HTMLコード
```html
<h2>好きな食べ物ランキング</h2>
<ol>
    <li>カレーライス</li>
    <li>ラーメン</li>
　　<li>ハンバーグ</li>
</ol>
```
ブラウザ
<h2>好きな食べ物ランキング</h2>
<ol>
    <li>カレーライス</li>
    <li>ラーメン</li>
    <li>ハンバーグ</li>
</ol>


## 定義リスト
定義リスト　dl (definition list)　ブロック要素

定義語
dt (definition term)　ブロック要素

定義説明
dd (definition description)　ブロック要素

## 定義リスト②
```html
<h2>好きな食べ物</h2> HTML
<dl>
    <dt>ハンバーグ</dt>
        <dd>ソースはデミグラスが好きです。</dd>
    <dt>ラーメン</dt>
        <dd>味噌ラーメン最高！</dd>
</dl>
```
リスト(ul)に説明文をつけたい時、dlを使います。

## リンク
a (anchor) インライン要素
href (hyper reference)
`<a href=“index.html”>トップへ</a>`
           相対パス
`<a href=“index.html” target=“_blank”>トップへ</a>`
別ウィンドウで開く

## 画像
img (image) インライン要素
`<img src=“img/sample.jpg” alt=“テスト画像”>`
altは画像の説明文です。
srcは画像ファイルのURLです。
何らかのエラーで画像が表示されないときにaltのテキストが
表示されます。必ず入れるようにしましょう。

## テーブル
テーブル
table (table) ブロック要素
テーブル行
tr (table row) ブロック要素
テーブル見出し
th (table header) ブロック要素
テーブルデータ
td (table data) ブロック要素

```html
<table>
    <tr>
        <th>好きな食べ物</th>
        <td>ハンバーグ</td>
        <td>ラーメン</td>
    </tr>
    <tr>
        <th>好きなスポーツ</th>
        <td>サッカー</td>
        <td>野球</td>
    </tr>
</table>
```
<table>
    <tr>
        <th>好きな食べ物</th>
        <td>ハンバーグ</td>
        <td>ラーメン</td>
    </tr>
    <tr>
        <th>好きなスポーツ</th>
        <td>サッカー</td>
        <td>野球</td>
    </tr>
</table>
※デザインはCSSで作ります


```html
<table>
    <tr>
        <th>好きな食べ物</th>
        <th>好きなスポーツ</th>
        </tr>
    <tr>
        <td>ハンバーグ</td>
        <td>サッカー</td>
    </tr>
    <tr>
        <td>ラーメン</td>
        <td>野球</td>
    </tr>
</table>
```
<table>
    <tr>
        <th>好きな食べ物</th>
        <th>好きなスポーツ</th>
    </tr>
    <tr>
        <td>ハンバーグ</td>
        <td>サッカー</td>
    </tr>
    <tr>
        <td>ラーメン</td>
        <td>野球</td>
    </tr>
</table>
※デザインはCSSで作ります

## 試しに作ってみよう

```
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>Job庵</title>
    </head>
    <body>
        <p>Job庵プログラムです</p>
    </body>
</html>
```
資料の順番に書いていこう。
