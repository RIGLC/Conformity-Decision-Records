# CDR Cybersecurity, Lauren Challis

## B1: CIS Controls uitgewerkt in beleidstukken

*M1: Passend niveau van cybersecurity en consistentie | Grondslag: Art. 15.1*  

**Context and Problem Statement**

Er was veel informatie over initiatieven rondom de cybersecurity van Hansken, maar het was niet gestructureerd en gecentraliseerd, en daarom kon compliance met cybersecurity standaarden niet bewezen worden. Daarom moet er een beleidstructuur komen om hier richting aan te geven, dit heet ook wel een ISMS (Information, security management system). Toekomstdroom is gecertificeerd te worden voor de ISO70001. 

**Considered options**  
* CIS controls en bijbehorende beleidsstukken opzetten

**Decision outcome**  
Chosen option: B1: CIS Controls, er zijn 18 beleidsstukken opgezet, dus een per CIS control. Deze staan op Confluence (link). CIS en NIST zijn veel gehanteerde standaard manieren binnen de overheid en min JenV om cybersecurity in te regelen. In het beleid van CIS zit NIST verwerkt. 

**Consequences**
* Good, because: er is structuur, er staat een basis voor de informatiebeveiliging, je geeft mensen handvaten, maar creeert ook een stok om mee te slaan. Je kan ook compliance aantonen. 
* Bad, because: het is bureaucratischer, meer papierwerk. Gemiddelde developer wordt niet blij van het lezen van 18 beleidsstukken. Developers moeten nu ook extra securitytaken oppakken die meer tijd kosten. In sum, het is veiliger, maar het werkt vanuit de developers oogpunt niet lekkerder.  

## B2: Externe pentesten

*M1: Passend niveau van cybersecurity en consistentie · M4: Bescherming adversariele aanvallen | Grondslag: Art. 15.1, 15.5*
Er is een pentest beleid opgesteld door het IT-security team, dit staat in nummer 18 van de CIS-control beleidsstukken. 

*Context and problem statement*
Het is JenV beleid en volgens de BIO moet er bij grote releases een pentest uitgevoerd worden. Pentesten worden uitgevoerd om vertrouwen bij de partners te krijgen, en om het eigen systeem te controleren. Daarnaast wordt de pentest extern uitgevoerd omdat dit ervoor zorgt dat een bias naar het eigen systeem voorkomen wordt, en dat er een nieuwe en frisse blik op de werking van het systeem komt. 

* Periodieke externe pentests, uitgevoerd bij grote wijzigingen of 1x per jaar, of op verzoek (bijv. van externen). Bevindingen gaan naar de proceseigenaar/systeemeigenaar. Er is beleid over termijnen waarbinnen geconstateerde kwetsbaarheden worden verholpen.

Chosen option: "B2: Externe pentests als primaire aanvalssimulatie", omdat er pentests worden uitgevoerd door een externe partij. Bevindingen worden gecategoriseerd en binnen vastgestelde termijnen opgevolgd. De teamlead doet de uitvraag naar een externe partij om een pentest te doen, deze externe partijen zijn o.a. Sopra Steria. De overheid biedt zelf ook pentesten aan (NAAM), maar deze duurt een stuk langer en is wel gedetailleerder dan de meeste commerciele pentesten. Overheidspentesten worden nu gedaan wanneer de software geacredditeerd moet worden voor intern gebruik. Overheidspentesten duren een stuk langer voordat er iemand langs kan komen. Het IT-security team kijkt na of de teamlead deze uitvraag heeft gedaan, en zijn betrokken vanaf begin tot einde (van intake, tot het gecentraliseerd opslaan van het eindrapport van de pentest). IT-security team zorgen er ook voor de findings uit het rapport worden opgevolgd binnen een bepaalde tijd, hier is het IT-security team de controlerende factor. 

* Good, because: je hebt een externe check, dus je voorkomt bias. Pentest-auditors zijn gespecialiseerd in hun vak, meer dan een willekeurige developer. En het dient als een bewijs naar buiten toe dat je cybersecurity serieus neemt. Het toont aan dat je als organisatie niet alleen vertrouwt op eigen kunde, maar ook een externe mee laat kijken om eventuele blinde vlekken te detecteren. 
* Bad, because: in het ergste geval zou een pentest ervoor kunnen zorgen dat het systeem uit de lucht gaat voor een korte periode. Maar over het algemeen gebeurd het in een gecontroleerde omgeving, en is die kans hier op minimaal. Risico kan zijn dat de externe partij die de pentest uitvoert het niet goed doet, en belangrijke fouten over het hoofd ziet. 

