# APIM ❤️ OpenAI

## [セマンティックキャッシングラボ](semantic-caching.ipynb)

[![flow](../../images/semantic-caching.gif)](semantic-caching.ipynb)

[セマンティックキャッシングポリシー](https://learn.microsoft.com/en-us/azure/api-management/azure-openai-semantic-cache-lookup-policy)を試すためのプレイグラウンド。

azure-openai-semantic-cache-lookupポリシーは、事前に設定された外部キャッシュからAzure OpenAI Chat Completion APIおよびCompletion APIリクエストのレスポンスのキャッシュルックアップを行います。プロンプトのベクトル近接性を以前のリクエストと比較し、特定の類似度スコアの閾値を使用して動作します。レスポンスをキャッシュすることで、バックエンドのAzure OpenAI APIへの帯域幅と処理要求を削減し、API消費者が感じるレイテンシを減少させます。

### 結果

![result](result.png)

### 前提条件

- [Python 3.8以降のバージョン](https://www.python.org/)がインストールされていること
- [Pandasライブラリ](https://pandas.pydata.org)がインストールされていること
- [VS Code](https://code.visualstudio.com/)がインストールされ、[Jupyterノートブック拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)が有効になっていること
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)がインストールされていること
- Contributor権限を持つ[Azureサブスクリプション](https://azure.microsoft.com/en-us/free/)があること
- [Azure OpenAIへのアクセス](https://aka.ms/oai/access)が許可されていること、またはモックサービスを有効にすること
- [Azure CLIでAzureにサインイン](https://learn.microsoft.com/en-us/cli/azure/authenticate-azure-cli-interactively)していること

### 🚀 始めましょう

[セマンティックキャッシングノートブック](semantic-caching.ipynb)を開き、提供された手順に従って進めてください。

### 🗑️ リソースのクリーンアップ

ラボが終了したら、追加の料金を避け、Azureサブスクリプションを整理するために、デプロイしたすべてのリソースをAzureから削除する必要があります。
そのためには、[リソースのクリーンアップノートブック](clean-up-resources.ipynb)を使用してください。