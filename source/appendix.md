# Markdownの再現テスト
いくつかのマークダウン表記をSphinxで変換した。<br>
commonmarkで対応していない表記も試している。<br>
- 参考：対応マークダウン。
  - [commonmark](https://commonmark.org/)
  - [GitHub](https://docs.github.com/ja/github/writing-on-github/basic-writing-and-formatting-syntax)

## 見出しレベル2
### 見出しレベル3
#### 見出しレベル4
##### 見出しレベル5

## 文字装飾
★ソース  
```
**強調**
*斜体*
~~打消し~~
```

★変換結果  
**強調**  
*斜体*  
~~打消し千~~  


## 箇条書き
★ソース
```markdown
- a
- b
- c
  - c.1
  - c.2

1. Title
2. Title
3. Title
```
★変換結果  
- a
- b
- c
  - c.1
  - c.2

1. Title
2. Title
3. Title

## タスクリスト
★ソース
```markdown
- [x] a
- [ ] b
- [ ] c
```
★変換結果  
- [x] a
- [ ] b
- [ ] c

## チェックボックス(HTML)
★ソース
```
<input type="checkbox" value="true">a</input>
```

★変換結果  
<input type="checkbox" value="true">a</input>




## 引用
★ソース
```markdown
> こちにちは
>> こんにちは
```
★変換結果  
> こちにちは
>> こんにちは

## 画像
★ソース
```markdown
![image](img/img.png)
```
★変換結果  
![image](img/img.png)


## リンク
★ソース
```markdown
https://www.google.co.jp/
[Google](https://www.google.co.jp/)
```
★変換結果  
https://www.google.co.jp/  
[Google](https://www.google.co.jp/)  


## テーブル
拡張機能（sphinx_markdown_tables）があればテーブル表現を変換できる。<br>

★ソース
```markdown
|a|b|c|
|-----|-----|-----|
|1|2|3|
|a|b|c|
|あ|い|う|
```

★変換結果  

|a|b|c|
|-----|-----|-----|
|1|2|3|
|a|b|c|
|あ|い|う|

## コードブロック
★ソース
````
```python
from sys import os
def test:
    print()
```
````

★変換結果  
```python
from sys import os
def test:
    print()
```



## 水平線
★ソース
```markdown

---

```

★変換結果  

---

## blockdiag
http://blockdiag.com/ja/blockdiag/sphinxcontrib.html  
★ソース
````
```eval_rst
.. blockdiag::
   :desctable:

   blockdiag {
      A -> B -> C;
   }
```
````

★変換結果  
```eval_rst
.. blockdiag::
   :desctable:

   blockdiag {
      A -> B -> C;
   }
```

## actdiag
http://blockdiag.com/ja/actdiag/sphinxcontrib.html  
★ソース
````
```eval_rst
.. actdiag::

    actdiag admin {
      A -> B -> C;
    }
```
````

★変換結果
```eval_rst
.. actdiag::

    actdiag admin {
      A -> B -> C;
    }
```
a