# Common Pitfalls and Distractor Patterns

> Mistakes that look right on the exam but lose points. Each entry pairs the wrong choice candidates pick with the correct one and the rule that distinguishes them.

## Service Selection

### Picking single-service when multi-service is the WAF answer

**Pitfall**: Provisioning Computer Vision, Language, and Speech as separate resources for "isolation."

**Reality**: For an app using three or more services, the **multi-service Azure AI Services** resource is the simpler, lower-friction default. Use single-service only when SKUs/regions diverge or billing must be split.

### Custom Vision when Image Analysis already covers the case

**Pitfall**: Training Custom Vision for "detect cars in parking lot" or "extract receipt totals."

**Reality**: **Image Analysis** already detects cars/people/objects. **Document Intelligence** already extracts receipts. Custom Vision is for *domain-specific* classes (your defect taxonomy, your product SKUs).

### Custom Speech when prebuilt voice + SSML solves it

**Pitfall**: Custom Neural Voice for "use a calm voice."

**Reality**: Pick a **prebuilt neural voice** with the right style (e.g., `en-US-JennyNeural` with `style="customerservice"`). Custom Neural Voice requires governance approval and is for unique brand voices.

## Generative AI and Azure OpenAI

### "Just raise temperature" to fix hallucinations

**Pitfall**: Adjusting temperature when answers are wrong.

**Reality**: Hallucination is a *grounding* problem. Add **RAG**, enable **groundedness detection**, or pin retrieval to authoritative sources. Lowering temperature reduces creativity but cannot introduce facts.

### Fine-tune for evolving knowledge

**Pitfall**: Recommending fine-tuning when the source data refreshes weekly.

**Reality**: Fine-tuning bakes data into weights - stale within a release cycle. **RAG** is correct. Fine-tune for tone/format or to shrink prompts at scale.

### API keys instead of managed identity

**Pitfall**: Storing the AOAI key in App Service configuration "for simplicity."

**Reality**: WAF security pillar fails. Production: **managed identity** with the *Cognitive Services OpenAI User* role assignment. Keys are dev-only.

### Confusing model name with deployment name

**Pitfall**: Pointing client SDKs at `gpt-4o`.

**Reality**: Client code uses the **deployment name** chosen at deployment time, not the model name. Same model can have multiple deployments at different SKUs/regions.

## Retrieval and Search

### Semantic ranker as a fix for missing results

**Pitfall**: "Add semantic ranker to improve search relevance."

**Reality**: Semantic ranker reorders the top 50 results from an existing query. It does not change *which* documents are retrieved. Missing exact matches -> use **hybrid search**.

### Confusing semantic ranker with Semantic Kernel

**Pitfall**: Treating *Semantic Kernel* as a search feature.

**Reality**: **Semantic Kernel** is an open-source orchestration SDK. **Semantic ranker** is a paid Azure AI Search feature. Unrelated.

### Over-chunking long structured documents

**Pitfall**: Splitting a 200-page manual into 256-token chunks for "better recall."

**Reality**: Loses cross-section context. Use **parent-child chunking**: index small chunks for retrieval, return the parent section to the model.

## Document Intelligence and Vision

### Prebuilt invoice when inputs are non-standard

**Pitfall**: Trying to force the prebuilt invoice model on receipts that always include a custom loyalty section.

**Reality**: Prebuilt invoice extracts standard fields. For added domain fields, use a **custom neural** model trained on your samples; or compose prebuilt + custom.

### Read API for structured forms

**Pitfall**: OCR'ing an invoice with the Read API and parsing fields with regex.

**Reality**: Document Intelligence returns **fields with confidence**. Use the appropriate prebuilt or custom model - regex over Read output is fragile and loses confidence semantics.

### Confusing Face detection with identification

**Pitfall**: "Use the Face API to identify users from a photo."

**Reality**: **Face identification and verification** require Microsoft-approved Limited Access for governed scenarios. **Detection** (find faces, attributes) is generally available. Many exam scenarios test this distinction.

## Language and Speech

### CLU instead of Custom Question Answering

**Pitfall**: Using CLU when users ask FAQs.

**Reality**: **Custom Question Answering** matches questions to authored Q/A pairs. **CLU** classifies *intents* and extracts entities. Mix via **orchestration workflow** for FAQ + transactional in one bot.

### PII detection vs Content Safety

**Pitfall**: Using Content Safety to redact phone numbers.

**Reality**: **PII detection** (Azure AI Language) is the correct service. Content Safety classifies harmful content categories.

### Real-time transcription for batch files

**Pitfall**: Streaming pre-recorded audio through real-time STT.

**Reality**: For uploaded files, use **Batch Transcription** - async, cost-efficient, per-file SAS URL inputs.

## Responsible AI

### Direct-only prompt shields on RAG

**Pitfall**: Enabling only direct attack detection on a RAG agent.

**Reality**: Direct catches user-typed jailbreaks. **Indirect** catches adversarial instructions smuggled in retrieved documents (the more dangerous case in RAG). Always enable both.

### Blocklist as the only filter

**Pitfall**: Listing forbidden phrases instead of using severity filters.

**Reality**: Blocklists are for **specific known phrases**. Severity filters are the primary line of defense and adapt to paraphrase.

## Operations

### Logging prompts at INFO level

**Pitfall**: Treating prompts and completions like normal app logs.

**Reality**: They can contain PII and prompt-injection payloads. Use **Foundry tracing** (with redaction) or scrub before sending to Application Insights. Configure data residency on the workspace.

### Public endpoint AOAI in production

**Pitfall**: Leaving public network access on for dev convenience.

**Reality**: WAF security pillar fails. Production: **private endpoint** + disable public access + private DNS. Use a separate dev resource if needed.