---

## B3: CVE-scanning

*M1: Passend niveau van cybersecurity en consistentie · M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Grondslag: Art. 15.1, 15.5*

Hansken maakt gebruik van externe software-componenten en bibliotheken. Vraag: hoe wordt Hansken geïnformeerd over nieuw ontdekte kwetsbaarheden in gebruikte componenten?

* Geautomatiseerde CVE-scanning op de software-componenten van Hansken.

Chosen option: "B3: CVE-scanning voor kwetsbaarheden in componenten", omdat CVE-scanning is ingericht om bekende kwetsbaarheden in gebruikte componenten te detecteren.

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B4: OWASP dependency scan

*M1: Passend niveau van cybersecurity en consistentie · M10: Bescherming side-channel aanvallen | Grondslag: Art. 15.1, 15.5*

Naast CVE-scanning worden ook kwetsbaarheden in de applicatie-afhankelijkheden systematisch in kaart gebracht. Vraag: hoe worden kwetsbaarheden in de afhankelijkheden van de applicatie bijgehouden?

* OWASP dependency scan, uitgevoerd naast CVE-scanning.

Chosen option: "B4: OWASP dependency scan voor applicatie-afhankelijkheden", omdat een OWASP dependency scan is geïmplementeerd als aanvullende maatregel op de CVE-scanning.

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B5: SAST-tooling

*M1: Passend niveau van cybersecurity en consistentie · M4: Bescherming adversariele aanvallen | Grondslag: Art. 15.1, 15.5*

Beveiligingsproblemen kunnen tijdens de ontwikkeling in de broncode worden geïntroduceerd. Vraag: hoe worden beveiligingsproblemen in de broncode vroegtijdig gedetecteerd?

* SAST-tooling (Static Application Security Testing), ingezet bij grote wijzigingen of jaarlijks.

Chosen option: "B5: SAST-tooling voor beveiligingsproblemen in broncode", omdat SAST-tooling is ingericht voor het detecteren van beveiligingsproblemen in de broncode van Hansken.

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B6: SBOM

*M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen · M3: Voorkomen manipulatie datasets | Grondslag: Art. 15.5 (raakt ook Art. 10.5)*

Om de samenstelling van het systeem en de ingezette databronnen transparant te maken, is een register nodig. Vraag: hoe worden de samenstelling van Hansken en de databronnen in kaart gebracht?

* SBOM (Software Bill of Materials) als centraal register, tevens dienend als dataleveranciersregister. Checksumcontroles op binnenkomende data waarborgen de integriteit van databronnen.

Chosen option: "B6: SBOM als dataleveranciersregister en transparantie-instrument", omdat de bronnen van dataverzameling zijn in kaart gebracht via de SBOM, die tevens dient als dataleveranciersregister. De betrouwbaarheid van binnenkomende data wordt gewaarborgd door checksumcontroles.

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B7: Container-signing

*M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Grondslag: Art. 15.5*

Hansken wordt uitgerold via containers. Vraag: hoe wordt geborgd dat alleen geautoriseerde en ongemanipuleerde containers worden uitgerold?

* Container-signing: uitgerolde artefacten worden gesigneerd om de integriteit te waarborgen.

Chosen option: "B7: Container-signing voor integriteitsborging van uitrol", omdat het systeem draait in containers waarbij artefacten worden gesigneerd om de integriteit te waarborgen.

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B8: Vierogen-/zesogenprincipe

*M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Grondslag: Art. 15.5*

Een individuele medewerker kan onbedoeld of opzettelijk kwetsbare wijzigingen doorvoeren. Vraag: hoe wordt voorkomen dat een enkele medewerker zonder controle wijzigingen aanbrengt?

* Vierogen-/zesogenprincipe: wijzigingen vereisen goedkeuring van meerdere personen, geborgd via Git.

Chosen option: "B8: Vierogen-/zesogenprincipe voor wijzigingsbeheer", omdat het vierogen- respectievelijk zesogenprincipe wordt gehanteerd om wijzigingen door meerdere personen te laten controleren. Wijzigingen zijn herleidbaar doordat de ontwikkeling in Git plaatsvindt.

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B9: SSO zonder 2FA

