## Thema's beslisboom
  
| Vraag | Eis (AI-verordening) |
|---|---|
| Raakt de wijziging aan HOE het model beslist of scoort? | Nauwkeurigheid |
| Raakt de wijziging aan WAT er gebeurt als het misgaat of de invoer slecht is? | Robuustheid |
| Raakt de wijziging aan WIE er bij kan of of de data integer is? | Cybersecurity |
| Raakt de wijziging aan HOE een medewerker de uitkomst ziet of erop kan reageren? | Menselijk toezicht |
| Raakt de wijziging aan WELKE data wordt gebruikt voor training of validatie? | Datagovernance |
| Raakt de wijziging aan HOE het systeem wordt uitgelegd aan gebruikers of derden? | Transparantie |
| Raakt de wijziging aan WAT er in productie wordt gemonitord of gesignaleerd? | Post-market monitoring |
| Raakt de wijziging aan HOE fouten of schade worden geregistreerd en gemeld? | Serieuze incidenten |
| Raakt de wijziging aan WAT er wordt vastgelegd over de werking van het systeem? | Technische documentatie |
| Raakt de wijziging aan HOE er automatisch wordt vastgelegd wat het systeem doet? (logging) | Registratie |   

## Toelichting thema's   
**Conformiteitsbeoordeling**   
De verplichtingen rondom conformiteit zijn verspreid over meerdere artikelen en bijlagen van de Europese AI-verordening. Dit komt doordat conformiteit een overkoepelend thema is dat raakvlakken heeft met alle eisen uit Hoofdstuk III, Sectie 2 van de verordening. Voor de beoordeling van conformiteit specifiek, is Artikel 43 het belangrijkste artikel. Daarnaast zijn ook Bijlage VI en Bijlage VII relevant. Vanwege hun onderlinge samenhang worden deze hier gezamenlijk behandeld:

* Artikel 43 (Conformiteitsbeoordeling): Dit artikel beschrijft de voorwaarden waaraan voldaan moet worden om aan te tonen dat een hoog-risico AI-systeem voldoet aan de gestelde eisen.
* Bijlage VI (Conformiteitsbeoordeling op basis van interne controle): Deze bijlage beschrijft hoe een conformiteitsbeoordeling uitgevoerd kan worden via interne controle, dat wil zeggen door de aanbieder van het AI-systeem zelf.
* Bijlage VII (Conformiteit op basis van een beoordeling van het kwaliteitsmanagementsysteem en de technische documentatie): Deze bijlage richt zich op de beoordeling van het kwaliteitsmanagementsysteem én de technische documentatie, waarbij een aangemelde instantie (notified body) betrokken is.   

**Menselijk toezicht**  
Dit artikel bepaalt dat hoogrisico-AI-systemen moeten worden uitgerust met de benodigde technische functies om menselijk toezicht mogelijk te maken.

Het artikel is opgedeeld in de volgende vijf punten:

* Continu toezicht: Er moet effectief toezicht kunnen worden gehouden zolang de systemen in gebruik zijn.

* Risicobeheersing: Er moeten mechanismen komen die de risico's voor de gezondheid tot een minimum beperken.

* Verantwoordelijkheid: De rollen en verantwoordelijkheden moeten duidelijk worden vastgelegd.

* Transparantie en traceerbaarheid: Er moeten processen worden ingericht die zorgen voor transparantie, uitlegbaarheid en traceerbaarheid van het systeem.

* Biometrische identificatie: Bij systemen die gebruikmaken van biometrische identificatie moet menselijk toezicht te allen tijde gegarandeerd zijn.


**Data en datagovernance**  
In de context van AI is datagovernance het geheel van elementen (zoals beleid, procedures, processen en normen) dat wordt ingezet om te garanderen dat de data voor het trainen, valideren en testen van AI-systemen geschikt, relevant en voldoende representatief zijn.

Daarnaast zorgt het ervoor dat de data voldoen aan de gestelde eisen voor kwaliteit en volledigheid.

Een goede datagovernance is essentieel om AI-systemen correct en volgens hun beoogde doel te laten functioneren. Het ontbreken hiervan kan leiden tot bevooroordeelde (biased) of onnauwkeurige resultaten. Dit kan zich vervolgens vertalen in risico's voor de gezondheid, de veiligheid of de grondrechten van gebruikers.   

**Transparantie**  
De verplichtingen omtrent het genereren van transparantie zijn hoofdzakelijk te vinden in een artikel van de Europese AI-verordening, Artikel 13 "Transparantie en verstrekking van informatie aan inzetters".

* AI-systemen moeten zo ontworpen en ontwikkelt worden dat gebruikers het systeem passend kunnen begrijpen en gebruiken.
* Er moet een gebruiksinstructie verstrokken worden die beknopte, volledige, correcte en duidelijke informatie bevatten die relevant, toegankelijk en begrijpelijk is voor gebruikers.

