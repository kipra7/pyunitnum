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
