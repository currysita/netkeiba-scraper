netkeiba-scraper をforkして改良してみました。

#オリジナルとの相違点
- build.sbt の修正
-- scala-xml を追加。昔は標準で含まれてたそうです。
-- scalikejdbc のバージョンを 2.5.2 にしました。取得する時にエラーが出ていたので、URLを直接開いて使用可能なバージョンを探しました。
- URLの変更
-- httpのURLが廃止されているので、httpsに変更しまいた。
- sbt.batを修正
-- sbtconfig.txt が見つからない警告が出てたのに対処しました。リポジトリ内に sbtconfig.txt を含めてそれを読むようにしました。
- sbtconfig.txt の内容
-- xmxを1024Mに設定。現代のPCならほぼ大丈夫でしょう。若干速度が改善しました。
- テーブルの構造を修正
-- 馬の名前を取得するよう修正しました。
-- タイムが文字列しかなかったので、real型の秒数として取得するようにしました。
- その他
-- 無効なレース情報を追加しました。

以下はオリジナルの README.md の内容です。

#使い方
以下のコマンドを上から順に実行していけば最後に素性が作成される。
```
sbt "run collecturl"
```
レース結果が載っているURLを収集して「race_list.txt」に保存する。
```
sbt "run scrapehtml"
```
レース結果のHTMLをスクレイピングしてhtmlフォルダに保存する。HTMLをまるごとスクレイピングするので結構時間がかかる。
```
sbt "run extract"
```
HTMLからレース結果を抜き出しSQLiteに保存する。
```
sbt "run genfeature"
```
レース結果を元にして素性を作りSQLiteに保存する。