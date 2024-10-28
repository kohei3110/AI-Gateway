# APIM ❤️ OpenAI

## [高度な負荷分散ラボ](advanced-load-balancing.ipynb)

[![flow](../../images/advanced-load-balancing.gif)](advanced-load-balancing.ipynb)

Azure OpenAIエンドポイントまたはモックサーバーのリストに対して高度な負荷分散を試すためのプレイグラウンド。

このロードバランサーは、[スマートロードバランサーリポジトリ](https://github.com/andredewes/apim-aoai-smart-loadbalancing)からフォークしたカスタムポリシー構成に基づいており、以下の強化を追加しています：

- 名前付き値からロードバランサーの構成を読み込みます
- バックエンドを使用して、組み込みのサーキットブレーカ機能との組み合わせを可能にします
- エンドポイントの追加/変更やロードバランサーの構成のためにポリシーを変更する必要がありません
- 任意の数のOpenAIエンドポイントを動的にサポートします

### 前提条件

- [Python 3.8以降のバージョン](https://www.python.org/)がインストールされていること
- [VS Code](https://code.visualstudio.com/)がインストールされ、[Jupyterノートブック拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)が有効になっていること
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)がインストールされていること
- Contributor権限を持つ[Azureサブスクリプション](https://azure.microsoft.com/en-us/free/)があること
- [Azure OpenAIへのアクセス](https://aka.ms/oai/access)が許可されていること、またはモックサービスを有効にすること
- [Azure CLIでAzureにサインイン](https://learn.microsoft.com/en-us/cli/azure/authenticate-azure-cli-interactively)していること

### 🚀 始めましょう

[Jupyterノートブック](advanced-load-balancing.ipynb)を開き、提供された手順に従って進めてください。

### 🗑️ リソースのクリーンアップ

ラボが終了したら、追加の料金を避け、Azureサブスクリプションを整理するために、デプロイしたすべてのリソースをAzureから削除する必要があります。
そのためには、[リソースのクリーンアップノートブック](clean-up-resources.ipynb)を使用してください。