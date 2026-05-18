# Moonly – Landing Page

Modern, sötét témájú, magyar nyelvű landing page a **Moonly** női egészség és menstruációs ciklus követő mobilalkalmazás számára.

## Technológia

- **HTML5** – szemantikus jelölőnyelv
- **Tailwind CSS** (CDN) – utility-first CSS framework
- **Egyedi CSS** (`styles.css`) – placeholder jelölés, scrollbar, animációk
- **Google Fonts** – Gabarito (sans, fő betűtípus) + Fraunces (serif, dekoratív címek)

A teljes stílus a **`Mode 1.tokens.json`** Figma változókból építkezik. A színek a Tailwind config-ban így vannak elnevezve:

| Tailwind név | HEX | Eredeti név |
|---|---|---|
| `bg-text` / `text-text` | `#F5E5F6` | Text |
| `bg-background` | `#1C091E` | Background |
| `bg-primary` | `#DA93E2` | Primary |
| `bg-secondary` | `#7B1F85` | Secondary |
| `bg-accent` | `#D3C120` | Accent |
| `bg-foreground` | `#250F28` | Foreground |
| `bg-period` | `#E56164` | PeriodColor |
| `bg-period-dark` | `#863E3F` | PeriodColor Dark |
| `bg-blueish` | `#6165E5` | Blueish |
| `bg-blueish-dark` | `#3D4091` | Blueish Dark |
| `bg-babyblue` | `#61A7E5` | BabyBlue |
| `bg-moonly-gold` | `#F1C768` | Moonly Gold |
| `bg-moonly-gold-dark` | `#967B3F` | Moonly Gold Dark |

## Futtatás

Egyszerűen nyisd meg az `index.html` fájlt egy modern böngészőben.

Helyi szerver futtatásához (ajánlott):

```bash
python3 -m http.server 8000
# vagy
npx serve .
```

Majd nyisd meg: `http://localhost:8000`

## Szerkezet

```
moonly_pages/
├── index.html           # A teljes landing page
├── styles.css           # Egyedi CSS kiegészítések
├── Mode 1.tokens.json   # Figma színek (referencia)
└── README.md            # Ez a fájl
```

## Asset placeholderek – Hol kell képeket cserélni?

Minden cserélendő elem a `.asset-placeholder` CSS osztályt viseli, és vizuálisan **finom átlós csíkokkal** van jelölve. Az alábbi placeholderek várnak feltöltésre, sorrendben az oldalon:

### 1. Navigáció – Logo (1 db)
- **Pozíció:** felső sáv, bal oldal
- **Méret:** 44×44 px (lekerekített négyzet)
- **Tipp:** SVG ajánlott, vagy 2× PNG (88×88 px)
- **Jelenleg:** „M" betű gradiens háttéren

### 2. Hero – Telefon mockup (1 db)
- **Pozíció:** hero szekció jobb oldal
- **Méret:** 360×760 px (9:19 arány)
- **Formátum:** PNG, átlátszó háttér ajánlott
- **Jelenleg:** lila színátmenetes placeholder lebegő animációval
- **Megjegyzés:** keret nélküli screenshot, a 12 px-es foreground border keretként funkcionál

### 3. Press / Logo bar (5 db)
- **Pozíció:** hero alatt
- **Méret:** ~120×40 px egyenként
- **Formátum:** SVG monochrome (vagy fehér PNG, átlátszó háttér)
- **Jelenleg:** „Logo 1–5" feliratos téglalapok

### 4. Kutatás – Fő vizuál (1 db)
- **Pozíció:** „246 nő hangja" szekció jobb oldal
- **Méret:** 800×1000 px (4:5)
- **Formátum:** JPG vagy PNG
- **Tartalom ötletek:** kutatási infografika, csapat fotó, abstract grafikon, vagy egy szimbolikus kép

### 5. Kutatás – Idézet kártya háttér (opcionális)
- **Pozíció:** lebegő idézet kártya a fő vizuál előtt
- **Megjegyzés:** jelenleg csak szöveges, de cserélheted résztvevő fotójára (kis kör avatár)

### 6. Betét – Fő termék fotó (1 db)
- **Pozíció:** „Új betét" szekció bal oldal
- **Méret:** 1000×1000 px (négyzet)
- **Formátum:** PNG, átlátszó háttér ajánlott
- **Tartalom:** a betét fő képe, lehetőleg studio fotó

