# mock up Documentation

## タイムライン
動画やテキストなど、mock upで管理するオブジェクトに時間情報を付与したものを**クリップ**と呼びます。
タイムラインとはクリップを管理する、`mTimeLine`型のオブジェクトです。

### タイムラインの生成

```nim
import mockuppkg/[timeline]

var main_timeline = Timeline()
```

タイムラインは、必ず**可変変数**で定義しなければなりません。

### タイムラインにクリップを設置する
タイムラインオブジェクトにクリップを追加します。
同じフレームにオブジェクトを重複して追加することはできません。
追加に成功した場合はクリップの識別番号を、失敗した場合は `none(UUID)` を返します。

```nim
import clips

var
  tl = TimeLine()
  video_uuid = tl[1].push(Clip())
```