# APIM ❤️ OpenAI

## [組み込みロギングラボ](built-in-logging.ipynb)

[![flow](../../images/built-in-logging.gif)](built-in-logging.ipynb)

[API Managementの組み込みロギング機能](https://learn.microsoft.com/en-us/azure/api-management/observability)を試すためのプレイグラウンドです。リクエストはApplication Insightsにログされ、提供された[ノートブック](openai-usage-analysis-workbook.json)を使用してリクエスト/レスポンスの詳細やトークン使用量を簡単に追跡できます。

### 前提条件

- [Python 3.8以降のバージョン](https://www.python.org/)がインストールされていること
- [Pandasライブラリ](https://pandas.pydata.org)がインストールされていること
- [VS Code](https://code.visualstudio.com/)がインストールされ、[Jupyterノートブック拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)が有効になっていること
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)がインストールされていること
- Contributor権限を持つ[Azureサブスクリプション](https://azure.microsoft.com/en-us/free/)があること
- [Azure OpenAIへのアクセス](https://aka.ms/oai/access)が許可されていること、またはモックサービスを有効にすること
- [Azure CLIでAzureにサインイン](https://learn.microsoft.com/en-us/cli/azure/authenticate-azure-cli-interactively)していること

### 🚀 始めましょう

[Jupyterノートブック](built-in-logging.ipynb)を開き、提供された手順に従って進めてください。

### 🗑️ リソースのクリーンアップ

ラボが終了したら、追加の料金を避け、Azureサブスクリプションを整理するために、デプロイしたすべてのリソースをAzureから削除する必要があります。
そのためには、[リソースのクリーンアップノートブック](clean-up-resources.ipynb)を使用してください。