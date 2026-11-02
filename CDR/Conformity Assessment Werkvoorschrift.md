# Werkvoorschrift: Conformity Assessment (CA)

**Documenttype:** Werkvoorschrift  
**Versie:** 0.1  
**Auteur:** AI Compliance Officer  
**Datum:** september 2026  
**Status:** Concept

## 1. Doel en achtergrond

Een **Conformity Assessment** (CA) legt per AI-systeem en per wettelijk thema vast welke besluiten zijn genomen om aan de EU AI-verordening te voldoen. Het document volgt de MADR-structuur (Markdown Any Decision Records) en maakt aantoonbaar — richting toezichthouder en intern — hoe en waarom specifieke maatregelen zijn gekozen.

Per thema (bijv. cybersecurity, databeheer, menselijk toezicht) bestaat één CA-document. Dat document bevat meerdere individuele besluiten, elk beschreven als een afzonderlijk MADR-record.

De CA is **geen eenmalig product**: het is een levend document dat wordt bijgehouden zolang het AI-systeem in gebruik is.


## 2. Wanneer maak je een Conformity Assessment?

Een nieuwe CA wordt opgesteld wanneer:

- een AI-systeem voor het eerst wordt beoordeeld op een specifiek wettelijk thema (initieel nulpunt), of
- een thema nog niet eerder gedocumenteerd is voor een bestaand systeem.

Een bestaande CA wordt herzien wanneer (zie ook deel B, §6):

- een significante wijziging plaatsvindt in het systeem of de maatregelen,
- er een incident heeft plaatsgevonden dat raakt aan het thema,
- er nieuwe pentest-bevindingen of post-market monitoring feedback is,
- de jaarlijkse herzieningsdatum bereikt is, of
- de toezichthouder om aanvullende documentatie verzoekt.


## 3. Naamgeving en opslag

**Bestandsnaam:** `CA-[artikelnummer]-[systeemnaam]-[volgnummer]`

Voorbeelden:
- `CA-015-HANSKEN-01` → Conformity Assessment voor Art. 15, systeem Hansken, eerste versie
- `CA-010-HANSKEN-01` → Conformity Assessment voor Art. 10, systeem Hansken

**Opslag:** in de centrale map van het AICO-team, per systeem georganiseerd.  
**Versienummering:** major.minor (bijv. `0.1` = concept, `1.0` = formeel vastgesteld).

## 4. Structuur van een Conformity Assessment

Elk CA-document bevat de volgende vaste secties:

| Sectie | Inhoud |
|---|---|
| **Frontmatter** | Status, datum, besluitvormers, rechtsgrondslag, scope |
| **1. Besluiten** | Per besluit een MADR-record (zie §5) |
| **2. Maatregelen niet van toepassing** | Welke maatregelen buiten scope vallen en waarom |
| **3. Motivering t.o.v. wettelijke eis** | Traceerbaarheidstabel: maatregel → AIV-artikel |
| **4. Bevestiging conformiteit** | Overzicht conformiteitsstatus per maatregel |
| **5. Openstaande acties** | Acties die nog moeten worden uitgevoerd |


## 5. Structuur van een individueel besluit (MADR)

Elk besluit binnen de CA volgt onderstaande vaste opbouw. **Vul alleen in wat je weet.** Velden waarvoor geen informatie beschikbaar is, markeer je expliciet als *niet gedocumenteerd — nader in te vullen*.

```
### [Besluitnummer]: [Korte titel]
Adresseert: [maatregel(en)]  |  Grondslag: [AIV-artikel(en)]

#### Context and Problem Statement
[Beschrijf het probleem of de afweging in 2-4 zinnen. Sluit af met een vraag
 die het besluit afbakent.]

#### Considered Options
* [Gekozen optie — beschrijf kort]
* [Overwogen alternatief, indien gedocumenteerd]

#### Decision Outcome
Chosen option: "[titel gekozen optie]", omdat [korte motivering die aansluit
 op de wettelijke eis].

#### Consequences
* Good, because [positief gevolg — indien gedocumenteerd]
* Bad, because [negatief gevolg / restrisico — indien gedocumenteerd]
```

**Regels:**
- Verzin **nooit** voor- of nadelen die niet in het bronmateriaal staan. Markeer ze als niet gedocumenteerd.
- Overwogen alternatieven neem je alleen op als ze expliciet zijn besproken.
- De "Decision Outcome" verwijst altijd naar de gekozen optie bij naam.

## Deel A — Voor de AI Compliance Officer

### A1. Voorbereiding

Doe het volgende voordat je het interview ingaat:

1. Bepaal het AI-systeem en het thema (welk AIV-artikel).
2. Zoek de relevante maatregelenlijst op (bijv. M1–M11 voor Art. 15 cybersecurity).
3. Raadpleeg de **invulinstructie** van het betreffende thema. De invulinstructie bevat de interviewvragen per maatregel en is een apart werkdocument — het maakt geen onderdeel uit van de CA zelf.
4. Stel vast wie de thema-eigenaar is (degene met de technische kennis van het thema).

### A2. Het interview

