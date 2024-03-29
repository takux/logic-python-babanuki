# ババ抜きプログラム - ロジック構築でPython中級者を目指すプログラミングコース


- [ババ抜きプログラム - ロジック構築でPython中級者を目指すプログラミングコース](https://www.udemy.com/course/logic_python_babanuki/?referralCode=D4CD90B669B82FA756C1)

次のリンクでは他のコースも含め、お得なクーポンを配布していますのでぜひご覧ください。

=- [講師ホームページ](https://www.takux.one)

<br />

## はじめに

こちらのリポジトリでは [Udemyのババ抜きプログラムコース](https://www.udemy.com/course/logic_python_babanuki/?referralCode=D4CD90B669B82FA756C1) で使用しているソースコードを掲載しています。各セクション終了時点ごとのソースコードを各 secフォルダ へ掲載しています。

<br />

## 講師の環境

本コースでの講師の環境次のようになります。

- 実行環境: Google Colab
- Python: 3.7系  
  ＊colabでは3.7系でしたので念の為記載しています。しかしながらそれ以上に高いバージョンでも問題ないと思います。（参考までに）3.9や3.10以上では関数注釈へより詳細な型指定を記載しておくこともできます。typingモジュールを使えば3.7系でも詳細な注釈を付けることもできます。
- PC: Mac

<br />

## 補足情報

<br />

### 補足1. ペアを捨てる機能をなぜset関数だけでできないか？

トランプでペアになってカードを捨てる場合については次のようにしたいということになります。

```python
# 現在の手札
a = ['A', 'A', '2', '2', '2', '3']

# ペアを捨てた結果次のようにしたい。
# ['2', '3']
```

これをset関数ならできるか試してみると、次のような結果になります。


```python
a = ['A', 'A', '2', '2', '2', '3']

print(list(set(a)))
# ['A', '2', '3']
```

この例では本来「A」は捨てて、「2」と「3」だけにすべきなのに、set関数では「A」が残ってしまっています。
ここからも分かるように、set関数の場合は、ある要素が重複していた場合に1つだけにするということです。


コースの中で作ったinitial_putdown関数を使えばうまくいきます。

```python
a = ['A', 'A', '2', '2', '2', '3']

print(initial_putdown(b))
# ['2', '3']
```
<br />

### 補足2. お世話になったページ

下記では本コース作成において参考になったページを載せさせていただきます。

#### typingを使った型注釈: あっきーさんのページ

本コースではtypingモジュールは使いませんでしたが、下記あっきーさんのページを参考に、
typingを使って書くと、より理解しやすいコードになると思います。

https://qiita.com/papi_tokei/items/2a309d313bc6fc5661c3

#### 切り上げ（math.ceil）について: nkmk.meさんのページ

nkmk.meさんのページも読みやすいページで、よく拝見させていただいています。

https://note.nkmk.me/python-math-floor-ceil-int/

#### set関数について: nkmk.meさんのページ

こちらもnkmk.meさんのページです。

https://note.nkmk.me/python-set/


