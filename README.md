# Docker

rails development environment by docker

# setup

```
$ git clone git@github.com:koukic/docker-rails
Please change the directory name
$ cd directoryname
$ docker-compose build
$ docker-compose run --rm app bin/yarn install
$ docker-compose run --rm app rake tmp:create

change git remote url
$ git remote set-url origin https://github.com/koukic/~
```
databaseはbuildの時に生成されます

ディレクトリー名を変更したい場合
```
docker-compose rm
docker rmi　imageid
```
としてbuildをする
その後他のコンテナが起動していないことを
docker psで確認する
