### 正規表現オブジェクトと JavaScript の String メソッド
```
var a = new RegExp("[0-9]+", "g")
```
### グローバルフラグ g
```
target = "@@@123   456XXX789"
target.match(a)
```
![image](https://user-images.githubusercontent.com/1501327/179153813-6c1bc4be-cb83-48ef-a22e-463cb2b6472e.png)

### String.replace は必ず正規表現( g ) でやりましょう
```
target.replace( new RegExp("X","g"),"y")
```
▲ XXX を yyy に変える

```
target.replace( a,"数字")
'@@@数字   数字XXX数字'
```

### WEBページ内の URL 一覧を配列に入れる
```
var a = document.body.innerHTML
var b = a.match(new RegExp('href=".+?"',"g"))
```