**Nauwkeurigheid**  
In het kader van de Europese AI-verordening is nauwkeurigheid (accuracy) een vereiste om de risico's voor de gezondheid, veiligheid en grondrechten te beperken. Het vaststellen en bewaken van de nauwkeurigheid maakt het mogelijk om het gedrag van het AI-systeem te borgen en te controleren in relatie tot het beoogde doel en de gebruikte datasets. De wetgeving verplicht dat dit prestatieniveau consistent blijft en aansluit bij de stand van de techniek gedurende de gehele levenscyclus van het systeem, van marktintroductie tot uitfasering.

Nauwkeurigheid staat niet op zichzelf, maar heeft een directe samenhang met andere compliance-domeinen binnen deze Confluence-ruimte. Het vormt een directe drie-eenheid met de pagina's Cybersecurity & Robuustheid en is nauw verbonden met de pagina Transparantie & Gebruiksinstructies. De verordening vereist namelijk dat de verwachte prestatiemetrieken en de nauwkeurigheidsgraden voor specifieke (groepen) personen helder worden gecommuniceerd aan de inzetter. De verplichte vastlegging van deze niveaus, drempelwaarden en interpretatie-instructies staat beschreven op de pagina Technische Documentatie, in samenhang met de pagina's voor Data Governance en Menselijk toezicht.

Om te voorkomen dat de prestaties en nauwkeurigheidsspecificaties na ingebruikname degraderen—bijvoorbeeld door verouderde softwarebibliotheken of wijzigingen in de data—biedt deze pagina de noodzakelijke stappen om aan de wettelijke vereisten te voldoen:

* Het analyseren van kritieke punten in de levenscyclus van het AI-systeem om consistente prestaties te garanderen.

* Het selecteren van de meest geschikte metrieken voor het specifieke model en het bepalen van de bijbehorende doelfunctie (target function) tijdens de training.

* Het inrichten van concrete maatregelen en mechanismen om de nauwkeurigheid in de praktijk doorlopend te bewaken.

* Het compliant documenteren en vastleggen van het volledige proces en de bijbehorende resultaten.  

**Robuustheid**  
Dit artikel stelt eisen aan drie fundamentele aspecten: nauwkeurigheid, robuustheid en cybersecurity. Omdat cybersecurity en nauwkeurigheid in aparte thema'sworden behandeld, focust deze sectie zich specifiek op de robuustheid van hoogrisico-AI-systemen (lid 1 en 4).

* Lid 1 – Prestaties gedurende de levenscyclus: AI-systemen moeten gedurende hun hele levenscyclus voldoende nauwkeurig en robuust blijven. Prestaties mogen na ingebruikname niet verslechteren door bijvoorbeeld verouderde softwarebibliotheken of veranderende data. Systemen moeten vooraf gedefinieerde, taakspecifieke minimumniveaus van robuustheid (en bijbehorende metrieken) behalen en behouden om de veiligheid en werking te garanderen.

* Lid 4 – Bescherming tegen fouten en storingen: Er moeten maatregelen worden genomen die beschermen tegen fouten, storingen of inconsistenties.  

**Cybersecurity**  
Dit thema is onderdeel van hetzelfde artikel als robuustheid en nauwkeurigheid, maar deze sectie richt zich specifiek op cybersecurity (lid 1 en 5).

* Lid 1 – Cybersecurity over de hele levenscyclus: AI-systemen moeten gedurende hun complete levenscyclus uniform beschikken over een passend cybersecurityniveau.

* Lid 5 – AI-specifieke beveiliging: Dit lid vormt de basis voor deze gids en richt zich op specifieke cybersecuritymaatregelen en -componenten voor AI.

Weerbaarheid tegen aanvallen Volgens Artikel 15 moeten AI-systemen zo worden ontworpen en ontwikkeld dat ze bestand zijn tegen misbruik door derden, adversarial attacks (vijandige aanvallen) en data poisoning (het manipuleren van trainingsdata).

Aanvallen kunnen worden uitgevoerd door zowel legitieme als illegitieme gebruikers die het systeem misbruiken voor illegale doeleinden die afwijken van het beoogde gebruiksdoel. Denk hierbij aan een legitieme gebruiker die het systeem hackt of misbruikt om zoekopdrachten en gegevens van eerdere gebruikers te achterhalen.   

