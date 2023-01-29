# array関数  

## array()
**配列を生成する**  
array()と型を定義するためのもの。関数ではない。　　
[]でも宣言可能
```php
$array = array();
$array = [];
```


## is_array()
**変数が配列か判定する**

## explode()
**文字列を文字列により分割**  
ファイル読み込みなどで改行・カンマ区切りで使用  
```php
explode( 区切り文字列, 文字列 );
```

## implode()
**配列要素を文字列により連結**

## array_column()
**入力配列から単一のカラムの値を返す**  
PHP5.5から  
配列から特定の要素を取得したい場面で使用。
```php
array_column(配列, 列キー, インデックスキー);
```

## array_keys()
**配列のキーすべて、あるいは一部を返す**

## in_array()
**配列に値があるかチェック**

## array_values()
**配列のすべての値を返す**  
値を取り出すために使用。

## array_diff()
**配列の差を計算する**  
```php
array_diff(比較元の配列, 比較対象の配列)
```

## array_key_exists()
**指定したキーまたは添字が配列にあるか調べる**  
if文でよく使う

## array_merge()
**ひとつまたは複数の配列をマージする**  
**array+arrayとの違い**  
配列の場合  
array_merge  
キーが同じでも完全にマージされている。  
array1 + array2  
両方の配列に同じキーが存在する場合は前方の配列が残り、 後方の配列は無視されている。  
  
連想配列の場合  
array_merge  
両方の配列に同じキーが存在する場合は、後方の配列が優先される。  
array1 + array2  
両方の配列に同じキーが存在する場合は、前方の配列が優先される。  

## array_search()
**指定した値を配列で検索し、見つかった場合最初のキーを返す**  
```php
array_search ( mixed $needle , array $haystack [, bool $strict = FALSE ] ) : mixed
```
$needle  
第1引数の$needleが探す値です。  

$haystack  
第2引数の$haystackは走査対象の配列です。  

$strict  
第3引数の$strictをTRUEにすると、array_searchは厳密な型比較を行います。  

返り値  
値が見つかった場合はそれに対応するキー、見つからなかった場合はFALSEを返します。  
また、PHP 5.3.0以降から無効な引数を渡されたときはNULLを返すようになりました。  




