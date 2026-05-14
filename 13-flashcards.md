# Flashcards: Active Recall

> Click any card to reveal the answer. Use the **Domain pager bottom-right** to switch between exam areas. ~50 cards across 6 domains.

<section class="fc-section" data-fc-title="Plan & Manage AI Solutions">
<h2>1 - Plan & Manage AI Solutions</h2>

<div class="flashcard-grid">

<div class="flashcard"><div class="fc-q">Multi-service vs single-service Cognitive Services resource?</div><div class="fc-a">Multi-service = one key/endpoint for many services, simpler billing. Single = isolated quota/region/SKU.</div></div>

<div class="flashcard"><div class="fc-q">Authenticate to Azure AI service securely from app?</div><div class="fc-a"><strong>Managed identity</strong> with Microsoft Entra ID auth. Avoid keys in code.</div></div>

<div class="flashcard"><div class="fc-q">Restrict an AI service to private network?</div><div class="fc-a">Private endpoint + disable public network access; private DNS zone <code>privatelink.cognitiveservices.azure.com</code>.</div></div>

<div class="flashcard"><div class="fc-q">Microsoft Responsible AI principles (6)?</div><div class="fc-a">Fairness, Reliability & Safety, Privacy & Security, Inclusiveness, Transparency, Accountability.</div></div>

<div class="flashcard"><div class="fc-q">Customer-managed key (CMK) - when required?</div><div class="fc-a">Compliance (HIPAA, FedRAMP). Set CMK at create time; cannot retrofit on most services.</div></div>

<div class="flashcard"><div class="fc-q">F0 vs S0 tier?</div><div class="fc-a">F0 = free, low quota, dev/test. S0 = standard, paid, prod throughput & SLA.</div></div>

<div class="flashcard"><div class="fc-q">Monitor AI service usage and throttling?</div><div class="fc-a">Azure Monitor metrics (<code>TotalCalls</code>, <code>BlockedCalls</code>, <code>TotalErrors</code>) + diagnostic settings to Log Analytics.</div></div>

<div class="flashcard"><div class="fc-q">Move a Cognitive Services resource to another region?</div><div class="fc-a">Not supported in place - recreate in target region, redeploy, migrate data/training.</div></div>

</div>
</section>

<section class="fc-section" data-fc-title="Generative AI & Foundry">
<h2>2 - Generative AI & Foundry</h2>

<div class="flashcard-grid">

<div class="flashcard"><div class="fc-q">Foundry hub vs project?</div><div class="fc-a">Hub = shared infra (storage, KV, ACR, connections). Project = workspace for agents/flows/evals; inherits hub.</div></div>

<div class="flashcard"><div class="fc-q">RAG vs fine-tuning trade-off?</div><div class="fc-a">RAG = fresh/private data, citations, cheap. Fine-tune = tone/format/narrow domain.</div></div>

<div class="flashcard"><div class="fc-q">PTU vs PaYG deployment?</div><div class="fc-a">PTU = reserved throughput, predictable latency. PaYG = per-token, no commitment, throttled by quota.</div></div>

<div class="flashcard"><div class="fc-q">temperature vs top_p - best practice?</div><div class="fc-a">Vary <strong>one</strong>. Temp 0 for deterministic, ~0.7 for creative chat.</div></div>

<div class="flashcard"><div class="fc-q">Stream tokens to client?</div><div class="fc-a">Set <code>stream=True</code> on chat completion; client reads SSE chunks.</div></div>

<div class="flashcard"><div class="fc-q">Block jailbreaks and indirect prompt injection?</div><div class="fc-a"><strong>Prompt Shields</strong> in Content Safety - user attack + indirect attack detection.</div></div>

<div class="flashcard"><div class="fc-q">Best embeddings model for multilingual RAG?</div><div class="fc-a"><code>text-embedding-3-large</code> or Cohere Embed-Multilingual.</div></div>

<div class="flashcard"><div class="fc-q">Distribute AOAI traffic across regions for HA?</div><div class="fc-a">APIM as AI Gateway with <strong>load-balanced backend pool</strong> + token limits + semantic caching.</div></div>

</div>
</section>

<section class="fc-section" data-fc-title="Computer Vision Solutions">
<h2>3 - Computer Vision Solutions</h2>

<div class="flashcard-grid">

<div class="flashcard"><div class="fc-q">Image Analysis 4.0 features?</div><div class="fc-a">Captions, dense captions, tags, objects, people, smart crops, OCR (Read) - all from Florence.</div></div>

<div class="flashcard"><div class="fc-q">Custom Vision - minimum images per class?</div><div class="fc-a">15 per tag minimum; 50+ recommended. Balanced classes & varied lighting/angle.</div></div>

<div class="flashcard"><div class="fc-q">Object detection vs image classification?</div><div class="fc-a">Classification = label whole image. Object detection = bounding boxes for multiple objects.</div></div>

<div class="flashcard"><div class="fc-q">Face API - Verify vs Identify vs Find Similar?</div><div class="fc-a">Verify (1:1), Identify (1:N PersonGroup), Find Similar (visually similar). Identity ops are Limited Access.</div></div>

<div class="flashcard"><div class="fc-q">Read API best for what?</div><div class="fc-a">Multipage printed + handwritten OCR; async; better than legacy OCR.</div></div>

<div class="flashcard"><div class="fc-q">Spatial analysis service does what?</div><div class="fc-a">Counts/tracks people in video streams (occupancy, distancing). Runs on Edge container.</div></div>

<div class="flashcard"><div class="fc-q">Video Indexer use case?</div><div class="fc-a">Auto-extract speakers, transcripts, faces, topics, sentiment, OCR from video.</div></div>

