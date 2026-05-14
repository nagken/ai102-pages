# AI-102 - Reference Architectures

> Real architectures from the [Azure Architecture Center](https://learn.microsoft.com/azure/architecture/browse/) that map directly to AI-102 exam topics. Each entry calls out which **skills-measured area** it reinforces.

## Domain 1 - Plan and Manage an Azure AI Solution

| Architecture | Topic it reinforces |
| --- | --- |
| [Baseline Microsoft Foundry chat reference architecture](https://learn.microsoft.com/azure/architecture/ai-ml/architecture/baseline-microsoft-foundry-chat) | Foundry resource + projects, Agent Service, deployments, identity |
| [Baseline Microsoft Foundry chat in an Azure landing zone](https://learn.microsoft.com/azure/architecture/ai-ml/architecture/baseline-microsoft-foundry-landing-zone) | Private endpoints, managed identity, CMK, policy guardrails, hub-spoke |
| [Advanced monitoring for Azure OpenAI through a gateway](https://learn.microsoft.com/azure/architecture/ai-ml/guide/azure-openai-gateway-monitoring) | Tracing, App Insights, token analytics, chargeback via APIM |
| [MLOps technical paper](https://learn.microsoft.com/azure/architecture/ai-ml/guide/mlops-technical-paper) | CI/CD with evaluation gates |

## Domain 2 - Implement Generative AI Solutions

| Architecture | Topic it reinforces |
| --- | --- |
| [Baseline OpenAI end-to-end chat](https://learn.microsoft.com/azure/architecture/ai-ml/architecture/baseline-openai-e2e-chat) | RAG chat on App Service / Container Apps with AI Search + Key Vault |
| [Build language model pipelines with memory](https://learn.microsoft.com/azure/architecture/ai-ml/openai/architecture/openai-language-model-memory) | Conversation state, function calling |
| [AI and ML in multitenant solutions](https://learn.microsoft.com/azure/architecture/guide/multitenant/approaches/ai-and-ml) | Tenant isolation, PTU vs Standard, cost attribution |
| [Extract and analyze call center data](https://learn.microsoft.com/azure/architecture/ai-ml/openai/architecture/call-center-openai-analytics) | Summarization, sentiment, evaluation |

## Domain 3 - Implement Agentic Solutions

| Architecture | Topic it reinforces |
| --- | --- |
| [Baseline Microsoft Foundry chat (Agent Service)](https://learn.microsoft.com/azure/architecture/ai-ml/architecture/baseline-microsoft-foundry-chat) | Tools, memory, tracing, content safety, autonomy via Foundry Agent Service |
| [AI agent orchestration patterns](https://learn.microsoft.com/azure/architecture/ai-ml/guide/ai-agent-design-patterns) | Single vs multi-agent, A2A, MCP tools |
| [Conversational AI customer service](https://learn.microsoft.com/azure/architecture/ai-ml/architecture/conversational-ai) | Voice-in / voice-out agent pattern |

## Domain 4 - Implement Computer Vision Solutions

| Architecture | Topic it reinforces |
| --- | --- |
| [Vision AI solutions with Azure](https://learn.microsoft.com/azure/architecture/ai-ml/architecture/vision-ai-solutions) | Image analysis, OCR, custom vision, video indexer |
| [Image classification on Azure](https://learn.microsoft.com/azure/architecture/ai-ml/architecture/intelligent-apps-image-processing) | Vision pipeline architecture |
| [Visual search](https://learn.microsoft.com/azure/architecture/solution-ideas/articles/visual-search) | Embeddings + vector search for images |

## Domain 5 - Implement NLP and Speech Solutions

| Architecture | Topic it reinforces |
| --- | --- |
| [Speech-to-text transcription pipeline](https://learn.microsoft.com/azure/architecture/ai-ml/architecture/speech-to-text-transcription-pipeline) | STT + custom speech for domain accuracy |
| [Conversational AI customer service](https://learn.microsoft.com/azure/architecture/ai-ml/architecture/conversational-ai) | Bot + Language + Speech composition |
| [Suggest content tags with NLP](https://learn.microsoft.com/azure/architecture/ai-ml/architecture/website-content-tagging-keyphrase) | Entity / key phrase extraction |

## Domain 6 - Implement Knowledge Mining and Document Intelligence

| Architecture | Topic it reinforces |
| --- | --- |
| [Knowledge mining with Azure AI Search](https://learn.microsoft.com/azure/architecture/solution-ideas/articles/ai-search-skillsets) | Skillsets, enrichment, hybrid + semantic search |
| [Knowledge mining business search engine](https://learn.microsoft.com/azure/architecture/solution-ideas/articles/business-process-search-engine) | Custom skills, integrated vectorization |
| [Automate document processing with AI Document Intelligence](https://learn.microsoft.com/azure/architecture/example-scenario/ai/automate-document-processing-azure-form-recognizer) | Document Intelligence -> grounded data |

## How to use this page

1. Pick one architecture per study session.
2. Identify which AI-102 skill area it reinforces.
3. Re-answer the [exam decision reference](07-exam-cheatsheet.md) with that architecture as the worked example.