*M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Grondslag: Art. 15.5*

Hansken is toegankelijk voor medewerkers van opsporingsdiensten. Vraag: welk authenticatiemechanisme wordt ingezet voor toegang tot Hansken?

* SSO (single sign-on) zonder 2FA.
* SSO met 2FA (niet geïmplementeerd: binnen Hansken is geen 2FA beschikbaar).

Chosen option: "B9: SSO zonder 2FA als authenticatiemechanisme", omdat binnen Hansken geen 2FA beschikbaar is; wel staat Hansken SSO toe. Toegang wordt verder beperkt via een access list. Het risico van ontbrekende 2FA wordt bij de eerstvolgende herziening opnieuw beoordeeld.

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B10: Audit logging

*M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Grondslag: Art. 15.5*

Om afwijkend of ongeautoriseerd gebruik te detecteren, is monitoring van systeemgebruik nodig. Vraag: hoe wordt het gebruik van Hansken gemonitord?

* Audit logging zonder real-time alertering. Afwijkend gebruik wordt achteraf gedetecteerd.

Chosen option: "B10: Audit logging zonder real-time alertering", omdat ongeoorloofd of afwijkend gebruik wordt gedetecteerd via audit logging, waarbij op dit moment nog geen alertering is ingericht.

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B11: Aanpak bescherming tegen data poisoning

*M3: Voorkomen manipulatie datasets · M5: Bescherming systeemdefecten AI-systeem zelf | Grondslag: Art. 15.5*

De AI-modellen in Hansken zijn getraind op forensische data. Als trainingsdata of het model worden gemanipuleerd, kunnen uitkomsten onbetrouwbaar worden. Vraag: hoe wordt het model beschermd tegen manipulatie van trainingsdata en het model zelf?

* Het model wordt niet meer geüpdatet. De ontwikkelaars van het model (DBS) zijn niet dezelfde partij als degenen die het model in Hansken integreren (NFI).

Chosen option: "B11: Aanpak bescherming trainingsdata en model tegen data poisoning", omdat het model niet meer wordt geüpdatet. De scheiding tussen de modellerende partij (DBS) en de integrerende partij (NFI) biedt een organisatorische beveiligingslaag. De exacte beschermingsmaatregelen bij DBS zijn nog niet bevestigd (zie Openstaande acties, punt 2).

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B12: Jailbreak-detectie

*M8: Bescherming jailbreak-aanvallen | Grondslag: Art. 15.5*

Hansken bevat een copiloot-component. Jailbreaking kan ertoe leiden dat het systeem buiten zijn bedoelde grenzen wordt gebruikt. Vraag: welke maatregelen worden getroffen om jailbreaking te voorkomen en te detecteren?

* Op eigen hardware worden softwareproducten ingezet voor de detectie van jailbreaking.

Chosen option: "B12: Jailbreak-detectie op eigen hardware", omdat op eigen hardware softwareproducten zijn ingezet voor jailbreak-detectie. Of OpenHansken en de copiloot hier inherent in voorzien is nog niet nagegaan (zie Openstaande acties, punt 3).

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B13: Social engineering operators

*M11: Bescherming social engineering | Grondslag: Art. 15.5*

Operators van Hansken kunnen worden misleid via social engineering. Vraag: welke maatregelen beschermen operators tegen social engineering?

* Combinatie van: VGB-B screening, lokaal inloggen, e-learning, MFA en een time-out.

Chosen option: "B13: Social engineering maatregelen voor operators", omdat hiertegen de volgende maatregelen zijn getroffen: een VGB-B screening, de mogelijkheid om alleen lokaal in te loggen, e-learning, MFA en een time-out. Communicatiebeleid is nog in opbouw (zie Openstaande acties, punt 4).

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## 2. Maatregelen niet van toepassing

De onderstaande maatregelen zijn na beoordeling als niet van toepassing beschouwd voor de architectuur en het gebruik van Hansken. Per maatregel is de motivering opgenomen.

## M6: Bescherming inversieaanvallen en modeldiefstal

