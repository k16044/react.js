# Node.js
node.jsの公式サイトからインストールもできるが...
Homebrew使ってインストールしよう!

## Homebrewとは？
- MacOSにおいて、ソフトウェアの導入を単純化するパッケージ管理システムのひとつ
- 必要なパッケージのインストールやアンインストール、アップデートが必要な時、公式サイト等からダウンロードしなくても、コマンド一つで出来てしまう! 

## Homebrewをインストールする前に...
- まずは、Homebrewをインストールするのに必要なコマンドを打てる準備
- 下記のコマンドをターミナルに入力して、Command Line Toolsをインストール

        xcode-select --install

- 上記のコマンド入力後、いろいろな画面が表示されるが、インストールや同意するを押して進めてください
- 「ソフトフェアがインストールされました」と表示されればOK

## Homebrewをインストール
- Homebrewのホームページ( https://brew.sh/index_ja )からインストールするコマンドをコピーして、ターミナルにペーストする
- 最後に

        Installation Successful!
    と表示されていれば成功しているはず
- 念のために下記のコマンドを実行して、本当にインストールされているか確認

        brew update　#一応updateして最新にしておく
        brew -v
<br>

Homebrew 1.8.2
Homebrew/homebrew-core (git revision c7e09; last commit 2018-11-08)
Homebrew/homebrew-cask (git revision 67afc; last commit 2018-11-07)
- 上記のような表示されればOK
- バージョンの数字は違っていても大丈夫

## 現バージョンの確認
    node -v

