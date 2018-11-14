# MacにNode.jsをインストール
Node.jsの公式サイトからインストールもできるが...
Homebrew使ってインストールしよう!

## インストールの流れ
1. Homebrewのインストール
2. nodebrewのインストール
3. Node.jsのインストール

## Homebrewとは？
- MacOSにおいて、ソフトウェアの導入を単純化するパッケージ管理システムのひとつ
- 必要なパッケージのインストールやアンインストール、アップデートが必要な時、公式サイト等からダウンロードしなくても、コマンド一つで出来てしまう! 

## Homebrewをインストールする前に...
- まずは、Homebrewをインストールするのに必要なコマンドを打てる準備
- 下記のコマンドをターミナルに入力して、Command Line Toolsをインストール

        $ xcode-select --install

- 上記のコマンド入力後、いろいろな画面が表示されるが、インストールや同意するを押して進めてください
- 「ソフトフェアがインストールされました」と表示されればOK

## Homebrewをインストール
- Homebrewのホームページ( https://brew.sh/index_ja )からインストールするコマンドをコピーして、ターミナルにペーストする
- 最後に

        Installation Successful!
    と表示されていれば成功しているはず
- 念のために下記のコマンドを実行して、本当にインストールされているか確認

        $ brew update　#一応updateして最新にしておく
        $ brew -v
<br>

    Homebrew 1.8.2
    Homebrew/homebrew-core (git revision c7e09; last commit 2018-11-08)
    Homebrew/homebrew-cask (git revision 67afc; last commit 2018-11-07)
- 上記のような表示されればOK
- バージョンの数字は違っていても大丈夫

## nodebrewとは
- Node.jsのバージョン管理ツール
- 複数のバージョンのNode.jsをインストールしたり、切り替え等々ができる

## nodebrewをインストール
    $ brew install nodebrew

- 上記のコマンドでインストール後、下記コマンドでnodebrewのバージョンが確認できる

        $ nodebrew -v

- nodebrewが使いやすいように環境パスを通す
- bashの場合、下記コマンドを入力

        $ echo 'export PATH=$HOME/.nodebrew/current/bin:$PATH' >> ~/.bash_profile

- bash以外で使いたいときは各シェルの適したファイルに追記する
- 追記した後、ターミナルを再起動

## Node.jsとは
- ブラウザ以外のプラットフォームで動作するJavaScriptの実行環境

## Node.jsをインストール
- 下記のコマンドでインストール可能なバージョンが表示される

        $ nodebrew ls-remote

- 上記コマンドで以下のようなエラーが発生する場合がある

        Fetching: https://nodejs.org/dist/v7.10.0/node-v7.10.0-darwin-x64.tar.gz
        Warning: Failed to create the file 
        Warning: /Users/whoami/.nodebrew/src/v7.10.0/node-v7.10.0-darwin-x64.ta
        Warning: r.gz: No such file or directory

        curl: (23) Failed writing body (0 != 941)
        download failed: https://nodejs.org/dist/v7.10.0/node-v7.10.0-darwin-x64.tar.gz

    その時はディレクトリを作成

        $ mkdir -p ~/.nodebrew/src

- 最新バージョンのインストールは下記のコマンドを入力

        $ nodebrew install-binary latest

- バージョンを指定してインストールする場合は、下記のコマンドを入力

        $ nodebrew install-binary {version}

- コマンドでインストールされたバージョンの確認は、下記のコマンドを入力

        $ nodebrew ls
        v11.1.0

        current: none

- インストール直後はcurrent: noneとなっているため、必要なバージョンを有効化する
- インストールされたnodeの有効化は下記のコマンドを入力

        $ nodebrew use v11.1.0

- 現バージョンの確認

        $ node -v

# create-react-app
## create-react-appとは
- ビルド設定などなしにReactの開発を簡単にはじめられることを目的としたFacebookが提供する開発ツール

## インストール
    $ sudo npm install -g create-react-app
