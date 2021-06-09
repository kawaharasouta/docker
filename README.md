# docker

ローカルで動かすコンテナ用のレポジトリ．

### sphinx

sphinx用
wikiとhobbiesのビルドに使う．

### tex

tex用
だけど結局まだ動かしてない．

### local_nginx

wikiとhobbiesをサブドメインで分けて表示する用．




## 実際のローカルコンテナ環境構築
上の他に https://hub.docker.com/r/yutarohayakawa/elixir を利用する．

```
//! sphinx document(wiki, hobbies) を cloneする
$ git clone https://github.com/kawaharasouta/wiki ~/git/wiki
$ git clone https://github.com/kawaharasouta/hobbies ~/git/hobbies

//! このリポジトリをcloneする
$ git clone https://github.com/kawaharasouta/docker ~/git/docker

//! sphinx と local_nginx をビルドする
// ここ後でコマンド書くけど今はめんどいのであとで． わかんなかったら各ディレクトリを見たら書いてある． 

//! local_nginx を起動する．
// めんどいので略．

//! elixirコンテナを起動とひとまず動作確認のためnginxのコードをぶん投げておく．
$ mkdir ~/projects
$ docker run --name elixir -p 8090:80 -v ~/projects:/usr/local/elixir/http/projects -d yutarohayakawa/elixir
$ docker exec elixir ./add_project -r https://github.com/nginx/nginx -n nginx


