jekyllを使用してHPを作成しました．

- `about.md` : 研究概要
- `wlab_access.md` : アクセス，関連リンク
- `activities.md` : 研究室での活動
- `_posts/` : お知らせを1ブログを単位として公開
- `member.md` : メンバ一覧
  - `members/` : 個別ページ


# usage

## いきなりpushしたくないとき（なれていない時）

やり方はいくつかありますがここでは1例を紹介します．

### fork

[github](https://github.com/wkblab/wkblab.github.io/)のforkというボタンをクリックして，自分のアイコンを選んでください．

### clone

```
$ git clone git@github.com:wkblab/wkblab.github.io.git
$ cd wkblab.github.io
```

### remoteとしてforkした方を追加

```
git remote add local git@github.com:YOUR-github-account-id/wkblab/wkblab.github.io.git
```

- `local` の部分は何でもよいです．
- `YOUR-github-account-id`は自分のアカウント名 (あるいは `git@~~~.git` はforkしたリポジトリのcloneボタンででてくるリンクを貼り付けるだけでよいです)

### 編集してから反映

```
$ git add .
$ git commit -m "編集内容をここに書く"
$ git push local master # 2回目以降はgit push -f local master
```

### PRを送る

forkした方のリポジトリから `[New pull request]` を出します．

### 2回目以降

最新版のwkblab.github.ioのページをもってくる

```
$ git fetch origin master
$ git reset --hard origin/master
```

[編集してから反映させます]&[PRを送る]と同じです．

-----

## 直接pushする方法
### まずcloneします

```
$ git clone git@github.com:wkblab/wkblab.github.io.git
$ cd wkblab.github.io
```

### 必要なgemをインストールします

```
$ bundle install --path vendor/bundle # jekyllに必要なgemをbundleを使ってインストール
$ bundle exec jekyll server # localhostを立ち上げて確認する場合
```

### 編集してから反映させます．

```
$ git add .
$ git commit -m "編集内容をここに書く"
$ git push
```

# その他
テーマは [paper](https://github.com/dbtek/paper)をベースにしています．
