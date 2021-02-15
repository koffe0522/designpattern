# イテレータ

## イテレータとは

- イテレータは「データの流れを表現する」オブジェクト
- イテレータは自身を戻り値とする`__iter__`メソッド、次の要素を返す`__next__`メソッドを持つ
- `__next__`メソッドでは、要素が尽きたら StopIteration 例外を発生する

## 反復可能オブジェクトとは

- 「要素を一度に 1 つずつ返せる」オブジェクト
- それが内包するイテレータを返す`__iter__`メソッドを持つ

```python
bookShelf = BookShelf()
    bookShelf.append(Book(name="Aroun d the World in 80 days"))
    bookShelf.append(Book(name="Bible"))
    bookShelf.append(Book(name="Cinderella"))
    bookShelf.append(Book(name="Daddy-Long-Legs"))
    for book in bookShelf:
        print(book.getName())

'''
Aroun d the World in 80 days
Bible
Cinderella
Daddy-Long-Legs
'''
```
