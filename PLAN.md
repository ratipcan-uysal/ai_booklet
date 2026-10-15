# AI Engineering: Concepts That Matter — Kavram Envanteri & Sayfa Bütçesi

> Amaç: 250 kavramı **~120**'ye düşürmek, derinliği en önemli ~35 kavramda
> yoğunlaştırmak, kitabı **~100-110 sayfada** tutmak.

## Katman modeli

| Tier | Muamele | Sayfa/kavram | Adet | Toplam |
|---|---|---|---|---|
| **1 · Derin** | Tam 13-aşama + 2-3 diyagram | ~5 | 10 | ~50 |
| **2 · Standart** | Problem→Tanım→Zihinsel Model→1 diyagram→Ne zaman→Anti-pattern | ~1 | 25 | ~25 |
| **3 · Glossary** | 2-3 satır tanım | satır | ~85 | ~10 |

## Sayfa bütçesi (~105 sayfa)

| Bölüm | Sayfa |
|---|---|
| Ön kısım (kapak, içindekiler, nasıl okunmalı, ilkeler özeti) | 6 |
| PART I — Think Like an AI Engineer | 10 |
| PART II — Building an AI System (Tier 1 + Tier 2 kavramlar) | 45 |
| PART III — Making AI Production Ready | 18 |
| PART IV — Engineering Decisions (decision frameworks) | 6 |
| PART V — Engineering Failures (anti-pattern kataloğu) | 6 |
| PART VI — Modern AI Ecosystem (atlas) | 4 |
| PART VII — AI Engineering Playbook | 5 |
| Appendix (glossary, timeline, reading list, ilke posteri) | 8 |
| **Toplam** | **~108** |

---

## TIER 1 — Derin Kavramlar (tam 13-aşama) — 15 kavram

> Seçim ölçütü: (a) temel, (b) gerçek mimari karar içeriyor, (c) sık yanlış anlaşılıyor.
> Sayfa sınırı yok — kalite önce. Tahmini ~75-90 sayfa.

1. **AI ≠ Traditional Software** ⭐ — olasılıksal düşünmenin zemini *(yazılıyor)*
2. **Prompt & System Prompt** — modeli "programlama" biçimin
3. **Context Engineering** — (Context Window, Token, Compression burada toplanır)
4. **Embedding** — anlamın para birimi
5. **RAG** ✅ *(pilot tamamlandı)*
6. **Fine-tuning** ⭐ — RAG'in tamamlayıcısı; kalıcı davranış/üslup
7. **Tool Calling** — (Function Calling burada toplanır)
8. **MCP** — entegrasyon standardı (güncel + karar yoğun)
9. **Memory** — (Working / Long-term / Episodic / Semantic burada toplanır)
10. **Reasoning** ⭐ — (Chain of Thought / Reflection / Planning)
11. **Agent** — hedef + araç + döngü
12. **Workflow** ⭐ — Agent'ın karşıtı; kontrollü adımlar (Agent-vs-Workflow kararı)
13. **Eval** — production'ın kalbi
14. **Observability** ⭐ — (Tracing / Telemetry / Cost)
15. **Guardrails & Safety** — (Prompt Injection / Jailbreak burada toplanır)

⭐ = bu turda Tier 1'e yükseltilen +5 kavram.

---

## TIER 2 — Standart Kavramlar (~1 sayfa)

**Understanding Users:** Intent · Conversation · Persona
**Context:** Retrieval · Summarization · Prompt Chaining · Context Builder
**Knowledge (RAG'i destekler):** Chunking · Vector Database · Similarity Search · Hybrid Search · Re-ranking
**Actions:** API · Authentication & Authorization · A2A
**Reasoning:** Chain of Thought · Reflection · Planning · Router · Workflow · Subagent · Multi-Agent
**Eval Infra:** Benchmark · Golden Dataset · Judge Model · Rubrics
**Observability:** Tracing · Prompt Versioning · Cost Tracking
**Reliability:** Regression · Continuous Evaluation · Canary · Shadow Testing
**Safety:** PII · Moderation · Sandboxing

---

## TIER 3 — Glossary (2-3 satır)

Token, Fine-tuning, Temperature, Top-p, Sampling, Latency, Throughput, Quantization,
Distillation, Context Window, Hallucination, Grounding, Few-shot, Zero-shot, In-context
Learning, Frequency/Presence Penalty, Logprobs, Tokenizer, Vector, Cosine Similarity,
Index, Recall@k, Precision, Top-k Retrieval, Cross-encoder, Bi-encoder, Sparse/Dense
Retrieval, BM25, Knowledge Graph, Telemetry, Logs, Span, Trace ID, Eval Set, Drift,
Guardrail Policy, Red-teaming, Alignment, RLHF, DPO, LoRA, PEFT, Adapter, Inference,
Serving, Batching, KV-Cache, Streaming, Function Schema, JSON Mode, Structured Output,
Stop Sequence, Idempotency, Rate Limit, Backoff, Circuit Breaker, Fallback Model,
Model Router, Embedding Drift, Reranker, Semantic Cache, Prompt Template, Variable
Injection, Output Parser, Validation, Schema Enforcement, Agent Loop, ReAct, Scratchpad,
Memory Store, Episodic/Semantic Memory, Vector Store, Hybrid Index, Chunk Overlap...
*(tam liste yazım sırasında doldurulacak — hedef ~85)*

---

## Kararlar (senin onayına açık)

- [ ] Tier 1 listesi 10 kavram — promote/demote etmek istediğin var mı?
- [ ] "Reasoning"i derin mi yapalım yoksa CoT/Reflection/Planning ayrı Standart mı? *(şu an: ayrı Standart)*
- [ ] Sayfa hedefi ~105 kabul mü, yoksa daha sıkı ~90 mı isteriz?
