# pyunitnum (coming soon...)
Python and numpy library to simplify dimensional analysis and regulation between different systems of units (mainly for solid state physics.)


## What is Possible with This Library? : Some Examples

- Calculations with automatic dimensional analysis of variables and constants (so you can avoid some calculation errors)
- Mutual conversion between systems of units (i.e. SI and CGS-gauss)
- Smooth integration with numpy, pandas, and xarray


## 以下、構想（日本語）

Pythonの整数、小数や、それを含む配列などのデータ構造、Numpy配列、Pandasやxarrayの各カラム等々に物理における「単位」を登録できるようなメソッドを追加する。

既存の変数同士を演算してできた新しい変数に次元解析を与え、次元を自動的に追加する。

基本SI単位系にして、わざわざ変える際はいちいち指定するか、setunitsystemみたいな関数を用意してデフォルトの単位系をセットできるようにする。

次元や単位系は適切に出力できるようにする。(classにしてstrメソッドでどうにかするしかないかな)


### 詳細な構想・テスト

#### ベース
ひとまず次元についてはデコレーターとして実装すればよさそう。あんまりなじみがないので慣れないときつい。まずは適当でいいので作ってみよう。

最初は「変数に次元を追加して表示するだけの機能」を作り、演算等は後から実装していく。

たとえば変数a: np.adarrayに「グラム」という単位を追加するなら、pu.set(a, "g")みたいな感じで作れないかと思ってる。

#### メソッド

#### 演算アルゴリズム
とりあえず同じ単位系同士の計算はトライ木の最小共通祖先とかをうまく使って簡潔に実装できないかなと思ってる。そこまでムキになって難しいアルゴリズムを使うべきかは不明。
こういうのが好きだから色々考えちゃうけど、後から考えればいい話ではある。
