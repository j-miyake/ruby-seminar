Ruby入門以前（4時間目 条件分岐）
=
身近な問題を例に、Rubyのプログラムを書いてみましょう（[3時間目 ハッシュ](period03.md)の続きです）。
もし、〜だったら
-
プログラミングで必ず使用するといっても過言ではないものが`条件分岐`です。これ自体はそれほど難しくありませんが、複雑に入り組んだ条件分岐を読み解くのは少し慣れが必要です。最初は簡単な条件分岐から覚えていきましょう。

条件分岐には、`if 〜 else`を使います。
例えば、値段が高いりんごに対して「Expensive!」、安いりんごに対して「Cheap!」と表示させたいとき、以下のようなプログラムを書きます。
```ruby
apple = 200
if apple > 100
  puts "Expensive!"
else
  puts "Cheap!"
end
```
上記のプログラムは、appleが100円以上であれば "Expensive!"と表示し、そうでなければ "cheap!"と表示します。
実際に書いてみましょう。`if1.rb`というファイルを作成して、上記のプログラムを書いてください。書けたら実行してみましょう。以下のように表示されるはずです。
```
Expensive!
```
上記のプログラムの最初の行を`apple = 50`に書き換えて、もういちど実行してみてください。今度は、以下のように表示されるはずです。
```
Cheap!
```
このように、`if 〜 else`を使うことで、条件によってプログラムの動作を変えることができます。


変化する物語
-
`if 〜 else`を応用して、Rubyで物語を書いてみましょう。まず、何も条件分岐のない物語を書いてみます。
```ruby
puts "Tom is 10 years old."
puts "Tom is hangly."
puts "Tom goes to a restaurant."
puts "Tom eats a dish of beef."
puts "Tom is thirsty."
puts "Tom drinks a grass of coke."
```
上記を実行すると、以下のように表示されます。
```
Tom is 10 years old.
Tom is hangly.
Tom goes to a restaurant.
Tom eats a dish of beef.
Tom is thirsty.
Tom drinks a grass of coke.
```
これだけでは、面白くないので、Tomの状態に合わせて物語が変化するようにしてみましょう。
```ruby
age = 20
status = "thirsty"

puts "Tom is #{age} years old."

if status == "thirsty"
  puts "Tom is thirsty."
  if age < 20
    puts "Tom drinks a grass of coke."
  else
    puts "Tom drinks a grass of beer."
  end
else
  puts "Tom is not thirsty."
end
```
`if2.rb`という名前のファイルを作成して、上記のプログラムを書いてみましょう。書けたら実行してみてください。以下のように表示されるはずです。
```
Tom is 20 years old.
Tom is thirsty.
Tom drinks a grass of beer.
```
このプログラムの`age`の部分を20未満に書き換えて、もういちど実行してみましょう。以下のように表示されるはずです。
```
Tom is 10 years old.
Tom is thirsty.
Tom drinks a grass of coke.
```
更に、このプログラムの`status`の値を "thirsty"以外の文字（たとえば hungry）に書き換えて、もういちど実行してみましょう。以下のように表示されるはずです。
```
Tom is 10 years old.
Tom is not thirsty.
```

このプログラムでは、`if 〜 else` が入れ子になっています。慣れるまでは読むのに時間がかかるかもしれませんが、じっくり動作を読み解いていってください。

練習問題
-
1. 1から20までの配列`[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, ..., 20]`を作成し、その中で2と3の両方で割り切れる数のみを表示してください。割ったときに余りが0になるものを"割り切れる"とみなします。割ったときの余りを求めるには、`%` を使ってください（ http://www.namaraii.com/rubytips/?数値#l4 ）。
