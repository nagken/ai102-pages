# AI-102 Concept & Reference Index

> A single index of every concept used in this study guide, with links back to the **official Microsoft Learn documentation** that supports it. Use it to verify facts, dive deeper on any decision, or hand to a teammate who needs the source-of-truth article.
>
> Anchor: [Microsoft Learn AI-102 study guide](https://learn.microsoft.com/credentials/certifications/resources/study-guides/ai-102) - [Exam AI-102 page](https://learn.microsoft.com/credentials/certifications/azure-ai-engineer/) - [Azure AI documentation](https://learn.microsoft.com/azure/ai-services/) - [Microsoft Foundry documentation](https://learn.microsoft.com/azure/ai-foundry/) - [Azure Architecture Center - AI](https://learn.microsoft.com/azure/architecture/ai-ml/).

---

## Skill 1 - Plan and manage an Azure AI solution (~15-20%)

### Foundry, resources, and deployment

| Concept | Microsoft Learn |
|---|---|
| Azure AI services umbrella | [What are Azure AI services](https://learn.microsoft.com/azure/ai-services/what-are-ai-services) |
| Microsoft Foundry overview | [What is Microsoft Foundry](https://learn.microsoft.com/azure/ai-foundry/what-is-azure-ai-foundry) |
| Foundry hubs and projects | [AI resources concepts](https://learn.microsoft.com/azure/ai-foundry/concepts/ai-resources) |
| Multi-service vs single-service AI resource | [Multi-service resource](https://learn.microsoft.com/azure/ai-services/multi-service-resource) |
| Model catalog | [Foundry model catalog](https://learn.microsoft.com/azure/ai-foundry/how-to/model-catalog-overview) |
| Deploy a model | [Deploy Azure OpenAI models](https://learn.microsoft.com/azure/ai-foundry/how-to/deploy-models-openai) |
| Endpoint selection (managed vs serverless vs container) | [Deployment types](https://learn.microsoft.com/azure/ai-foundry/concepts/deployments-overview) |
| Azure AI containers | [Container support](https://learn.microsoft.com/azure/ai-services/cognitive-services-container-support) |
| SDKs and REST | [Foundry SDKs](https://learn.microsoft.com/azure/ai-foundry/how-to/develop/sdk-overview) |

### Security, identity, and networking

| Concept | Microsoft Learn |
|---|---|
| Authentication options | [Authenticate Azure AI services](https://learn.microsoft.com/azure/ai-services/authentication) |
| Microsoft Entra ID and managed identity | [Use managed identity](https://learn.microsoft.com/azure/ai-services/openai/how-to/managed-identity) |
| Azure Key Vault for keys | [Key Vault overview](https://learn.microsoft.com/azure/key-vault/general/overview) |
| Private endpoints / network isolation | [Configure virtual networks](https://learn.microsoft.com/azure/ai-services/cognitive-services-virtual-networks) |
| Customer-managed keys | [CMK for Azure AI services](https://learn.microsoft.com/azure/ai-services/encryption/cognitive-services-encryption-keys-portal) |
| Data privacy and residency | [Data, privacy, security for Azure AI](https://learn.microsoft.com/legal/cognitive-services/openai/data-privacy) |

### Monitoring and operations

| Concept | Microsoft Learn |
|---|---|
| Azure Monitor for AI services | [Monitor Azure AI services](https://learn.microsoft.com/azure/ai-services/diagnostic-logging) |
| Diagnostic logs and metrics | [Diagnostic settings](https://learn.microsoft.com/azure/azure-monitor/essentials/diagnostic-settings) |
| Application Insights for AI apps | [Application Insights](https://learn.microsoft.com/azure/azure-monitor/app/app-insights-overview) |
| Foundry tracing | [Trace your application](https://learn.microsoft.com/azure/ai-foundry/how-to/develop/trace-application) |
| Cost planning and quotas | [Plan and manage costs](https://learn.microsoft.com/azure/ai-services/plan-manage-costs) - [Quotas and limits](https://learn.microsoft.com/azure/ai-services/openai/quotas-limits) |

### Responsible AI

| Concept | Microsoft Learn |
|---|---|
| Responsible AI overview | [Responsible AI](https://learn.microsoft.com/azure/ai-services/responsible-use-of-ai-overview) |
| Microsoft Responsible AI Standard | [Standard documentation](https://learn.microsoft.com/azure/machine-learning/concept-responsible-ai) |
| Transparency notes | [Transparency note for Azure OpenAI](https://learn.microsoft.com/legal/cognitive-services/openai/transparency-note) |
| Azure AI Content Safety | [Content Safety overview](https://learn.microsoft.com/azure/ai-services/content-safety/overview) |
| Prompt Shields and groundedness detection | [Prompt Shields](https://learn.microsoft.com/azure/ai-services/content-safety/concepts/jailbreak-detection) - [Groundedness detection](https://learn.microsoft.com/azure/ai-services/content-safety/concepts/groundedness) |

---

## Skill 2 - Implement generative AI solutions (~15-20%)

| Concept | Microsoft Learn |
|---|---|
| Azure OpenAI in Foundry | [Azure OpenAI overview](https://learn.microsoft.com/azure/ai-foundry/openai/overview) |
| Models reference (GPT, embeddings, image, audio) | [Models](https://learn.microsoft.com/azure/ai-foundry/openai/concepts/models) |
| Chat completions API | [Chat completions](https://learn.microsoft.com/azure/ai-foundry/openai/how-to/chatgpt) |
| Image generation (DALL-E / GPT-Image) | [Image generation](https://learn.microsoft.com/azure/ai-foundry/openai/how-to/dall-e) |
| Embeddings | [Embeddings](https://learn.microsoft.com/azure/ai-foundry/openai/concepts/understand-embeddings) |
| Prompt engineering | [Prompt engineering techniques](https://learn.microsoft.com/azure/ai-foundry/openai/concepts/prompt-engineering) |
| System messages and grounding | [System message guidance](https://learn.microsoft.com/azure/ai-foundry/openai/concepts/system-message) |
| Model parameters (temperature, top_p, max tokens) | [Parameters](https://learn.microsoft.com/azure/ai-foundry/openai/reference) |
| Retrieval-augmented generation (RAG) | [RAG with AI Search](https://learn.microsoft.com/azure/search/retrieval-augmented-generation-overview) |
| Bring-your-own-data with Azure OpenAI | [Use your data](https://learn.microsoft.com/azure/ai-foundry/openai/concepts/use-your-data) |
| Prompt flow | [Prompt flow](https://learn.microsoft.com/azure/ai-foundry/how-to/prompt-flow) |
| Fine-tuning | [Fine-tune a model](https://learn.microsoft.com/azure/ai-foundry/openai/how-to/fine-tuning) |
| Evaluation in Foundry | [Evaluation approach](https://learn.microsoft.com/azure/ai-foundry/concepts/evaluation-approach-gen-ai) |
| Built-in evaluators (groundedness, relevance, etc.) | [Evaluation metrics](https://learn.microsoft.com/azure/ai-foundry/concepts/evaluation-metrics-built-in) |
| Content filtering for Azure OpenAI | [Content filters](https://learn.microsoft.com/azure/ai-foundry/openai/concepts/content-filter) |

---

## Skill 3 - Implement agentic solutions (~10-15%)

| Concept | Microsoft Learn |
|---|---|
| Foundry Agent Service overview | [Agents overview](https://learn.microsoft.com/azure/ai-foundry/agents/overview) |
| Create an agent | [Quickstart: build an agent](https://learn.microsoft.com/azure/ai-foundry/agents/quickstart) |
| Agent tools (file search, code interpreter, function tools, OpenAPI) | [Tools](https://learn.microsoft.com/azure/ai-foundry/agents/how-to/tools/overview) |
| Connected agents and orchestration | [Connected agents](https://learn.microsoft.com/azure/foundry/agents/concepts/workflow) |
| Threads, runs, and messages | [Concepts](https://learn.microsoft.com/azure/ai-foundry/agents/concepts/threads-runs-messages) |
| Microsoft Agent Framework | [Agent Framework overview](https://learn.microsoft.com/agent-framework/overview) |
| Function calling in Azure OpenAI | [Function calling](https://learn.microsoft.com/azure/ai-foundry/openai/how-to/function-calling) |
| Tool use and orchestration patterns | [Patterns for AI agents](https://learn.microsoft.com/azure/architecture/ai-ml/guide/ai-agent-design-patterns) |
| Tracing for agents | [Tracing](https://learn.microsoft.com/azure/ai-foundry/how-to/develop/trace-application) |
| Responsible AI for agents | [RAI for agents](https://learn.microsoft.com/legal/ai-code-of-conduct) |

---

## Skill 4 - Implement computer vision solutions (~15-20%)

| Concept | Microsoft Learn |
|---|---|
| Azure AI Vision overview | [Vision overview](https://learn.microsoft.com/azure/ai-services/computer-vision/overview) |
| Image analysis 4.0 (tags, captions, dense captions, smart crops) | [Image analysis](https://learn.microsoft.com/azure/ai-services/computer-vision/concept-tag-images-40) |
| Read OCR | [Read API](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-ocr) |
| Custom Vision (classification and object detection) | [Custom Vision](https://learn.microsoft.com/azure/ai-services/custom-vision-service/overview) |
| Face service | [Face overview](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-identity) |
| Spatial Analysis | [Spatial Analysis](https://learn.microsoft.com/azure/ai-services/computer-vision/intro-to-spatial-analysis-public-preview) |
| Azure AI Video Indexer | [Video Indexer](https://learn.microsoft.com/azure/azure-video-indexer/video-indexer-overview) |
| Multimodal (GPT-4o vision) | [Vision-enabled chat](https://learn.microsoft.com/azure/ai-foundry/openai/concepts/gpt-with-vision) |
| Vision SDK | [Vision SDK](https://learn.microsoft.com/azure/ai-services/computer-vision/sdk/overview-sdk) |

---

## Skill 5 - Implement NLP and speech solutions (~15-20%)

### Language

| Concept | Microsoft Learn |
|---|---|
| Azure AI Language overview | [Language service](https://learn.microsoft.com/azure/ai-services/language-service/overview) |
| Sentiment analysis and opinion mining | [Sentiment analysis](https://learn.microsoft.com/azure/ai-services/language-service/sentiment-opinion-mining/overview) |
| Key phrase extraction | [Key phrase extraction](https://learn.microsoft.com/azure/ai-services/language-service/key-phrase-extraction/overview) |
| Named entity recognition | [NER](https://learn.microsoft.com/azure/ai-services/language-service/named-entity-recognition/overview) |
| Personally identifiable information detection | [PII detection](https://learn.microsoft.com/azure/ai-services/language-service/personally-identifiable-information/overview) |
| Language detection | [Language detection](https://learn.microsoft.com/azure/ai-services/language-service/language-detection/overview) |
| Text summarization | [Summarization](https://learn.microsoft.com/azure/ai-services/language-service/summarization/overview) |
| Conversational Azure AI Language CLU (CLU) | [CLU](https://learn.microsoft.com/azure/ai-services/language-service/conversational-language-understanding/overview) |
| Custom NER | [Custom NER](https://learn.microsoft.com/azure/ai-services/language-service/custom-named-entity-recognition/overview) |
| Custom text classification | [Custom text classification](https://learn.microsoft.com/azure/ai-services/language-service/custom-text-classification/overview) |
| Custom question answering | [Question answering](https://learn.microsoft.com/azure/ai-services/language-service/question-answering/overview) |
| Migration from LUIS / QnA Maker | [Migrate from LUIS](https://learn.microsoft.com/azure/ai-services/language-service/conversational-language-understanding/how-to/migrate-from-luis) |

### Translator

| Concept | Microsoft Learn |
|---|---|
| Translator overview | [Translator overview](https://learn.microsoft.com/azure/ai-services/translator/translator-overview) |
| Custom Translator | [Custom Translator](https://learn.microsoft.com/azure/ai-services/translator/custom-translator/overview) |
| Document Translation | [Document Translation](https://learn.microsoft.com/azure/ai-services/translator/document-translation/overview) |

### Speech

| Concept | Microsoft Learn |
|---|---|
| Azure AI Speech overview | [Speech service](https://learn.microsoft.com/azure/ai-services/speech-service/overview) |
| Speech to text | [Speech to text](https://learn.microsoft.com/azure/ai-services/speech-service/speech-to-text) |
| Text to speech and SSML | [SSML](https://learn.microsoft.com/azure/ai-services/speech-service/speech-synthesis-markup) |
| Custom Speech | [Custom Speech](https://learn.microsoft.com/azure/ai-services/speech-service/custom-speech-overview) |
| Custom neural voice | [Custom neural voice](https://learn.microsoft.com/azure/ai-services/speech-service/custom-neural-voice) |
| Speech translation | [Speech translation](https://learn.microsoft.com/azure/ai-services/speech-service/speech-translation) |
| Speaker recognition | [Speaker recognition](https://learn.microsoft.com/azure/ai-services/speech-service/speaker-recognition-overview) |

---

## Skill 6 - Knowledge mining and information extraction (~15-20%)

### Azure AI Search

| Concept | Microsoft Learn |
|---|---|
| Azure AI Search overview | [What is AI Search](https://learn.microsoft.com/azure/search/search-what-is-azure-search) |
| Indexes and fields | [Index overview](https://learn.microsoft.com/azure/search/search-what-is-an-index) |
| Indexers and data sources | [Indexer overview](https://learn.microsoft.com/azure/search/search-indexer-overview) |
| Skillsets and AI enrichment | [Cognitive search concepts](https://learn.microsoft.com/azure/search/cognitive-search-concept-intro) |
| Built-in skills | [Built-in skills](https://learn.microsoft.com/azure/search/cognitive-search-predefined-skills) |
| Custom skills | [Custom skills](https://learn.microsoft.com/azure/search/cognitive-search-custom-skill-interface) |
| Knowledge store | [Knowledge store](https://learn.microsoft.com/azure/search/knowledge-store-concept-intro) |
| Query types - full text, filters, scoring | [Query overview](https://learn.microsoft.com/azure/search/search-query-overview) |
| Semantic ranking | [Semantic ranking](https://learn.microsoft.com/azure/search/semantic-search-overview) |
| Vector search and hybrid search | [Vector search](https://learn.microsoft.com/azure/search/vector-search-overview) |
| Suggesters and autocomplete | [Suggesters](https://learn.microsoft.com/azure/search/index-add-suggesters) |
| Synonym maps | [Synonym maps](https://learn.microsoft.com/azure/search/search-synonyms) |

### Document Intelligence and Content Understanding

| Concept | Microsoft Learn |
|---|---|
| Azure AI Document Intelligence overview | [Document Intelligence](https://learn.microsoft.com/azure/ai-services/document-intelligence/overview) |
| Prebuilt models (invoice, receipt, ID, layout, etc.) | [Model overview](https://learn.microsoft.com/azure/ai-services/document-intelligence/concept-model-overview) |
| Custom models | [Custom models](https://learn.microsoft.com/azure/ai-services/document-intelligence/concept-custom) |
| Composed models | [Composed models](https://learn.microsoft.com/azure/ai-services/document-intelligence/concept-composed-models) |
| Azure AI Content Understanding | [Content Understanding](https://learn.microsoft.com/azure/ai-services/content-understanding/overview) |

---

## Cross-cutting frameworks

| Concept | Microsoft Learn |
|---|---|
| Azure Architecture Center - AI/ML | [AI/ML guides](https://learn.microsoft.com/azure/architecture/ai-ml/) |
| Reference architectures for AI | [Browse architectures](https://learn.microsoft.com/azure/architecture/browse/?products=azure-ai) |
| Cloud Adoption Framework - AI scenario | [CAF AI scenario](https://learn.microsoft.com/azure/cloud-adoption-framework/scenarios/ai/) |
| Well-Architected Framework | [WAF overview](https://learn.microsoft.com/azure/well-architected/) |
| Azure pricing calculator | [Pricing calculator](https://azure.microsoft.com/pricing/calculator/) |
| Azure TCO calculator | [TCO calculator](https://azure.microsoft.com/pricing/tco/calculator/) |

---

## Exam logistics

| Resource | Link |
|---|---|
| Exam AI-102 page | [AI-102 exam](https://learn.microsoft.com/credentials/certifications/azure-ai-engineer/) |
| Skills measured | [Study guide](https://learn.microsoft.com/credentials/certifications/resources/study-guides/ai-102) |
| Microsoft Learn AI engineer learning paths | [Browse learning paths](https://learn.microsoft.com/training/browse/?products=azure&roles=ai-engineer) |
| Practice assessment | [AI-102 practice assessment](https://learn.microsoft.com/credentials/certifications/azure-ai-engineer/) |
| Microsoft Certification renewal | [Renew your certification](https://learn.microsoft.com/credentials/certifications/renew-your-microsoft-certification) |

---

 **Back to:** [00-MASTER-INDEX.md](00-MASTER-INDEX.md) - **Decision reference:** [07-exam-cheatsheet.md](07-exam-cheatsheet.md) - **Extras:** [08-extra-ai102-concepts.md](08-extra-ai102-concepts.md)
