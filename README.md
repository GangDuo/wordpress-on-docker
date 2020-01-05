# wordpress-on-docker

## wp-cliコンテナを立ち上げてコマンドを実行する
docker-compose run cli wp user list

## 記事を予約投稿する
wp post create --post_title=<ブログのタイトル> --post_content=<ブログの本文> --post_status=future --post_date='2020-12-01 07:00:00'

## ファイルから本文を作成する
$ wp post create ./post-content.txt --post_category=201,345 --post_title='Post from file'

## 記事を更新する
wp post update <投稿ID> --post_title=<ブログのタイトル> --post_content=<ブログの本文>

## タグを作成する
wp term create post_tag <タグ名> --slug=<タグのスラッグ>

# タグを記事に設定する
wp post term add <投稿ID> post_tag <タグのスラッグ>

## for featured image from url
wp post meta add <投稿ID> fifu_image_url <画像のURL>

## カテゴリを記事に設定する
wp post update <投稿ID> --post_category=2
