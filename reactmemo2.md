# JSXとは

# トランスパイラ(トランスコンパイラ):Babel

# CLI経由でBabelを実行する方法
    $ mkdir babel-cli-example && cd babel-cli-example
    $ echo "{}" > package.json
    $ npm install --save-dev babel-cli babel-preset-react

- babel-cli:BabelをCLI上で動作させるためのパッケージ
- babel-preset-react:Reactを使った開発を行う時に必要なBabelプラグインをまとめたパッケージ

<br>

input.js

    ReactDOM.render(
        <h1>Hello, babel!</h1>,
        document.getElementById('root')
    );

<br>

- 下記のコマンドを入力することで、対象のファイルの中身がJSXからJavaScriptに変換されていることがわかる

        $ ./node_modules/.bin/babel --presets=react input.js
        ReactDOM.render(React.createElement(
            'h1',
            null,
            'Hello, babel!'
        ), document.getElementById('root'));

<br>

- 下記コマンドを入力することで、標準出力ではなく指定のファイルに出力される

        $ ./node_modules/.bin/babel --presets=react input.js --out-file output.js
