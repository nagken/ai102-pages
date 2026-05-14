# Azure Architecture Center

> The **[Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/)** is Microsoft's official catalog of reference architectures, design patterns, decision guides, and Well-Architected workload guidance. Browse the full catalog at [learn.microsoft.com/azure/architecture/browse](https://learn.microsoft.com/en-us/azure/architecture/browse/) and filter by product, category, or scenario.

## How to use it for AI-102

1. **Find a reference architecture close to your workload** in the browse catalog.
2. Read the **Well-Architected** review for that scenario.
3. Steal the **Bicep / Terraform** from the linked sample.
4. Adapt the **decision guides** (network, identity, data) to your constraints.

## Top entry points

| Resource | Why it matters for AI-102 |
| --- | --- |
| [Architecture Center home](https://learn.microsoft.com/en-us/azure/architecture/) | Curated landing page; start here. |
| [Browse architectures](https://learn.microsoft.com/en-us/azure/architecture/browse/) | Filterable catalog. Filter on **AI + Machine Learning**, **Azure OpenAI**, **Cognitive Services**. |
| [AI architecture design](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/) | RAG, vision, language, speech, document intelligence patterns. |
| [Cloud design patterns](https://learn.microsoft.com/en-us/azure/architecture/patterns/) | Retry, Circuit Breaker, Throttling, Cache-Aside. |
| [Well-Architected for AI workloads](https://learn.microsoft.com/en-us/azure/well-architected/ai/) | Five pillars applied to AI. |

## Reference architectures most relevant to AI-102

| Architecture | What it shows |
| --- | --- |
| [Baseline OpenAI end-to-end chat reference](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/architecture/baseline-openai-e2e-chat) | Production RAG: AOAI + AI Search + APIM + private endpoints + identity. |
| [Azure OpenAI fine-tuning architecture](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/architecture/azure-openai-fine-tuning) | When to fine-tune, how to land it, evaluation gates. |
| [Image classification with Computer Vision](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/idea/image-classification-with-vision-services) | Image Analysis vs Custom Vision decision. |
| [Knowledge mining for content research](https://learn.microsoft.com/en-us/azure/architecture/solution-ideas/articles/knowledge-mining-business-process-management) | End-to-end pipeline using AI Search + AI services. |
| [Custom document processing](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/architecture/automate-document-processing-azure-form-recognizer) | Document Intelligence with prebuilt + custom models. |
| [Real-time speech transcription](https://learn.microsoft.com/en-us/azure/architecture/solution-ideas/articles/speech-to-text-transcription-pipeline) | Speech service streaming pipeline. |
| [Conversational bot reference](https://learn.microsoft.com/en-us/azure/architecture/example-scenario/ai/conversational-bot) | CLU + Custom Question Answering + orchestration. |

## Decision guides worth bookmarking

- [Choose an AI service](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/choose-ai-services)
- [Choose a chat solution architecture](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/choose-chat-architecture)
- [Designing a RAG solution](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/rag/rag-solution-design-and-evaluation-guide)
- [Choose a data store](https://learn.microsoft.com/en-us/azure/architecture/guide/technology-choices/data-store-decision-tree)

## Patterns you should know for the exam

| Pattern | When to apply |
| --- | --- |
| **Retry / Circuit Breaker** | Calls into AOAI / AI services to absorb transient throttling. |
| **Throttling / Rate Limiting** | Per-tenant quota over a shared model deployment (often via APIM). |
| **Cache-Aside** | Cache embeddings or response payloads. |
| **Sidecar / Ambassador** | Inject Content Safety + telemetry around model calls. |
| **Saga** | Multi-step agent or document-pipeline orchestration with compensations. |
| **Backends for Frontends (BFF)** | UI calls a thin API; API calls AI services with managed identity. |
