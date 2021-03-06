[![Build Status](https://travis-ci.org/miyohide/magazine.rubyist.net.svg?branch=master)](https://travis-ci.org/miyohide/magazine.rubyist.net)

# Rubima on Jekyll

次期るびま本体のサイトです。

# 記事について

記事は、`articles/号数/_posts/日付-記事名.md`として作成してください。画像ファイルなどは`images/号数-記事名`以下に配置してください。
記事はPull Requestで受け付け、リリースのタイミングでmergeします。

# 書式

Markdownです。具体的には、[kramdown](https://kramdown.gettalong.org/)を使っています。
詳細な文法は[kramdownのSyntaxページ](https://kramdown.gettalong.org/syntax.html)を参照してください。

# リリース作業について

次の手順で行います。今のところ、GitHub Pages上で動かすことを考えています。

1. 受け付けたリリース対象の記事のPull Requestをmergeします。
1. 次のことがTravisでできそうなので、実装すれば良さそう。
- `bundle exec jekyll build`を実行します。
- `_site`にサイトが生成されるので`git commit`して`gh-page`ブランチにcommit、`git push`します。

上記のようにしているのは、amazonの書影をとるためにpluginを使用しているため。これを解決できれば、特にcloneしなくても動かせるものと考えています。

# 移行

URLが`http://magazine.rubyist.net/?xxx`から`https://magazine.rubyist.net/xxx`に変わるため、なんらかの移行作業が必要になるかと思います。
案としては、以下のもの。

1. 移行しない。リリースのタイミングで切り替える。
1. 現システムを動かしているサイトにてURLが変わったことを表示するようする。

# 影響

- るりま
  - いくつかのページにおいて`http://magazine.rubyist.net/`を参照しているところがあるので、修正を依頼するpull requestを出す。
- www.ruby-lang.org
  - 過去のリリースのお知らせについてURLを変更するPull Requestを出す？
- 地域Ruby会議レポート
  - URLを変更するPull Requestを出す


