# 超ざっくりな説明readme

## 超ざっくりな書く要素の入ってるファイル説明
### config.toml
- メインであるHOMEの各パーツいじれるところ
- ヘッダーとかフーターとかのあたりもここで弄れる
- 要素のあり、なしなど
- ルーティングもこのへん
- **困ったらここ弄るんだろうくらいのメイン部分**

### static
- 画像ファイル置き場
- ただここ以外に置かれているものもある（次に説明）
- とりあえずロゴとか大きい画像とかだいたいここだろう

### data
- （多分）大きい要素の中の、小さな要素を入れておくところ
- carousel: HOMEの一番上にある横にスライドできる部分
- clients: 一番下の方にあるクライアントの部分
- features: （デフォなら）６個並んでる、上から２個目の要素
- testimonials: 人物紹介みたいなことろ

### content
- 記事とかのどんどん更新していく系の入れどころ
- dir名は多分設定によって変わりますねえ
- contact.md, faq.md は、そのまんまそのページの内容書いてある
- blog/ はまんま投稿記事

### archtypes/default.md
わからんけど、多分記事を投稿するときのデフォ設定とかかな？

### その他
理解不能予測不可能無理無理蝸牛

## コンテンツのmdにつけられる設定とかなんとか
以下一例
### content/blog/*
- title = "TIIITLLE": **タイトル**
- date = "2015-10-10T13:07:31+02:00": **日付**
- tags = ["hoge"]: **タグ**
- categories = ["hage"]: **カテゴリ**
- banner = "img/banners/banner-5.jpg": **一覧表示のときのバナー画像**
サンプル記事にはないが、「draft = false」というものがデフォルトで設定されていて、trueにすると記事が非公開になる

### content/contact.md
- title = "Contact": **タイトル**
- id = "contact": **何かに紐づいていて、ここが変わるとエラーが起きることだけわかる**

### content/faq.md
- title = "FAQ": **タイトル**
- description = "Frequently asked questions": **HTMLのmetaタグ設定**
- keywords = ["FAQ","How do I","questions","what if"]: **HTMLのmetaタグ設定**
idを下手にそれっぽくつけたら、それはそれでエラー出た

### content/*
メニューを新たに追加したいときは、ここにmd増やせばいけた（例: member.md)。  
mdを増やして、かつconfig.tomlでメニューバーに要素追加したらそんな感じに

## その他
- HOMEのスライドするやつのバックグラウンド画像: themes/static/img/photogrid.jpg