### 7. Betét – Részlet fotók (3 db)
- **Pozíció:** fő termékfotó alatt, három kis négyzet
- **Méret:** 400×400 px egyenként
- **Tartalom javaslatok:**
  - Anyag közelkép (organikus pamut)
  - Csomagolás
  - Életstílus fotó (használat közben, diszkréten)

### 8. App showcase – 3 telefon képernyő
- **Pozíció:** „Szép. Egyszerű. A tied." szekció
- **Méretek:**
  - Bal és jobb: 220×465 px (9:19, ferdén)
  - Középső: 260×549 px (9:19)
- **Formátum:** PNG, ajánlott tartalmak:
  - Bal: **Naptár nézet** (period naplózó)
  - Közép: **Főképernyő**
  - Jobb: **Statisztikák / grafikon**

### 9. Tudástár – Cikk borítók (3 db)
- **Pozíció:** „Orvosi tudástár" szekció
- **Méret:** 800×600 px (4:3)
- **Formátum:** JPG vagy WebP
- **Témajavaslat:**
  1. Ciklus fázisai (period színű háttér)
  2. PMS vs PMDD (kék színű háttér)
  3. Hormonok és táplálkozás (arany színű háttér)

### 10. Vélemények – Avatárok (3 db)
- **Pozíció:** „Több ezer nő már megtalálta" szekció
- **Méret:** 48×48 px (kör)
- **Formátum:** JPG/PNG, fejlövés portré
- **Jelenleg:** színátmenet + monogram

### 11. CTA – QR kód (1 db)
- **Pozíció:** „Készen állsz, hogy megismerd magad?" szekció
- **Méret:** 192×192 px (négyzet, lekerekített)
- **Formátum:** PNG, fehér háttéren fekete QR
- **Generálás:** pl. https://www.qr-code-generator.com – app store smart link-re mutasson

### 12. Footer – Logo (1 db)
- **Pozíció:** footer bal oldal
- **Méret:** 40×40 px
- **Megegyezik** a navigáció logójával, kisebb méretben

## Placeholderek elrejtése élesítéskor

Amikor minden képet feltöltöttél, a `.asset-placeholder` osztály vizuális jelölését (az átlós csíkokat) így rejtheted el:

```html
<body class="bg-background text-text font-sans antialiased overflow-x-hidden hide-placeholders">
```

Egyszerűen add hozzá a `hide-placeholders` osztályt a `<body>` elemhez.

## Szekciók áttekintése

1. **Navigáció** – sticky, glassmorph blur
2. **Hero** – cím, leírás, CTA gombok, statisztikák + telefon mockup
3. **Press logók** – „Bemutatkozott itt" bar
4. **Funkciók** – 6 kártyás grid (ciklus, hangulat, tudástár, statisztika, emlékeztető, adatvédelem)
5. **Ekoszisztéma intro** – „Három pillér, egyetlen küldetés"
6. **01. Kutatás** – 246 nő hangja, kutatási statisztikák, idézet kártya
7. **02. Betét** – új termék fejlesztés alatt, jellemzők, várólista űrlap
8. **03. App showcase** – 3 képernyős telefon csokor + feature lista
9. **Hogyan működik** – 3 lépéses folyamat
10. **Orvosi tudástár** – 3 cikk preview
11. **Vélemények** – 3 testimonial card
12. **GYIK** – 5 nyitható kérdés
13. **CTA / Letöltés** – App Store + Google Play + QR kód
14. **Footer** – logo, linkek, közösségi média

## Akadálymentesség

- Szemantikus HTML (`<nav>`, `<section>`, `<article>`, `<footer>`)
- `aria-label` ott, ahol szükséges
- Fókuszálható elemeken láthatóságot biztosító outline
- `prefers-reduced-motion` támogatás (animációk lekapcsolása)
- Minden szín WCAG AA kontrasztot teljesít a háttéren

## Élesítés előtt

A Tailwind CDN gyors prototípusra ideális, **éles használatra** érdemes:

1. Telepíteni a Tailwind CLI-t / PostCSS-t és kibuildelni a CSS-t
2. Cserélni a `<script src="https://cdn.tailwindcss.com">` sort a buildelt fájlra
3. A betűtípusokat optionálisan self-hostolni
4. Hozzáadni meta open graph képeket
5. Bevezetni egy favicon-t
