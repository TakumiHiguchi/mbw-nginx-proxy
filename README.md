# music.branchwith-nginx-proxy

music.branchwithのReverseProxyサーバを立てるやつです。

## 注意
- dockerが使える環境はご自身でご用意してください。

## 使い方
### 1.music.branchwith-nginx-proxyの起動
1. mbw-nginx-proxy をcloneしましょう
  ```
  $ git clone https://github.com/TakumiHiguchi/mbw-nginx-proxy.git
  ```

2. ディレクトリに移動しましょう
  ```
  $ cd mbw-nginx-proxy
  ```

3. dockerちゃんに全てお任せしましょう
  ```
  $ docker-compose build
  $ docker-compose up
  ```

### 2.music.branchwith-apiの起動
4. music.branchwith apiをcloneしましょう
  ```
  $ git clone https://github.com/TakumiHiguchi/mbw_api.git
  ```

5. ディレクトリに移動しましょう
  ```
  $ cd mbw_api
  ```
  
6. dockerちゃんに全てお任せしましょう
  ```
  $ docker-compose build
  $ docker-compose up
  ```

7. テストデータを流します
  ```
  $ docker-compose run web bundle exec rails db:seed
  ```

music.branchwith-apiの詳しいREADMEは、[music.branchwith-api](https://github.com/TakumiHiguchi/mbw_api)のREADMEを見てください。

以下利用したいサービスを起動してください。

### music.branchwith
1. music.branchwith をcloneしましょう
  ```
  $ git clone https://github.com/TakumiHiguchi/music.branchwith.git
  ```

2. ディレクトリに移動しましょう
  ```
  $ cd music.branchwith
  ```

3. dockerちゃんに全てお任せしましょう

4. join [mbw.localhost](http://mbw.localhost/)

music.branchwithの詳しいREADMEは、[music.branchwith](https://github.com/TakumiHiguchi/music.branchwith)のREADMEを見てください。

### music.branchwith webGUI
1. music.branchwith webGUI をcloneしましょう
  ```
  $ git clone https://github.com/TakumiHiguchi/mbw_webgui.git
  ```

2. ディレクトリに移動しましょう
  ```
  $ cd mbw_webgui
  ```

3. dockerちゃんに全てお任せしましょう
  ``` 
  $ docker-compose build
  $ docker-compose run node yarn install
  $ docker-compose up
  ```

6. join [mbw-webgui.localhost](http://mbw-webgui.localhost/)

music.branchwith webGUIの詳しいREADMEは、[music.branchwith webGUI](https://github.com/TakumiHiguchi/mbw_webgui)のREADMEを見てください。