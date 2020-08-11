# 簡易的なアプリを作ってみよう
- はじめに、Reactを使ってHello,World!を表示するアプリケーションを作ってみよう

<br>

    $ create-react-app my-app



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

# webpack
- webpackは、モジュールハンドラーと呼ばれるツール
- モジュールハンドラーとは、ES Modulesや、Node.jsで利用されているCommonJSのモジュール方式で記述されたソースファイルを束ねて、ブラウザで実行可能な静的なJavaScriptファイルを出力する
- Webのフロントエンド開発でnpmパッケージを多用するようになった昨今、必須のツール

        # 作業ディレクトリの作成
        $ mkdir webpack-example
        $ cd webpack-example

        # 空のpackage.jsonの作成
        $ echo "{}" > package.json

        # webpack, babel関連パッケージのインストール
        $ npm install --save-dev \
          webpack \
          babel-loader \
          babel-core \
          babel-preset-react
        
        # react, react-domのインストール
        $ npm install --save react react-dom

        # バージョンの表示
        $ ./node_modules/.bin/webpack --version
        4.26.0

        バージョンの確認をする際
        Do you want to install 'webpack-cli' (yes/no): 
        がでてきたら、
        yes
        と入力し、インストール後もう一度コマンド入力すると、バージョンの確認ができる

