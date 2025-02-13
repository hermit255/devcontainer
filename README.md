### 前提
devcontainerという名前のコンテナを環境にするので、事前に名前指定でイメージを作成しておきましよう

```shell
docker build . -t devcontainer
```

### 使い方
- cloneしたフォルダでVSCodeを開く
- VSCodeウインドウの左下角にある `><` をクリック
- `Reopen in container` を選択
    - 初回はコンテナ内にVSCodeをインストールするので10分以上かかる場合もある