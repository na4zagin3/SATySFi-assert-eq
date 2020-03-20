# 使い方

作成したパッケージが想定した機能を持っているかを確認することができます。

`assert-eq arabic (1+2) 3`などのように、`assert-eq <function> <left> <right>`のように与えることで、`<left>`と`<right>`が一致するかどうかを確かめることができます。

ここで与える`<function>`は`<left>`や`<right>`での値を文字列に変換するための関数です。

多くの値については[debug-show-value](https://github.com/puripuri2100/SATySFi-debug-show-value)パッケージが役に立つでしょう。

また、エラー報告をわかりやすくするために、チェックする関数にラベルを付けることができます。これは`assert-eq ?:(<label>) <function> <left> <right>`のように、最初にオプション引数の形で与えてください。

# 提供関数など

モジュール名：`AssertEq`

- `assert-eq : string?-> ('a -> string) -> 'a -> 'a -> unit`
- `direct \assert-eq : [string?; ('a -> string);'a; 'a] inline-cmd`
- `direct +assert-eq : [string?; ('a -> string);'a; 'a] block-cmd`

組版時には`\assert-eq`コマンドは`inline-nil`と同じ挙動をし、`+assert-eq`は`block-nil`と同じ挙動をします。
