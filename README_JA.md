--------------------------------
【バージョン】
--------------------------------
v5


--------------------------------
【概要】
--------------------------------
このサンプルプログラムは、Rubyを使用して各APIを呼び出す処理のサンプルです。

--------------------------------
【内容物】
--------------------------------
conf/
  - config.yml          : 各種IDを記述する設定ファイルです。

src/jp/co/yahoo/adsdisplayapi/
  - sample/       : レポートのサンプルです。

--------------------------------
【環境設定】
--------------------------------
Ruby環境を構築するために、以下をインストールしてください。

1. Ruby 2.7以上のバージョン
2. gem 3.1.2以上
3. OpenAPI generator 4.2.3以上の4.x系
4. confディレクトリ配下にあるconfig.ymlに各IDを記述します。
  - account_id          : アカウントIDを記述してください(必須)。
  - access_token        : アクセストークンを記述してください(必須)。

--------------------------------
【実行】
--------------------------------
OpenAPI Generatorを実行しRuby用のclientを生成します。
※インストール方法によってOpenAPI Generatorの実行方法に違いがあります。以下の例はHomebrewでインストールした場合です。
```
openapi-generator generate -i https://yahoojp-marketing.github.io/ads-display-api-documents/design/v5/Route.yaml -g ruby -o ./
```

直下にopenapi_client.gemspecが生成されるので、ビルドします。
```
gem build openapi_client.gemspec
```
gem installを実行します。
```
gem install ./openapi_client-1.0.0.gem
```

実行例
```
ruby src/jp/co/yahoo/adsdisplayapi/sample/ReportDefinitionServiceSample.rb 
```

--------------------------------
ご注意：　Yahoo!広告 ディスプレイ広告 API - サンプルコードの利用に関して
--------------------------------

Yahoo! JAPANの提供するAPIに関するサンプルコードは、別途Yahoo! JAPANとの間で締結いただいた当該APIの提供に関する契約に基づき、APIユーザー様に提供されるものであり、Yahoo! JAPANとの間で当該契約を締結いただいていない場合は、サンプルコードをご利用いただけません。
また、APIユーザー様に予め通知することなく、サンプルコードの内容や仕様の変更または提供の停止もしくは中止をする場合があります。ご了承のうえご利用ください。