**Registratie**    
De verplichtingen voor het genereren van registraties zijn hoofdzakelijk vastgelegd in twee artikelen van de Europese AI-verordening: Artikel 12 (Registratiebeheer) en Artikel 19 (Automatisch gegenereerde logbestanden). Daarnaast zijn ook de verplichtingen voor verantwoordelijken voor de inzet van AI-systemen relevant, zoals vastgelegd in Sectie 3 van Hoofdstuk III (Verplichtingen van aanbieders en gebruiksverantwoordelijken van hoog-risico AI-systemen en andere betrokken partijen), meer specifiek Artikel 26 (Verplichtingen van gebruiksverantwoordelijken van hoog-risico AI-systemen). Vanwege de aard en inhoud van deze artikelen worden zij hier gezamenlijk behandeld:

* Artikel 12 (Registratiebeheer): Dit artikel bepaalt dat hoog-risico AI-systemen (HRAIS) de technische mogelijkheden moeten bevatten voor het automatisch genereren van registraties. Daarnaast worden een aantal voorwaarden gesteld waaraan deze registraties moeten voldoen.
* Artikel 19 (Automatisch gegenereerde logbestanden): Dit artikel geeft aan dat aanbieders van HRAIS de logbestanden die automatisch door het systeem worden gegenereerd — zoals bedoeld in Artikel 12 — moeten bewaren, voor zover deze bestanden onder hun beheer vallen.
* Artikel 26 (Verplichtingen van gebruiksverantwoordelijken van hoog-risico AI-systemen): Met betrekking tot de bewaring van registraties (lid 6) bepaalt dit artikel dat gebruiksverantwoordelijken van HRAIS de automatisch gegenereerde logbestanden — zoals bedoeld in Artikel 12 — moeten bewaren, voor zover deze bestanden onder hun beheer vallen.

**Post-market monitoring**   
Artikel 72 Post market monitoring bespreekt de factoren die vereist zijn voor de implementatie en documentatie van systemen voor toezicht na het in de handel brengen van AI-systemen met een hoog risico. Hiermee wordt beoogd te garanderen dat dergelijke systemen blijven voldoen aan de noodzakelijke vereisten die zijn uiteengezet in de AI-verordening zodra ze op de markt zijn gebracht, en gedurende de gehele levenscyclus van het systeem.

De kernmaatregelen:

* Het opzetten van toezichtsystemen die evenredig zijn aan de risico's.

* Het verzamelen, documenteren en analyseren van relevante gegevens over de prestaties van AI-systemen.

* Het opstellen van een plan voor toezicht na het in de handel brengen als onderdeel van de technische documentatie.

* De acceptatie van bestaande toezichtdocumentatie indien deze voldoet aan bepaalde wetgevingshandelingen en financiële regelgeving.

**Serieuze incidenten**   
Om te beginnen is het belangrijk om het concept van een "ernstig incident" helder te krijgen (Artikel 3, lid 49 van de AI-verordening). Dit is een incident of gebrekkige werking van een AI-systeem dat direct of indirect leidt tot:

* de dood of ernstige gezondheidsschade van een persoon;
* een ernstige en onomkeerbare ontregeling van kritieke infrastructuur;
* een inbreuk op Unierechtelijke grondrechten, of ernstige schade aan eigendommen of het milieu.
* De verplichtingen om dit te melden zijn vastgelegd in Artikel 73 van de Europese AI-verordening, "Melding van ernstige incidenten". Dit artikel verplicht tot de kennisgeving van ernstige incidenten aan de marktoezichtautoriteiten.

**Technische documentatie**   
De verplichtingen voor het opstellen van adequate technische documentatie zijn hoofdzakelijk vastgelegd in Artikel 11 (Technische documentatie) van de Europese AI-verordening. Dit artikel werkt nauw samen met Bijlage IV, waarin de specifieke inhoudseisen staan, en Artikel 18 (Bewaring van documentatie).

Vanwege hun sterke onderlinge samenhang worden deze onderdelen hier gezamenlijk behandeld:

* Artikel 11 (Technische documentatie): Dit artikel bepaalt de algemene kenmerken waar de technische documentatie van een AI-systeem aan moet voldoen. Dit loopt uiteen van de plicht om de documentatie op te stellen vóórdat het systeem op de markt komt, tot de eis om deze voortdurend actueel te houden. De documentatie moet zo zijn opgesteld dat deze objectief aantoont dat het systeem voldoet aan de eisen uit Hoofdstuk 3, Sectie II van de verordening.

* Artikel 18 (Bewaring van documentatie): Dit artikel gaat over het beheer en de opslag van alle relevante documenten. Naast de technische documentatie zelf, wordt hierin de bewaartermijn vastgelegd. Ook staat hier beschreven welke documentatie beschikbaar moet zijn zolang het systeem operationeel is en welke onderdelen gearchiveerd moeten blijven.

* Bijlage IV: Deze bijlage vormt de praktische checklist voor Artikel 11. Hierin wordt de minimale inhoud gedefinieerd die in de technische documentatie moet worden opgenomen.

