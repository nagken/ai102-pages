# Hands-On Labs and Sample Repositories

> Curated, executable references for AI-102 topics. All links point to official Microsoft Learn modules, Azure-Samples repositories, or service quickstarts.

## Microsoft Learn - Sandbox-Backed Modules

| Module | What you build |
| --- | --- |
| [Get started with Azure AI services](https://learn.microsoft.com/training/modules/get-started-azure-ai/) | Provision a multi-service resource and call it from code. |
| [Get started with Azure OpenAI Service](https://learn.microsoft.com/training/modules/get-started-openai/) | Deploy a model, run completions and chat in the playground, call from code. |
| [Implement Azure AI Content Safety](https://learn.microsoft.com/training/modules/moderate-content-detect-harm-azure-ai-content-safety/) | Severity scoring, blocklists, prompt shields, groundedness. |
| [Analyze images with Azure AI Vision](https://learn.microsoft.com/training/modules/analyze-images/) | Captions, tags, objects, OCR via Image Analysis. |
| [Develop computer vision solutions with Azure](https://learn.microsoft.com/training/paths/develop-computer-vision-solutions-azure/) | Image Analysis, Custom Vision, Face. |
| [Read text in images and documents with the Computer Vision service](https://learn.microsoft.com/training/modules/read-text-images-documents-with-computer-vision-service/) | Read API for printed and handwritten text. |
| [Develop natural language solutions](https://learn.microsoft.com/training/paths/develop-language-solutions-azure-ai/) | Text analytics, translation, CLU, Custom Question Answering. |
| [Recognize and synthesize speech](https://learn.microsoft.com/training/modules/recognize-synthesize-speech/) | STT, TTS, neural voices, SSML. |
| [Translate speech with the Azure AI Speech service](https://learn.microsoft.com/training/modules/translate-speech-speech-service/) | Real-time speech translation. |
| [Develop solutions with Azure AI Document Intelligence](https://learn.microsoft.com/training/paths/extract-information-from-text-with-azure-ai-services/) | Prebuilt + custom models, layout analysis. |
| [Build a RAG-based generative AI app with Azure AI Foundry](https://learn.microsoft.com/training/modules/build-copilot-ai-studio/) | End-to-end RAG with AI Search and Azure OpenAI. |
| [Implement vector search with Azure AI Search](https://learn.microsoft.com/training/modules/improve-search-results-vector-search/) | Vector index, embeddings, hybrid + semantic ranker. |

## Azure-Samples Reference Repositories

| Repository | Purpose |
| --- | --- |
| [Azure-Samples/azure-search-openai-demo](https://github.com/Azure-Samples/azure-search-openai-demo) | Reference RAG implementation: chat over your own data with AI Search + Azure OpenAI. |
| [Azure-Samples/AI-Gateway](https://github.com/Azure-Samples/AI-Gateway) | API Management as an AI gateway: token limits, semantic caching, multi-region routing. |
| [Azure-Samples/openai](https://github.com/Azure-Samples/openai) | Azure OpenAI samples: chat, embeddings, fine-tuning, function calling, image, audio. |
| [Azure-Samples/cognitive-services-quickstart-code](https://github.com/Azure-Samples/cognitive-services-quickstart-code) | Multi-language quickstarts across Vision, Language, Speech, Document Intelligence. |
| [Azure-Samples/azure-search-vector-samples](https://github.com/Azure-Samples/azure-search-vector-samples) | Vector and hybrid search examples in Python, C#, JavaScript. |
| [Azure-Samples/Content-Safety-Samples](https://github.com/Azure-Samples/Content-Safety-Samples) | Prompt Shields, severity, blocklists, groundedness. |
| [Azure-Samples/azure-ai-vision-sdk](https://github.com/Azure-Samples/azure-ai-vision-sdk) | Vision SDK samples for Image Analysis. |
| [Azure-Samples/cognitive-services-speech-sdk](https://github.com/Azure-Samples/cognitive-services-speech-sdk) | Speech SDK samples across STT, TTS, translation. |
| [Azure-Samples/document-intelligence-code-samples](https://github.com/Azure-Samples/document-intelligence-code-samples) | Document Intelligence samples for prebuilt and custom models. |
| [Azure-Samples/contoso-chat](https://github.com/Azure-Samples/contoso-chat) | RAG retail chat with prompt flow, evaluations, and CI/CD via azd. |

## Service Quickstarts

| Quickstart | Outcome |
| --- | --- |
| [Azure OpenAI quickstart](https://learn.microsoft.com/azure/ai-services/openai/quickstart) | First chat completion call. |
| [AI Search vector quickstart](https://learn.microsoft.com/azure/search/search-get-started-vector) | First vector index and hybrid query. |
| [Document Intelligence quickstart](https://learn.microsoft.com/azure/ai-services/document-intelligence/quickstarts/get-started-sdks-rest-api) | First prebuilt model call. |
| [Speech service quickstart](https://learn.microsoft.com/azure/ai-services/speech-service/get-started-speech-to-text) | First STT call. |
| [Content Safety quickstart](https://learn.microsoft.com/azure/ai-services/content-safety/quickstart-text) | First severity classification call. |

## Azure Developer CLI Templates

| Command | Template |
| --- | --- |
| `azd init -t azure-search-openai-demo` | Full RAG reference architecture, deployable in one command. |
| `azd init -t contoso-chat` | RAG with prompt flow + evaluations + GitHub Actions. |
| `azd init -t azure-ai-content-safety` | Content Safety reference deployment. |

> Tip: `azd template list --source awesome-azd` returns the official template catalog.

## Recommended Practice Path

1. Provision a multi-service Azure AI Services resource and call three services from one key.
2. Deploy `azure-search-openai-demo` and observe the full retrieval+generation flow.
3. Add Content Safety prompt shields and groundedness detection.
4. Replace sample data with your own; tune chunking and analyze evaluator scores.
5. Front the deployment with API Management using the AI-Gateway template.
6. Add managed identity throughout - replace any remaining keys.
