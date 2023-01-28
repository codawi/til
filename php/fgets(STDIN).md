# paizaのスキルチェックで出てくるfgets(STDINE)について
## 入力値が複数ある場合
### 改行されている場合
入力例  
10  
5  

```php
echo fgets(STDIN); //10が表示される
echo fgets(STDIN); //5が表示される
```
 
### 入力値がスペース区切りの場合
入力例
10 5  
  
**PHPの場合explode関数を使う**  
explode関数とは文字列を指定した区切り文字で分割し、配列に代入する関数  
```explode("区切り文字", 文字列);```

入力例を分割する場合
```php
$input = fgets(STDIN);
$array = explode(" ",$input);
$a = $array[0]; //$aに10が入る
$b = $array[1]; //$bに5が入る
```  

**※fgets(STDIN)で取得した型は必ず文字列型**  
PHPは型を柔軟に判断してくれるので四則演算には問題ないが、厳密判定の===を使う場合は注意。
