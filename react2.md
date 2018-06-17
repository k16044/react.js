# 第2章　Hello Worldその2
## コードの解説
### JSX

ソースコードの中にHTMLを書けるように、JavaScriptのシンタックス拡張。FacebookはReactでコードを書く時にJSXを使うことを推奨している。

変数への代入

    const title = <h1>Hello, World</h1>; 
### 変数の展開

    const name = 'pirosikick';
    const className = 'title';
    const title = <h1 title={className}>Hello, {name}</h1>;