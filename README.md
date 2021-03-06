# subject-220715

### JavaScript 基礎
```
location.href = "about:blank"
```

```
document.body
```

```
document.body.innerHTML = "<input>"
```

![image](https://user-images.githubusercontent.com/1501327/179126082-94575fa5-3a1b-4874-8bee-9700c6fd3645.png)

```
document.getElementsByTagName("input")[0].value
```

```
document.body.innerText = "<input><input>"
```

```
console.dir( document )
```

```
document.body.appendChild( a )
```

### jQuery の読み込み
```
var b = document.createElement("script")
document.head.appendChild( b )
b.src = "https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"
```

### jQuery
```
$("body").html()
$("body").text()
$("body").text("<input>")
$("body").html("<input>")
```

### jQuery で新しいコントロール( 要素 ) を追加( この場合、body )
```
var c = $("<input>")
c.appendTo( $("body") )
```
```
$("<input>").appendTo( $("body") )
```

### 対象全てに同じメソッドを実行する
```
$("input").val("山田太郎")
```

### 個別に属性を変更
```
$("input").eq(0).prop("type","button")
$("input").eq(1).prop("type","radio")
$("input").eq(2).prop("type","checkbox")
```

### DOM への参照の取得
```
$("input").get(0).value = "鈴木次郎"
$("input").get(1).value = "田中一郎"
$("input").get(2).value = "織田信長"
```

### class の追加
```
$("input").addClass("btn btn-primary")
$("input").addClass("entry")
```

### インラインスタイルの変更
```
$("input").css("background-color","pink")
```

### 文字列のままのコントロールを作成して使用する
```
$("<input type='button' value='別のボタン' id='inp'>").appendTo( $("body") )
```

### 複数オブジェクトのループ処理
```
$("input").each( function( index ){
   console.log(index)
   console.log(this)
   console.log(  $(this).val()  )
} )
```
