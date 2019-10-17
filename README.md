# About

2019年10月12日0時～2019年10月16日11時までの期間を対象に、一時間ごとの停電情報を収集しました。
このデータを加工して、以下のようなプロパティを持つ GeoJSON を作成しました。

- hours : 当該小地域の累積停電時間 (最大で108時間)
- label : 市区町村コード/都道府県名/市区町村名/小地域名


# Data

## [停電情報:東京電力分](https://github.com/frogcat/teideninfo201910/blob/master/data.json)

[東京電力停電情報:住所から検索](http://teideninfo.tepco.co.jp/html/00000000000.html) 配下の停電情報を一時間ごとにスクレイピングしてデータを集めました。

- 小地域ポリゴンは [統計LOD](http://data.e-stat.go.jp/lodw/) から取得した国勢調査小地域のポリゴンデータを加工(simplify)して作成しました。
- 東京電力の使用する小地域名と国勢調査の小地域名が完全一致する場合にのみポリゴンを付与して GeoJSON に収録しています
- 収録されなかったデータは [error.txt](https://github.com/frogcat/teideninfo201910/blob/master/error.txt)



## [停電情報:中部電力分](https://github.com/frogcat/teideninfo201910/blob/master/data.chubu.json)


[中部電力停電情報:停電状況のお知らせ(過去の停電)](https://teiden.chuden.jp/p/teiden_kosu/day/) 配下の停電情報をスクレイピングしてデータを集めました。

- 小地域ポリゴンは [統計LOD](http://data.e-stat.go.jp/lodw/) から取得した国勢調査小地域のポリゴンデータを加工(simplify)して作成しました。
- 中部電力の使用する小地域名に対して国勢調査の小地域名が先頭一致する場合にポリゴンを付与して GeoJSON に収録しています
- 収録されなかったデータは [error.chubu.txt](https://github.com/frogcat/teideninfo201910/blob/master/error.chubu.txt)  にまとめています


# License

CC-BY 4.0

# Demo / Preview

- <https://frogcat.github.io/teideninfo201910/>