<div class="flashcard"><div class="fc-q">Run a vision model offline?</div><div class="fc-a">Export Custom Vision model to <strong>ONNX/TensorFlow/CoreML</strong> or deploy as Docker container.</div></div>

</div>
</section>

<section class="fc-section" data-fc-title="NLP & Speech Solutions">
<h2>4 - NLP & Speech Solutions</h2>

<div class="flashcard-grid">

<div class="flashcard"><div class="fc-q">Language service capabilities?</div><div class="fc-a">Sentiment, key phrase, entity recognition (NER, PII), language detection, summarization, CLU, custom NER, custom text classification, QnA.</div></div>

<div class="flashcard"><div class="fc-q">CLU vs Question Answering?</div><div class="fc-a">CLU = intent + entities for command/dialog. QnA = answer from KB of question/answer pairs.</div></div>

<div class="flashcard"><div class="fc-q">Custom NER - how many docs to label?</div><div class="fc-a">~10 minimum per entity; 50+ recommended; balanced & varied.</div></div>

<div class="flashcard"><div class="fc-q">Translator - what's a custom model used for?</div><div class="fc-a">Domain-specific translations (medical/legal/technical) trained via Custom Translator with parallel corpus.</div></div>

<div class="flashcard"><div class="fc-q">Speech-to-text streaming vs batch?</div><div class="fc-a">Streaming = SDK realtime captions. Batch = REST URL submit, async transcription of many files.</div></div>

<div class="flashcard"><div class="fc-q">Custom Speech vs Custom Voice?</div><div class="fc-a">Custom Speech = better STT for jargon/accents. Custom Voice = bespoke synthesized voice (Limited Access).</div></div>

<div class="flashcard"><div class="fc-q">SSML used for what?</div><div class="fc-a">Speech Synthesis Markup Language - control pronunciation, prosody, voice, breaks, emphasis in TTS.</div></div>

<div class="flashcard"><div class="fc-q">Pronunciation Assessment in Speech SDK?</div><div class="fc-a">Scores accuracy/fluency/completeness per phoneme - language learning scenarios.</div></div>

</div>
</section>

<section class="fc-section" data-fc-title="Knowledge Mining & Document Intelligence">
<h2>5 - Knowledge Mining & Document Intelligence</h2>

<div class="flashcard-grid">

<div class="flashcard"><div class="fc-q">Azure AI Search indexer pipeline stages?</div><div class="fc-a">Crack -> enrich (skillset) -> project to index/KB. Trigger on schedule or manual.</div></div>

<div class="flashcard"><div class="fc-q">Knowledge store vs index?</div><div class="fc-a">Index = queryable. Knowledge store = enrichments persisted to blob/table for downstream analytics.</div></div>

<div class="flashcard"><div class="fc-q">Custom skill in skillset?</div><div class="fc-a">WebApi skill calling your function/API; receives JSON, returns enrichments.</div></div>

<div class="flashcard"><div class="fc-q">Document Intelligence prebuilt models?</div><div class="fc-a">Invoice, receipt, ID, W-2/1098/1099, business card, health insurance card, contract, layout, Read, general document.</div></div>

<div class="flashcard"><div class="fc-q">Custom template vs custom neural model?</div><div class="fc-a">Template = same layout, fewer samples. Neural = varying layouts, more flexible, more training.</div></div>

<div class="flashcard"><div class="fc-q">Composed model in DocIntel?</div><div class="fc-a">Combine multiple custom models behind one model ID; routes to best match.</div></div>

<div class="flashcard"><div class="fc-q">Hybrid search in AI Search?</div><div class="fc-a">BM25 keyword + vector, fused with RRF. Add semantic ranker for L2 reranking.</div></div>

<div class="flashcard"><div class="fc-q">Security trim search results per user?</div><div class="fc-a">Add group-id field per doc; query filter <code>search.in()</code> with caller's group claims.</div></div>

</div>
</section>

<section class="fc-section" data-fc-title="Agents & Responsible AI">
<h2>6 - Agents & Responsible AI</h2>

<div class="flashcard-grid">

<div class="flashcard"><div class="fc-q">Foundry Agent Service tools?</div><div class="fc-a">File search, code interpreter, function calling, OpenAPI, Bing grounding, AI Search, Logic Apps, Fabric data agent, connected agents.</div></div>

<div class="flashcard"><div class="fc-q">Agent thread vs run vs message?</div><div class="fc-a">Thread = conversation. Messages = entries. Run = one execution of agent over thread.</div></div>

<div class="flashcard"><div class="fc-q">Ground an agent only in your docs?</div><div class="fc-a">Attach AI Search index + system prompt with refusal rules + groundedness eval.</div></div>

<div class="flashcard"><div class="fc-q">Content Safety categories?</div><div class="fc-a">Hate, sexual, self-harm, violence (severity 0-7) + Prompt Shields + protected material + groundedness.</div></div>

<div class="flashcard"><div class="fc-q">Eval metrics built into Foundry?</div><div class="fc-a">Groundedness, relevance, retrieval, fluency, coherence, similarity + risk (violence/self-harm/sexual/hate, jailbreak, protected material).</div></div>

<div class="flashcard"><div class="fc-q">Trace agent calls end-to-end?</div><div class="fc-a">Enable tracing -> OpenTelemetry -> App Insights. View timelines in Foundry/Azure Monitor.</div></div>

<div class="flashcard"><div class="fc-q">Limited Access services?</div><div class="fc-a">Custom Neural Voice, Face Identify/Verify, Speaker Recognition. Require application + RAI approval.</div></div>

<div class="flashcard"><div class="fc-q">Transparency note vs system message?</div><div class="fc-a">Transparency note = MS doc on intended use/limits. System message = prompt instruction shaping behavior.</div></div>

</div>
</section>