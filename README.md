# HTML Part3 その他編

## 目次
- セクションを理解しよう
- `<div>`を理解しよう
- `<span>`を理解しよう
- ブロック要素とは？
- インライン要素とは？
- 試しに作ってみよう

## セクションを理解しよう
以下のタグは必ず覚えましょう。
`<header>` グループの頭に該当する情報の塊
`<footer>` グループの足に該当する情報の塊
`<article>` 独立したコンテンツ(ブログ記事など)の塊            
`<nav>` メニュー、ナビゲーション情報の塊
`<aside>` 補足情報の塊
`<section>`それ以外の情報の塊

例：header,footer
```html
<!DOCTYPE html>
<html>
　<head>
　　<title>サンプル</title>
　</head>
　<body>
　　<header><p>グループの頭に該当する</p></header>←
        <div>メインコンテンツ</div>
　　<footer><p>グループの足に該当する</p></footer>←
</body>
</html>
```
例：nav
```html
<header>
    <p>グループの頭に該当する</p>
    <nav>←
        <ul>
            <li><a href=“#”>HOME</a></li>
            <li><a href=“#”>会社情報</a></li>
        </ul>
    </nav>←
</header>
```
例：article
```html
省略
</header>
    <article>←
        <h1>独立したコンテンツ</h1>
        <p>例えば、ブログ記事などに使います</p>
    </article>←
<footer>グループの足に該当する</footer>
```
例：section
```html
<article>
    <h1>独立したコンテンツ</h1>
    <section>←
        <h2>sectionに見出しは必須</h2>
        <p>コンテンツ</p>
    </section>←
    <section>←
        <h2>sectionに見出しは必須</h2>
　       <p>コンテンツ</p>
    </section>←
</article>
```
sectionは見出しがある情報の塊をまとめる時に使います。

## `<div>`を理解しよう

`<div></div>`は情報をまとめる時に使います

`<div>`を細かく詳細に分類したものが

`<header><footer><article><section><nav><aside>`

用途は基本的に同じ、上記タグ以外で情報をまとめたい時に`<div>`を使う

情報をまとめるって何？

## 例えば
何かのコンテンツ1

コンテンツコンテンツコンテンツコンテンツコンテンツコンテンツ

何かのコンテンツ2

コンテンツコンテンツコンテンツコンテンツコンテンツコンテンツ

↑各コンテンツを分けたい！

```html
<div>←
    <h2>何かのコンテンツ</h2>
    <p>コンテンツコンテンツコンテンツ</p>
</div>←
<div>←
    <h2>sectionに見出しは必須</h2>
    <p>コンテンツ</p>
</div>←
```
まとめたいコンテンツを`<div>`で囲います

```
<div style="border:1px solid #ccc; margin:10px;">
    <h2>何かのコンテンツ</h2>
    <p>コンテンツコンテンツコンテンツ</p>
</div>
<div style="border:1px solid #ccc; margin:10px;">
　<h2>sectionに見出しは必須</h2>
<p>コンテンツ</p>
</div>
```
わかりやすいように線を引いてみる

結果こうなります。
<div style="border:1px solid #ccc; margin:10px;">
    <h2>何かのコンテンツ</h2>
    <p>コンテンツコンテンツコンテンツ</p>
</div>
<div style="border:1px solid #ccc; margin:10px;">
　<h2>sectionに見出しは必須</h2>
<p>コンテンツ</p>
</div>

## `<span>`を理解しよう
`<div>`のインライン要素バージョンが`<span>`

何かのコンテンツ1

コンテンツコンテンツコンテンツコンテンツコンテンツ「コンテンツ」←ここだけ色を変えたい

何かのコンテンツ2

コンテンツコンテンツコンテンツコンテンツコンテンツコンテンツ

```html
<h2>何かのコンテンツ1 </h2>
<p>コンテンツコンテンツ
    <span style="color:red;">コンテンツ</span>
</p>
<h2>sectionに見出しは必須</h2>
    <p>コンテンツ</p>
</div>
```
結果こうなります。
<h2>何かのコンテンツ1 </h2>
<p>コンテンツコンテンツ
    <span style="color:red;">コンテンツ</span>
</p>
<h2>sectionに見出しは必須</h2>
    <p>コンテンツ</p>
</div>

## ブロック要素 インライン要素とは？

## ブロック要素とは？
ブロック要素とはブロック(一つの塊)として扱われるHTMLタグ

`<div>　<p>　<ul>　<table>`
`<h1> ~ <h6>`等が該当

ブロック要素は必ず改行されます

## インライン要素とは？
インライン要素とは行の中の一部として扱われるHTMLタグ

`<a>　<img>　<span>`等が該当

インライン要素は改行されません

## ブロック インライン要素とは？
`<p>`と`<a>`で例えると・・・

```html
<p><a href=“#”>何らかのリンク</a></p>
```
`<p>`はブロック要素

`<a>`はインライン要素

インライン要素は一般的に内側にいれます
<br><br>


`<p>`と`<a>`で例えると・・・
```
<p>何らかの<a href=“#”>リンク</a></p>
```
インライン要素はどこに入れても改行されない

## 試しに作ってみよう
```html
<!DOCTYPE html>
<html>
    <head>
        <title>サンプル</title>
    </head>
    <body>
        <header><p>グループの頭に該当する</p></header>
　　  <footer><p>グループの足に該当する</p></footer>
    </body>
</html>
```

```html
..省略
<header>
    <p>グループの頭に該当する</p>
    <nav>
        <ul>
            <li><a href=“#”>HOME</a></li>
            <li><a href=“#”>会社情報</a></li>
        </ul>
    </nav>
</header>
..省略
```

```html
..省略
</header>
    <article>
        <h1>独立したコンテンツ</h1>
        <p>例えば、ブログ記事などに使います</p>
　　</article>
<footer>グループの足に該当する</footer>
..省略
```

```html
..省略
<article>
    <h1>独立したコンテンツ</h1>
    <section>
        <h2>sectionに見出しは必須</h2>
        <p>コンテンツ</p>
    </section> 
    <section>
        <h2>sectionに見出しは必須</h2>
        <p>コンテンツ</p>
    </section>
</article>
..省略
```
