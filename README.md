
### このレポジトリについて

docker-composeを使用したNuxt3環境です

viteが使えないとか、色々問題はありますが


### 環境のつくりかた


1. 適当な場所に `git clone`
2. `test_nuxt3`フォルダに移動
3. `docker-compose build`
4. `docker-compose run --rm sample npx nuxi init nuxt3-app`
5. docker-compose.ymlの中身を書き換えましょう（超ダサい）

    `working_dir: /` -> `working_dir: /nuxt3-app` 
6. `docker-compose run --rm sample yarn install`
7. nuxt.config.tsのdefineNuxtConfig内に以下を追加

    `vite: false`
8. `docker-compose up -d`

- 途中でdocker-compose.ymlを書き換えるという謎な工程が必要なので、そのうち作り替えます

- nodeのversion(17.0.1)がunsupportedなのでそのうち作り替えます

- vite,falseにしなくていい方法ないかなぁ
