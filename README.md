# simple-json-server-test
適当なJSONの応答を返すコンテナを作るための Dockerfile などのサンプル

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

あとは任意のコンテナリポジトリにプッシュして煮るなり焼くなり。
