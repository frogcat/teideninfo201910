# About

[東京電力停電情報:住所から検索](http://teideninfo.tepco.co.jp/html/00000000000.html) 配下の停電情報を
2019年10月12日0時～2019年10月16日11時までの間、一時間ごとに合計108回スクレイピングしてデータを集めました。

このデータを加工して、以下のようなプロパティを持つ [data.json](https://github.com/frogcat/teideninfo201910/blob/master/data.json) (小地域ポリゴンを複数持つ GeoJSON) を作成しました。

- hours : 当該小地域の累積停電時間 (最大で108時間)
- label : 市区町村コード/都道府県名/市区町村名/小地域名

小地域ポリゴンは [統計LOD](http://data.e-stat.go.jp/lodw/) から取得した国勢調査小地域のポリゴンデータを加工(simplify)して作成しました。

# License

CC-BY 4.0

# Demo / Preview

- <https://frogcat.github.io/teideninfo201910/>


# Note

- 東京電力の使用する小地域名と国勢調査の小地域名が完全一致する場合にのみポリゴンを付与して GeoJSON に収録しています
- 完全一致しなかった場合は GeoJSON にデータが収録されていません
- 収録されなかったデータは [error.txt](https://github.com/frogcat/teideninfo201910/blob/master/error.txt) にまとめています
- 当該期間中に停電が発生しなかった小地域のポリゴンは収録されていません
