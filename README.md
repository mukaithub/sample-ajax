# sample-ajax
授業中のリソースの置き場所

ajaxのgetを行う為のテンプレート
## jQuery 側の json オブジェクトの準備
``` javscript
formData = {};
```
{} は空のオブジェクト
``` javscript
formData["param1"] = "テスト";
```
formData のプロパティはformData["プロパティ文字列"]に値をセットして作成される

formData のプロパティは formData.プロパティ文字列と書くこともできます
``` javscript
formData.param1 = "テスト";
```
## jQuery 側からサーバへデータを送る
``` javscript
data: formData
```
``` javscript
{
	"param1": "テスト"
}
```
http://localhost/app/form-action-json.php?param1=%E3%83%86%E3%82%B9%E3%83%88&_=1626243759099

と言うフォーマットに jQuery に加工されてサーバの PHP が呼び出されます
## PHP でデータを受け取る
QuertyString と呼ばれる ? 以降の文字列が $_GET にセットされて PHP に入る
``` javscript
param1=%E3%83%86%E3%82%B9%E3%83%88&_=1626243759099
```
<b>$_GET["param1"]</b> に "テスト" がセットされて スーパーグローバル変数として利用可能となる。
