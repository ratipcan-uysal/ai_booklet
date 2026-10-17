# AI Engineering: Concepts That Matter

Production AI sistemleri kurmak, analiz etmek ve doğru teknik kararları
tartışabilmek için **zihinsel modeller**. Teknik product manager, AI/yazılım
mühendisi, solution architect ve technical founder için ~110 sayfalık Türkçe
referans.

> Belirli bir araç veya framework öğretmez; AI sistemlerini *nasıl düşüneceğini*
> öğretir. Araçlar eskir, ilkeler kalır.

## 📥 İndir

En güncel PDF: **[Releases](../../releases/latest)** → `book.pdf`

## İçinde ne var

- **15 derin kavram** (RAG, Embedding, Prompt, Context Engineering, Fine-tuning,
  Tool Calling, MCP, Memory, Reasoning, Agent, Workflow, Eval, Observability,
  Guardrails…) — her biri problem → tanım → zihinsel model → diyagram → karar
  çerçevesi → anti-pattern → mühendislik ilkesi yapısıyla
- **25 Engineering Principle** (+ tek sayfa poster)
- **Karar Atlası** — 10 mimari karar, tek referansta
- **Capstone** — bir destek asistanını sıfırdan tasarlayan uçtan uca vaka
- **Top 30 Anti-pattern** kataloğu
- **Yapı Taşları** tablosu (Tool · Skill · MCP · Agent · Subagent, net ayrımla)
- Ekosistem haritası, Troubleshooting Playbook, Glossary, Timeline, Index

## Kimin için

Teknik derinliği olan; AI ürün kararları veren ya da etkileyen okur.
Basitleştirme yok — "nedir"in yanında "ne zaman kullanılmaz" da var.

## Kaynaktan derleme

```bash
tectonic book.tex
```

XeLaTeX (TeX Gyre fontları). Çıktı: `book.pdf`.

## Yapı

| Dosya | Ne |
|---|---|
| `book.tex` | İskelet: Part'lar ve bölüm sırası |
| `aibook.sty` | Tasarım sistemi (renk, font, makro, kutular) |
| `concepts/` | Bir kavram/kart = bir dosya |
| `PLAN.md` | Kavram envanteri ve sayfa bütçesi |

## Lisans

[CC BY-NC-ND 4.0](LICENSE) — paylaşabilir ve atıfla dağıtabilirsin; ticari
kullanım ve türev yoktur.
© 2026 Ratipcan Uysal
