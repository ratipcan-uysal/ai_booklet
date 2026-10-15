# AI Engineering Kitabı — İyileştirme Planı

**Hedef kitle:** Teknik Product Manager. Derinlik korunur (basitleştirme yok);
odak: eksiksizlik, kullanılabilirlik, güncellik, cila.

## Uygulama sırası (bağımlılığa göre fazlanmış)

> Not: Alfabetik Index en yüksek öncelikli ama **en sona** yapılır — sayfa no
> referansı verdiği için tüm içerik dondurulmadan yapılamaz.

### FAZ 1 — QA & hızlı düzeltmeler (pagination'ı bozmaz) ✅ TAMAM
- [x] **Diyagram tam-çözünürlük QA** (P0-2): tüm diyagramlar doğrulandı; embedding
      kümesi etiket sıkışıklığı düzeltildi (diğerleri oturum boyu doğrulanmıştı).
- [x] **Reading List'i pratikleştir** (P0-4): pratisyen kaynaklar öne alındı,
      akademik makaleler "bilmen yeter" dönüm noktalarına indirildi.
- [x] **Kategori etiketi denetimi** (P1-7): Prompt → "Interface · Arayüz";
      Agent+Workflow → "Orchestration · Orkestrasyon".

### FAZ 2 — İçerik eklemeleri (pagination değişir) — kısmen tamam
- [x] **Veri & Gizlilik kartı** (P0-3): `t2-data.tex`, Part III sonu. PM soruları +
      data flywheel + residency/GDPR + veri kalitesi.
- [x] **Build-vs-Buy** (P1-5): ayrı kart YAPILMADI (redundant — "Hangi Modeli
      Seçmeli?" açık/self-host + Ekosistem Atlas zaten kapsıyor); Glossary'ye terim eklendi.
- [x] **Künye/kolofon** (P1-9): kapağın arka yüzü; sürüm 1.0 · 2026, hedef okur, güncel-kalma notu.
- [ ] **Eval derinliği** (P2-10): başarı metriği tanımlama, offline/online, A/B.
- [ ] **Somut artefaktlar** (P2-12): capstone gibi RAG/Eval/Guardrails'e örnek.

### FAZ 3 — Pagination'a bağımlı (içerik donunca)
- [~] **Master Cheat Sheet** (P1-6): ATLANDI — redundant (AI Stack posteri + Karar
      Atlası + İlke Posteri + Ekosistem Atlası zaten konsolidasyon sağlıyor).
- [~] **Çapraz-referans sayfa no** (P1-8): ATLANDI — Alfabetik Index navigasyonu çözüyor.
- [x] **Alfabetik Index** (P0-1): `index.tex`, Appendix E. 2 sütun, harf grupları,
      sayfa no'lu (TOC'tan çekildi), Türkçe "bkz." çapraz-referansları.

### FAZ 4 — Final
- [x] **Tutarlılık denetimi** (P2-11): İlke #1–25 referansları doğrulandı (kırık yok);
      kategori etiketleri düzeltildi (Faz 1).
- [x] **Son tam QA** + derleme: 108 sayfa, hatasız.

## Durum — TAMAM
- Başlangıç: 104 sayfa → Final: 108 sayfa, 38 concept dosyası.
- Eklenen: Veri&Gizlilik, Offline/Online Eval kartları; eval artefaktı; künye;
  Build-vs-Buy glossary; **Alfabetik Index**.
- Düzeltilen: embedding diyagram etiketleri; Reading List (pratikleşti); kategori
  etiketleri; artifact kutusu global yapıldı.
- Atlanan (gerekçeli): Master Cheat Sheet, çapraz-ref sayfa no (redundant).
