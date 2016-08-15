jekyllを使用してHPを作成しました．

- `about.md` : 研究概要
- `wlab_access.md` : アクセス，関連リンク
- `activities.md` : 研究室での活動
- `_posts/` : お知らせを1ブログを単位として公開
- `member.md` : メンバ一覧
  - `members/` : 個別ページ


# usage


## まずcloneします

#+BEGIN_SRC shell
$ git clone git@github.com:wkblab/wkblab.github.io.git
$ cd wkblab.github.io
#+END_SRC

## 必要なgemをインストールします

```
$ bundle install --path vendor/bundle # jekyllに必要なgemをbundleを使ってインストール
$ bundle exec jekyll server # localhostを立ち上げて確認する場合
```

## 編集してから反映させます．

```
$ git add .
$ git commit -m "編集内容をここに書く"
$ git push
```

# その他
テーマは [[https://github.com/dbtek/paper][paper]]をベースにしています．
