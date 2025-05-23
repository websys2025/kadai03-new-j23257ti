## 自動販売機（データ構造と各種処理）のミニレポート
### Q5-1. 自動販売機の商品データついて説明せよ。
* データ構造（各項目とその説明
* 今回の商品データ配列"items"はオブジェクト型のデータである。
* items[0].nameというコードはitemsという配列の0番に格納されているデータを表し、.nameで0番データにある"name"という文を表す。今回でいうと"緑茶"を表している。
* 
* 連想配列の配列として定義するメリット
* コードの省略化や、大量のデータをキーを使って簡単に検索ができる。
### Q5-2. showItemListの処理内容について説明せよ。
* 配列の繰り返し処理
* for文でiが0からitems.length(7)までの間、繰り返す処理。
* これにより、iが1増えるだけで参照先を変更することができた。
* 
* 連想配列の参照方法
* items[i].idのように記述することにより、for文でiを1ずつ増やしていき配列データを参照していく。
* その結果、0番の緑茶のデータを出力し終わったら、次は1番,2番・・・と配列の長さ毎に参照していく。
### Q5-3. buyItemの処理内容について説明せよ。
* 商品購入の可否判定
* switch文を使い、商品ごとに条件を付けた。これにより、if文よりも視認性が良く、コードの処理手順を追いやすくなった。
そして、if文で在庫数が0の時に"在庫がありません"と出力するようにした。
* 
* 商品在庫を減らす処理
* Switch文を抜けて、case文の最初で、在庫から1減らす処理を追加、しかしこれでは永遠に１減らすため、
もし、在庫数がすでに0の場合、在庫がないメッセージとともに、在庫に0を代入するようにした。

* 商品番号のエラー処理
* buyItemの一番最初にif文で1-8の数値以外はすべてエラー扱いにする文を追加した。
内容は、「番号が8よりも大きいもしくは、1よりも小さい場合true」というものだ、
これにより、エラーの対策をすることができた。
### Q5-4. プログラムの考察
* データ構造について
* 今まで、配列となるととても視認性が悪かったり、コードからのアクセスが少し難しいと考える。
しかし、今回の連想配列は配列の一括管理や、キーを使った参照が可能なことから、配列よりもデータの
扱いが簡単であると考える。

* 商品一覧表示と購入処理を関数化したメリット
* 全く同じ内容のコードをコピーしなくても、再利用することができる。また、
今回は、商品一覧表示と購入処理を複数回を行っているため、関数化することで、
コードを省略化ができている。この簡単に再利用できること、コードの省略化が
一番のメリットだと考える。
### Q5-5. 感想
* 今回の課題で苦労したこと
* javaScriptをVScodeでの実行が分からなかった。
* javaScriptのエラー原因と、文法の理解
* 
* 演習を通して理解できたこと
* javaScriptの基礎知識
* 連想配列の扱いと、今までの配列との違い。
* 
* この自動販売機プログラムの追加機能や課題など
* 今回は商品番号をキーをとして、商品識別と在庫管理を行っていた。
追加機能として、連想配列に金額データを追加して、購入の際に
入力された金額よりも少なければ、購入できないという機能を追加してみたいと
考えた。