- Plan een werksessie met de thema-eigenaar (en eventueel andere betrokkenen).
- Loop de invulinstructie per maatregel door en noteer de antwoorden.
- Vraag expliciet door op:
  - Welke maatregelen **al actief** zijn ingericht.
  - Welke maatregelen **in uitvoering** zijn of nog moeten worden opgepakt.
  - Welke maatregelen **niet van toepassing** zijn en waarom.
  - Of er **alternatieve opties overwogen** zijn (ook al zijn ze niet gekozen).
- Verzin niets zelf. Als iets onduidelijk of niet bekend is, noteer het als openstaande vraag.

### A3. Document opstellen (nulpunt)

Na het interview:

1. Maak een nieuw CA-document aan met de juiste bestandsnaam (zie §3).
2. Vul de **frontmatter** in: status op `gedeeltelijk` of `niet conform` (nooit direct `conform` voor een nulpunt), datum, thema-eigenaar, rechtsgrondslag.
3. Schrijf per maatregel de besluiten uit in MADR-structuur (zie §5).
4. Besluiten waarvoor je geen informatie hebt: vermeld de context wel, maar markeer de opties en gevolgen als niet gedocumenteerd.
5. Vul de **traceerbaarheidstabel** in (sectie 3): koppel elk besluit aan de maatregel en het AIV-artikel.
6. Vul de **bevestigingstabel** in (sectie 4): geef per maatregel de conformiteitsstatus.
7. Noteer alle **openstaande acties** (sectie 5): onduidelijkheden, ontbrekende informatie, te ondernemen stappen.

### A4. Oplevering

1. Stuur de conceptversie naar de thema-eigenaar ter review.
2. Verwerk eventuele correcties (inhoudelijk, niet redactioneel).
3. Zet de versie op `0.1` en lever op aan de thema-eigenaar voor beheer.
4. Leg vast in de frontmatter wie het document heeft opgesteld en wie het beheert.


## Deel B — Voor de thema-eigenaar

### B1. Jouw rol

Als thema-eigenaar ben jij verantwoordelijk voor het actueel houden van de CA na de initiële oplevering door de AI Compliance Officer. Je bent degene met de technische kennis van het thema; de CO is de gesprekspartner en toetst of de CA voldoet aan de vereisten van de AI-verordening.

### B2. Wanneer update je de CA?

Je werkt de CA bij wanneer er iets **verandert in het systeem of de maatregelen** dat raakt aan de besluiten die er al in staan. Gebruik de onderstaande criteria om te bepalen of een wijziging **significant** is.

### B3. Wat is een significante wijziging?

Een wijziging is significant als:

- een maatregel die al in de CA staat **anders wordt ingericht** (bijv. andere tooling, ander proces),
- een **nieuwe maatregel** wordt toegevoegd of een bestaande vervalt,
- de **conformiteitsstatus** van een maatregel verandert (bijv. van gedeeltelijk naar conform),
- er een **beveiligingsincident of pentest-bevinding** is die raakt aan een besluit, of
- de **scope van het systeem** verandert (bijv. nieuw gebruikerstype, nieuwe module).

Kleine tekstuele correcties of updates van links/bewijsstukken zijn geen significante wijziging.

### B4. Hoe voer je een update door?

1. Ga naar het relevante besluit in de CA (bijv. B3 voor CVE-scanning).
2. Pas de tekst aan onder de juiste MADR-sectie.
3. Als een nieuwe optie werd overwogen: voeg die toe onder "Considered Options".
4. Als de gevolgen nu bekend zijn: vul de "Consequences" in (verwijder "niet gedocumenteerd").
5. Verhoog het versienummer (bijv. van `0.1` naar `0.2`).
6. Stuur een bericht naar de AI Compliance Officer met een korte toelichting op wat er is veranderd en of de wijziging significant was.

### B5. Status van het document

De status in de frontmatter geeft de conformiteitsstand per thema weer:

| Status | Betekenis |
|---|---|
| `niet conform` | Eén of meer maatregelen zijn niet ingericht; actie vereist |
| `gedeeltelijk` | De meeste maatregelen zijn ingericht, maar er zijn nog openstaande punten |
| `conform` | Alle verplichte maatregelen zijn aantoonbaar ingericht en gedocumenteerd |

De status wordt vastgesteld door de AI Compliance Officer op basis van de bevestigingstabel (sectie 4 van de CA). De thema-eigenaar past de status **niet zelfstandig** aan.

### B6. Jaarlijkse herziening

Ieder jaar controleert de thema-eigenaar — samen met de AI Compliance Officer — of de CA nog actueel is. Agenda-items voor de jaarlijkse herziening:

- Zijn alle openstaande acties afgehandeld?
- Zijn er nieuwe kwetsbaarheden of incidenten geweest?
- Zijn er wetswijzigingen of nieuwe richtsnoeren die raken aan het thema?
- Zijn er systeemwijzigingen geweest die nog niet zijn verwerkt?

Na de herziening wordt de versie verhoogd en de datum bijgewerkt.



## 6. Relatie tot andere documenten

| Document | Relatie |
|---|---|
| **Invulinstructie** (per thema) | Bevat de interviewvragen; separaat werkdocument, niet onderdeel van de CA |
| **Technische documentatie** | Bewijsstukken worden gelinkt vanuit de CA (sectie 1 frontmatter) |