*Motivering:* Niet van toepassing. Hansken is geen open-API systeem waarbij een aanvaller via herhaalde modeluitvraag het model kan reconstrueren. Toegang tot Hansken vereist autorisatie en is niet publiek beschikbaar.

## M7: Bescherming ontwijkingsaanvallen

*Motivering:* Niet van toepassing. Hansken is geen classificerend of generatief systeem waarbij invoermanipulatie leidt tot een andere classificatie of output ten gunste van de aanvaller.

## M9: Bescherming membership inference

*Motivering:* Niet van toepassing. Gebruikers beschikken over autorisatie en de gesloten architectuur van Hansken maakt het risico op membership inference minimaal.

## 3. Bevestiging conformiteit (invullen door AI-loket)

| Maatregel | Omschrijving | Grondslag | Status | Toelichting |
|---|---|---|---|---|
| M1 | Passend niveau van cybersecurity en consistentie | Art. 15.1 | Gedeeltelijk | CIS Controls-mapping aanwezig maar niet formeel getoetst. Consistentieprocedures nog niet formeel vastgelegd. |
| M2 | Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Art. 15.5 | Gedeeltelijk | CVE, SBOM, container-signing, vierogen-principe, SSO, access list aanwezig. Geen real-time alertering. |
| M3 | Voorkomen manipulatie datasets | Art. 15.5 | Gedeeltelijk | SBOM en checksumcontroles aanwezig. Data poisoning bescherming bij DBS nog open (actie 2). |
| M4 | Bescherming adversariele aanvallen | Art. 15.5 | Gedeeltelijk | Pentests en SAST aanwezig. Geen adversarial attack-oefeningen of red teaming. |
| M5 | Bescherming systeemdefecten AI-systeem zelf | Art. 15.5 | Gedeeltelijk | Gedeeltelijk beoordeeld; afhankelijk van antwoord DBS (actie 2). |
| M6 | Bescherming inversieaanvallen en modeldiefstal | Art. 15.5 | N.v.t. | Niet van toepassing. Hansken is geen open-API systeem; gebruikers beschikken over autorisatie. |
| M7 | Bescherming ontwijkingsaanvallen | Art. 15.5 | N.v.t. | Niet van toepassing. Geen classificerend/generatief systeem waarbij invoermanipulatie tot andere output leidt. |
| M8 | Bescherming jailbreak-aanvallen | Art. 15.5 | Gedeeltelijk | Detectie op eigen hardware aanwezig. Status OpenHansken/copiloot nog open (actie 3). |
| M9 | Bescherming membership inference | Art. 15.5 | N.v.t. | Niet van toepassing. Gesloten architectuur; gebruikers beschikken over autorisatie. |
| M10 | Bescherming side-channel aanvallen | Art. 15.5 | Gedeeltelijk | OWASP dependency scan en firewall aanwezig. Volledige inventarisatie niet afgerond. |
| M11 | Bescherming social engineering | Art. 15.5 | Geadresseerd | VGB-B, e-learning, MFA, SSO, time-out, lokale toegang aanwezig. Communicatiebeleid in opbouw (actie 4). |

## 4. Openstaande acties + tijdslijn

1. **CIS Controls-mapping formeel toetsen** — de uitgevoerde mapping van Hansken op de CIS Controls is nog niet formeel gevalideerd. Actie: laten reviewen door een onafhankelijke partij of intern toetsingskader. **Dit doen wij uiterlijk voor datum x. Op datum Y updaten wij de CDR.**
2. **Beschermingsmaatregelen bij DBS navragen** — de maatregelen die DBS treft ter bescherming van de trainingsdata en het model zijn nog niet bevestigd. Actie: schriftelijke bevestiging opvragen bij DBS.
3. **Jailbreak-detectie OpenHansken en copiloot nagaan** — of OpenHansken en de copiloot-component inherent voorzien in jailbreak-detectie is nog niet onderzocht. Actie: navragen bij de technisch eigenaar van de copiloot.
4. **Communicatiebeleid social engineering afronden** — het beleid voor veilige communicatie tussen klanten en toezichthoudende medewerkers is nog in opbouw. Actie: afronden en vastleggen als onderdeel van de beveiligingsrichtlijnen.
5. **Scope OpenHansken bevestigen** — of OpenHansken en de copiloot expliciet onder de scope van deze CA vallen dient formeel te worden bevestigd door de systeemeigenaar.
