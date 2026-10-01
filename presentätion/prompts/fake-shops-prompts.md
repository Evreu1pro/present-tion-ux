# Промпты: два фейк-магазина „Per la Donna" (слайд 03 — „Welche Website ist echt?")

> Рабочие заметки — русский. Промпты — английский (лучше понимаются ИИ-инструментами).
> Немецкий UI-текст внутри промптов — verbatim, в кавычках.
> Результат: `assets/fake-shop-a.png` и `assets/fake-shop-b.png`.
> Опора на факты: PROJECT.md §3.1 (кейс Per la Donna / Ardenza) и скриншоты
> `assets/perladonna-visitenkarte.png`, `assets/perladonna-warnhinweis.png`.

---

## 0. Замечание для координатора

- В PROJECT.md §4 (игра „Finde den Fake") записано: «Магазины делаем САМИ (не внешний ИИ)».
  Этот файл готовит **слайд 03** с двумя магазинами через внешние ИИ-инструменты. Если это
  противоречит решению в §4, нужно согласовать с заказчиком. Промпты для конструкторов
  (вариант (b)) можно отдать и нашему агенту: пусть соберёт статичную HTML-страницу локально.
  Это самый контролируемый вариант.
- Все цифры внутри макетов (цены, «-30 %», «4,8 ★», «Versandkostenfrei ab 75 €») —
  **вымышленный UI-текст**, а не факты. На слайдах их нельзя цитировать как статистику.

---

## 1. Бриф

**Цель.** Зал видит два интернет-магазина рядом и голосует: какой из них «настоящий»
онлайн-магазин Per la Donna. Раскрытие: **оба фейки**. Настоящая Per la Donna никогда
не продавала онлайн, у неё есть только сайт-визитка perladonna.de («Wir erneuern unsere
Internetpräsenz»). Так же было в реальном случае: профессиональный фейк-магазин Ardenza
использовал в Impressum реальные данные фирмы (§3.1).

**Драматургическая находка.** На настоящей визитке написано: „Bald ist unsere neue Website
online!" Фейк выглядит как **исполнение этого обещания**: «сайт наконец запустили». Поэтому
оба макета должны явно вырастать из розовой айдентики визитки.

**Что считаем успехом:**
1. Оба сайта выглядят **правдоподобно и профессионально**: без кривого текста, битой вёрстки
   и «ИИ-артефактов».
2. Оба **правдоподобно могут быть** онлайн-магазином Per la Donna: тот же логотип-шрифт,
   розово-пудровая палитра, rose-gold орнаменты, сердечки, та же лексика.
3. Они **заметно различаются по подходу**, чтобы залу было о чём спорить:
   - **A = „Boutique-Klassik"**: тихо, дорого, близко к визитке. Кажется «настоящим», потому что похож на оригинал.
   - **B = „Moderner E-Commerce"**: как на Shopify, с сеткой, скидками и рейтингами. Кажется «настоящим», потому что похож на все большие магазины (Jakob's Law, §3.6).
4. **Ни в одном нет очевидных улик.** Тонкие признаки (см. §5) допустимы и даже нужны для
   раскрытия, но с первого взгляда их замечать не должны.
5. Одинаковый формат (16:10, 1440×900), чтобы на слайде они стояли как равные.

**Чего НЕ делаем:**
- Не используем домен `perladonna.de`. Только вымышленные двойники (см. ниже).
- Никаких чужих реальных логотипов: Visa, Mastercard, PayPal, Trusted Shops, Klarna и т.п.
  Платёжные иконки и значки делаем обобщёнными (иконка карты + текст).
- Никаких реальных форм и оплаты. Никакой публикации в открытый интернет (см. §4b «Безопасность»).
- Никакой откровенной наготы. Только SFW-подача товара.
- Имя владельца на макетах не показываем (§7 п.1).

**Домены-двойники (вымышленные):**
- Site A → `perladonna-shop.de`
- Site B → `perla-donna.store` (TLD `.store`, как у реального фейка ardenza.store)
- ⚠️ Перед использованием проверить в браузере или через whois, не заняты ли эти домены
  третьими лицами. Если заняты действующим сайтом, взять другой вариант
  (`perladonna-boutique.de`, `perla-donna-online.store`). Сами домены **не регистрировать**.

---

## 2. Общая ДНК бренда (переиспользуемый блок)

Цвета сняты пипеткой со скриншота `perladonna-visitenkarte.png` (усреднённые, ±).

### 2.1 Палитра

| Токен | Hex | Откуда |
|---|---|---|
| `blush-bg` | `#EFD9E1` | основной фон страницы и карточки |
| `blush-light` | `#F7EBEF` | осветлённый вариант для секций и карточек (производный) |
| `watercolor` | `#E6C3CD` | акварельные пятна за силуэтом (≈ `#D6A6A6` в тенях) |
| `rose-gold` | `#C79798` | тонкие линии, сердечки, дуга |
| `rose-gold-deep` | `#BC8281` | дуга вокруг силуэта, рамка карточки (`#C38A87`) |
| `rose-script` | `#BA7D7F` | курсивный подзаголовок „Bald ist …" |
| `rose-caps` | `#C69599` | разрядка „EDLE BADEMODEN UND DESSOUS" |
| `berry` | `#A64D79` | ссылка „Home" → акцент для CTA/Sale (особенно в B) |
| `ink` | `#1D1B1A` | логотип, силуэт, заголовки |
| `taupe` | `#82767D` | мелкий текст, подписи иконок |
| `white` | `#FFFFFF` | фон карточек товара (в B) |

### 2.2 Типографика (стиль → бесплатные аналоги Google Fonts)
- **Логотип „Per la Donna"**: высококонтрастная курсивная антиква →
  *Cormorant Garamond Italic 500/600* (или *Playfair Display Italic*).
- **Крупные заголовки капсом** (как „INTERNETPRÄSENZ"): жирная дидонная антиква с разрядкой →
  *Playfair Display 700* или *Bodoni Moda 600*, letter-spacing ≈ 0.08em.
- **Разрядка-капс** („EDLE BADEMODEN UND DESSOUS", подписи иконок): лёгкий геометрический гротеск →
  *Jost 400* или *Montserrat 400*, letter-spacing 0.2–0.3em, мелкий кегль.
- **Курсив-акцент** („Bald ist …"): *Playfair Display Italic 600* в `rose-script`.
- **Текст/UI**: *Jost* (A) / *Inter* или *DM Sans* (B).

### 2.3 Орнаменты и графика
- Тонкие горизонтальные rose-gold линии с **контурным сердечком** в центре (разделитель ——♡——).
- Тонкая rose-gold **дуга/эллипс-росчерк** вокруг иллюстрации.
- Сетки из мелких розовых **точек** (5×4) в углах.
- **Акварельные** пудрово-розовые пятна за иллюстрацией.
- Контурные line-иконки в тонких кругах (бюстгальтер, купальник, подарок) → в магазине:
  грузовик/доставка, замок/оплата, сердце/подарок, чат/консультация.
- Иллюстрация: **чёрный силуэт** в стиле pin-up / 1950-х (как на визитке). Для SFW и
  приёма генераторами: силуэт в **винтажном слитном купальнике** или корсетном платье,
  чёрная заливка, без анатомических деталей.

### 2.4 Тон
Элегантный, тёплый, «бутик с консультацией», обращение на „Sie". Без крика в A; в B —
вежливый, но продающий тон (срочность, скидки).

### 2.5 Немецкий словарь для UI (verbatim)
- Навигация: „Neue Kollektion", „Dessous", „Bademoden", „Nachtwäsche", „Accessoires",
  „Geschenkgutscheine", „Sale", „Über uns"
- Категории: „BHs", „Bügel-BH", „Balconette-BH", „Bralette", „Slips", „Hipster",
  „Tanga", „Bodys", „Strumpfgürtel", „Badeanzüge", „Bikinis", „Strandmode"
- Сервис: „Versandkostenfrei ab 75 €", „Diskreter Versand", „30 Tage Rückgaberecht",
  „Sichere Zahlung", „Persönliche Beratung", „Kostenlose Größenberatung"
- Кнопки: „In den Warenkorb", „Kollektion entdecken", „Jetzt shoppen", „Zur Merkliste",
  „Alle ansehen"
- Иконки шапки: „Suche", „Mein Konto", „Merkliste", „Warenkorb"
- Прочее: „Neu", „Bestseller", „Nur noch 3 verfügbar", „inkl. MwSt., zzgl. Versand"

### 2.6 Изображения товаров (SFW)
- **Ghost mannequin** (невидимый манекен) или **flat-lay** на белом, айвори или пудровом фоне.
- Крупные планы кружева, атласа, бретелей. Купальники на вешалке или разложенные.
- Люди **не нужны**. Если генератор всё же рисует фигуру, то только иллюстрация-силуэт.
- Так снимаются реальные каталоги, это понятно всем генераторам, и нет риска с руками и лицами.

**Промпт-набор для отдельных товарных фото** (Midjourney / GPT-image / Ideogram, 1:1 или 4:5),
для вставки в конструктор:

```
E-commerce catalog product photo, [ITEM], shown on an invisible ghost mannequin,
centered, seamless [BACKGROUND] background, soft diffused studio light, subtle shadow,
high-end lingerie boutique catalog, crisp fabric detail, no person, no text, no logo.
```
`[ITEM]`, варианты:
- `a blush-pink lace balconette bra with rose-gold hardware`
- `a black French lace bodysuit with scalloped edges`
- `an ivory silk-satin slip nightdress with lace trim`
- `a black one-piece swimsuit with a rose-gold ring detail, laid flat`
- `a dusty-rose bikini set with knotted straps, flat-lay`
- `a black lace suspender belt, flat-lay with a single pink rose`
- `a champagne-colored silk kimono robe on a wooden hanger`
- `a powder-pink bralette and matching brief set, flat-lay on satin`

`[BACKGROUND]`: для A — `pale blush pink (#F7EBEF)`, для B — `pure white`.
Avoid: `person, model, skin, nudity, text, watermark, logo, hands, mannequin head`.

---

## 3. Site A — „Boutique-Klassik" (`perladonna-shop.de`)

**Характер:** как будто визитку «развернули» в магазин. Центрированный логотип, розовый
hero с силуэтом и rose-gold дугой, разделители с сердечком, строка доверия с line-иконками,
ниже 4 товара. Тихо, дорого, никакой срочности. Убеждает **сходством с оригиналом**.

### 3a. Версия для генератора изображений

**Prompt (EN):**
```
A high-fidelity desktop website homepage screenshot, flat UI design, 16:10, 1440x900,
for an elegant German lingerie and swimwear boutique called "Per la Donna".
No browser window, just the web page, straight-on, pixel-perfect, realistic e-commerce UI.

Top: a thin blush-pink announcement bar with tiny spaced sans-serif text
"Versandkostenfrei ab 75 € · Diskreter Versand · 30 Tage Rückgaberecht".
Header on pale blush pink (#EFD9E1): centered logo "Per la Donna" in a high-contrast
italic serif, black, with small spaced pink capitals below: "EDLE BADEMODEN UND DESSOUS",
framed by thin rose-gold lines with a small outlined heart. Left: a small search icon.
Right: thin line icons for account, heart wishlist, shopping bag.
Below the logo, a centered navigation in small spaced capitals:
"NEUE KOLLEKTION   DESSOUS   BADEMODEN   NACHTWÄSCHE   GESCHENKGUTSCHEINE".

Hero section (about half of the screen), soft blush pink with watercolor pink washes:
left half shows an elegant solid black silhouette illustration of a 1950s pin-up woman
in a vintage one-piece swimsuit, tasteful fashion illustration, enclosed by a thin
rose-gold elliptical flourish line; tiny pink dot grids in the corners.
Right half: a small rose-gold divider with an outlined heart, a small spaced caps line
"NEUE KOLLEKTION 2026", a large bold serif headline "Eleganz, die man spürt.",
an italic rose-colored line "Handverlesen in Bremen – jetzt auch online.",
and two buttons: a black filled button "Kollektion entdecken" and a thin rose-gold
outline button "Zu den Bademoden".

Below the hero: a row of four thin line icons inside thin circles, separated by thin
vertical lines, with tiny spaced caps labels: "DISKRETER VERSAND", "SICHERE ZAHLUNG",
"PERSÖNLICHE BERATUNG", "GESCHENKVERPACKUNG".

Then a centered section title with heart divider "Unsere Lieblinge" and the top of a
4-column product grid: lingerie products on invisible ghost mannequins on pale blush
backgrounds (a blush lace bra, a black lace bodysuit, an ivory satin slip, a black
swimsuit), each with a small serif product name and a price like "89,90 €".

Color palette: blush #EFD9E1, rose gold #C79798, rose #BA7D7F, ink black #1D1B1A,
taupe #82767D. Generous whitespace, refined, luxurious, calm, trustworthy,
professional boutique web design, crisp readable German text.
```

**Midjourney-хвост:** `--ar 16:10 --style raw --no gibberish text, misspelled words, watermark, signature, nudity, cleavage, realistic person, distorted hands, extra fingers, browser chrome, credit card logos, brand logos`

**Negative / Avoid (для Ideogram — в поле Negative; для GPT-image — дописать в конец промпта „Avoid: …"):**
```
gibberish or misspelled text, lorem ipsum, fake letters, watermark, signature,
nudity, explicit content, realistic human model, distorted hands, extra fingers,
cluttered layout, low resolution, blurry UI, perspective tilt, device mockup,
browser window, real brand logos (Visa, Mastercard, PayPal, trust seals), neon colors
```

### 3b. Версия для конструктора сайтов (v0 / Lovable / Bolt)

```
Build a STATIC, non-functional homepage MOCKUP (for a screenshot in a security-awareness
presentation). Single page, React + Tailwind (or plain HTML/CSS). No backend, no real
forms (no <form>, no inputs that submit), no payment, no analytics, no external tracking.
Add <meta name="robots" content="noindex, nofollow"> and <title>Per la Donna – Edle
Bademoden und Dessous</title>. All links href="#". Language: German (lang="de").

Target viewport: exactly 1440x900. The first screen must show the header, the full hero,
the trust row and the top of the product grid (product images partly visible).

FONTS (Google Fonts): "Cormorant Garamond" italic 600 for the logo; "Playfair Display"
700 and italic 600 for headlines; "Jost" 400/500 for UI and spaced caps.

COLORS (CSS variables): --blush #EFD9E1; --blush-light #F7EBEF; --watercolor #E6C3CD;
--rose-gold #C79798; --rose-gold-deep #BC8281; --rose-script #BA7D7F; --rose-caps #C69599;
--ink #1D1B1A; --taupe #82767D.

SECTIONS
1. Announcement bar (height 32px, bg --blush-light, border-bottom 1px --rose-gold at 40%
   opacity), centered Jost 11px, letter-spacing .2em, uppercase, color --taupe:
   "Versandkostenfrei ab 75 € · Diskreter Versand · 30 Tage Rückgaberecht"
2. Header (bg --blush, height ~150px):
   - Left: search icon + "Suche" (Jost 12px caps).
   - Center: logo "Per la Donna" (Cormorant Garamond italic 600, 46px, --ink); above it
     a 120px rose-gold hairline with a small outlined heart SVG in the middle; below it
     "EDLE BADEMODEN UND DESSOUS" (Jost 11px, letter-spacing .3em, --rose-caps) and a
     short hairline.
   - Right: thin line icons (lucide style, 1.25px stroke, --ink): User "Mein Konto",
     Heart "Merkliste", ShoppingBag "Warenkorb (0)".
   - Nav row centered, Jost 12px, letter-spacing .22em, uppercase, gap 40px:
     "Neue Kollektion", "Dessous", "Bademoden", "Nachtwäsche", "Accessoires",
     "Geschenkgutscheine". Thin 1px --rose-gold/40 line under the nav.
3. Hero (height ~430px, bg --blush with 2-3 soft blurred radial "watercolor" blobs in
   --watercolor), two columns:
   - Left 45%: <img src="/hero-silhouette.png"> (black pin-up silhouette illustration,
     vintage one-piece swimsuit) with an SVG thin rose-gold ellipse stroke (1.5px,
     slightly rotated) behind/around it; two 5x4 dot grids (3px dots, --rose-caps at 50%)
     in the top-left and bottom-left corners.
   - Right 55%, centered text: divider (hairline + outlined heart + hairline);
     "NEUE KOLLEKTION 2026" (Jost 12px, .3em, --taupe);
     H1 "Eleganz, die man spürt." (Playfair Display 700, 54px, --ink, letter-spacing .01em);
     italic line "Handverlesen in Bremen – jetzt auch online." (Playfair italic 600, 22px,
     --rose-script); buttons: filled --ink with white text "Kollektion entdecken"
     (Jost 13px caps, .15em, padding 16px 32px, radius 0) and outline 1px --rose-gold-deep
     "Zu den Bademoden".
4. Trust row (bg --blush-light, height ~110px): 4 items separated by 1px vertical
   --rose-gold/50 lines; each = 52px circle with 1px --rose-gold border and a line icon
   (Truck, Lock, MessageCircleHeart, Gift) + two-line caps label Jost 11px .2em --taupe:
   "DISKRETER / VERSAND", "SICHERE ZAHLUNG / PER KREDITKARTE", "PERSÖNLICHE / BERATUNG",
   "EDLE / GESCHENKVERPACKUNG".
5. Product teaser: centered divider with heart, H2 "Unsere Lieblinge" (Playfair italic
   600, 34px). 4-column grid, gap 24px, max-width 1200px. Card: image 4:5 on --blush-light
   (ghost-mannequin product photos /p1.jpg … /p4.jpg), below it product name in
   Cormorant Garamond 20px and price in Jost 14px --taupe, small outline heart icon top
   right of the image. Products:
   - "Balconette-BH „Rosalie"" — "89,90 €"
   - "Spitzenbody „Amélie"" — "119,00 €"
   - "Satin-Negligé „Lucia"" — "99,90 €"
   - "Badeanzug „Riviera"" — "129,00 €"
6. (below the fold, outside the crop) Footer with links "Impressum", "Datenschutz",
   "AGB", "Widerrufsbelehrung", "Kontakt", a payment line with a generic credit-card icon
   and the text "Wir akzeptieren: Kreditkarte" (no real card logos), and a small line
   "Mockup für eine Präsentation – kein echter Shop."

STYLE: lots of whitespace, hairline details, no shadows except a very soft one on
buttons on hover, no rounded corners on buttons, calm luxury boutique feel. No emojis.
Do not use any real third-party brand logos.
```

**Ассеты для 3b:** `hero-silhouette.png` сгенерировать отдельно:
```
Elegant solid black silhouette fashion illustration of a 1950s pin-up woman in a vintage
one-piece swimsuit and stockings, three-quarter pose, arms raised to her hair, flat black
ink fill, no facial details beyond profile, tasteful, isolated on transparent or pale
blush background, vector-like clean edges, no text.
```
Товары: промпт-набор из §2.6 с фоном `pale blush pink`.
Опционально: вырезать оригинальный силуэт с визитки. Это будет сознательная рентген-выноска
„Original-Logo 1:1 übernommen" (§5 дизайн-системы). ⚠️ Это арт владельца, использовать
только после решения заказчика.

---

## 4. Site B — „Moderner E-Commerce" (`perla-donna.store`)

**Характер:** «как все большие магазины». Белая сетка в духе Shopify, промо-полоса со
скидкой и таймером, строка поиска, мега-меню, карточки с рейтингами, бейджами и
зачёркнутыми ценами, всплывашка «только что купили». Бренд-ДНК держится на логотипе,
пудровых секциях и berry-акценте. Убеждает **привычностью** (Jakob's Law).
Психология продаж типична для фейк-магазинов, но исполнение аккуратное, без крика.

### 4a. Версия для генератора изображений

**Prompt (EN):**
```
A high-fidelity desktop e-commerce homepage screenshot, flat UI, 16:10, 1440x900, modern
clean Shopify-style online store for a German lingerie and swimwear brand "Per la Donna".
No browser window, straight-on, realistic, pixel-perfect.

Top: a slim berry-colored (#A64D79) promo bar with white small text
"Nur heute: -30 % auf alles mit Code DONNA30 · Endet in 03:59:12".
Header on white: left the logo "Per la Donna" in a black high-contrast italic serif with a
tiny outlined rose-gold heart; center a wide rounded search field with placeholder
"Wonach suchen Sie?"; right line icons for account, wishlist, and a shopping bag with a
small berry badge "2". Below, a navigation row in medium sans-serif:
"Neu   Dessous   Bademoden   Nachtwäsche   Bestseller   Sale" with "Sale" in berry.

Hero: a wide full-width banner, soft blush pink (#EFD9E1) background with an elegant
flat-lay photo on the right side: blush lace lingerie and a black swimsuit on pink satin
with a few rose petals, no person. On the left: a small pill badge "Sommer-Sale", a large
bold serif headline "Bis zu -50 %", a sans-serif subline
"auf ausgewählte Dessous & Bademoden", and a black rounded button "Jetzt shoppen".

Below: a light grey-pink USP strip with four small check-icon items:
"Kostenloser Versand ab 49 €", "30 Tage Rückgabe", "Sichere Zahlung per Kreditkarte",
"4,8 / 5 Kundenbewertung".

Then the section title "Bestseller" with a link "Alle ansehen" and the top of a
4-column product grid with white cards: products on invisible ghost mannequins on white
backgrounds, small berry badges "-30 %" and "Nur noch 3 verfügbar", five small gold
rating stars with a count, strikethrough old price in grey and new price in berry,
e.g. "119,00 €" crossed out, "83,30 €".

Bottom-left corner: a small white rounded notification card with a thumbnail:
"Sabine aus München hat gerade Body „Amélie" gekauft · vor 2 Min."

Palette: white, blush #EFD9E1, berry #A64D79, rose gold #C79798, ink #1D1B1A.
Clean, modern, professional, trustworthy, crisp readable German text, consistent spacing.
```

**Midjourney-хвост:** `--ar 16:10 --style raw --no gibberish text, misspelled words, watermark, nudity, realistic person, distorted hands, brand logos, credit card logos, clutter, neon`

**Negative / Avoid:** тот же список, что в 3a, плюс
`cheap-looking design, flashing banners, too many colors, comic sans, amazon-like logo`.

> Мега-меню в генераторе изображений лучше **не открывать**: слишком много мелкого
> текста, он точно поплывёт. Мега-меню — только в версии 4b.

### 4b. Версия для конструктора сайтов (v0 / Lovable / Bolt)

```
Build a STATIC, non-functional e-commerce homepage MOCKUP for a screenshot in a
security-awareness presentation. React + Tailwind (shadcn/ui components are fine).
No backend, no real forms, no inputs that submit (render the search field as a styled
div or a readOnly input outside any <form>), no checkout, no payment SDKs, no analytics.
<meta name="robots" content="noindex, nofollow">, <title>Per la Donna | Dessous &
Bademoden online kaufen</title>, lang="de". All links href="#".

Target viewport exactly 1440x900; above the fold must show promo bar, header, nav with
the "Dessous" mega-menu OPEN (controlled by a state flag `megaOpen=true`, so it stays
visible for the screenshot), the hero (partly covered by the mega-menu on the left),
the USP strip and the top of the product grid.

FONTS: "Cormorant Garamond" italic 600 (logo only), "Playfair Display" 700 (hero
headline), "Inter" 400/500/600 (all UI).
COLORS: --white #FFFFFF; --blush #EFD9E1; --blush-light #F7EBEF; --berry #A64D79;
--rose-gold #C79798; --ink #1D1B1A; --muted #82767D; --line #EADDE2; --star #C9A227.

SECTIONS
1. Promo bar (36px, bg --berry, white Inter 13px 500, centered):
   "Nur heute: −30 % auf alles mit Code DONNA30" + a live-looking countdown pill
   "Endet in 03:59:12" (static text is fine).
2. Header (white, 76px, max-width 1320px, border-bottom 1px --line):
   - Left: logo "Per la Donna" (Cormorant Garamond italic 600, 32px, --ink) with a tiny
     outlined heart SVG in --rose-gold after it.
   - Center: search field 520px, radius 999px, bg --blush-light, magnifier icon,
     placeholder "Wonach suchen Sie?".
   - Right: lucide icons User ("Anmelden"), Heart, ShoppingBag with --berry badge "2",
     labels Inter 12px --muted.
3. Nav row (48px, Inter 14px 500): "Neu", "Dessous" (active, underline 2px --ink),
   "Bademoden", "Nachtwäsche", "Bestseller", "Marken-Looks", "Sale" (--berry).
4. Mega-menu under "Dessous" (white panel, shadow-lg, width ~980px, padding 32px,
   4 columns):
   - "BHs": "Bügel-BH", "Balconette-BH", "Push-up-BH", "Bralette", "Spacer-BH"
   - "Slips": "Hipster", "Tanga", "Brazilian", "Taillenslip"
   - "Kollektionen": "Spitze", "Brautwäsche", "Basics", "Große Größen"
   - Promo tile: image /mega.jpg (flat-lay) with caption "Neue Kollektion" and link
     "Jetzt entdecken →".
5. Hero (height ~420px, bg --blush, radius 16px, inside 1320px container):
   left text block — pill badge "Sommer-Sale" (bg white, --berry text), H1 "Bis zu −50 %"
   (Playfair Display 700, 64px), subline "auf ausgewählte Dessous & Bademoden" (Inter 18px),
   black button radius 999px "Jetzt shoppen"; small note "Nur solange der Vorrat reicht".
   Right: image /hero-flatlay.jpg (lingerie + swimsuit flat-lay on pink satin, no person).
6. USP strip (bg --blush-light, 56px, 4 items with lucide Check icons, Inter 13px):
   "Kostenloser Versand ab 49 €" · "30 Tage Rückgabe" · "Sichere Zahlung per Kreditkarte"
   · "★ 4,8 / 5 Kundenbewertung".
7. Product grid: header row "Bestseller" (Inter 24px 600) + link "Alle ansehen →".
   4 columns, gap 20px. Card: white, border 1px --line, radius 12px; image 4:5
   (/b1.jpg … /b4.jpg, white bg ghost mannequin); top-left badge pill ("−30 %" bg --berry
   white text, or "Bestseller" bg --ink); top-right heart button; body: product name
   Inter 15px 500; stars row (5 small --star stars) + "(128)"; price row: old price
   line-through --muted 13px + new price --berry 16px 600; 3 color swatch dots; full-width
   outline button "In den Warenkorb". Scarcity line on one card in --berry 12px:
   "Nur noch 3 verfügbar". Products:
   - "Spitzen-Bralette „Nora"" — "59,90 €" → "41,93 €" (212)
   - "Body „Amélie"" — "119,00 €" → "83,30 €" (128)
   - "Bikini-Set „Capri"" — "89,00 €" → "62,30 €" (96)
   - "Balconette-BH „Rosalie"" — "79,90 €" → "55,93 €" (174)
8. Social-proof toast fixed bottom-left (white card, shadow, radius 12px, 320px,
   40px thumbnail): "Sabine aus München hat gerade Body „Amélie" gekauft" / "vor 2 Min.",
   small close "×".
9. (below the fold) Footer: "Impressum", "Datenschutz", "AGB", "Versand & Zahlung",
   "Kontakt"; payment row: generic card icon + text "Kreditkarte" only (no real logos,
   no PayPal); small line "Mockup für eine Präsentation – kein echter Shop."

STYLE: modern, clean, generous but denser than a boutique site, consistent 8px spacing
grid, subtle shadows, rounded 12px cards, no emojis, no real third-party brand logos.
```

**Ассеты для 4b:** `hero-flatlay.jpg`, `mega.jpg`:
```
Overhead flat-lay e-commerce hero photo: blush-pink lace lingerie set and a black
one-piece swimsuit arranged on soft pink silk satin, a few rose petals, a small gold
jewelry dish, soft natural light, luxury catalog style, no person, no text, no logo.
```
Товары — набор из §2.6 с фоном `pure white`.

### 4b.1 Безопасность для маршрута «конструктор» (для обоих сайтов)
- v0, Lovable и Bolt по умолчанию создают **публичные превью-URL**. Страница с реальным
  именем фирмы в открытом интернете — это ровно тот вред, о котором доклад.
  Поэтому: проект **private**, **не нажимать Publish/Deploy**, без кастомного домена.
  После скриншота проект удалить или экспортировать код и смотреть **локально** (`npm run dev`).
- В каждом макете `noindex` и строка «Mockup für eine Präsentation – kein echter Shop»
  в футере, вне кадра.
- Никаких полей, которые что-то отправляют.

---

## 5. Какой маршрут выбрать (рекомендация)

**Рекомендация: конструктор (вариант b) как основа, генератор изображений только для
ассетов** (силуэт, flat-lay, товары). Причины:

1. **Читаемость текста.** Главное в этой сцене — немецкий UI-текст: „Versandkostenfrei",
   „NACHTWÄSCHE", „Rückgaberecht", цены с „€", умлауты, кавычки „…". Генераторы изображений
   до сих пор регулярно ломают буквы в длинных строках. Любая буква-каша — это та самая
   «очевидная улика», которая сломает игру. В конструкторе текст — настоящий шрифт.
2. **Точный контроль.** Hex-цвета, шрифты, ровно 1440×900, одинаковый масштаб у A и B,
   мега-меню «застывает» в открытом состоянии через state.
3. **Правки за минуты.** Цену, скидку или улику для раскрытия меняем в коде, без новой генерации.
4. **Честность тезиса Teil 3.** Работает фраза «этот магазин ИИ собрал за X минут»
   (время замерить при сборке; до замера — плейсхолдер `[X — beim Bauen messen]`).

**Если всё-таки генератор изображений:** из них лучше всего с текстом справляются
Ideogram и GPT-image, Midjourney хуже. (Оценка на момент написания, проверить на текущих
версиях.) Держать текст коротким, мега-меню не открывать. Результат проверять при 100 %
на каждую букву. Учесть, что GPT-image отдаёт 3:2 (1536×1024), и его придётся кадрировать
до 16:10.

**Адресная строка:** в скриншот **не** включать. Рамку браузера и URL
(`perladonna-shop.de` / `perla-donna.store`) лучше дорисовать в `index.html` живым текстом:
так он чёткий, редактируемый, и рентген может повесить на него выноску „Gefälschte Domain".
(Это задача агента, который ведёт `index.html`; этот файл его не трогает.)

---

## 6. Тонкие улики для раскрытия

Легенда: **[FALL]** — из реального кейса (§3.1 / `perladonna-warnhinweis.png`);
**[GENERISCH]** — типичный паттерн фейк-магазинов, в кейсе Per la Donna **не** задокументирован
(на слайдах подавать как «typisches Muster», не как факт кейса).

### Site A — „Boutique-Klassik"
| Улика | Где видно | Тип |
|---|---|---|
| Магазин вообще продаёт Dessous/Bademoden онлайн, а настоящая Per la Donna «verkauft grundsätzlich keine Hygienewaren wie Bademoden oder Dessous über das Internet» | весь сайт | **[FALL]** |
| Домен `perladonna-shop.de` ≠ `perladonna.de` (домен с визитки) | рамка URL на слайде | **[FALL]** (принцип: чужой домен; конкретное имя вымышлено) |
| „Sichere Zahlung per Kreditkarte": оплата **только кредиткой**, PayPal и т.п. нет | строка доверия, футер | **[FALL]** |
| Impressum: имя фирмы настоящее, но данные «in Teilen verändert und unvollständig» | ссылка в футере, показать в раскрытии (без имени владельца) | **[FALL]** |
| Контактная форма остаётся без ответа | не видно; рассказать устно | **[FALL]** |
| „Handverlesen in Bremen – jetzt auch online.": фейк «исполняет» обещание визитки „Bald ist unsere neue Website online!" | hero | наша драматургия (не факт кейса) |

### Site B — „Moderner E-Commerce"
| Улика | Где видно | Тип |
|---|---|---|
| TLD `.store`, как у ardenza.store | рамка URL | **[FALL]** (параллель; сам домен вымышлен) |
| „Sichere Zahlung per Kreditkarte", в футере только иконка карты, без PayPal | USP-полоса, футер | **[FALL]** |
| Таймер „Endet in 03:59:12" + „Nur heute: −30 %" | промо-полоса | **[GENERISCH]**, рентген-выноска „Künstliche Dringlichkeit" |
| „Nur noch 3 verfügbar" | карточка товара | **[GENERISCH]** |
| Всплывашка „Sabine aus München hat gerade … gekauft" | левый нижний угол | **[GENERISCH]** |
| „4,8 / 5" и количество отзывов без ссылки на независимую платформу | USP-полоса, карточки | **[GENERISCH]** |
| Скидки до −50 % в «люксовом» сегменте | hero | **[GENERISCH]** |

> Улики должны быть **мелкими**: обычный размер UI, без выделения. Их раскрывает
> рентген (клавиша `X`), а не сам скриншот.

---

## 7. Чек-лист скриншота и экспорта

- [ ] **Размер:** оба кадра **1440×900 CSS-px (16:10)**, снимать с **DPR 2** →
      итоговый PNG **2880×1800**. Оба строго одинакового размера.
- [ ] **Как снять (Chrome):** DevTools → Device Toolbar → Responsive → 1440 × 900,
      DPR 2 → меню ⋮ → „Capture screenshot" (именно этот пункт, а не „full size").
- [ ] **Кадр:** только страница, без рамки браузера, панели задач и курсора. Сверху —
      промо-полоса, снизу — видимый верх товарной сетки (карточки срезаны примерно на половине).
- [ ] **Состояния:** A — без hover. B — мега-меню открыто, toast виден, курсор не в кадре.
- [ ] **Шрифты загружены:** перед снимком дождаться веб-шрифтов, чтобы не было FOUT
      с Times/Arial.
- [ ] **Текст:** проверить при 100 % каждую строку: умлауты (ä ö ü ß), „€" после числа
      с пробелом („89,90 €"), немецкие кавычки „…", нет английских остатков
      („Add to cart", „Search").
- [ ] **Нет реальных чужих логотипов** (Visa, Mastercard, PayPal, Trusted Shops, Klarna).
- [ ] **Нет имени владельца** и реального адреса в видимой части.
- [ ] **Генератор изображений:** довести до 16:10 кадрированием, не растягиванием.
      Если исходник меньше 2880 px, лучше взять 1440×900, чем апскейлить с артефактами.
- [ ] **Файлы:** `assets/fake-shop-a.png` (Boutique-Klassik) и
      `assets/fake-shop-b.png` (Moderner E-Commerce). PNG, sRGB. Если файл больше ~3 МБ,
      прогнать через оптимизатор PNG (без потерь, например oxipng/TinyPNG).
- [ ] **Уборка:** проекты в v0/Lovable/Bolt не опубликованы или удалены. Домены не регистрировались.
- [ ] Записать фактическое время сборки каждого макета (для тезиса Teil 3 «ИИ собрал за X минут»).
