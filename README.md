<h1>Python Study Memo</h1>
<h2>Type 型 6/3 </h2>

- String ==> Text str "Hello" "test" 文字列
- Int ==> Integer int 123 456  整数
- Float ==>  Float 123.45  456.78  小数
- Boolean ==> True or False  真偽値
- List ==> List abc = ["a", "b", "c"]  リスト

```python
print(abc)
#  "a", "b", "c"
print(abc[0])
#  a
print(abc[3])
#  Error
print(abc[-2])
#  b
print(abc[-1])
#  c
print(abc[0:-2])
# == print(abc[-2])
#  ["a", "b"]
```

```python
print(abc[1:-2])
#  b

a1 = "Hello"
a2 = "World"
a3 = a1 + a2
print(a1 + a2)
#  HelloWorld

print(a3)
#  HelloWorld

a = 1
# a 変数 = 1 値
a = a + 1
print( a)
#  2
```

さらに
```Python
a += 1
print(a)
#  3
```

- 関数 function
```Python
def test(a):
    return a
```

```Python
b = 2
print(test(b))
#  2
```

<h2>デバッグ 6/17</h2>

```python
a = 1
b = "test"
print(a + b)
```

実行結果
```
Traceback (most recent call last):
  File "C:\Users\sxu\Desktop\Test\Python Tests\PythonTestScript.py", line 4, in <module>
    print(a + b)
          ~~^~~
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

#### 大事なライン：
```
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```
エラーの種類を特定

```
line 4, in <module>
    print(a + b)
```
エラーが発生したラインを特定

#### キーワード：
- Error
- Exception == 例外

例外処理 `try-except`
```python
try:
    a = 1
    b = "test"
    print(a + b)
except TypeError as e:
    print(f"TypeError: {e}")
```

動作解説： `try` 内で起きた例外を `except` 内で一回格納し、`TypeError` に当てはまるものを変数 `e` として扱って以降の処理で扱う
