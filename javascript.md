# javascriptで簡単なオンクリックイベントを発生させる
## 実現したこと
リンクをクリックしたら別ウィンドウで任意のhtmlファイルを開けるようにする
## やったこと
・表示したいhtmlファイルを用意する
・遷移元のhtmlファイルを修正する
・オンクリックイベントを発生させるjavascriptコードを上記に追加
## 実際に書いたコード
<html>
<a href="#" onClick="javascript:sample_sanple2(); return false;">sample</a>

<javascript>
<script type="text/javascript">
<!---

// サンプル.htmlを表示
var open_sample_sample2 = function () {
var height=100%
    window.open('/sample/sample.html', 'sample', 'menubar=no, toolbar=no, location=no, status=no')
}
//--->
</script>
