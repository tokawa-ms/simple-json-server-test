# simple-json-server-test
## What's this?
適当なJSONの応答を返すコンテナを作るためのサンプルです。

JSON 形式でデータを定義するだけで、その JSON の中身を REST API の応答として返してくれる便利な OSS ([json-server](https://github.com/typicode/json-server)) があったので、活用させていただきました。
また、Azure Container Apps などで動作させられる Docker Container としてビルドするための Dockerfile も作ってみました。

## How to Use
### ローカル実行

```node
npm run json-server
```
### コンテナとしてローカルで実行

```bash
docker build . -t <tag>
docker run -p <任意のポート番号>:3000 <tag>
```

あとは任意のコンテナリポジトリにプッシュして煮るなり焼くなりできます。

### Azure Container Apps で実行
以下の手順で Azure Container Apps で実行できます。

- コンテナイメージを Azure Container Repository にプッシュ
- Azure Container Apps でコンテナイメージを指定してアプリを作成
  - このとき、Ingress のポート番号は 3000 に設定
- Azure Container Apps で作成したアプリの URL にアクセスして動作確認

## References
[json-server](https://github.com/typicode/json-server)

[クイック スタート:Azure portal を使用して Azure コンテナー レジストリを作成する](https://learn.microsoft.com/ja-jp/azure/container-registry/container-registry-get-started-portal?tabs=azure-cli)

[クイックスタート: Azure portal を使用して最初のコンテナー アプリをデプロイする](https://learn.microsoft.com/ja-jp/azure/container-apps/quickstart-portal)
