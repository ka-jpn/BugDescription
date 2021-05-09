不具合を説明するためのプロジェクト

Blazor webassemblyのプロジェクトをhostedで作成したものをIndex.razorだけ内容を変更したもの。

Index.razorの構文にエラーがある旨がエラー一覧ウィンドウに表示されます。
３行目の@onkeyup="KeyUp"を削除するか、５行目の<div />を削除するとエラーが消えます。

@onkeyupの代わりに@onkeydownでも同様にエラーになります。
他の@on{DOM EVENT}="{DELEGATE}"構文でも同様かは未検証です。
Blazor webassembly + hosted 以外の場合にも同様かは未検証です。
