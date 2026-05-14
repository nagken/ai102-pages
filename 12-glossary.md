# Glossary and Acronym Reference

> Authoritative, exam-focused definitions for the terms, acronyms, and product names that appear in AI-102 scenarios.

## Azure AI Services Foundations

| Term | Definition |
| --- | --- |
| **Azure AI Services** | Multi-service umbrella resource that exposes Vision, Language, Speech, Document Intelligence, and Translator behind one endpoint and key. |
| **Single-service resource** | Per-service Azure resource (e.g., Computer Vision, Speech) with isolated billing, region, and SKU. |
| **F0 / S0** | Free and standard pricing tiers. F0 has tight per-second and per-month limits and is single-region. |
| **Endpoint** | The HTTPS URL the SDK or REST client targets; tied to a region. |
| **Subscription key** | Static authentication key; suitable for dev. Production should use Entra ID + managed identity. |

## Generative AI and Azure OpenAI

| Term | Definition |
| --- | --- |
| **Azure OpenAI Service** | Azure-hosted OpenAI models (GPT, embeddings, image, audio) with enterprise networking, identity, and content safety. |
| **Deployment** | A named model instance bound to a region and capacity tier. The deployment name is what client code targets, not the model name. |
| **Model version** | Specific dated release (e.g., `gpt-4o-2024-11-20`). Auto-update can be on or pinned. |
| **PTU** | Provisioned Throughput Unit; reserved capacity for predictable latency. |
| **Token** | Input/output unit; pricing and rate limits are per 1K tokens. |
| **Context window** | Max tokens (input + output) per call. |
| **Function calling / tool use** | Model returns structured calls the host app must execute and feed back. |
| **Fine-tuning** | Training a base model on labeled examples to bake in tone or format. |

## Microsoft Foundry

| Term | Definition |
| --- | --- |
| **Microsoft Foundry** | Unified Azure platform for building, evaluating, and operating AI applications and agents. |
| **Foundry project** | Workload-scoped resource owning model deployments, connections, evaluations, and tracing. |
| **Foundry hub** | Optional shared resource for networking, identity, and connections across projects. |
| **Connection** | Typed credential reference (AOAI, AI Search, Storage, custom REST) used without embedding secrets. |
| **Prompt flow** | Visual/code orchestration of LLM calls, Python tools, and evaluations as a DAG. |

## Retrieval-Augmented Generation

| Term | Definition |
| --- | --- |
| **RAG** | Retrieval-Augmented Generation - retrieve grounding context, inject into prompt, then generate. |
| **Vector search** | Similarity search over embedding vectors. |
| **Hybrid search** | BM25 keyword + vector combined via Reciprocal Rank Fusion (RRF). |
| **Semantic ranker** | Microsoft-trained L2 reranker in Azure AI Search. |
| **Embedding** | Dense vector representation of text or images. |
| **Chunking** | Splitting source documents into retrievable units. |
| **Indexer** | AI Search component that pulls from a data source, runs a skillset, writes to an index. |
| **Skillset** | Ordered cognitive enrichments applied during indexing. |

## Computer Vision

| Term | Definition |
| --- | --- |
| **Image Analysis** | Caption, tags, objects, people, OCR, and dense captions. |
| **OCR (Read API)** | Extracts printed and handwritten text with bounding boxes. |
| **Custom Vision** | Build classification or object detection models from labeled images. |
| **Face API** | Detection, attributes, similarity, identification (governed access for identification). |
| **Spatial Analysis** | Container-deployed people-counting and zone analytics. |
| **Image Embeddings** | Multimodal vectors used in image search and Vision-Language retrieval. |

## Language and Speech

| Term | Definition |
| --- | --- |
| **NER** | Named Entity Recognition. |
| **PII detection** | Personally Identifiable Information detection and redaction. |
| **CLU** | Conversational Azure AI Language CLU (intents and entities for chat). |
| **Custom Question Answering** | Knowledge-base QnA service in Azure AI Language. |
| **STT** | Speech-to-text. |
| **TTS** | Text-to-speech with neural voices. |
| **SSML** | Speech Synthesis Markup Language for fine-grained TTS control. |
| **Custom Speech** | Acoustic and language model adaptation for your domain. |
| **Translator** | Real-time and document translation. |

## Document Intelligence

| Term | Definition |
| --- | --- |
| **Prebuilt model** | Read, layout, invoice, receipt, ID, business card, contract, W-2 - ready to use. |
| **Custom model (template)** | Trained on visually consistent forms; few examples needed. |
| **Custom model (neural)** | Trained on varied layouts; needs more examples. |
| **Composed model** | Merges multiple custom models behind one endpoint. |
| **Add-on capability** | Optional features (formula extraction, font properties, barcode, query fields). |

## Responsible AI

| Term | Definition |
| --- | --- |
| **Azure AI Content Safety** | Severity scoring, blocklists, prompt shields, groundedness, protected material. |
| **Prompt Shields** | Detect direct user jailbreaks and indirect (RAG-document) prompt injection. |
| **Groundedness detection** | Score whether an answer is supported by provided sources. |
| **Severity level** | 0/2/4/6 across hate, sexual, self-harm, violence. |
| **Responsible AI Standard** | Microsoft's accountability, fairness, reliability, transparency, privacy, inclusiveness framework. |

## Identity and Operations

| Term | Definition |
| --- | --- |
| **Managed identity** | Azure-issued service identity; preferred for service-to-service auth. |
| **Entra ID** | Microsoft identity platform issuing tokens. |
| **Private endpoint** | Private-IP NIC in your VNet that fronts an Azure service. |
| **API Management (APIM)** | Azure gateway for token limits, semantic caching, content safety, multi-region routing. |
| **Application Insights** | APM service; telemetry sink for AI workloads and Foundry tracing. |
