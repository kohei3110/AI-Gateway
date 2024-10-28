# APIM ❤️ OpenAI

## [バックエンドサーキットブレーカラボ](backend-circuit-breaking.ipynb)

[![flow](../../images/backend-circuit-breaking.gif)](backend-circuit-breaking.ipynb)

Azure OpenAIエンドポイントまたはモックサーバーに対して、APIMの組み込み[バックエンドサーキットブレーカ機能](https://learn.microsoft.com/en-us/azure/api-management/backends?tabs=bicep)を試すためのプレイグラウンド。

### 前提条件

- [Python 3.8以降のバージョン](https://www.python.org/)がインストールされていること
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)がインストールされていること
- [VS Code](https://code.visualstudio.com/)がインストールされていること
- アクセス権限を持つ[Azureサブスクリプション](https://azure.microsoft.com/en-us/free/)があること
- [Azure OpenAIへのアクセス](https://aka.ms/oai/access)が許可されていること、またはモックサービスを有効にすること
- [Azure CLIでAzureにサインイン](https://learn.microsoft.com/en-us/cli/azure/authenticate-azure-cli-interactively)していること

### 始めましょう

[Jupyterノートブック](backend-circuit-breaking.ipynb)を開き、提供された手順に従って進めてください。

### 🗑️ リソースのクリーンアップ

ラボが終了したら、追加の料金を避け、Azureサブスクリプションを整理するために、デプロイしたすべてのリソースをAzureから削除する必要があります。
そのためには、[リソースのクリーンアップノートブック](clean-up-resources.ipynb)を使用してください。