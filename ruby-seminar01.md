Ruby入門以前（第1回 最初のプログラム）
===
Rubyを通してプログラミングの基礎を勉強しましょう。今回は、Rubyのプログラムを自分で書いて実行できるようにするところまでを解説します。

準備
-
[RailsInstaller](http://railsinstaller.org/en) から、あなたのOSに適したインストールパッケージをダウンロードしてください。ダウンロードが完了したら、ダウンロードしたパッケージを開きましょう。Rubyのインストールが始まるはずです。インストールが完了したら、次の節に進んでください。

はじめてのRubyプログラミング
-
早速、Rubyのプログラムを書いてみましょう。ターミナル（Windowsではコマンドプロンプト）を開いて、`irb`と入力してください。irbはRubyの簡単なプログラムを実行するためのソフトウェアです。
```
irb
```
すると、以下のような文字が表示されます。「さあ、ここにプログラムを書いてください」という意味です。
```
irb(main):001:0>
```
ここにプログラムを書きます。今回は、最も簡単なプログラムを書きましょう。キーボードから`puts "Hello!"`と入力してください。
```
irb(main):001:0> puts "Hello!"
```
`"Hello!"`と入力したら、Enterキーを押しましょう。すると以下のように表示されます。
```
irb(main):001:0> puts "Hello!"
Hello!
=> nil
irb(main):002:0>  
```

ファイルにプログラムを書いて実行する
-
今度は少し長いプログラムを書いてみましょう。先ほど使った irb は長いプログラムを書くのには適していませんので、今度はファイルにプログラムを書いて、それを実行してみましょう。

###フォルダの作成
まずは、デスクトップに `ruby` というフォルダを作ってください。

フォルダを作ったら、ターミナルで、そのフォルダに移動します。

MacOSの方は、以下のように入力してください。
```
cd /Users/xxxx/Desktop/ruby
```
Windowsの方は、以下のように入力してください。
```
cd C:\Users\xxxx\Desktop\ruby
```
###プログラムを書く
移動できたら、プログラムを書いてみましょう。お好きなテキストエディタを開いて、以下のように書いてください。
```ruby
puts "Hello world!"
puts "Hello Ruby!"
puts "Hello Programming!"
```
上記のように書けたら、このファイルを`hello.rb`という名前で、先ほどデスクトップに作った `ruby`フォルダの中に保存してください。

###プログラムを実行する
プログラムのファイルを保存できたら、そのプログラムを実行してみましょう。Macの方はターミナル上で`ls`
と入力してください。Windowsの方は`dir`と入力してください。すると、以下のように表示されます。
```
hello.rb
```
これは先ほどあなたが作成して保存したファイルです。さて、このファイルに書かれたプログラムを実行してみましょう。以下のように入力し、Enterキーを押してください。
```sh
ruby hello.rb
```
すると、以下のように表示されます。
```
Hello world!
Hello Ruby!
Hello Programming!
```
ここまでできたら、Rubyでプログラミングする方法を一通り学んだことになります。ウェブ上のRuby解説サイトや、Rubyの入門書などを参考にしながら、Rubyプログラミングを楽しみましょう！

練習問題
-
1. `hello.rb` の中身を書き換えて実行してみましょう。
2. `foods.rb` というファイルを作り、実行すると以下のように表示されるプログラムを書きましょう。

```
Apple
Banana
Carrot
```