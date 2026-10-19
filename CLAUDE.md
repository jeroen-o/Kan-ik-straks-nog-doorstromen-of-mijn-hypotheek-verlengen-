# Kan ik straks nog doorstromen of mijn hypotheek verlengen?

Onafhankelijke gesprekshulp over hypotheekregels **nu en straks**, in Nederland en Europa. Live op
https://jeroen-o.github.io/Kan-ik-straks-nog-doorstromen-of-mijn-hypotheek-verlengen-/ (GitHub Pages vanaf `main`).

Doel: een gesprek met de klant op gang brengen. De klant ziet wat er in Europa en in andere landen gebeurt, kiest
zelf uit drie scenario's (mild, strakker, streng) en ziet wat dat voor zijn eigen situatie kan betekenen.
Uitgangspunt: de regels worden strakker; hoe streng is onzeker.

## Afbakening: wat hoort hier wel en niet

Dit project is **niet** de demosite **demo-hypotheekkantoor** (repo `jeroen-o/demo-hypotheekkantoor`, live op
https://demo-hypotheek-kantoor.nl/). Die site gaat over een fictief hypotheekadvieskantoor.

| Hoort hier | Hoort in demo-hypotheekkantoor |
| --- | --- |
| Regels nu en straks, nieuws over bankbeleid (Rabobank, ABN AMRO, ING) | Het fictieve kantoor, zijn diensten, kosten, nazorg en documenten |
| Toekomstscenario's, stressscenario, rol van ECB/EBA/DNB | Rekenhulppagina's van het kantoor |
| De gesprekshulp en de Europa-vergelijking | Uitleg vanuit het kantoor over woning, fundering en verduurzaming |

- Geen gegevens of branding van het demokantoor op deze site (geen "Demo Hypotheek kantoor", geen fictieve AFM-,
  KvK- of Kifid-nummers, geen links naar demo-pagina's).
- Neutrale toon: geen "wij" van een kantoor; verwijs naar "een hypotheekadviseur".
- Twijfel je bij een nieuwe opdracht in welke repo iets hoort? Vraag het de gebruiker voordat je bouwt.

## Werkwijze

- Elke pagina is één zelfstandig HTML-bestand: CSS en JavaScript inline, geen build-stap, geen externe scripts of
  API's, geen cookies, geen `localStorage`. Pagina's: `index.html` (gesprekshulp), `regels.html`,
  `scenario-2035.html`, `europa.html`, plus `404.html`.
- Printen via `window.open()` (werkt ook in een iframe, zoals Google Sites), nooit `window.print()` direct.
- Nederlands, u-vorm, Nederlandse getalnotatie (`&euro;&nbsp;1.234,56`); euro-invoervelden met duizendtalpunten.
- Bij nieuwe of gewijzigde pagina's: `sitemap.xml`, `llms.txt`, canonical, `og:*` en JSON-LD bijwerken.
  Metabeschrijvingen hoogstens 160 tekens; één `<h1>` per pagina.
- Controleer na wijzigingen dat alle interne links en ankers bestaan en dat de JSON-LD geldig is.

## Inhoud en compliance

- Alles is een indicatie of scenario met een datum ("stand ..."). Scenario-uitspraken krijgen een zekerheidslabel:
  besloten, waarschijnlijk of mogelijk. Presenteer een verwachting nooit als feit.
- Vermeld bronnen; markeer wat niet in een primaire bron is gecontroleerd.
- Benoem bij AFM- of compliance-relevante claims het risico. Niet sturen naar een product en niet inspelen op angst.
