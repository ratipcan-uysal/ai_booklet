# AI Engineering: Concepts That Matter

Türkçe LaTeX kitap, 170x240 mm. Git deposu değil. Hedef okur teknik PM;
derinlik korunur, basitleştirme yok. Tüm metin Türkçe, terimler (`fallback`, `retry`) İngilizce kalır.

## Dosyalar
- `book.tex`: iskelet; Part'lar ve `\input{concepts/X.tex}` sırası burada. `aibook.sty`: tüm renk, font, makro, kutu.
- `concepts/`: bir kavram/kart = bir dosya. Tier 1 doğrudan adıyla (`rag.tex`), Tier 2 `t2-` önekiyle.
- `PLAN.md`: kavram envanteri ve sayfa bütçesi. `IMPROVEMENTS.md`: bitmiş iyileştirme planı (açık: Eval derinliği, somut artefaktlar).
- `book.pdf` üretilen çıktıdır, elle düzenleme.

## Derleme
`tectonic book.tex` (XeLaTeX, TeX Gyre fontları). TOC ve header ilk geçişte oturur; tectonic tekrarı kendi yapar.
Sayfa sayısı: `pdfinfo book.pdf | grep Pages`. Derleme ağır; makine yüklüyse önce `uptime`'a bak.

## Görsel kontrol
Kök dizine PNG bırakma (köktekiler eski kontrollerin artığı, sorulmadan silme).
```
mkdir -p /tmp/aibook-render && pdftoppm -png -r 80 -f 51 -l 53 book.pdf /tmp/aibook-render/p
```
Diyagram/etiket sıkışıklığı için `-r 150` ve tek sayfa. Bakıp bitince `rm -rf /tmp/aibook-render`.
Değişen sayfayı ve ondan sonrakileri bak: içerik eklemek tüm pagination'ı kaydırır.

## Yeni içerik ekleme
1. `concepts/<ad>.tex` aç; başlık yorumu + `\concept{Kategori · Türkçe}{Başlık}{tek satır vaat}` (Tier 1) ya da `\card{Başlık}{alt}` (Tier 2).
2. `book.tex`'te doğru Part/alt başlık altına `\input{concepts/<ad>.tex}   % ✅ ...` satırı ekle.
3. Tier 1 `\concept` yeni sayfa açar; Tier 2 `\card` akışta devam eder (clearpage yok), TOC'a kendisi girer.
4. Kavram bir terim içeriyorsa `glossary.tex`'e `\gloss{Terim}{tanım}` ekle.
5. Son adım: **`index.tex` sayfa numaraları elle yazılı** (`\ix{Agent}{51}`). Sayfa kayınca hepsi bayatlar; içerik donunca TOC'tan
   yeniden çek. Yeni kavramı da buraya ekle (`\ix`, eşanlamlı için `\ixsee`).

## Makrolar ve ortamlar (sty dışında stil uydurma)
- Tier 1 (13 aşama): her biri `\stage{N}{Ad}`; sıra Problem, Neden Var, Tarihçe, Tanım, Zihinsel Model, Mimari Diyagram, Karar Çerçevesi,
  Üretim Senaryosu, Anti-pattern, Alternatifler & Ödünleşimler, İlişkili Kavramlar, Özet, Mühendislik İlkesi (örnek: `rag.tex`).
- Tier 2: `\cl{Problem}`, `\cl{Tanım}`, `\cl{Model}`... run-in etiketler; kalıp `t2-data.tex`.
- Kutular: `problembox`, `mentalbox[başlık]`, `antibox[başlık]`, `principlebox` (bölüm sonu ilke), `prodbox[başlık]`, `artifact[başlık]` (mono kod/şema).
- Satır içi: `\term{}` (kavram adı, small caps), `\en{}` (İngilizce terim italik), `\keyline{}`, `\yr{}`/`\tlsep`+`timeline`, `\thd{}` + `tabularx` `L` sütunu.
- Renkler yalnız paletten: `ink accent accentdk softgray hairline wash warmwash warn good`. Yeni HEX tanımlama.
- Diyagram `tikzpicture` ile; sty'de `arrows.meta, positioning, calc, shapes.geometric, fit, backgrounds` yüklü.
- Metinde kısa çizgi `---`, Türkçe tırnak ``...'', `\&` kaçışı unutma.

## Editoryal kurallar (ayrıntı: PLAN.md)
- Katman: Tier 1 derin (13 aşama + 2-3 diyagram, ~5 sayfa), Tier 2 ~1 sayfa (Problem, Tanım, Zihinsel Model, 1 diyagram, Ne zaman, Anti-pattern), Tier 3 glossary 2-3 satır.
- Yeni kavram eklemeden önce PLAN.md envanterine bak; kavram birleştirilir (Function Calling Tool Calling içinde), çoğaltılmaz. Hedef ~120 kavram, ~105-110 sayfa.
- Her kavram bir probleme cevap olarak başlar: "nedir"in yanında "ne zaman kullanılmaz" da yazılır.
- Kitabın 25 mühendislik ilkesi var (`principles.tex`, poster `principles-poster.tex`). Atıf `(İlke \#N)` biçiminde; numarayı değiştirme, atıfları kırar.
- Kitap araç/framework öğretmez, zihinsel model kurar (İlke \#25). Güncel kalması için isimli ürün yerine kategori anlat.
- Redundant olan eklenmez (Master Cheat Sheet ve Build-vs-Buy kartı gerekçeyle atlandı); atlama gerekçesini IMPROVEMENTS.md'ye yaz.
