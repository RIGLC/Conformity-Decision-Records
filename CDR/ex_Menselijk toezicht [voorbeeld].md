# Menselijk toezicht gezichtsherkenningssysteem

| | |
|---|---|
| **status** | gedeeltelijk |
| **date** | 2026-09-15 |
| **end responsible** | Yolanda |
| **consulted** | Mary Tielman (AI Compliance Officer) |
| **rechtsgrondslag** | Art. 14.1 t/m 14.5 AI-verordening |
| **bewijsstukken** | ONTBREEKT, links toe te voegen |
| **herzieningsmoment** | Jaarlijks of eerder bij significante wijziging in het systeem of de werkinstructies |
| **scope** | AI-systeem 1 |


## 1. Besluiten

## B1: Elk resultaat vereist een menselijke beoordeling voordat het gebruikt wordt

*M1: Ontwerp en ontwikkel maatregelen voor effectief toezicht | Grondslag: Art. 14.1*

### Context and Problem Statement

Het AI-systeem geeft per zoekopdracht een lijst van mogelijke personen terug, gesorteerd op betrouwbaarheidsscore. Mag de output automatisch opgenomen worden in het dossier zodra de betrouwbaarheidsscore hoog genoeg is? Of moet een forensisch onderzoeker elk resultaat eerst handmatig beoordelen?

### Considered Options

* Verplichte menselijke beoordeling van elk resultaat, ongeacht de betrouwbaarheidsscore.
* Automatisch doorsturen naar het dossier bij een score boven een vastgestelde drempelwaarde (bijv. vanaf 95%), handmatige beoordeling alleen bij twijfelgevallen (alles onder 95%).

### Decision Outcome

"Verplichte menselijke beoordeling van elk resultaat", omdat VISUS-uitkomsten worden gebruikt in strafrechtelijke context. Een fout, ook bij een hoge score, kan ernstige gevolgen hebben voor een verdachte. Bovendien kan de betrouwbaarheidsscore misleidend zijn bij slechte beeldkwaliteit of wanneer de referentiedatabase onvolledig is. De wet vereist dat de operator de uitkomst altijd kan beoordelen en afwijzen.

### Consequences

* Goed, want elke conclusie over een identiteit is menselijk gevalideerd voordat er consequenties aanzitten.
* Slecht, want dit vertraagt de doorlooptijd, zeker bij grote aantallen vergelijkingen. Dit vraagt om realistische capaciteitsplanning binnen het team.

## B2: Het AI-systeem geeft aan welke gezichtskenmerken de betrouwbaarheidsscore hebben bepaald

*M2: Maak een mens-machine-interface mogelijk · M7: Borg de transparantie | Grondslag: Art. 14.1, 14.4.a, 14.4.c, 14.5*

### Context and Problem Statement

Een betrouwbaarheidsscore van 87% zegt weinig als de onderzoeker niet weet welke kenmerken die score hebben veroorzaakt. Heeft het systeem gematcht op huidskleur, achtergrond van het beeld, kleding? Die informatie is nodig om te bepalen of het resultaat betrouwbaar is.

### Considered Options

* Alleen de eindscore en de lijst van mogelijk geïdentificeerde mensen tonen, zonder visuele toelichting.
* Een gemarkeerde laag tonen op het beeld, waaruit blijkt welke gebieden het zwaarst hebben meegewogen in de match.

### Decision Outcome

"Gemarkeerde laag met gewogen gebieden", omdat de onderzoeker zo zelf kan beoordelen of het systeem heeft gematcht op betrouwbare kenmerken, of juist op aan transformatie onderhevige kenmerken zoals haardracht of baard. Alleen met die informatie is een weloverwogen menselijke beslissing mogelijk.

### Consequences

* Goed, want de onderzoeker kan een slecht gemotiveerde hoge score herkennen en afwijzen.
* Goed, want dit verlaagt het risico van een onjuiste identificatie die alleen steunt op een percentage.
* Slecht, want de visuele uitleg vereist interpretatie. Niet alle onderzoekers lezen een heatmap/laag over het beeld even goed. Training is noodzakelijk.


## 2. Conformiteit per maatregel

| Maatregel | Omschrijving | Grondslag | Besluiten | Status | Toelichting |
|---|---|---|---|---|---|
| M1 | Ontwerp en ontwikkel maatregelen voor effectief toezicht | Art. 14.1 | B1 | Gedeeltelijk | Verplichte menselijke verificatie is ingericht. Formele werkinstructie ontbreekt nog. |
| M2 | Maak een mens-machine-interface mogelijk | Art. 14.1, 14.4.a, 14.4.c, 14.5 | B2 | Gedeeltelijk | Heatmap/laag over beeld beschikbaar in de testomgeving, nog niet uitgerold naar productie. |
| M3 | Stel een governance-model op | Art. 14.1, 14.3.a, 14.3.b, 14.4.b, 14.4.d | B3 | Gedeeltelijk | [fictief verhaal] |
| M4 | Zorg voor bewustwording en implementeer geforceerde fouten | Art. 14.1, 14.4.b | B4 | Niet conform | Trainingsprogramma is nog niet ontwikkeld. |
| M5 | Richt human in/on the loop in | Art. 14.1, 14.3.a, 14.3.b, 14.4.d, 14.4.e | B5 | Conform | [fictief verhaal] |
| M6 | Richt het risicobeheer in | Art. 14.1, 14.2, 14.3.a, 14.3.b | B6 | Niet conform | [fictief verhaal] |
| M7 | Borg de transparantie | Art. 14.1, 14.4.a, 14.4.c | B7 | Gedeeltelijk | [fictief verhaal] |
| M8 | Leg records vast | Art. 14.1, 14.4.d, 14.4.e | B8 | Gedeeltelijk | [fictief verhaal] |

## 3. Openstaande acties

1. **Werkinstructie verplichte menselijke beoordeling formeel vaststellen**, de verplichting bestaat operationeel maar is niet schriftelijk verankerd. **Deadline**:  10 Februari 2027. CDR updaten zodra de instructie is vastgesteld en gepubliceerd.
2. **Laag/Heatmap uitrollen naar productie**, de heatmap-functionaliteit is klaar in de testomgeving maar nog niet beschikbaar voor de forensisch onderzoekers. **Deadline**: 10 November 2026, afhankelijk van de releaseplanning. CDR updaten na uitrol.
   
