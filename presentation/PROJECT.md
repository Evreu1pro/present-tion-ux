# PROJECT.md — „Die Architektur der Täuschung"

> **Zweck dieser Datei / Назначение файла**
> Единый источник правды (single source of truth) для проекта-презентации.
> Любой ИИ-агент или человек, подключившийся к проекту, должен прочитать этот файл ПЕРВЫМ.
> Здесь: концепция, проверенные факты с источниками, структура, дизайн-система,
> правила и открытые вопросы. При изменениях — обновлять этот файл и вести Changelog внизу.
>
> **Рабочие языки:** контент на слайдах — немецкий (verbatim, не переводить);
> рабочее обсуждение и заметки — русский; дизайн-токены — английский.
> **Дата последнего обновления:** 2026-09-30

---

## 1. О чём презентация

**Titel:** Die Architektur der Täuschung
**Untertitel:** Wie Betrugsnetzwerke offizielle Design-Systeme und UX-Psychologie als Waffe nutzen

**Формат вывода:** не классические слайды, а **сайт-слайдшоу** (один самостоятельный
HTML-файл, листается стрелками, работает офлайн и с проектора).

**Главный тезис доклада:** онлайн-мошенничество — это не «кривые письма с ошибками»,
а **архитектура**, собранная из наших же стандартов доверия: официальных дизайн-систем,
UX-паттернов и привычек пользователя. Обман выглядит профессионально именно потому,
что использует нашу собственную работу против нас.

**Драматургия (сквозная линия):**
Игра «найди фейк» (с подвохом) → реальный случай (Per la Donna) → «визуально разницы нет»
→ почему так (открытые киты + ИИ) → что под капотом (объяснение механизма) → кто несёт
ответственность → (возможный финал с решениями).

---

## 2. Мета-параметры (ОТКРЫТЫЕ ВОПРОСЫ — требуют ответа заказчика)

| Параметр | Статус | Заметка |
|---|---|---|
| **Аудитория** | ❓ не задана | Технари / менеджмент / клиенты? Влияет на глубину Teil 4. |
| **Длительность** | ❓ не задана | Влияет на число слайдов и темп. |
| **Язык презентации** | ✅ немецкий | Обсуждение — русский. |
| **Teil 6 (решения)** | ❓ не решён | Финал с выводами или заканчиваем вопросом «кто виноват»? |
| **Мостик «поддельные загрузки»** | ❓ не решён | Фейк-Chrome/WhatsApp — искать документированный пример или не включать? |
| **Имя владельца на слайдах** | ❓ | В прессе есть; на слайдах предлагается «der Inhaber». |
| **История «1.800 € в 4 минуты»** | ❓ без источника | Реальный кейс или собирательный? Без источника — убрать. |
| **ShopNova vs Per la Donna (сквозной сюжет)** | ✅ РЕШЕНО (2026-09-30) | **Везде реальный кейс.** Per la Donna / Ardenza проходит через интро и все слайды 1.1–1.3. ShopNova выводим из Teil 1. Бренды — нашими демонстративными знаками, не оригинальной айдентикой. |

---

## 3. Проверенные факты и источники

> ⚠️ **Правило:** никаких выдуманных цифр на слайдах. Любая цифра — либо из списка ниже
> с источником, либо помечена как плейсхолдер `[… — Quelle einfügen]`.

### 3.1 Главный кейс — „Per la Donna" (Bremen)
- Магазин женского белья «Per la Donna», Katharinenpassage, Бремен. Владелец продаёт
  **только офлайн**, интернет-магазина никогда не имел (сайт-визитка perladonna.de без продаж).
- Конец марта 2026: звонок покупателя из Франкфурта — «когда придёт заказ?». Так владелец узнал о фейке.
- Фейк работал под брендом **„Ardenza"** (ardenza.store / .de / .com), но в **Impressum стояли
  РЕАЛЬНЫЕ данные** фирмы: «Per la donna Mode- und Handels GmbH», «Herr Albrecht Friedrich».
- Скриншот-предупреждение владельца (есть в проекте: `assets/perladonna-warnhinweis.png`):
  фейк активен с **22.02.2026**, заявление в полицию Бремена подано **27.03.2026**,
  данные в Impressum «in Teilen verändert und unvollständig», оплата **только кредитной картой**
  (PayPal нет), форма обратной связи не отвечает.
- Watchlist Internet внёс ardenza.store в список мошеннических магазинов (07.05.2026).
- **Ключевая цитата владельца (для Teil 2):**
  „Bei genauem Hinsehen lässt sich der Shop zwar als Fake erkennen, doch **dem Laien ist
  dieser Blick meist nicht möglich.**"
- **Ключевая идея кейса:** стандартный совет «проверь Impressum» здесь НЕ работает —
  проверка находит настоящую GmbH, настоящий адрес, настоящего человека.
  **Проверка сама подтверждает обман.** Оригинала не существовало вовсе.
- Источники: Weser-Kurier, 26.05.2026 (Christoph Barth) —
  https://www.weser-kurier.de/bremen/wirtschaft/bremer-einzelhaendler-betroffen-damendessous-aus-dem-fake-shop-doc85wyhu2bz2dk3klui5e
  и комментарий —
  https://www.weser-kurier.de/bremen/wirtschaft/fake-shops-betrug-im-internet-ist-ein-zeitgemaesses-verbrechen-doc85yefehgf1faer0jh7i
  Watchlist Internet — https://www.watchlist-internet.at/liste-betruegerischer-shops/shop/ardenzastore

### 3.2 Масштаб и реклама (vzbv, 06.11.2025)
- **50 %** из 653 проверенных фейк-магазинов крутят рекламу в Google или Meta.
- У 5 самых крупных — минимум **134 млн** показов рекламы (Google-платформы).
- **12 %** онлайн-покупателей за 2 года стали жертвами фейк-магазина (опрос Forsa, 09.2025, n=1503).
- **70 %** сталкивались с подозрительными магазинами; **51 %** — неоднократно.
- Жалоб в 2024 году: **> 10 000** (+47 % к 2023); за 1–3 кв. 2025: **> 8 000**.
- Цитата Ramona Pop (vzbv): „Wer mit Werbung sein Geld verdient, darf sich nicht aus
  der Verantwortung stehlen!"
- Источник: https://www.vzbv.de/pressemitteilungen/jeder-zweite-fakeshop-schaltet-werbung-auf-google-oder-meta

