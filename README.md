# Docker

rails development environment by docker

# setup

```
$ git clone git@github.com:koukic/docker-rails
Please change the directory name
$ cd directoryname
$ docker-compose build
$ docker-compose run --rm web bin/yarn install
if you need
$ docker-compose run --rm web yarn install --check-files
$ docker-compose run --rm web rake tmp:create

change git remote url
$ git remote set-url origin https://github.com/koukic/~
```
databaseはbuildの時に生成されます

ディレクトリー名を変更したい場合
```
docker-compose rm
docker rmi　imageid
if you need
docker volume rm ~
```
ただし 二回目以降はrmi imageidとするのはimageidが同じものが二つあるので注意
としてbuildをする
その後他のコンテナが起動していないことを
docker psで確認する

# mysqlの接続
```
$ docker-compose exec mysql bash
$ mysql --password=koukic sample_app_development
```
