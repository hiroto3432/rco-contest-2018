# くるくる寿司 テスター
* これは [第2回 日本橋ハーフマラソン 本戦](https://rco-contest-2018-final.contest.atcoder.jp/) の [問題B - くるくる寿司](https://rco-contest-2018-final.contest.atcoder.jp/tasks/rco_contest_2018_final_b) のテストを行うプログラムです。
* これを用いることで、ローカル環境で回答プログラムを実行し、スコアを確認できます。
* このプログラム上で計算された得点は、当コンテストでの得点ではありません。また、このプログラム上で計算された得点は、当コンテストでの得点を保証するものではありません。
* このプログラムを使用することによるあらゆる損害は保障しかねますので、予めご了承ください。
* このプログラムに関する質問は受け付けていません。予めご了承ください。
* このプログラムの一部を、コンテストの解答に流用してもかまいません。

# コンパイル
`Tester.java` を設置したディレクトリで、以下のコマンドを実行してください。

```bash
javac -encoding UTF-8 Tester.java
```

# 実行
コンパイル後、 `-command` オプションにあなたの回答プログラムを実行するコマンドを渡してテスターを実行すると、テスターが問題の仕様にしたがってあなたのプログラムとやりとりを行い、スコアを計算します。また、好きな乱数シードを整数で与えることができます（与えない場合は、毎回異なる値が乱数シードとして使われます）。

以下のコマンドは、回答プログラムが `a.out` という実行可能バイナリにコンパイルされて `Tester.class` と同じディレクトリに配置されており、 `334` という値を乱数シード値としてテストを実行する場合の例です。
```bash
java Tester -seed 334 -command "./a.out"
```
回答プログラムをRubyで `main.rb` というファイルに記述している場合は、たとえば次のようになります。 `-command` に渡すオプションは、スペースが含まれていても１つの文字列として認識されるよう、`"` で囲ってください。
```bash
java Tester -seed 334 -command "ruby main.rb"
```

`-Q` に続けて整数を渡すと、問題パラメタの `Q` を好きな値に変更して実行できます。

```bash
java Tester -seed 334 -command "./a.out" -Q 100
```

# デバッグ
あなたの回答プログラムが標準エラー出力へ出力した内容は、テスターの標準エラー出力へリダイレクトして書き出します。

また、テスターに `-debug` というオプションを与えると、各クエリの詳細な情報をテスターの標準エラー出力に書き出します。 `Q*6` 行出力されるので、`-Q` に小さい値を指定して実行することをおすすめします。このオプションを指定した例を以下に示します。
```bash
java Tester -seed 334 -command "./a.out" -debug -Q 10
```