### 3.3 Масштаб одного оператора (Generalstaatsanwaltschaft Bamberg, PM 12/2026, 18.05.2026)
- Один человек (62 г.), **> 140 фейк-магазинов**, ~**8 000 заказов**, ущерб в среднем
  шестизначном диапазоне, деятельность минимум с 2023.
- Арестован на Филиппинах (03.2025), передан в Германию (конец 04.2026).
- ⚠️ В **официальном** релизе **ИИ НЕ упоминается**. Заголовок «с ИИ» — интерпретация блога
  wortfilter, НЕ первоисточник. → Кейс использовать только ради масштаба, не ради «ИИ».
- Источник: https://www.justiz.bayern.de/gerichte-und-behoerden/generalstaatsanwaltschaft/bamberg/presse/2026/12.php

### 3.4 ИИ понижает порог входа (Netcraft, 2025)
- **darcula-suite v3** — фишинг-как-сервис: клонирует любой сайт **по ссылке**
  (вводишь URL → редактируемая копия со всеми ассетами).
- С ~апреля 2025 добавлен генеративный ИИ: авто-перевод страниц под страну жертвы,
  генерация форм ввода.
- С марта 2024 Netcraft заблокировал **> 90 000** доменов darcula.
- Источники: https://www.netcraft.com/blog/darcula-v3-phishing-kits-targeting-any-brand
  https://www.netcraft.com/blog/ai-enabled-darcula-suite-makes-phishing-kits-more-accessible-easier-to-deploy

### 3.5 Кража Impressum как метод (Watchlist Internet, 22.04.2026)
- Мошенники берут реквизиты реальных фирм (название, адрес, налоговый номер) → жертва их
  проверяет в реестрах → всё «сходится» → обман выглядит достоверно, а репутация реальной
  фирмы страдает. Единственный работающий способ оплаты — предоплата/перевод.
- Источник: https://www.watchlist-internet.at/news/fake-shops-anhaenger/

### 3.6 Опора: дизайн = набор блоков + «Heuristisches Vertrauens-Caching» (наш тезис · слайд 06)
- Jakob's Law (Jakob Nielsen / NN Group): пользователи ждут, что сайт работает как другие.
- Steve Krug, „Don't Make Me Think" (2000): пользователь не думает, действует по привычке.
- **Тезис «Alles nur Bausteine» (слайд 06, тезис доклада, НЕ измеренный факт):** веб-визуал собирается
  из готовых блоков: шапка, меню, баннер, полоса доверия, карточки товаров, всплывашка «hat gerade
  gekauft». Блоки берутся из UI-китов, дизайн-систем и ИИ-инструментов (Google и других компаний).
  Их копируют (Strg+C / Strg+V) без понимания общей структуры — и этого хватает даже на лендинг для
  первой приманки. ИИ сам собирает из тех же блоков новые варианты. Профи или новичок — внешне результат
  одинаковый. Это «повторяемое искусство», как копирование картин: чтобы скопировать, понимать не нужно.
- **Чем подкреплено:** ИИ-клонирование сайтов — §3.4 (darcula); Material Design — open source, Apple HIG —
  «frei zugänglich» (формулировки — Teil 3). Три домена одного фейка ardenza.store/.de/.com — §3.1.
  **На слайде без источника (= иллюстрация):** «откуда» каждый блок („UI-Kit", „Vorlage", „KI-Bild",
  „Plugin") — это пример, а не анализ реального Ardenza. Google и Apple на слайде 06 названы **только текстом** (без логотипов, §7.1):
  „z. B. Material Design (Google) · Human Interface Guidelines (Apple)" — формулировки как в Teil 3.
- Вывод доклада: мошенники эксплуатируют ровно этот UX-принцип — привычные блоки выглядят «как всегда».

### 3.7 ИИ-ассистенты ведут на фейк (Netcraft 07/2025 · Guardio Labs 08/2025)
- **Netcraft, 01.07.2025:** модели GPT-4.1 естественными вопросами задавали, где логин-страница
  50 брендов → 131 хостнейм / 97 доменов; **34 %** доменов НЕ принадлежали бренду
  (29 % — не зарегистрированы / припаркованы / неактивны, 5 % — посторонние фирмы).
  Пример: Perplexity на запрос логина Wells Fargo выдал фишинговую страницу на Google Sites.
  https://www.netcraft.com/blog/large-language-models-are-falling-for-phishing-scams
- **Guardio Labs „Scamlexity“, 08/2025:** ИИ-браузер-агент (Perplexity Comet) по команде
  «купи Apple Watch» сам оформил покупку в фейковом магазине (сделан исследователями),
  подставив сохранённую карту и адрес. (Не каждый раз — поведение нестабильно.)
  https://guard.io/labs/scamlexity-we-put-agentic-ai-browsers-to-the-test-they-clicked-they-paid-they-failed
- ⚠️ **Gemini:** задокументированного случая «Gemini в браузере подменил ссылку на фейк» НЕ найдено
  (наоборот: Google встраивает Gemini Nano в Chrome как защиту от скама). На слайдах Gemini не называть.

---

## 4. Структура презентации (контент слайдов)

> Немецкий текст — verbatim для слайдов. Русский — описание визуала/логики.
> Статус: ✅ в прототипе / 🔜 спроектировано, не собрано / 💡 идея.

### Teil 0 — Titel ✅
- Экран логина «глитчит» → под ним чертёж → заголовок + подзаголовок.
- Meta-строка: „FALLSTUDIE · SICHERHEIT & UX".

### Slide 00 · INTRO — Suchly-промо (3 фейк-объявления) ✅ (собрано другой сессией)
- **Реализовано в index.html** (`data-id="intro"`, ПЕРЕД titel, `data-steps="1"`). Белый «промо»-экран,
  автоплей ~16 с. Управление: `R` — повтор; `?t=ms` — заморозить кадр (для QA/скриншотов).
- **После клика (обновл. present-tion-68):** магазин B «прорисовывается» (скелетон → `assets/fake-shop-b.jpg`
  тремя полосами: header, hero blur-up, остальное) → появляется вымышленная бот-проверка **«VeriGate»**
  („Einen Moment, bitte …", намёк на домен ardenza.store, чекбокс „Ich bin kein Roboter"). Шаг 1 (`→`/клик по
  чекбоксу): курсор кликает → спиннер → зелёная галка „Verifiziert" → авто-переход на следующий слайд (titel).
  ⚠️ Поддельная CAPTCHA — известный скам-паттерн, но в §3 источника НЕТ → используется ТОЛЬКО как визуальный
  переход, без утверждений на слайде.
- ✅ **СЮЖЕТ УНИФИЦИРОВАН (решено 2026-09-30):** весь Teil 1 — на реальном кейсе
  Per la Donna / ardenza.*. ShopNova выводится. Статус конвертации 1.1–1.3: 🔜 в работе.
- **Сюжет анимации:** вымышленный поисковик **„Suchly"** (радужный градиентный вордмарк;
  слайд 1.1 тоже использует вордмарк Suchly) → запрос „per la donna online shop"
  (магазин, которого никогда не было) → **3 рекламных объявления, все фейковые**, на
  задокументированных доменах **ardenza.store / ardenza.de / ardenza.com** (§3.1) с
  скопированным знаком Per la Donna → остальные результаты и «Wikipedia»-панель = серые
  нечитаемые скелетоны → курсор кликает объявление №1 → появляется грузящийся скелетон
  магазина «Per la Donna» (сам фейк-магазин — следующий шаг).
