# EchoMap

EchoMap（エコーマップ）は、世界中のライブラジオや環境音を地図上のピンから聴けるサーバーレスWebアプリです。

## 使い方

1. `index.html` をブラウザで開きます。
2. 地図上のピンをクリックすると、その都市のライブストリームを再生します。
3. `Random Jump` ボタンで、登録済み都市のどこかへランダムに移動して再生できます。

## GitHub Pagesで公開する

このリポジトリはHTML/CSS/JavaScriptだけで動くため、GitHub Pagesにそのまま公開できます。

1. GitHubのリポジトリ設定を開きます。
2. **Pages** を選びます。
3. 公開元に現在のブランチとルートディレクトリを指定します。
4. 保存後、発行されたURLへアクセスします。

## 音源を追加する

`index.html` 内の `audioSpots` 配列に、次の形式で1件追加してください。

```js
{
  city: "都市名",
  country: "国名",
  station: "放送局名",
  coordinates: [緯度, 経度],
  streamUrl: "https://...",
  sourceUrl: "https://放送局や配信元のページ",
}
```

HTTPSの直接再生できるストリームURLを使うと、GitHub Pagesでも混在コンテンツの警告を避けられます。
