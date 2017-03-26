MyProperties
================================================================================

JavaのPropertiesクラスのラッパークラスにJavafx用の便利メソッドを追加したクラス。

- Version      : 1.1.0
- Java Version : 1.8.0_121
- Author       : 次郎 (Jiro)
- Since        : Mar 07, 2017
- Last Changed : Mar 07, 2017

ライブラリ概要
--------------------------------------------------------------------------------

Propertiesクラスを利用する際の手間のかかるカスタムなどの一切をラッピングして、セ
ット、storeといった機能のみを提供する。

基本的にはただのラッパークラスだが、getProperty()といったメソッドがStringではな
く`Optional<String>`を返却する。

Stageクラスを引数に渡すとラッピングしたPropertiesからx, y, width, height,
isMaximizedキーでそれらの値のセットを試みるメソッドを持つ。これはそれらのキーが
存在しなかった場合`null`エラーを出さず、Stageのプロパティも変更しない。

出力するファイルはインスタンス生成時のFileのパスにxml形式で生成する。properties
ファイルとして生成するように設定を変更する方法を持たない。