# APIM ❤️ OpenAI

## [コンテンツフィルタリングラボ](content-filtering.ipynb)

[![flow](../../images/content-filtering.gif)](content-filtering.ipynb)

- [Azure AI Content Safety](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/overview)のテキストモデレーションとプロンプトシールドを試すためのプレイグラウンド。コンテンツフィルタリングソフトウェアは、アプリが規制を遵守したり、ユーザーにとって意図した環境を維持するのに役立ちます。

### 前提条件

- [Python 3.8以降のバージョン](https://www.python.org/)がインストールされていること
- [Pandasライブラリ](https://pandas.pydata.org)がインストールされていること
- [VS Code](https://code.visualstudio.com/)がインストールされ、[Jupyterノートブック拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)が有効になっていること
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)がインストールされていること
- Contributor権限を持つ[Azureサブスクリプション](https://azure.microsoft.com/en-us/free/)があること
- [Azure OpenAIへのアクセス](https://aka.ms/oai/access)が許可されていること、またはモックサービスを有効にすること
- [Azure CLIでAzureにサインイン](https://learn.microsoft.com/en-us/cli/azure/authenticate-azure-cli-interactively)していること

### 🚀 始めましょう

[コンテンツフィルタリングJupyterノートブック](content-filtering.ipynb)または[プロンプトシールドJupyterノートブック](prompt-shielding.ipynb)を開き、提供された手順に従って進めてください。

### 🗑️ リソースのクリーンアップ

ラボが終了したら、追加の料金を避け、Azureサブスクリプションを整理するために、デプロイしたすべてのリソースをAzureから削除する必要があります。
そのためには、[リソースのクリーンアップノートブック](clean-up-resources.ipynb)を使用してください。