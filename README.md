# BUFFALOのNAS LS510D0301Gが自動的に作成する画像サムネイルを削除したい
[https://www.buffalo.jp/product/detail/ls510d0301g.html](https://www.buffalo.jp/product/detail/ls510d0301g.html)

BUFFALOのNAS LS510D0301Gは、画像ファイルに対してサムネイルを自動的に作成する。ユーザーマニュアルによれば7つの隠しフォルダが作成される。

商品情報 > 取扱説明書 > ユーザーマニュアル（PDF）
> 共有フォルダーに画像ファイルを保存すると、以下の隠しフォルダーが作成され、そのフォルダー内に画像サムネイルが作成されます。
> .thumbnail、.webaxs_3L、.webaxs_L、.webaxs_LL、.webaxs_M、.webaxs_S、.webview

**参考情報**  
このクソ仕様のNASをどうにかしたい！(怒)  
[http://aoimizuna.doorblog.jp/archives/54989108.html](http://aoimizuna.doorblog.jp/archives/54989108.html)

## 環境
- Windows 11 Pro 22H2

## 作成された画像サムネイルの隠しフォルダを削除する

### 作業1 最上位のフォルダ名を "." (ピリオド) から始めて隠しフォルダにする
隠しフォルダにすることで、以降は画像サムネイルが作成されなくなるらしい。

変更前のフォルダ名
```
\\LS510D24a\homes\backup-YYYYMMDD
```

変更後のフォルダ名
```
\\LS510D24a\homes\.backup-YYYYMMDD
```

### 作業2 エクスプローラーでフォルダを開いて画像サムネイルの隠しフォルダを検索する
エクスプローラーの右上のフォルダ内の検索で画像サムネイルの隠しフォルダの名前の一部を入力する。

エクスプローラーで開くフォルダの例
```
\\LS510D24a\homes\.backup-YYYYMMDD\photo
```

検索する名前
- .thum
- .webaxs
- .webview

検索結果のフォルダを全て削除する。
