まず初めに、dockerとvirtualbox をインストールすること

1.適当な場所に展開して、docker-compose.ymlの階層にcd
2. docker-machine create --driver virtualbox docker-compose_wp
3. eval $(docker-machine env docker-compose_wp)
4. docker-compose up -d
　※2,3の 「docker-compose_wp 」の表記は、てきとうに変更する
5.表示のURLを確認するコマンド　「docker-machine ls 」
　URLに書かれている「tcp://192.168.99.*** 」までがIPアドレス
 docker-compose.ymlの　wordpress 「ports」の7001 がポート番号
 ですから、表示のURLは　「http://192.168.99.***:7001」となります
 ※portsの7001は変更可能です
6.phpmyadminを表示するURL「http://192.168.99.***:8080」 
 docker-compose.ymlの　phpmyadmin 「ports」の8080 がポート番号
 ですから、表示のURLは　「http://192.168.99.***:8080」となります
 ※portsの8080は変更可能です
　
---------------
主なコマンド
docker-compose を一時停止
 docker-compose stop
 
docker-compose 起動
 docker-compose up -d

docker-machine の起動確認
 docker-machine ls

docker-machine の停止
 docker-machine stop

docker-machine の削除
 docker-machine rm


