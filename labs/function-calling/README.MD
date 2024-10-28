# APIM ❤️ OpenAI

## [関数呼び出しラボ](function-calling.ipynb)

[![flow](../../images/function-calling.gif)](function-callingg.ipynb)

Azure Functions APIとAPIMを使用して、OpenAIの[関数呼び出し](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/function-calling?tabs=non-streaming%2Cpython)機能を試すためのプレイグラウンド。

大まかに言うと、関数を使用する作業は次の3つのステップに分けられます：

1. 関数とユーザーの入力を使用してチャット完了APIを呼び出す
2. モデルの応答を使用してAPIまたは関数を呼び出す
3. 関数からの応答を含めて再度チャット完了APIを呼び出し、最終的な応答を得る

### 結果

![result](result.png)

### 前提条件

- [Python 3.8以降のバージョン](https://www.python.org/)がインストールされていること
- [Pandasライブラリ](https://pandas.pydata.org/)がインストールされていること
- [VS Code](https://code.visualstudio.com/)がインストールされ、[Jupyterノートブック拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)が有効になっていること
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)がインストールされていること
- [Azure Functions Core Tools](https://learn.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=windows%2Cisolated-process%2Cnode-v4%2Cpython-v2%2Chttp-trigger%2Ccontainer-apps&pivots=programming-language-python#install-the-azure-functions-core-tools)がインストールされていること
- Contributor権限を持つ[Azureサブスクリプション](https://azure.microsoft.com/en-us/free/)があること
- [Azure OpenAIへのアクセス](https://aka.ms/oai/access)が許可されていること、またはモックサービスを有効にすること
- [Azure CLIでAzureにサインイン](https://learn.microsoft.com/en-us/cli/azure/authenticate-azure-cli-interactively)していること

### 🚀 始めましょう

[Jupyterノートブック](built-in-logging.ipynb)を開き、提供された手順に従って進めてください。

### 🗑️ リソースのクリーンアップ

ラボが終了したら、追加の料金を避け、Azureサブスクリプションを整理するために、デプロイしたすべてのリソースをAzureから削除する必要があります。
そのためには、[リソースのクリーンアップノートブック](clean-up-resources.ipynb)を使用してください。