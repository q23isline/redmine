# redmine

## はじめにやること

```bash
git clone 'https://github.com/redmine/redmine.git'
cp redmine/Gemfile docker/local/ruby/Gemfile
docker-compose build
docker-compose up -d
docker exec -it app bundle exec rake db:migrate
docker exec -it app env REDMINE_LANG=ja
docker exec -it app bundle exec rake redmine:load_default_data
# 入力を求められたら ja を入力
```

## 動作確認

### URL

- <http://localhost>

### ログイン情報

こちらから変わっていなければ、以下  
[Redmineガイド | Redmineのインストール | Step 10 - ログイン](http://guide.redmine.jp/RedmineInstall/#step-10-)

- Username
  - admin
- Password
  - admin
