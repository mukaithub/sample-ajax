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
