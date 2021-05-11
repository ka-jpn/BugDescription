Update 2021/5/11

[Japanese : my native language]

試行錯誤する中でこのエラーについて新しいことが分かりました。

・`<div></div>`は有効ですが`<div />`は有効ではない

・ネストの深さは関係ない

根本的なことでは、私が「`<div />`は有効ではない」ことを知らなかったのが原因のようです。
しかし@on{DOM EVENT}="{DELEGATE}"構文を使用していない場合はエラーが出ず、使用しているとエラーが出るのは原因が分かりにくい要因でした。

[English : not my native language, cannot guarantee the accuracy of the meaning]

Through trial and error, I found something new about this error.

· `<div></div>` is valid but `<div />` is not

・ The depth of nesting does not matter

The root cause seems to be that I didn't know that "` <div /> `is not valid".
However, if you didn't use the @on {DOM EVENT} = "{DELEGATE}" syntax, wouldn't get an error, and if did, would get an error. the cause was hard to understand.

[↓ old contents]

[following content 2021/5/11 ~ 2021/5/11]

[Japanese : my native language]
不具合を説明するためのプロジェクト
Blazor webassemblyのプロジェクトをhostedで作成したものをIndex.razorだけ内容を変更したもの。

@on{DOM EVENT}="{DELEGATE}"構文を使用して、かつネストが深いとエラーになります。
![alt text](https://user-images.githubusercontent.com/83901976/117737819-a10e1e80-b235-11eb-9d96-c872271f602c.png)

このように@on{DOM EVENT}="{DELEGATE}"構文を削除するか、一番内側のdivを削ることでエラー表示は消えます。
![alt text](https://user-images.githubusercontent.com/83901976/117737825-a2d7e200-b235-11eb-8930-9ec859f8f4ff.png)
![alt text](https://user-images.githubusercontent.com/83901976/117737810-9bb0d400-b235-11eb-9e94-c3bd0f2a7ab7.png)

[English : not my native language, cannot guarantee the accuracy of the meaning]
A project to explain the bug
A Blazor webassembly with hosted project created, with only Index.razor modified.

Using the @on {DOM EVENT} = "{DELEGATE}" syntax and deep nesting will result in an error.
![alt text](https://user-images.githubusercontent.com/83901976/117737819-a10e1e80-b235-11eb-9d96-c872271f602c.png)

By deleting the @on {DOM EVENT} = "{DELEGATE}" syntax like this or removing the innermost div, the error display disappears.
![alt text](https://user-images.githubusercontent.com/83901976/117737825-a2d7e200-b235-11eb-8930-9ec859f8f4ff.png)
![alt text](https://user-images.githubusercontent.com/83901976/117737810-9bb0d400-b235-11eb-9e94-c3bd0f2a7ab7.png)

[following content 2021/5/9 ~ 2021/5/11]

不具合を説明するためのプロジェクト

Blazor webassemblyのプロジェクトをhostedで作成したものをIndex.razorだけ内容を変更したもの。

Index.razorの構文にエラーがある旨がエラー一覧ウィンドウに表示されます。
３行目の@onkeyup="KeyUp"を削除するか、５行目のdivを削除するとエラーが消えます。

@onkeyupの代わりに@onkeydownでも同様にエラーになります。
他の@on{DOM EVENT}="{DELEGATE}"構文でも同様かは未検証です。
Blazor webassembly + hosted 以外の場合にも同様かは未検証です。
