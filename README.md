# APIM ❤️ OpenAI - 🧪 [GenAI Gateway機能](https://techcommunity.microsoft.com/t5/azure-integration-services-blog/introducing-genai-gateway-capabilities-in-azure-api-management/ba-p/4146525)のためのラボ [Azure API Management](https://learn.microsoft.com/en-us/azure/api-management/api-management-key-concepts)

[![Open Source Love](https://firstcontributions.github.io/open-source-badges/badges/open-source-v1/open-source.svg)](https://github.com/firstcontributions/open-source-badges)

## 新機能 ✨

➕ [**コンテンツフィルタリング**](labs/content-filtering/content-filtering.ipynb)と[**プロンプトシールド**](labs/content-filtering/prompt-shielding.ipynb)のラボを追加しました。  
➕ OpenAIモデルベースのルーティングを使用した[**モデルルーティング**](labs/model-routing/model-routing.ipynb)ラボを追加しました。  
➕ [Azure AI Studio Prompt Flow](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/prompt-flow)をAzure API Managementと共に試すための[**プロンプトフロー**](labs/prompt-flow/prompt-flow.ipynb)ラボを追加しました。  
➕ [**バックエンドプール負荷分散**](labs/backend-pool-load-balancing/backend-pool-load-balancing.ipynb)ラボに`priority`と`weight`パラメータを追加しました。  
➕ Azure API ManagementでOpenAIストリーミングをテストするための[**ストリーミング**](streaming.ipynb)ツールを追加しました。  
➕ [Azure API Managementトレース機能](https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-api-inspector)を使用してOpenAI APIをデバッグおよびトラブルシューティングするための[**トレース**](tools/tracing.ipynb)ツールを追加しました。  
➕ [**GPT-4o推論**](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb)ラボに画像処理を追加しました。  
➕ Azure Functions上のサンプルAPIを使用した[**関数呼び出し**](labs/function-calling/function-calling.ipynb)ラボを追加しました。

## 目次

1. [🧠 GenAI Gateway](#-genai-gateway)
1. [🧪 ラボ](#-labs)
1. [🚀 はじめに](#-getting-started)
1. [🔨 ツール](#-tools)
1. [🏛️ Well-Architected Framework](#-well-architected-framework)    <!-- markdownlint-disable-line MD051 -->
1. [🎒 ショーケース](#-show-and-tell)
1. [🥇 その他のリソース](#-other-resources)

AIの急速な進歩により、組織が業界の最前線に立ち続けるためには、実験主導のアプローチが求められています。AIがさまざまな分野でゲームチェンジャーとなる中、その完全な潜在能力を活用するためには、迅速なイノベーションの軌道を維持することが重要です。

**AIサービス**は主に**API**を通じてアクセスされるため、**AIサービス**の消費を管理および統制するための堅牢で効率的なAPI管理戦略が不可欠です。

**AIサービス**の拡大と**API**とのシームレスな統合に伴い、API管理の基本原則を拡張する包括的な**AI Gateway**パターンの需要が高まっています。これにより、先進的なユースケースの実験を加速し、この急速に進化する分野でのさらなるイノベーションの道を開くことができます。**AI Gateway**のよく設計された原則は、**インテリジェントアプリ**を本番環境に自信を持って展開するためのフレームワークを提供します。

## 🧠 GenAI Gateway

![AI-Gateway flow](images/ai-gateway.gif)

このリポジトリでは、一連の実験的なラボを通じて**AI Gateway**パターンを探ります。[Azure API Management](https://learn.microsoft.com/en-us/azure/api-management/api-management-key-concepts)の[GenAI Gateway機能](https://techcommunity.microsoft.com/t5/azure-integration-services-blog/introducing-genai-gateway-capabilities-in-azure-api-management/ba-p/4146525)は、これらのラボ内で重要な役割を果たし、AIサービスAPIをセキュリティ、信頼性、パフォーマンス、全体的な運用効率、およびコスト管理と共に処理します。主な焦点は[Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-services/openai/overview)にあり、これは大規模言語モデル（LLM）の標準リファレンスを設定します。ただし、同じ原則と設計パターンは、他のLLMにも適用可能です。

## 🧪 ラボ

AIの分野で特にPythonの支配力が高まっていることを認識し、Jupyterノートブックの強力な実験能力と共に、以下のラボはJupyterノートブックを中心に構成されており、Pythonスクリプト、[Bicep](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview?tabs=bicep)ファイル、および[Azure API Managementポリシー](https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-policies)のステップバイステップの指示が含まれています：

|  |  |
| -- | -- |
|  |  |
| [**🧪 バックエンドプール負荷分散**](labs/backend-pool-load-balancing/backend-pool-load-balancing.ipynb) (組み込み) | [**🧪 高度な負荷分散**](labs/advanced-load-balancing/advanced-load-balancing.ipynb) (カスタム) |
| [![flow](images/backend-pool-load-balancing-small.gif)](labs/backend-pool-load-balancing/backend-pool-load-balancing.ipynb) | [![flow](images/advanced-load-balancing-small.gif)](labs/advanced-load-balancing/advanced-load-balancing.ipynb) |
| Azure API Managementの[バックエンドプール機能](https://learn.microsoft.com/en-us/azure/api-management/backends?tabs=bicep)を使用して、Azure OpenAIエンドポイントまたはモックサーバーのリストに対して負荷分散を試すためのプレイグラウンド。| カスタム[Azure API Managementポリシー](https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-policies)に基づいた高度な負荷分散を試すためのプレイグラウンド。 |
| [🦾 Bicep](labs/backend-pool-load-balancing/main.bicep) ➕ [⚙️ ポリシー](labs/backend-pool-load-balancing/policy.xml) ➕ [🧾 ノートブック](labs/backend-pool-load-balancing/backend-pool-load-balancing.ipynb) 🟰 [💬](../../issues/16 "フィードバックループディスカッション") | [🦾 Bicep](labs/advanced-load-balancing/main.bicep) ➕ [⚙️ ポリシー](labs/advanced-load-balancing/policy.xml) ➕ [🧾 ノートブック](labs/advanced-load-balancing/advanced-load-balancing.ipynb) 🟰 [💬](../../issues/17 "フィードバックループディスカッション") |
|  |  |
|  |  |
| [**🧪 アクセス制御**](labs/access-controlling/access-controlling.ipynb) | [**🧪 トークンレート制限**](labs/token-rate-limiting/token-rate-limiting.ipynb) |
| [![flow](images/access-controlling-small.gif)](labs/access-controlling/access-controlling.ipynb) | [![flow](images/token-rate-limiting-small.gif)](labs/token-rate-limiting/token-rate-limiting.ipynb) |
| 特定のユーザーやクライアントによるOpenAPI APIへのより細かいアクセスを可能にするために、アイデンティティプロバイダーを使用して[OAuth 2.0認証機能](https://learn.microsoft.com/en-us/azure/api-management/api-management-authenticate-authorize-azure-openai#oauth-20-authorization-using-identity-provider)を試すためのプレイグラウンド。  |  [トークンレート制限ポリシー](https://learn.microsoft.com/en-us/azure/api-management/azure-openai-token-limit-policy)を試すためのプレイグラウンド。トークン使用量が超過すると、呼び出し元は429ステータスコードを受け取ります。 |
| [🦾 Bicep](labs/access-controlling/main.bicep) ➕ [⚙️ ポリシー](labs/access-controlling/policy.xml) ➕ [🧾 ノートブック](labs/access-controlling/access-controlling.ipynb) 🟰 [💬](../../issues/25 "フィードバックループディスカッション") | [🦾 Bicep](labs/token-rate-limiting/main.bicep) ➕ [⚙️ ポリシー](labs/token-rate-limiting/policy.xml) ➕ [🧾 ノートブック](labs/token-rate-limiting/token-rate-limiting.ipynb) 🟰 [💬](../../issues/26 "フィードバックループディスカッション") |
|  |  |
|  |  |
| [**🧪 トークンメトリクスの発行**](labs/token-metrics-emitting/token-metrics-emitting.ipynb) | [**🧪 セマンティックキャッシング**](labs/semantic-caching/semantic-caching.ipynb) |
| [![flow](images/token-metrics-emitting-small.gif)](labs/token-metrics-emitting/token-metrics-emitting.ipynb) | [![flow](images/semantic-caching-small.gif)](labs/semantic-caching/semantic-caching.ipynb) |
| [トークンメトリクス発行ポリシー](https://learn.microsoft.com/en-us/azure/api-management/azure-openai-emit-token-metric-policy)を試すためのプレイグラウンド。このポリシーは、Azure OpenAIサービスAPIを通じて大規模言語モデルトークンの消費に関するメトリクスをApplication Insightsに送信します。 | [セマンティックキャッシングポリシー](https://learn.microsoft.com/en-us/azure/api-management/azure-openai-semantic-cache-lookup-policy)を試すためのプレイグラウンド。プロンプトのベクトル近接性を以前のリクエストと比較し、特定の類似度スコアの閾値を使用します。 |
| [🦾 Bicep](labs/token-metrics-emitting/main.bicep) ➕ [⚙️ ポリシー](labs/token-metrics-emitting/policy.xml) ➕ [🧾 ノートブック](labs/token-metrics-emitting/token-metrics-emitting.ipynb) 🟰 [💬](../../issues/28 "フィードバックループディスカッション") | [🦾 Bicep](labs/semantic-caching/main.bicep) ➕ [⚙️ ポリシー](labs/semantic-caching/policy.xml) ➕ [🧾 ノートブック](labs/semantic-caching/semantic-caching.ipynb) 🟰 [💬](../../issues/27 "フィードバックループディスカッション") |
|  |  |
|  |  |
| [**🧪 レスポンスストリーミング**](labs/response-streaming/response-streaming.ipynb) | [**🧪 ベクトル検索**](labs/vector-searching/vector-searching.ipynb) |
| [![flow](images/response-streaming-small.gif)](labs/response-streaming/response-streaming.ipynb) | [![flow](images/vector-searching-small.gif)](labs/vector-searching/vector-searching.ipynb) |
| Azure API ManagementとAzure OpenAIエンドポイントを使用してレスポンスストリーミングを試し、[ストリーミング](https://learn.microsoft.com/en-us/azure/api-management/how-to-server-sent-events#guidelines-for-sse)に関連する利点と欠点を探るためのプレイグラウンド。| Azure AI Search、Azure OpenAI埋め込み、およびAzure OpenAI完了を使用して[検索強化生成（RAG）パターン](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview)を試すためのプレイグラウンド。 |
| [🦾 Bicep](labs/response-streaming/main.bicep) ➕ [⚙️ ポリシー](labs/response-streaming/policy.xml) ➕ [🧾 ノートブック](labs/response-streaming/response-streaming.ipynb) 🟰 [💬](../../issues/18 "フィードバックループディスカッション") | [🦾 Bicep](labs/vector-searching/main.bicep) ➕ [⚙️ ポリシー](labs/vector-searching/policy.xml) ➕ [🧾 ノートブック](labs/vector-searching/vector-searching.ipynb) 🟰 [💬](../../issues/19 "フィードバックループディスカッション") |
|  |  |
|  |  |
| [**🧪 組み込みロギング**](labs/built-in-logging/built-in-logging.ipynb) | [**🧪 SLMセルフホスティング**](labs/slm-self-hosting/slm-self-hosting.ipynb) (phy-3) |
| [![flow](images/built-in-logging-small.gif)](labs/built-in-logging/built-in-logging.ipynb) | [![flow](images/slm-self-hosting-small.gif)](labs/slm-self-hosting/slm-self-hosting.ipynb) |
| [Azure API Managementの組み込みロギング機能](https://learn.microsoft.com/en-us/azure/api-management/observability)を試すためのプレイグラウンド。リクエストをApp Insightsにログして詳細とトークン使用量を追跡します。 | [Azure API Managementセルフホステッドゲートウェイ](https://learn.microsoft.com/en-us/azure/api-management/self-hosted-gateway-overview)を使用して、OpenAI API互換性を持つセルフホステッド[phy-3 Small Language Model (SLM)](https://azure.microsoft.com/en-us/blog/introducing-phi-3-redefining-whats-possible-with-slms/)を試すためのプレイグラウンド。 |
| [🦾 Bicep](labs/built-in-logging/main.bicep) ➕ [⚙️ ポリシー](labs/built-in-logging/policy.xml) ➕ [🧾 ノートブック](labs/built-in-logging/built-in-logging.ipynb) 🟰 [💬](../../issues/20 "フィードバックループディスカッション") | [🦾 Bicep](labs/slm-self-hosting/main.bicep) ➕ [⚙️ ポリシー](labs/slm-self-hosting/policy.xml) ➕ [🧾 ノートブック](labs/slm-self-hosting/slm-self-hosting.ipynb) 🟰 [💬](../../issues/21 "フィードバックループディスカッション") |
|  |  |
|  |  |
| [**🧪 GPT-4o推論**](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb) | [**🧪 メッセージ保存**](labs/message-storing/message-storing.ipynb) |
| [![flow](images/GPT-4o-inferencing-small.gif)](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb)  | [![flow](images/message-storing-small.gif)](labs/message-storing/message-storing.ipynb) |
| 新しいGPT-4oモデルを試すためのプレイグラウンド。GPT-4o（"o"は"omni"の略）は、テキスト、音声、ビデオの入力を組み合わせて処理し、テキスト、音声、画像形式で出力を生成するように設計されています。 | [イベントハブへのログ](https://learn.microsoft.com/en-us/azure/api-management/log-to-eventhub-policy)ポリシーを通じて、メッセージの詳細をCosmos DBに保存するテスト用プレイグラウンド。このポリシーを使用すると、DBに保存するデータ（プロンプト、完了、モデル、リージョン、トークンなど）を簡単に制御できます。 |
| [🦾 Bicep](labs/GPT-4o-inferencing/main.bicep) ➕ [⚙️ ポリシー](labs/GPT-4o-inferencing/policy.xml) ➕ [🧾 ノートブック](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb) 🟰 [💬](../../issues/29 "フィードバックループディスカッション") |# APIM ❤️ OpenAI - 🧪 [GenAI Gateway機能](https://techcommunity.microsoft.com/t5/azure-integration-services-blog/introducing-genai-gateway-capabilities-in-azure-api-management/ba-p/4146525)のためのラボ [Azure API Management](https://learn.microsoft.com/en-us/azure/api-management/api-management-key-concepts)

[![Open Source Love](https://firstcontributions.github.io/open-source-badges/badges/open-source-v1/open-source.svg)](https://github.com/firstcontributions/open-source-badges)

## 新機能 ✨

➕ [**コンテンツフィルタリング**](labs/content-filtering/content-filtering.ipynb)と[**プロンプトシールド**](labs/content-filtering/prompt-shielding.ipynb)のラボを追加しました。  
➕ OpenAIモデルベースのルーティングを使用した[**モデルルーティング**](labs/model-routing/model-routing.ipynb)ラボを追加しました。  
➕ [Azure AI Studio Prompt Flow](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/prompt-flow)をAzure API Managementと共に試すための[**プロンプトフロー**](labs/prompt-flow/prompt-flow.ipynb)ラボを追加しました。  
➕ [**バックエンドプール負荷分散**](labs/backend-pool-load-balancing/backend-pool-load-balancing.ipynb)ラボに`priority`と`weight`パラメータを追加しました。  
➕ Azure API ManagementでOpenAIストリーミングをテストするための[**ストリーミング**](streaming.ipynb)ツールを追加しました。  
➕ [Azure API Managementトレース機能](https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-api-inspector)を使用してOpenAI APIをデバッグおよびトラブルシューティングするための[**トレース**](tools/tracing.ipynb)ツールを追加しました。  
➕ [**GPT-4o推論**](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb)ラボに画像処理を追加しました。  
➕ Azure Functions上のサンプルAPIを使用した[**関数呼び出し**](labs/function-calling/function-calling.ipynb)ラボを追加しました。

## 目次

1. [🧠 GenAI Gateway](#-genai-gateway)
1. [🧪 ラボ](#-labs)
1. [🚀 はじめに](#-getting-started)
1. [🔨 ツール](#-tools)
1. [🏛️ Well-Architected Framework](#-well-architected-framework)    <!-- markdownlint-disable-line MD051 -->
1. [🎒 ショーケース](#-show-and-tell)
1. [🥇 その他のリソース](#-other-resources)

AIの急速な進歩により、組織が業界の最前線に立ち続けるためには、実験主導のアプローチが求められています。AIがさまざまな分野でゲームチェンジャーとなる中、その完全な潜在能力を活用するためには、迅速なイノベーションの軌道を維持することが重要です。

**AIサービス**は主に**API**を通じてアクセスされるため、**AIサービス**の消費を管理および統制するための堅牢で効率的なAPI管理戦略が不可欠です。

**AIサービス**の拡大と**API**とのシームレスな統合に伴い、API管理の基本原則を拡張する包括的な**AI Gateway**パターンの需要が高まっています。これにより、先進的なユースケースの実験を加速し、この急速に進化する分野でのさらなるイノベーションの道を開くことができます。**AI Gateway**のよく設計された原則は、**インテリジェントアプリ**を本番環境に自信を持って展開するためのフレームワークを提供します。

## 🧠 GenAI Gateway

![AI-Gateway flow](images/ai-gateway.gif)

このリポジトリでは、一連の実験的なラボを通じて**AI Gateway**パターンを探ります。[Azure API Management](https://learn.microsoft.com/en-us/azure/api-management/api-management-key-concepts)の[GenAI Gateway機能](https://techcommunity.microsoft.com/t5/azure-integration-services-blog/introducing-genai-gateway-capabilities-in-azure-api-management/ba-p/4146525)は、これらのラボ内で重要な役割を果たし、AIサービスAPIをセキュリティ、信頼性、パフォーマンス、全体的な運用効率、およびコスト管理と共に処理します。主な焦点は[Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-services/openai/overview)にあり、これは大規模言語モデル（LLM）の標準リファレンスを設定します。ただし、同じ原則と設計パターンは、他のLLMにも適用可能です。

## 🧪 ラボ

AIの分野で特にPythonの支配力が高まっていることを認識し、Jupyterノートブックの強力な実験能力と共に、以下のラボはJupyterノートブックを中心に構成されており、Pythonスクリプト、[Bicep](https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/overview?tabs=bicep)ファイル、および[Azure API Managementポリシー](https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-policies)のステップバイステップの指示が含まれています：

|  |  |
| -- | -- |
|  |  |
| [**🧪 バックエンドプール負荷分散**](labs/backend-pool-load-balancing/backend-pool-load-balancing.ipynb) (組み込み) | [**🧪 高度な負荷分散**](labs/advanced-load-balancing/advanced-load-balancing.ipynb) (カスタム) |
| [![flow](images/backend-pool-load-balancing-small.gif)](labs/backend-pool-load-balancing/backend-pool-load-balancing.ipynb) | [![flow](images/advanced-load-balancing-small.gif)](labs/advanced-load-balancing/advanced-load-balancing.ipynb) |
| Azure API Managementの[バックエンドプール機能](https://learn.microsoft.com/en-us/azure/api-management/backends?tabs=bicep)を使用して、Azure OpenAIエンドポイントまたはモックサーバーのリストに対して負荷分散を試すためのプレイグラウンド。| カスタム[Azure API Managementポリシー](https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-policies)に基づいた高度な負荷分散を試すためのプレイグラウンド。 |
| [🦾 Bicep](labs/backend-pool-load-balancing/main.bicep) ➕ [⚙️ ポリシー](labs/backend-pool-load-balancing/policy.xml) ➕ [🧾 ノートブック](labs/backend-pool-load-balancing/backend-pool-load-balancing.ipynb) 🟰 [💬](../../issues/16 "フィードバックループディスカッション") | [🦾 Bicep](labs/advanced-load-balancing/main.bicep) ➕ [⚙️ ポリシー](labs/advanced-load-balancing/policy.xml) ➕ [🧾 ノートブック](labs/advanced-load-balancing/advanced-load-balancing.ipynb) 🟰 [💬](../../issues/17 "フィードバックループディスカッション") |
|  |  |
|  |  |
| [**🧪 アクセス制御**](labs/access-controlling/access-controlling.ipynb) | [**🧪 トークンレート制限**](labs/token-rate-limiting/token-rate-limiting.ipynb) |
| [![flow](images/access-controlling-small.gif)](labs/access-controlling/access-controlling.ipynb) | [![flow](images/token-rate-limiting-small.gif)](labs/token-rate-limiting/token-rate-limiting.ipynb) |
| 特定のユーザーやクライアントによるOpenAPI APIへのより細かいアクセスを可能にするために、アイデンティティプロバイダーを使用して[OAuth 2.0認証機能](https://learn.microsoft.com/en-us/azure/api-management/api-management-authenticate-authorize-azure-openai#oauth-20-authorization-using-identity-provider)を試すためのプレイグラウンド。  |  [トークンレート制限ポリシー](https://learn.microsoft.com/en-us/azure/api-management/azure-openai-token-limit-policy)を試すためのプレイグラウンド。トークン使用量が超過すると、呼び出し元は429ステータスコードを受け取ります。 |
| [🦾 Bicep](labs/access-controlling/main.bicep) ➕ [⚙️ ポリシー](labs/access-controlling/policy.xml) ➕ [🧾 ノートブック](labs/access-controlling/access-controlling.ipynb) 🟰 [💬](../../issues/25 "フィードバックループディスカッション") | [🦾 Bicep](labs/token-rate-limiting/main.bicep) ➕ [⚙️ ポリシー](labs/token-rate-limiting/policy.xml) ➕ [🧾 ノートブック](labs/token-rate-limiting/token-rate-limiting.ipynb) 🟰 [💬](../../issues/26 "フィードバックループディスカッション") |
|  |  |
|  |  |
| [**🧪 トークンメトリクスの発行**](labs/token-metrics-emitting/token-metrics-emitting.ipynb) | [**🧪 セマンティックキャッシング**](labs/semantic-caching/semantic-caching.ipynb) |
| [![flow](images/token-metrics-emitting-small.gif)](labs/token-metrics-emitting/token-metrics-emitting.ipynb) | [![flow](images/semantic-caching-small.gif)](labs/semantic-caching/semantic-caching.ipynb) |
| [トークンメトリクス発行ポリシー](https://learn.microsoft.com/en-us/azure/api-management/azure-openai-emit-token-metric-policy)を試すためのプレイグラウンド。このポリシーは、Azure OpenAIサービスAPIを通じて大規模言語モデルトークンの消費に関するメトリクスをApplication Insightsに送信します。 | [セマンティックキャッシングポリシー](https://learn.microsoft.com/en-us/azure/api-management/azure-openai-semantic-cache-lookup-policy)を試すためのプレイグラウンド。プロンプトのベクトル近接性を以前のリクエストと比較し、特定の類似度スコアの閾値を使用します。 |
| [🦾 Bicep](labs/token-metrics-emitting/main.bicep) ➕ [⚙️ ポリシー](labs/token-metrics-emitting/policy.xml) ➕ [🧾 ノートブック](labs/token-metrics-emitting/token-metrics-emitting.ipynb) 🟰 [💬](../../issues/28 "フィードバックループディスカッション") | [🦾 Bicep](labs/semantic-caching/main.bicep) ➕ [⚙️ ポリシー](labs/semantic-caching/policy.xml) ➕ [🧾 ノートブック](labs/semantic-caching/semantic-caching.ipynb) 🟰 [💬](../../issues/27 "フィードバックループディスカッション") |
|  |  |
|  |  |
| [**🧪 レスポンスストリーミング**](labs/response-streaming/response-streaming.ipynb) | [**🧪 ベクトル検索**](labs/vector-searching/vector-searching.ipynb) |
| [![flow](images/response-streaming-small.gif)](labs/response-streaming/response-streaming.ipynb) | [![flow](images/vector-searching-small.gif)](labs/vector-searching/vector-searching.ipynb) |
| Azure API ManagementとAzure OpenAIエンドポイントを使用してレスポンスストリーミングを試し、[ストリーミング](https://learn.microsoft.com/en-us/azure/api-management/how-to-server-sent-events#guidelines-for-sse)に関連する利点と欠点を探るためのプレイグラウンド。| Azure AI Search、Azure OpenAI埋め込み、およびAzure OpenAI完了を使用して[検索強化生成（RAG）パターン](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview)を試すためのプレイグラウンド。 |
| [🦾 Bicep](labs/response-streaming/main.bicep) ➕ [⚙️ ポリシー](labs/response-streaming/policy.xml) ➕ [🧾 ノートブック](labs/response-streaming/response-streaming.ipynb) 🟰 [💬](../../issues/18 "フィードバックループディスカッション") | [🦾 Bicep](labs/vector-searching/main.bicep) ➕ [⚙️ ポリシー](labs/vector-searching/policy.xml) ➕ [🧾 ノートブック](labs/vector-searching/vector-searching.ipynb) 🟰 [💬](../../issues/19 "フィードバックループディスカッション") |
|  |  |
|  |  |
| [**🧪 組み込みロギング**](labs/built-in-logging/built-in-logging.ipynb) | [**🧪 SLMセルフホスティング**](labs/slm-self-hosting/slm-self-hosting.ipynb) (phy-3) |
| [![flow](images/built-in-logging-small.gif)](labs/built-in-logging/built-in-logging.ipynb) | [![flow](images/slm-self-hosting-small.gif)](labs/slm-self-hosting/slm-self-hosting.ipynb) |
| [Azure API Managementの組み込みロギング機能](https://learn.microsoft.com/en-us/azure/api-management/observability)を試すためのプレイグラウンド。リクエストをApp Insightsにログして詳細とトークン使用量を追跡します。 | [Azure API Managementセルフホステッドゲートウェイ](https://learn.microsoft.com/en-us/azure/api-management/self-hosted-gateway-overview)を使用して、OpenAI API互換性を持つセルフホステッド[phy-3 Small Language Model (SLM)](https://azure.microsoft.com/en-us/blog/introducing-phi-3-redefining-whats-possible-with-slms/)を試すためのプレイグラウンド。 |
| [🦾 Bicep](labs/built-in-logging/main.bicep) ➕ [⚙️ ポリシー](labs/built-in-logging/policy.xml) ➕ [🧾 ノートブック](labs/built-in-logging/built-in-logging.ipynb) 🟰 [💬](../../issues/20 "フィードバックループディスカッション") | [🦾 Bicep](labs/slm-self-hosting/main.bicep) ➕ [⚙️ ポリシー](labs/slm-self-hosting/policy.xml) ➕ [🧾 ノートブック](labs/slm-self-hosting/slm-self-hosting.ipynb) 🟰 [💬](../../issues/21 "フィードバックループディスカッション") |
|  |  |
|  |  |
| [**🧪 GPT-4o推論**](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb) | [**🧪 メッセージ保存**](labs/message-storing/message-storing.ipynb) |
| [![flow](images/GPT-4o-inferencing-small.gif)](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb)  | [![flow](images/message-storing-small.gif)](labs/message-storing/message-storing.ipynb) |
| 新しいGPT-4oモデルを試すためのプレイグラウンド。GPT-4o（"o"は"omni"の略）は、テキスト、音声、ビデオの入力を組み合わせて処理し、テキスト、音声、画像形式で出力を生成するように設計されています。 | [イベントハブへのログ](https://learn.microsoft.com/en-us/azure/api-management/log-to-eventhub-policy)ポリシーを通じて、メッセージの詳細をCosmos DBに保存するテスト用プレイグラウンド。このポリシーを使用すると、DBに保存するデータ（プロンプト、完了、モデル、リージョン、トークンなど）を簡単に制御できます。 |
| [🦾 Bicep](labs/GPT-4o-inferencing/main.bicep) ➕ [⚙️ ポリシー](labs/GPT-4o-inferencing/policy.xml) ➕ [🧾 ノートブック](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb) 🟰 [💬](../../issues/29 "フィードバックループディスカッション") |
| [**🧪 GPT-4o 推論**](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb) | [**🧪 メッセージ保存**](labs/message-storing/message-storing.ipynb) |
| [![フロー](images/GPT-4o-inferencing-small.gif)](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb)  | [![フロー](images/message-storing-small.gif)](labs/message-storing/message-storing.ipynb) |
| 新しいGPT-4oモデルを試すためのプレイグラウンドです。GPT-4o（"o"は"omni"の略）は、テキスト、音声、ビデオの組み合わせを処理し、テキスト、音声、画像形式で出力を生成できます。 | [イベントハブへのログ](https://learn.microsoft.com/ja-jp/azure/api-management/log-to-eventhub-policy)ポリシーを通じてメッセージの詳細をCosmos DBに保存することをテストするプレイグラウンドです。このポリシーにより、DBに保存されるデータ（プロンプト、応答、モデル、リージョン、トークンなど）を制御できます。  |
| [🦾 Bicep](labs/GPT-4o-inferencing/main.bicep) ➕ [⚙️ ポリシー](labs/GPT-4o-inferencing/policy.xml) ➕ [🧾 ノートブック](labs/GPT-4o-inferencing/GPT-4o-inferencing.ipynb) 🟰 [💬](../../issues/29 "フィードバックディスカッション") | [🦾 Bicep](labs/message-storing/main.bicep) ➕ [⚙️ ポリシー](labs/message-storing/policy.xml) ➕ [🧾 ノートブック](labs/message-storing/message-storing.ipynb) 🟰 [💬](../../issues/34 "フィードバックディスカッション") |
|  |  |
|  |  |
| [**🧪 開発者ツール**（WIP）](labs/developer-tooling/developer-tooling.ipynb) | [**🧪 関数呼び出し**](labs/function-calling/function-calling.ipynb) |
| [![フロー](images/developer-tooling-small.gif)](labs/developer-tooling/developer-tooling.ipynb)  | [![フロー](images/function-calling-small.gif)](labs/function-calling/function-calling.ipynb) |
| Azure API Managementで利用可能な開発者ツールを使用して、AIサービスAPIを開発、デバッグ、テスト、および公開するためのプレイグラウンドです。 | Azure Functions APIとAzure API Managementを使用して、OpenAIの[関数呼び出し](https://learn.microsoft.com/ja-jp/azure/ai-services/openai/how-to/function-calling?tabs=non-streaming%2Cpython)機能を試すためのプレイグラウンドです。  |
| [🦾 Bicep](labs/developer-tooling/main.bicep) ➕ [⚙️ ポリシー](labs/developer-tooling/policy.xml) ➕ [🧾 ノートブック](labs/developer-tooling/developer-tooling.ipynb) 🟰 [💬](../../issues/35 "フィードバックディスカッション") | [🦾 Bicep](labs/function-calling/main.bicep) ➕ [⚙️ ポリシー](labs/function-calling/policy.xml) ➕ [🧾 ノートブック](labs/function-calling/function-calling.ipynb) 🟰 [💬](../../issues/36 "フィードバックディスカッション") |
|  |  |
|  |  |
| [**🧪 モデルルーティング**](labs/model-routing/model-routing.ipynb) | [**🧪 プロンプトフロー**](labs/prompt-flow/prompt-flow.ipynb) |
| [![フロー](images/model-routing-small.gif)](labs/model-routing/model-routing.ipynb)  | [![フロー](images/prompt-flow-small.gif)](labs/prompt-flow/prompt-flow.ipynb) |
| Azure OpenAIのモデルとバージョンに基づいてバックエンドへのルーティングを試すためのプレイグラウンドです。 | Azure API Managementで[Azure AI Studioのプロンプトフロー](https://learn.microsoft.com/ja-jp/azure/ai-studio/how-to/prompt-flow)を試すためのプレイグラウンドです。 |
| [🦾 Bicep](labs/model-routing/main.bicep) ➕ [⚙️ ポリシー](labs/model-routing/policy.xml) ➕ [🧾 ノートブック](labs/model-routing/model-routing.ipynb) 🟰 [💬](../../issues/37 "フィードバックディスカッション") | [🦾 Bicep](labs/prompt-flow/main.bicep) ➕ [⚙️ ポリシー](labs/prompt-flow/policy.xml) ➕ [🧾 ノートブック](labs/prompt-flow/prompt-flow.ipynb) 🟰 [💬](../../issues/38 "フィードバックディスカッション") |
|  |  |
|  |  |
| [**🧪 コンテンツフィルタリング**](labs/content-filtering/content-filtering.ipynb) | [**🧪 プロンプトシールド**](labs/content-filtering/prompt-shielding.ipynb) |
| [![フロー](images/content-filtering-small.gif)](labs/content-filtering/content-filtering.ipynb)  | [![フロー](images/content-filtering-small.gif)](labs/content-filtering/prompt-shielding.ipynb) |
| 潜在的に攻撃的、リスキー、または望ましくないコンテンツをフィルタリングするために、Azure API Managementと[Azure AI Content Safety](https://learn.microsoft.com/ja-jp/azure/ai-services/content-safety/overview)を統合することを試すプレイグラウンドです。 | LLMの入力を分析し、ユーザープロンプト攻撃とドキュメント攻撃という2つの一般的な種類の敵対的な入力を検出するAzure AI Content Safetyサービスのプロンプトシールドを試すプレイグラウンドです。 |
| [🦾 Bicep](labs/content-filtering/main.bicep) ➕ [⚙️ ポリシー](labs/content-filtering/content-filtering-policy.xml) ➕ [🧾 ノートブック](labs/content-filtering/content-filtering.ipynb) 🟰 [💬](../../issues/52 "フィードバックディスカッション") | [🦾 Bicep](labs/content-filtering/main.bicep) ➕ [⚙️ ポリシー](labs/content-filtering/prompt-shield-policy.xml) ➕ [🧾 ノートブック](labs/content-filtering/prompt-shielding.ipynb) 🟰 [💬](../../issues/53 "フィードバックディスカッション") |
|  |  |
|  |  |

### 実験のバックログ

* アシスタントの負荷分散
* Logic Apps RAG
* Semantic Kernelプラグイン
* PII処理
* Llama推論

> [!TIP]
> ご経験やご提案、アイデア、ラボのリクエストを共有していただくために、[フィードバックディスカッション](../../discussions/9)をご利用ください。

## 🚀 はじめに

### 前提条件

* [Python 3.8以降のバージョン](https://www.python.org/)をインストール
* [VS Code](https://code.visualstudio.com/)をインストールし、[Jupyterノートブック拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)を有効化
* [Azure CLI](https://learn.microsoft.com/ja-jp/cli/azure/install-azure-cli)をインストール
* コントリビューター権限を持つ[Azureサブスクリプション](https://azure.microsoft.com/ja-jp/free/)
* [Azure OpenAIへのアクセス](https://aka.ms/oai/access)が許可されているか、モックサービスを有効化
* [Azure CLIでAzureにサインイン](https://learn.microsoft.com/ja-jp/cli/azure/authenticate-azure-cli-interactively)

### クイックスタート

1. このリポジトリをクローンし、前提条件をローカルマシンに設定します。もしくは、[GitHub Codespace](https://codespaces.new/Azure-Samples/AI-Gateway/tree/main)を作成し、ブラウザまたはVS Codeで実行します。
2. 利用可能なラボを参照し、ニーズに最も合ったものを選択します。初心者には[バックエンドプール負荷分散](labs/backend-pool-load-balancing/backend-pool-load-balancing.ipynb)をお勧めします。
3. ノートブックを開き、提供された手順を実行します。
4. 要件に合わせて実験を調整します。共同作業に貢献したい場合は、[プルリクエストの提出](CONTRIBUTING.MD)をお願いいたします。

> [!NOTE]
> 🪲 修正や改善が必要な点があれば、遠慮なく新しい[issue](../../issues/new)を作成してください。

## 🔨 ツール

* [AI-Gatewayモックサーバー](tools/mock-server/mock-server.ipynb)は、OpenAI APIの動作とレスポンスを模倣するように設計されており、Azure API Managementとの統合や他のユースケースでのテストと開発に適した効率的なシミュレーション環境を作成します。[app.py](tools/mock-server/app.py)は、特定のユースケースに合わせてモックサーバーをカスタマイズできます。
* [トレース](tools/tracing.ipynb) - トレースを有効にしてOpenAI APIを呼び出し、トレース情報を返します。
* [ストリーミング](streaming.ipynb) - ストリームを有効にしてOpenAI APIを呼び出し、レスポンスをチャンクで返します。

## 🏛️ Well-Architected Framework

[Azure Well-Architected Framework](https://learn.microsoft.com/ja-jp/azure/well-architected/what-is-well-architected-framework)は、ワークロードの品質を向上させるデザインフレームワークです。以下の表は、ラボとWell-Architected Frameworkの柱を対応付け、アーキテクチャの実験を通じて成功への道を示します。

| ラボ  | セキュリティ | 信頼性 | パフォーマンス | 運用 | コスト |
| -------- | -------- |-------- |-------- |-------- |-------- |
| [リクエスト転送](labs/request-forwarding/request-forwarding.ipynb) | [⭐](#🏛️-well-architected-framework "ゼロトラスト、キー不要のアプローチ、マネージドIDとAzure API Managementのセキュリティ機能") | |  |  |  |
| [バックエンドサーキットブレーカ](labs/backend-circuit-breaking/backend-circuit-breaking.ipynb) | [⭐](#🏛️-well-architected-framework "ゼロトラスト、キー不要のアプローチ、マネージドIDとAzure API Managementのセキュリティ機能") | [⭐](#🏛️-well-architected-framework "サーキットブレーカ機能でOpenAIエンドポイントの可用性を制御") |  |  |  |
| [バックエンドプール負荷分散](labs/backend-pool-load-balancing/backend-pool-load-balancing.ipynb)  |[⭐](#🏛️-well-architected-framework "ゼロトラスト、キー不要のアプローチ、マネージドIDとAzure API Managementのセキュリティ機能")|[⭐](#🏛️-well-architected-framework "組み込み機能でリクエストを2つ以上のエンドポイントに分散し、回復力を確保")|[⭐](#🏛️-well-architected-framework "組み込み機能でリクエストを負荷分散し、パフォーマンスを向上")|  |  |
| [高度な負荷分散](labs/advanced-load-balancing/advanced-load-balancing.ipynb) |[⭐](#🏛️-well-architected-framework "ゼロトラスト、キー不要のアプローチ、マネージドIDとAzure API Managementのセキュリティ機能")|[⭐](#🏛️-well-architected-framework "カスタムポリシーでリクエストを2つ以上のエンドポイントに分散し、回復力を確保")|[⭐](#🏛️-well-architected-framework "カスタムポリシーでリクエストを負荷分散し、パフォーマンスを向上")|  |  |
| [レスポンスストリーミング](labs/response-streaming/response-streaming.ipynb)  |[⭐](#🏛️-well-architected-framework "ゼロトラスト、キー不要のアプローチ、マネージドIDとAzure API Managementのセキュリティ機能")| |[⭐](#🏛️-well-architected-framework "生成される際に完了を'ストリーム'することで、応答を早く得ることが可能")|  |  |
| [ベクトル検索](labs/vector-searching/vector-searching.ipynb) |[⭐](#🏛️-well-architected-framework "ゼロトラスト、キー不要のアプローチ、マネージドIDとAzure API Managementのセキュリティ機能")|[⭐](#🏛️-well-architected-framework "組み込み機能でリクエストを2つ以上のエンドポイントに分散し、回復力を確保")| [⭐](#🏛️-well-architected-framework "組み込み機能でリクエストを負荷分散し、パフォーマンスを向上")| |  |
| [組み込みロギング](labs/built-in-logging/built-in-logging.ipynb) |[⭐](#🏛️-well-architected-framework "ゼロトラスト、キー不要のアプローチ、マネージドIDとAzure API Managementのセキュリティ機能")|[⭐](#🏛️-well-architected-framework "組み込み機能でリクエストを2つ以上のエンドポイントに分散し、回復力を確保")|[⭐](#🏛️-well-architected-framework "組み込み機能でリクエストを負荷分散し、パフォーマンスを向上")|[⭐](#🏛️-well-architected-framework "リクエストはモニタリング、アラート、自動修復を可能にするために記録されます")|[⭐](#🏛️-well-architected-framework "Azure API Managementのサブスクリプションとトークン消費の関係によりコスト管理が可能")|
| [SLMセルフホスティング](labs/slm-self-hosting/slm-self-hosting.ipynb) |[⭐](#🏛️-well-architected-framework "モデルをセルフホストすることで、ネットワーク制限によりセキュリティ体制を改善できる可能性があります") | | [⭐](#🏛️-well-architected-framework "セルフホストされたモデルへの完全な制御によりパフォーマンスが向上する可能性があります") | | |

> [!TIP]
> [Azure OpenAI Serviceに関するAzure Well-Architected Frameworkの視点](https://learn.microsoft.com/ja-jp/azure/well-architected/service-guides/azure-openai)を参照して、追加のガイダンスを得てください。

## 🎒 ショーケース

> [!TIP]
> [VS Code Reveal拡張機能](https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal)をインストールし、AI-GATEWAY.mdを開いて下部の'slides'をクリックすると、VS Codeを離れることなくAIゲートウェイをプレゼンテーションできます。
> もしくは、[AI-GATEWAY.pptx](https://view.officeapps.live.com/op/view.aspx?src=https%3A%2F%2Fraw.githubusercontent.com%2FAzure-Samples%2FAI-Gateway%2Fmain%2FAI-GATEWAY.pptx&wdOrigin=BROWSELINK)を開いて、従来のPowerPointを体験してください。

## 🥇 その他のリソース

このトピックに関する多数のリファレンスアーキテクチャ、ベストプラクティス、スターターキットが利用可能です。包括的なソリューションやプロジェクトの開始地点が必要な場合は、提供されたリソースを参照してください。リファレンスアーキテクチャに統合できる追加の機能を発見するために、AI-Gatewayラボの活用を提案します。

* [AI Hub Gateway ランディングゾーン](https://github.com/Azure-Samples/ai-hub-gateway-solution-accelerator)
* [GenAI Gateway ガイド](https://aka.ms/genai-gateway)
* [Azure OpenAI + APIM サンプル](https://aka.ms/apim/genai/sample-app)
* [AI+APIの協働：AIワークロードでAPIを使用するメリットとベストプラクティス](https://techcommunity.microsoft.com/t5/apps-on-azure-blog/ai-api-better-together-benefits-amp-best-practices-using-apis/ba-p/4157120)
* [Azure OpenAIリソースを使用したゲートウェイソリューションの設計と実装](https://aka.ms/genai-gateway)
* [API Managementを使用したAzure OpenAIのPTU/TPMの使用 - スケーリングの秘密のソースを使用](https://github.com/Azure/aoai-apim)
* [APIMを使用したAzure OpenAIの管理](https://github.com/microsoft/AzureOpenAI-with-APIM)
* [Azure API Managementを使用して中央機能としてのAzure OpenAIを設定する](https://github.com/Azure/enterprise-azureai)
* [AIアプリ構築入門](https://github.com/Azure/intro-to-intelligent-apps)

> 私たちは、現在知られていない有用なコンテンツがあるかもしれないと考えています。このリストを改善するためのご提案や推奨を心よりお待ちしております。

### 🌐 WW GBB イニシアチブ

![GBB](images/gbb.png)

### 免責事項

> [!IMPORTANT]
> このソフトウェアはデモンストレーション目的で提供されています。いかなる目的にも信頼されることを意図していません。このソフトウェアの作成者は、ソフトウェアまたはその中に含まれる情報、製品、サービス、または関連するグラフィックスに関して、完全性、正確性、信頼性、適合性、または可用性について、明示または黙示のいかなる種類の表明または保証も行いません。そのため、そのような情報に依拠することは、厳密に自己責任で行ってください。