- ~~Раскрытие в конце Teil 1 („Alle drei sind Fake…")~~ → **заменено** игрой на слайдах 03–04
  (см. ниже): раскрытие „Keine ist echt." идёт сразу после игры.
- В Teil 3 усиление: «эти магазины ИИ собрал за X минут».

### Slide 03 · Игра „Welche Website ist echt?" ✅ (`data-id="spiel"`, после titel)
> Заменяет старую заметку «3 магазина, делаем сами». Теперь: **ДВА магазина, ОБА фейк**,
> скриншоты генерирует **внешний ИИ** (промпты: `prompts/fake-shops-prompts.md`).
- Почти без текста: „Welche Website ist *echt*?" + подпись „Eine davon ist das Original."
  (намеренная ложная подсказка — зал должен верить, что правильный ответ есть).
- Два окна браузера A / B (рамка и адресная строка — живой HTML, в скриншотах их нет):
  A = `perladonna-shop.de/dessous`, B = `perla-donna.store/collections/neu` — оба вымышлены,
  НЕ perladonna.de. Под окнами — метки „A" / „B".
- Курсор «сомневается»: ведёт к A, зависает (A приподнимается + свечение, курсор → «рука»,
  один раз почти кликает), уходит к B, возвращается в середину, дёргается… цикл ~18 с.
  Кривые траектории, профиль скорости minimum-jerk, лёгкий перелёт + коррекция, микродрожь.
- **Hover-зум (обновл. present-tion-68):** при наведении магазин увеличивается в центр (×1.55, 0.8 с),
  чтобы задние ряды читали детали; второй магазин + заголовок гаснут до 25 %, затем возврат и курсор
  идёт к другому. CSS только в `.s-spiel .pk-shop.is-hover`; паузы в `Hooks.spiel.PATH` увеличены
  (каждый магазин в зуме ≈ 5 с за проход).
- Шаг 1 (`→`): голосование — курсор паркуется между A и B, подпись „Handzeichen · A oder B?".
- `prefers-reduced-motion` / `?instant` → курсор статичен в середине.
- Тема: розовая «бутик»-тема Per la Donna (см. §5.1).

### Slide 04 · Auflösung „Keine ist echt." ✅ (`data-id="aufloesung"`)
- Beat 0: на обоих окнах штамп **FAKE** (розово-красный, «чернильная» текстура) +
  „Keine ist *echt*." / „Sie haben nach dem Original gesucht – es gab nie eins."
- Beat 1 (`→`): A и B уменьшаются в левую колонку; «Beweisstück» — приколотый вырез
  `assets/perladonna-warnhinweis.png` (**подпись/имя владельца закрыто плашкой**, подпись
  „Warnhinweis des Inhabers · Name geschwärzt") + настоящий `perladonna.de`
  (`assets/perladonna-visitenkarte.png`, обрезан до карточки) в окне браузера:
  „Das Original · perladonna.de — Nur eine Visitenkarte. Kein Shop. Nichts zu kaufen."
- Beat 2 (`→`): таймлайн ТОЛЬКО из §3.1: 22.02.2026 Fake-Shop „Ardenza" online
  (ardenza.store · .de · .com) → 27.03.2026 Strafanzeige bei der Polizei Bremen →
  07.05.2026 Watchlist Internet (ardenza.store gelistet) → „Und morgen? Der nächste Klon
  kann jederzeit auftauchen."
- ⚠️ В брифе заказчика было «Gerichtsverfahren / суд» — по источнику это **Strafanzeige**
  (заявление в полицию), НЕ судебный процесс. На слайде — „Strafanzeige".
- **Логотип „Per la Donna"** — наш демонстративный знак (круглая «P» + курсив Cormorant
  Garamond), НЕ оригинальная айдентика магазина.
- ⚠️ **Оговорка (важно для честности):** показ ardenza.* как объявлений в стиле Google —
  это **драматизация** (опора: vzbv §3.2, «50 % фейков рекламируются»), для самого Ardenza
  реклама НЕ задокументирована. Цифры на слайде не используются.

### Slide 05 · Das Ausmaß ✅ (`data-id="ausmass"`, после aufloesung, тёмная тема)
- Сверху 3 и снизу 3 крупные цифры vzbv (§3.2), count-up: **12 %** (Opfer, красный) · 70 % · 51 % /
  50 % (von 653 werben bei Google/Meta) · 134 Mio. Impressionen · > 10.000 Beschwerden 2024 (+47 %).
  Ремарка-источник вверху справа: „Quelle: vzbv, 06.11.2025 · Forsa-Umfrage 09/2025, n = 1.503“.
- По центру — окно Suchly: цикл из 4 запросов (per la donna online shop → sneaker → gartenmöbel →
  kaffeevollautomat), по 4 одинаковых результата, через паузу фейки получают штамп „Fake-Shop“
  (2/4, 1/4, 2/4, 1/4) и счётчик „2 von 4 · in dieser Suche“. Помечено **„Illustration · keine
  Messwerte“** — это НЕ статистика «каждая вторая ссылка — фейк». Кроме ardenza.* (§3.1) все
  бренды/домены вымышлены. Данные: `Hooks.ausmass.Q`.
- Шаг 1 (`→`): окно уезжает влево, цифры гаснут; в Suchly — **нachgestellte** „KI-Übersicht“,
  которая рекомендует ardenza.store как «официальный магазин» (штамп „Klon“). Справа: 34 %
  (Netcraft) + KI-Browser-Agent kauft im Fake-Shop (Guardio) — факты §3.7.

### Slide 06 · Alles nur Bausteine ✅ (`data-id="bausteine"`, после ausmass, перед 07 details, **светлая тема**)
> Тезис §3.6: дизайн — это набор блоков, которые копируют, улучшают и повторяют. v2 по замечаниям заказчика:
> светлый бело-розовый «деко-стиль» (референс — профессиональные pitch-деки: верхняя nav-полоса, (01)-нумерация,
> [скобочные] метки, крупный гротеск Inter Tight, тонкая сетка, мягкое розовое свечение) и **крупные подписи**
> (читаются из дальних рядов). Немецкий текст — **ЧЕРНОВИК**, заказчик пришлёт свой → заменить verbatim.
- **Тема:** `body.on-pink` + `body.pk-clean` (ставит `Hooks.bausteine`): фон blush без акварели/золотых дуг,
  сетка 160 px, хром розовый. Верхняя полоса = легенда эпизодов: (01) Zerlegen · (02) Vervielfältigen · (03) Vorlagen.
- Слева всегда: „[Das System dahinter]" · „Alles nur **Bausteine.**"; ниже — блок текущего эпизода.
- **(01) Zerlegen (автоплей ~3,5 с, `R` — повтор):** магазин B из игры стоит ровно → изометрия → расслаивается
  вверх; **в самом низу — сетка + пунктирный контур всех блоков** („Raster & Kontur — die unsichtbare Basis").
  Справа 8 крупных подписей (01)–(08) с прямыми выносками, у каждой «откуда блок»: Countdown-Leiste (Vorlage ·
  künstliche Eile) · Header & Suche (UI-Kit) · Navigation (UI-Kit) · Hero-Banner (KI-Bild + KI-Text) · Kauf-Popup
  (Plugin) · Vertrauens-Leiste (Vorlage · Siegel & Sterne) · Produkt-Karten (1 Karte · 4× kopiert) · Raster & Kontur.
  Красным — манипулятивные блоки. Текст: „Ein Shop ist kein Handwerk, sondern ein Baukasten …" + [UI-Kits]
  [Vorlagen] [KI-Werkzeuge] + крупное „08 Bausteine – mehr braucht dieser Shop nicht." (8 = число блоков нашей
  иллюстрации, не статистика).
- **(02) Vervielfältigen (петля):** блоки съезжаются, сайт поворачивается **лицом к залу** (адресная строка
  `perla-donna.store`). Из-за него по кругу выходят вверх и растворяются копии с другими именами в шапке:
  ardenza.store · ardenza.de · ardenza.com (§3.1) · perladonna-shop.de (вымышлен, из игры) — метка „Kopie".
  Слева: Strg+C → Strg+V (клавиши «нажимаются») · „Einmal gebaut – beliebig oft kopiert. Jede Kopie bekommt nur
  einen neuen Namen …".
- **(03) Vorlagen (петля ~14 с):** сайт приближается; курсор наводится на блоки, блок обводится „Vorlage", рядом
  всплывает **лист гайдлайна** („[Leitfaden] Komponente 01–03"): Header (① Logo ② Suche ③ Konto & Korb · „Nur das Logo
  tauschen.") → Hero-Banner (① Überschrift ② Text ③ Button ④ Bild · „Text & Bild einsetzen.") → Produktkarte (① Bild
  ② Badge ③ Name ④ Preis ⑤ Merkliste · „Produkt einsetzen."). Затем карточки пустеют, **шаблон карточки вытягивается**,
  **повторяется ×4** вдоль ряда („Vorlage × 4") и каждый слот **заполняется** товаром → по кругу.
  Слева: „Die Vorlage liefern die Großen gleich mit. Tech-Konzerne veröffentlichen Leitfäden und fertige Bausteine für ihre
  Oberflächen. Element anklicken, Vorlage übernehmen, eigene Inhalte einsetzen – und beliebig oft wiederholen." +
  „[Frei zugänglich] z. B. Material Design (Google) · Human Interface Guidelines (Apple)" + „[Wiederholbare Kunst] Wie die
  Kopie eines Gemäldes – verstehen muss man es nicht." (Перестановка блоков из v2 убрана по замечанию заказчика.)
  ⚠️ Листы гайдлайна — наши иллюстрации, НЕ скриншоты реальных гайдлайнов Google/Apple.
- Техника: слои (01) — нарезка `fake-shop-b-base.jpg`; фронт (02)/(03) — `fake-shop-b-clean.jpg` (без логотипа,
  иконок, текста/фото баннера и карточек) + движущиеся вырезки. `?instant` / reduced motion: статичный «веер»
  копий и лист гайдлайна карточки (фаза g-c).

### Slide 07 · Der Teufel steckt im Detail ✅ (`data-id="details"`, после bausteine, перед teil-1, **светлая тема как 06**, 5 эпизодов)
> v2 по замечаниям заказчика (2026-09-30): не тёмная, а светлая бело-розовая «деко»-тема слайда 06 (`body.on-pink` +
> `body.pk-clean`, ставит `Hooks.details`), верхняя полоса-легенда (01)–(05). Магазин B (`per-la-donna-mockups/shop-b-v2.html`)
> — **живой HTML** в окне браузера `perla-donna.store` (1440 px × .75) + добавлен **футер** с мелкими ошибками. Немецкий текст — **ЧЕРНОВИК**.
- **(01) Alles funktioniert (шаг 0):** курсор-покупатель в цикле: мега-меню → „Jetzt shoppen“ → корзина („reserviert für 09:59“)
  → поп-ап „−10 % extra“ → почти платит → **перезагрузка → таймер снова 03:59:12**. Чипы слева загораются по ходу.
- **(02) Der Blick (шаг 1, петля ~28 с):** «куда падает взгляд» — затемнение + прожектор прыгает от приманки к приманке, на окне
  остаются кружки-фиксации 1–7 с линией (как gaze plot), у каждой — пузырь «внутреннего голоса»: 1 „Bis zu −50 %“ (Rabatt Nr. 1) →
  2 −30 % Code (Nr. 2) → 3 Countdown (Zeitdruck) → 4 „4,8 / 5 aus 2.317“ (Zweifel? Bewertungen.) → 5 „Sabine hat gerade gekauft“ →
  6 „Nur noch 3“ (Knappheit) → 7 поп-ап „−10 %“ (Rabatt Nr. 3) → клик по кнопке покупки. Слева список 1–7 + шкала
  „Nachdenken → Kaufimpuls“ → „Kopf aus. Kaufen an.“ Помечено **„[schematisch · keine Messung]“** — иллюстрация, НЕ данные
  eye-tracking. Тепловую карту по решению заказчика не делаем.
- **(03) Gegenprüfen (шаг 2):** магазин размыт, 4 карточки (помечены „nachgestellt“) + метка 1 на домене: 1 Domain lesen ·
  2 WHOIS (22.02.2026 = дата §3.1) · 3 Impressum & Adresse (§3.1) · 4 Suche nach der Domain (Watchlist Internet) · 5 Preis vergleichen.
- **(04) Das Detail (шаг 3, петля):** страница прокручивается до футера, липкая шапка с таймером остаётся („▲ Laut · bleibt immer im
  Blick“ / „▼ Leise · ganz unten, klein, grau“), тосты продолжают всплывать. Курсор-**лупа** находит 5 ошибок, каждая — красная рамка +
  увеличенный пузырь: „Subscribe“ (Vorlagen-Rest) · „Widerufsrecht“ (Tippfehler) · „Telefon: –“ (Lücke im Impressum) ·
  service@perladonna-help.com (Fremde Domain) · „© 2019 Per la Dona“ (Name falsch; 2019 vs Domain 22.02.2026).
  ⚠️ Ошибки **нachgestellt** (не из реального Ardenza). Факт из кейса — в плашке: Impressum „in Teilen verändert und unvollständig“,
  форма обратной связи не отвечает (§3.1, Warnhinweis). Заголовок „Laut oben. Leise unten.“ Мысль: мошенники тоже ошибаются, но дизайн
  уводит взгляд от ошибок — нужна тщательность.
- **(05) Fazit (шаг 4):** „Einzeln harmlos. Zusammen ein Muster.“ + „Erst prüfen. Dann zahlen.“ + „Und gründlich lesen – gerade dort,
  wo keiner hinschaut.“ Окно остаётся на футере с отмеченными ошибками.
- Цифры — только цены самого макета и даты кейса; статистики нет. `R` — повтор текущего эпизода · `?instant` / reduced motion —
  без курсора, статичные конечные состояния. Данные эпизодов: `Hooks.details.GAZE` / `.ERRS`.

### Teil 1 — Der Hook (Real-World Case) ✅ (конвертирован на Per la Donna / Ardenza)
Вступление докладчика (актуальная версия — кейс Бремена):
> „Ende März 2026 klingelt in einem kleinen Dessousgeschäft in der Bremer Innenstadt das
> Telefon. Ein Kunde aus Frankfurt will wissen, wann seine Bestellung endlich ankommt.
> Der Inhaber ist irritiert – er verkauft ausschließlich im Laden. Einen Onlineshop hat er
> nie betrieben. Und doch existiert einer: professionell gestaltet, hochwertige Ware,
> sicherer Checkout – und im Impressum: sein Firmenname, seine Adresse, sein Name als
> Geschäftsführer. Wer misstrauisch wurde und nachprüfte, fand genau das, was er finden
> sollte: eine echte GmbH, ein echtes Geschäft, einen echten Menschen. Die Prüfung selbst
> hat den Betrug bestätigt."
> ✅ Сюжет: ВЕЗДЕ реальный кейс Per la Donna / Ardenza (решение §2). ShopNova выводится.
- **1.1 Der Vorfall:** сцена звонка → фейк-магазин Ardenza (домены ardenza.*) → путь через
  рекламу (факт 3.2: 50 %). Поисковик Suchly, знак Per la Donna — наш демонстративный.
- **1.2 Die menschliche Reaktion:** дизайн/SSL/Impressum (украденный, факт 3.5)/фирма
  существует — все проверки пройдены, мозг в режиме „Alles wie immer". (факт 3.6)
- **1.3 Der wirtschaftliche Schaden:** страдают ОБЕ стороны — покупатель и честный торговец
  (звонки, полиция, адвокат, репутация). Цифры из 3.2/3.3. Финал: «вещдок» — скриншот
  предупреждения Per la Donna (`assets/perladonna-warnhinweis.png`) + цитата владельца.

### Teil 2 — Die optische Falle (Echt vs. Klon) 🔜
- Два магазина рядом. 4 переключаемых слоя (строки таблицы источника):
  Grid & Spacing (8px) · Typografie · Micro-Interactions (hover/focus) · System-Status (Loader).
- ⚠️ URL-пример заменить с Amazon на вымышленные: `shopnova.de` vs `shopnova.de-kundenkonto.cc`.
  В «Рентгене» объяснить: домен читается СПРАВА НАЛЕВО; настоящий тут — `.cc`.
- System-Status связать с 2FA: пока крутится спиннер, данные пересылаются
  („Während Sie warten: Ihre Daten werden weitergeleitet").
- Финал: рамка смартфона, обрезанный URL, цитата владельца.

### Teil 3 — Die unabsichtlichen Helfer (Design-Systeme + KI) 🔜
- Ирония доступности: качественные дизайн-системы открыты/бесплатны → копировать «по кнопке».
- ⚠️ Точность формулировок:
  - Material Design — open source (Apache 2.0). ✅
  - Apple HIG / Design Resources — БЕСПЛАТНЫ, но НЕ open source (лицензия только под Apple-платформы).
    → писать „frei zugänglich", НЕ „quelloffen".
  - Tailwind / shadcn/ui — open source (MIT), но делают НЕ «Tech-Giganten».
    → формулировка „Tech-Konzerne und Open-Source-Communities".
- ИИ: оптимизирует и дорабатывает дизайн → со временем неотличимо от оригинала (факт 3.4 darcula).
- **«Эти 2 магазина из игры (слайд 03) сгенерировал ИИ за [X Minuten — Quelle/Messung einfügen]»** — тезис доказывается на сцене.
- Слайд «чек-лист с датой годности»: пункты зачёркиваются
  (~~Rechtschreibfehler~~ · ~~Unprofessionelles Design~~ · ~~Fehlendes Impressum~~ ·
  ~~Kein Schloss-Symbol~~ · ~~Bilder-Rückwärtssuche~~).
  Заголовок: „Die Checkliste hat ein Ablaufdatum." (прогноз = тезис докладчика, не факт).

### Teil 4 — Blick unter die Haube (уровень ОБЪЯСНЕНИЯ, не инструкция) 🔜
> ⚠️ Держать на уровне осведомлённости: ЧТО происходит и ПОЧЕМУ опасно.
> НЕ давать операционных деталей «как сделать».
- Смена ракурса: дизайнер → архитектор системы. Диаграмма-принцип:
  `[ Opfer ] → [ Betrugs-Proxy ] ⇄ [ Echte Plattform ] → [ Sitzung übernommen ]`
- Три причины, почему привычные защиты не срабатывают (карточки «Sie dachten → Realität»):
  1. **Der Proxy in der Mitte:** фейк = прокладка в реальном времени → даже 2FA не защищает.
  2. **Die unsichtbare Wand:** сканеру безопасности показывается безобидная страница,
     жертве — подделка. (хорошо ложится в «Рентген»: мы видим обман, автосканер — нет).
  3. **Die gemalte Adressleiste:** в in-app-браузере (TikTok/IG/Telegram) фальшивая
     адресная строка с замком — просто картинка. („Das Schloss = ein Bild").
- 💡 Опциональный мостик „Nicht nur Passwörter — auch Downloads": поддельные загрузки
  программ (fake Chrome/WhatsApp/лаунчеры) — та же архитектура доверия, крадут не логин,
  а ставят вредонос. ⚠️ Нужен документированный источник, иначе не включать.

### Teil 5 — Wer trägt Verantwortung? 🔜
> Переформулировка исходного «основного конфликта». Ставим ВОПРОСЫ, не даём правовую оценку.
- Круги ответственности:
  - **Designer/Entwickler:** дизайн нейтрален, намерение — нет. Решение сделать ловушку — у владельца.
  - **Plattformen (Werbung + Baukästen):** реклама доносит фейк (факт 3.2 + цитата Pop).
  - **Browser/Sicherheitssysteme:** защищают частично, но обман умеет прятаться (Teil 4).
  - **Nutzer:** «будь внимательнее» — не решение, если проверка подтверждает обман, а замок рисуется.
- Финальный тезис: обман построен из наших же стандартов доверия → защита должна быть
  системной, а не сваливаться на глаз отдельного человека.

### Teil 6 — Lösungen ❓ (не решён, см. §2)

---

## 5. Дизайн-система „Blueprint + X-Ray" (Bauplan & Röntgen)

**Концепция:** обман — это конструкция с чертежом. Сайт показывает идеальный интерфейс,
а «Рентген» проявляет под ним чертёжные линии и красные подписи-выноски обмана.

- **Тема:** тёмная. Фон ~`#070b14`. Тонкая чертёжная сетка (мелкая + крупная), приглушённый
  cyan/blue. Технические засечки, координаты, угловые перекрестия — как на архитектурном чертеже.
- **Типографика:** гротеск (Inter / Space Grotesk) для заголовков/текста; моноширинный
  (JetBrains / IBM Plex Mono) для URL, метрик, номеров, техписей. Есть системные фолбэки (офлайн).
- **Палитра:** cyan/blue = «структура» (нейтраль). ОДИН сигнальный красно-оранжевый
  (`#ff3b30` / `#ff4d2e`) — ТОЛЬКО там, где проявляется обман. Не «хакерский» китч, а премиально.
- **Сигнатурное взаимодействие — Röntgen (клавиша `X`):** полированный UI гаснет в каркас,
  проступают красные выноски: „Kopierte Komponente", „Gefälschte Domain", „Künstliche
  Dringlichkeit", „Original-Logo 1:1 übernommen", „Fremdes Impressum".

### 5.1 Исключение: розовая «бутик»-тема (только слайды 03–04, игра + раскрытие)
Намеренный разрыв с тёмным чертежом — мир «магазина», в стиле настоящей визитки
Per la Donna (`assets/perladonna-visitenkarte.png`). Премиально, без китча.
- **Токены** (`:root`, префикс `--pk-`): фон `--pk-bg #f2dde3` / `--pk-bg-2 #efd6de`,
  текст `--pk-ink #2b1c21`, rose-gold `--pk-gold #c98f86`, rose `--pk-rose #b76e79`,
  мелкий текст `--pk-rose-ink #9b5563`, штамп `--pk-stamp #c0304a`.
- **Шрифты:** Playfair Display (заголовки, курсив для акцентов) + Jost (разреженные капители);
  фолбэки Georgia/serif и Futura/Century Gothic/Segoe UI.
- **Орнамент:** линия — двойное сердечко — линия; точечные сетки в верхних углах; акварельные
  пятна (SVG turbulence) и тонкие rose-gold дуги — во вьюпорт-слое `.blush`.
- **Механика:** хуки ставят `body.on-pink` → `.blush` и `.pk-deco` проявляются, чертёжная рамка
  скрывается, нижняя панель (секция/счётчик/прогресс) перекрашивается в розовое. Весь прочий CSS
  — под `.s-pink`; другие слайды не затронуты. Рентген на 03–04 отключён.

---

## 6. Техническое состояние `index.html`

**Файл:** `index.html` — один самостоятельный файл (inline CSS+JS, без сборки,
Google Fonts + системные фолбэки). JS проходит `node --check`. Собрано: интро-слайд (slide 00,
на кейсе Suchly/Ardenza/Per la Donna) + 5 слайдов Teil 0–1 (см. §4).
⚠️ Идёт параллельная работа: сессия `present-tion-68` правит интро/1.1 (Suchly-вордмарк,
токены `--su-*`, `.paper`, `Hooks.intro`, `'r'`-key). Координация: только targeted Edit,
не full-file Write; предупреждать перед правкой её зон.

**Управление:**
- Вперёд (шаг/слайд): `→` / `Space` / `PageDown` / `Enter`
- Назад: `←` / `PageUp` / `Backspace` (возврат на последний шаг предыдущего слайда)
- `X` — Röntgen (только слайды с `data-xray`: 1.1 `vorfall` и 1.2 `reaktion`; сбрасывается при смене слайда)
- `R` — повтор анимации интро-слайда (slide 00) и расслоения магазина (slide 06 `bausteine`)
- `F` — полный экран; `Home` / `End` — первый/последний слайд
- Мышь/тач: клик по левому/правому краю экрана; свайп
- Низ: секция, точки-шаги, счётчик, кнопка X-Ray, прогресс-бар
- URL-hash хранит позицию (напр. `#reaktion/2`)
- Флаги для скриншотов: `?instant` (финальные состояния), `?xray` (сразу рентген),
  `?t=ms` (заморозить кадр анимации интро)

**Как расширять:** каждый слайд помечен комментариями в HTML/CSS/JS. Новый слайд —
`<section class="slide">` перед `<!-- /SLIDES -->`; поведение — хук перед `/* /HOOKS */`.
Выноски рентгена — атрибуты `data-xr` на элементах макета (label, note, side, position).
**Скрытые слайды (решение заказчика 2026-09-30):** презентация заканчивается на **07 details**. Слайды teil-1 · vorfall · reaktion · schaden
**не удалены**, а помечены `data-hidden` (не показываются, не считаются). Вернуть: убрать атрибут у `<section>` или открыть с `?all`.
Счётчик `NN / NN` и прогресс считаются из числа `.slide` автоматически (сейчас 11 слайдов:
01 intro · 02 titel · 03 spiel · 04 aufloesung · 05 ausmass · 06 bausteine · 07 details · 08 teil-1 · 09 vorfall · 10 reaktion · 11 schaden).

**Слоты изображений (ассеты):**
| Файл | Где | Статус |
|---|---|---|
| `assets/fake-shop-klassik.jpg` (1920×1080) | слайды 03–04, окно A (`perladonna-shop.de`) | ✅ скрин `Fake-Shop-Boutique-Klassik.html` |
| `assets/fake-shop-b.jpg` (1920×1080) | слайды 03–04, окно B (`perla-donna.store`); слайд 06 (всплывашка + копии) | ✅ скрин `per-la-donna-mockups/shop-b-v2.html` |
| `assets/fake-shop-b-base.jpg` (1920×1080) | слайд 06, слои блоков + вырезки | ✅ тот же shop-b-v2 без `.toast` (1440×810 @1.333) |
| `assets/fake-shop-b-clean.jpg` (1920×1080) | слайд 06, подложка для перестановки блоков | ✅ shop-b-v2 без toast, логотипа, иконок, текста/фото баннера, карточек |
| `assets/perladonna-warnhinweis.png` | слайд 04, «Beweisstück» (CSS-вырез карточки, имя закрыто) | ✅ |
| `assets/perladonna-visitenkarte.png` | слайд 04, «Das Original» (CSS-вырез карточки) | ✅ |
- Скриншоты магазинов: **16:10** (напр. 1440×900 @2x), БЕЗ рамки браузера/URL (их рисует HTML).
  Вставляются `object-fit: cover`, выравнивание по верху. Пока файла нет — розовая заглушка
  „Screenshot A/B folgt" (через `img onerror` → `.is-missing`), слайд работает и так.
- Просто положить файлы с этими именами в `assets/` — правок в `index.html` не нужно.

**Слабые места (доработать):**
- Пара leader-линий пересекает картинки (слайды 02 и 03).
- Каркас в рентгене можно сделать более «призрачным».
- `assets/perladonna-warnhinweis.png` — только слайд 04 (Beweisstück). Из 1.3 убран (без повтора).
- Не проверен офлайн-вид (фолбэки Segoe UI / Consolas) и свайп на реальном устройстве.
- ✅ Сюжет ShopNova полностью выведен из Teil 1 (1.1–1.3 на реальном кейсе). В глобальном CSS
  остался неиспользуемый комментарий/токен `--sn`/`.sn-logo` (стили `.sn` переиспользованы в 1.2).

---

## 7. Правила и ограничения (для всех агентов)

1. **Только вымышленные бренды.** Никаких копий логотипов/брендинга Amazon, Google, реальных
   банков. Вымышленные: «ShopNova», поисковик «Findr» и т.п. Реальные названия из кейса
   (Per la Donna, Ardenza, Bremen) допустимы — у них есть источник; имя владельца на слайдах
   лучше скрыть до решения заказчика.
2. **Никаких выдуманных цифр.** Только факты из §3 или явные плейсхолдеры `[… — Quelle einfügen]`.
3. **Никаких выдуманных источников.** Не ставить URL/цитату, которой нет в §3.
4. **Teil 4 — уровень осведомлённости, не инструкция.** Объясняем механизм и почему опасно;
   без пошаговых операционных деталей атаки.
5. **Макеты — не рабочие сайты.** Всё внутри презентации; никаких реальных форм сбора данных.
6. **Немецкий текст слайдов — verbatim.** Не переводить, не «улучшать» без запроса.
7. **Обновлять этот файл** при любых изменениях структуры/фактов + запись в Changelog.

---

## 8. Changelog

- **2026-09-30** — Создан PROJECT.md. Зафиксированы: концепция, кейс Per la Donna и факты
  §3.1–3.6 с источниками, структура Teil 0–5 + игра, дизайн-система, состояние прототипа
  `index.html` (5 слайдов на ShopNova), правила. Открытые вопросы в §2.
- **2026-09-30** — Сессия `present-tion-68` собрала интро-слайд (slide 00) на реальном кейсе
  (поисковик Suchly → запрос про Per la Donna → 3 фейк-объявления на доменах ardenza.*).
  Слайд 1.1 переведён с «Findr» на «Suchly». Добавлены управление `R` и флаг `?t=ms`.
  Зафиксирована оговорка про драматизацию рекламы Ardenza. Обновлены §4, §6.
- **2026-09-30** — РЕШЕНИЕ заказчика: сквозной сюжет — ВЕЗДЕ реальный кейс Per la Donna /
  Ardenza (не ShopNova). Запущена конвертация слайдов 1.1–1.3. §2, §4 обновлены.
- **2026-09-30** — Собраны слайды **03 „Welche Website ist echt?"** (`spiel`, игра: 2 фейк-магазина
  A/B, «сомневающийся» курсор, шаг-голосование) и **04 „Keine ist echt."** (`aufloesung`: штампы
  FAKE → Beweisstück-Warnhinweis с закрытым именем + настоящая визитка perladonna.de → таймлайн
  фактов §3.1). Новая розовая тема (§5.1, `body.on-pink`, токены `--pk-*`, Playfair Display + Jost).
  Слоты `assets/fake-shop-a.png` / `-b.png` с заглушкой (§6). Старая идея «3 магазина, делаем сами»
  заменена (§4). Уточнение: в брифе «суд» → по источнику **Strafanzeige** (не судебный процесс).
- **2026-09-30** — Собран слайд **05 „Das Ausmaß"** (`ausmass`, тёмная тема): цифры vzbv сверху/снизу
  (count-up), в центре Suchly-цикл из 4 запросов с одинаковыми результатами → штампы „Fake-Shop“
  (иллюстрация, не статистика); шаг 1 — нachgestellte KI-Übersicht рекомендует ardenza.store +
  факты §3.7 (Netcraft 34 %, Guardio „Scamlexity“). Добавлен §3.7; Gemini на слайде не называется
  (нет источника). Сессия `present-tion-ae` параллельно ставит 06 „Die Maschine“ сразу после.
- **2026-09-30** — Слайды Teil 1 **1.1 vorfall / 1.2 reaktion / 1.3 schaden** сконвертированы
  с вымышленного ShopNova на реальный кейс Per la Donna / Ardenza (мой build-агент, targeted Edits,
  node --check ok). 1.1: Suchly-запрос → объявление ardenza.store (оговорка «Dramatisierung» в рентгене).
  1.2: сравнение настоящей perladonna.de (визитка, без магазина) vs фейк ardenza.store с УКРАДЕННЫМ
  Impressum (та же бременская GmbH) — «проверка подтверждает обман»; heatmap/«Blinder Fleck» сохранены.
  1.3: заголовок „Zwei Opfer.", асимметрия усилий („Unser Aufwand" стек vs „Ctrl+C"), две жертвы
  (Käufer + ehrlicher Händler: Strafanzeige 27.03.2026), цифра vzbv 12 % (§3.2), плейсхолдеры ущерба,
  закрывающая цитата владельца „…dem Laien ist dieser Blick meist nicht möglich" + „…gegen uns."
  ✅ Warnhinweis-скриншот НЕ дублируется: остался только в слайде 04, из 1.3 убран.
  1.2: заголовок „Kein einziges Warnsignal." (игру A/B не дублирует — она в слайде 03).
  Переиспользованы классы интро (.suchly, .pd-mark, .pd-word, --su-*, --f-serif); 1.2 не зависит от `--pk-*`.
  ⚠️ Цитата „…dem Laien…" (§3.1, изначально для Teil 2) теперь закрывает 1.3 → в Teil 2 не повторять.
- **2026-09-30** — Сессия `present-tion-ae`: §3.6 переписан — «опора на ИИ»: модель «Die Maschine»
  (KI 1 анализирует данные и строит клон, который может рекламироваться лучше оригинала → KI 2 разносит
  его как «оригинал» → импульсивный покупатель — «заложник собственных желаний»); источники и драматизация
  разведены. Собран слайд **06 „Die Maschine"** (`maschine`, 3 шага, CSS-анимация руки с вымышленным
  KI-чипом, `R` — повтор; §4, §6). Порядок согласован с `present-tion-32`: 05 ausmass → 06 maschine → teil-1.
  Немецкий текст 06 — черновик до текста заказчика. Факты §3.7 на 06 не повторяются.
- **2026-09-30** — Слайды 03/04: в окна A/B подставлены готовые скрины (`assets/fake-shop-klassik.jpg` = A,
  `assets/fake-shop-b.jpg` = B / shop-b-v2). Окна `.pk-view` 500→450px (16:9 под скрины 1920×1080, без обрезки по бокам).
- **2026-09-30** — Сессия `present-tion-ae`: слайд 06 **переделан** по решению заказчика —
  „Die Maschine" (рука с KI-чипом, две ИИ) → **„Alles nur Bausteine"** (`data-id="bausteine"`): магазин B
  из игры наклоняется в изометрию и расслаивается на 7 блоков + 8-px-растр (подписи с выносками) →
  Strg+C / Strg+V и «откуда блок» → ИИ собирает копии ardenza.store/.de/.com → золотые рамы
  («Wiederholbare Kunst», „Original: nicht vorhanden"). §3.6 переписан под тезис «дизайн = набор блоков».
  Новый ассет `assets/fake-shop-b-base.jpg` (shop B без всплывашки). Немецкий текст — черновик.
- **2026-09-30** — Собран слайд **07 „Der Teufel steckt im Detail"** (`details`, после bausteine, перед teil-1,
  тёмная тема, 3 шага): магазин B как живой HTML в окне браузера + скриптовый курсор-покупатель (меню, корзина,
  поп-ап −10 %, перезагрузка → таймер всегда 03:59:12) → метки 1–6 «в магазине» → проверки 7–11 «снаружи»
  (карточки „nachgestellt") → Fazit „Einzeln harmlos. Zusammen ein Muster." Курсорная физика взята по ссылке
  из `Hooks.spiel` (без правки). Шрифт Cormorant Garamond дополнен прямым начертанием 500/600. §4, §6 обновлены.
- **2026-09-30** — Сессия `present-tion-ae`: слайд 06 „Alles nur Bausteine" **v2** по замечаниям заказчика —
  светлая бело-розовая «деко»-тема (`body.pk-clean`), крупные подписи (01)–(08), сетка + контур блоков как база в
  самом низу; эпизоды: (01) расслоение → (02) сайт лицом к залу, петля копий с другими именами → (03) приближение,
  блоки меняются местами по кругу. Золотые рамы убраны. Новый ассет `assets/fake-shop-b-clean.jpg`. §4, §6.
- **2026-09-30** — Сессия `present-tion-ae`: слайд 06, эпизод (03) переделан → **„Vorlagen"**: курсор наводится на
  шапку/баннер/карточку, всплывают листы гайдлайна с готовым шаблоном; шаблон карточки вытягивается, повторяется ×4
  и заполняется (петля). Перестановка блоков убрана. На слайде текстом названы Material Design (Google) и Human
  Interface Guidelines (Apple), без логотипов. §3.6, §4.
- **2026-09-30** — Слайд **07 „Der Teufel steckt im Detail“ v2** по замечаниям заказчика: светлая бело-розовая тема слайда 06
  (`on-pink` + `pk-clean`), верхняя легенда (01)–(05), 5 шагов (`data-steps="4"`). Новое: (02) «Der Blick» — прожектор взгляда по
  приманкам 1–7 с пузырями «внутреннего голоса» и шкалой „Nachdenken → Kaufimpuls“ (заменил красные метки 1–6 и демо-перезагрузку);
  (04) «Das Detail» — футер магазина с 5 нachgestellten ошибками, курсор-лупа. Проверки 7–11 перенумерованы в 1–5. §4 обновлён.
- **2026-09-30** — РЕШЕНИЕ заказчика: доклад заканчивается на слайде **07 „Der Teufel steckt im Detail“**. Слайды 08–11 (Teil 1: teil-1,
  vorfall, reaktion, schaden) скрыты атрибутом `data-hidden` (остаются в файле; `?all` показывает их снова). Счётчик теперь 07 / 07. §6.
