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

**Context and problem statement**
Het is JenV beleid en volgens de BIO moet er bij grote releases een pentest uitgevoerd worden. Pentesten worden uitgevoerd om vertrouwen bij de partners te krijgen, en om het eigen systeem te controleren. Daarnaast wordt de pentest extern uitgevoerd omdat dit ervoor zorgt dat een bias naar het eigen systeem voorkomen wordt, en dat er een nieuwe en frisse blik op de werking van het systeem komt. 

**Considered options**  
* Periodieke externe pentests, uitgevoerd bij grote wijzigingen of 1x per jaar, of op verzoek (bijv. van externen). Bevindingen gaan naar de proceseigenaar/systeemeigenaar. Er is beleid over termijnen waarbinnen geconstateerde kwetsbaarheden worden verholpen.

**Chosen option:**  
"B2: Externe pentests als primaire aanvalssimulatie", omdat er pentests worden uitgevoerd door een externe partij. Bevindingen worden gecategoriseerd en binnen vastgestelde termijnen opgevolgd. De teamlead doet de uitvraag naar een externe partij om een pentest te doen, deze externe partijen zijn o.a. Sopra Steria. De overheid biedt zelf ook pentesten aan (NAAM), maar deze duurt een stuk langer en is wel gedetailleerder dan de meeste commerciele pentesten. Overheidspentesten worden nu gedaan wanneer de software geacredditeerd moet worden voor intern gebruik. Overheidspentesten duren een stuk langer voordat er iemand langs kan komen. Het IT-security team kijkt na of de teamlead deze uitvraag heeft gedaan, en zijn betrokken vanaf begin tot einde (van intake, tot het gecentraliseerd opslaan van het eindrapport van de pentest). IT-security team zorgen er ook voor de findings uit het rapport worden opgevolgd binnen een bepaalde tijd, hier is het IT-security team de controlerende factor. 

* Good, because: je hebt een externe check, dus je voorkomt bias. Pentest-auditors zijn gespecialiseerd in hun vak, meer dan een willekeurige developer. En het dient als een bewijs naar buiten toe dat je cybersecurity serieus neemt. Het toont aan dat je als organisatie niet alleen vertrouwt op eigen kunde, maar ook een externe mee laat kijken om eventuele blinde vlekken te detecteren. 
* Bad, because: in het ergste geval zou een pentest ervoor kunnen zorgen dat het systeem uit de lucht gaat voor een korte periode. Maar over het algemeen gebeurd het in een gecontroleerde omgeving, en is die kans hier op minimaal. Risico kan zijn dat de externe partij die de pentest uitvoert het niet goed doet, en belangrijke fouten over het hoofd ziet. 

---

## B3: CVE-scanning

*M1: Passend niveau van cybersecurity en consistentie · M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Grondslag: Art. 15.1, 15.5*

**context and problem statement**
Er was weinig tot geen inzicht in de huidige kwetsbaarheden, omdat Kubernetes niet onder de standaard service valt. Kubernetes is een framework waar alle services op draaien, dat draait op de Openshift cluster, maar wijkt af van de servers die door de IB (intern NFI systeembeheerder) worden beheerd. IB beheerd wel het bouwblok waar Kubernetes op draait (het OpenShift cluster). Voor meer informatie over OpenShift cluster contact opzoeken met IB. Daardoor was er geen zicht op de Kubernetes omgeving. Door gebrek aan inzicht kon niet bijgestuurd worden op hoeveelheid kwetsbaarheden. CVE-scanning op Kubernetes is alleen voor Hansken intern NFI gebruik, op het moment dat de sammenwerkingspartner het zelf gaat hosten wordt geacht dat ze zelf de CVE-scanning doen. 

**CDR checken met Marijn van Wijngaarden of Nathan Tuinstra (ontwikkelt de CVE-scanning) van HDH.**

**Considered options**
* Zie lijst met overwegingen rondom CVE-scanning - bij Nathan opvragen

**Chosen option:**   
"B3: CVE-scanning Trivey. Wordt nu gedeployed, verwachting Q4 2026 gaat het op productie draaien. Trivey is een open-source externe partij. Niet noodzakelijk slechte consequentie, want het wordt lokaal gedraaid, maar er is een afhankelijkheid van een derde partij. Om dit risco af te dekken wordt Trivey lokaal gehost, maar je bent afhankelijk van de updates van de aanbieder van Trivey. 

* Good, because: geeft inzicht in de kwetsbaarheden, waar op aangestuurd kan worden bijvoorbeeld dmv het aannemen van extra FTE. Kan prioriteren door inzicht. Maakt applicatie veel veiliger. 
* Bad, because: Het kan extra belasting geven op de omgeving, waardoor je meer resources nodig hebt, zoals CPU-kracht, extra RAM, om de omgeving draaiende te houden.

---

## B4: OWASP dependency scan

*M1: Passend niveau van cybersecurity en consistentie · M10: Bescherming side-channel aanvallen | Grondslag: Art. 15.1, 15.5*
**Context and problem statement**
Er kunnen kwetsbaarheden optreden in de dependencies die gebruikt worden in de code. Deze kwetsbaarheden moeten opgespoord worden. 

Naast CVE-scanning worden ook kwetsbaarheden in de applicatie-afhankelijkheden systematisch in kaart gebracht. 

**Considered options**
* OWASP dependency scan, uitgevoerd naast CVE-scanning.

**Chosen option:**   
"B4: OWASP dependency scan voor applicatie-afhankelijkheden". 
Het is een soort CVE-scannning, maar het ziet toe op de dependencies die gebruikt worden in de code. Hansken downloadt een keer per dag de database van de National Vulnerability Databse (NVD), daar wordt interne code tegenaan gepushed, om te kijken of er kwetsbaarheden zijn in de gebruikte dependencies. De database van NVD wordt lokaal gedownload (geautomatiseerd via API key van NIST), en op deze lokale server wordt de code vergeleken met de database dependencies.


* Good, because: Je dependencies blijven up to date, je bent veiliger, is voor partners fijn om te weten dat we veilige dependencies gebruiken, wat geschreven wordt wordt ook getest. Is een lichte tool. 
* Bad, because: Afhankelijk van NIST, mocht NIST falen dan zijn we daar afhankelijk van. 

---

## B5: SAST-tooling

*M1: Passend niveau van cybersecurity en consistentie · M4: Bescherming adversariele aanvallen | Grondslag: Art. 15.1, 15.5*

**Context and problem statement**
Software kan kwetsbaar worden als je code slecht geschrevenn is. Mogelijke SQL-injecties kunnen zorgen voor het losmaken van sensitieve data. Vierogen principe ondervangt dit, maar blijft mensenwerk, en risico's komen voor. Om de risico's te verminderen is voorkeur voor SAST-tooling, die bekijkt de code en spot kwetsbaarheden. 

**Considered options**
* Sonarqube
* Alternatieven niet gedocumenteerd. 

**Chosen option:**  
"B5: Sonarqube. 

* Good, because: code wordt veiliger, extra handjes om mee te kijken, wordt meteen geupdate op basis van nieuwe kwetsbaarheden, is teveel werk voor mensen. Wordt lokaal gehost. 
* Bad, because: afhankelijkheid van falen van Sonarqube. Is een commerciele leverancier. 

---

## TO DO B6: SBOM

*M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen · M3: Voorkomen manipulatie datasets | Grondslag: Art. 15.5 (raakt ook Art. 10.5)*

**Context and problemstatement**
Om de samenstelling van het systeem en de ingezette databronnen transparant te maken, is een register nodig. Een SBOM creeert een lijst waar alle componenten, librariers, modules en dependencies, versies opgenomen worden. 

**Considered options**
 
**Chosen option:**  
Staat op de roadmap

* Good, because: 
* Bad, because: 

---

## TO DO B7: Container-signing

*M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Grondslag: Art. 15.5*

**Context and problem statement**
Iets wordt gepushed naar de klant, maar er moet zekerheid zijn dat degene die het opent ook degene is die het had moeten openen. Dus je file wordt beveiligd zodat alleen de persoon naar wie je het stuurt, het kan openen, in plaats van dat het netwerk waar je het naar stuurt het allemaal kan openen.   

**Considered options**

**Chosen option:**   
Staat op de roadmap

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## B8: Vierogenprincipe

*M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Grondslag: Art. 15.5*

**Context and problemstatement**   
Een individuele medewerker kan onbedoeld of opzettelijk kwetsbare wijzigingen doorvoeren. Om dit te voorkomen hanteer je dit principe. Jeroen van der Vegt

**Considered options**
* Vierogen: wijzigingen vereisen goedkeuring van meerdere personen, geborgd via Atlassian. Voordat code gepushed kan worden, gaat de code door vier verschillende omgevingen (development, test, acceptatie, productie omgeving). De persoon die hier naar kijkt is een tweede developer. 1 Developer die codeert, 1 developer die het bekijkt. Dan in sprint meetings nog bekeken. 

**Chosen option:**  
"B8: Vierogen voor wijzigingsbeheer", het wordt gehanteerd om wijzigingen door meerdere personen te laten controleren. Wijzigingen zijn herleidbaar doordat de ontwikkeling in Atlassian plaatsvindt.

* Good, because: fijn om twee personen te hebben die controleren, want mensen maken fouten. Is gewoon een standaard dubbelcheck. 
* Bad, because: Fouten kunnen altijd alsnog doorglippen. Maar dan heb je als back-up de SAST-tooling.  

---

## B9: SSO zonder 2FA

*M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Grondslag: Art. 15.5*

**Context and Problemstatement**
Er moet onderscheidt gemaakt worden in wie er toegang heeft tot Hansken, en welke delen van Hansken. 
Hier is een onderscheidt tussen het intern gebruik en de software. 

**Intern:**
* SSO met 2FA. Is het JenV-beleid, dit wordt opgevolgd.

**Software**
* Opvragen bij Jeroen van der Vegt en Gjalt Reitsma. 
  
**Considered options**

**Chosen option:**

* Good, because: 
* Bad, because: 

---

## B10: Audit logging

*M2: Bestand tegen ongeoorloofd gebruik en integriteitsschendingen | Grondslag: Art. 15.5*

**Context and problem statement**
Om afwijkend of ongeautoriseerd gebruik te detecteren, is monitoring van systeemgebruik nodig. Door audit logging kan je zien wat er gebeurd is mocht er een fout opgetreden zijn in de software. 

**Considered options**
* Logging van omgevingen zonder koppeling IT-security team.
* Logging van omgevingen met koppeling IT-security time. 

**Chosen option:**  
"B10: Audit logging zonder koppeling IT-security team. Staat op de roadmap om logging van omgevingen met koppeling naar IT-security team. Logging is er wel, maar monitoring voor security nog niet. Het staat op de planning om een SOC in te kopen. 

* Good, because: cyberlogging bestaat. IT-security is bezig met het inregelen van de monitoring van de cyberloggings. 
* Bad, because: cyberlogging wordt nog niet gemonitord.  

---

## NIET RELEVANT B11: Aanpak bescherming tegen data poisoning

*M3: Voorkomen manipulatie datasets · M5: Bescherming systeemdefecten AI-systeem zelf | Grondslag: Art. 15.5*

De AI-modellen in Hansken zijn getraind op forensische data. Als trainingsdata of het model worden gemanipuleerd, kunnen uitkomsten onbetrouwbaar worden. Vraag: hoe wordt het model beschermd tegen manipulatie van trainingsdata en het model zelf?

* Het model wordt niet meer geüpdatet. De ontwikkelaars van het model (DBS) zijn niet dezelfde partij als degenen die het model in Hansken integreren (NFI).

Chosen option: "B11: Aanpak bescherming trainingsdata en model tegen data poisoning", omdat het model niet meer wordt geüpdatet. De scheiding tussen de modellerende partij (DBS) en de integrerende partij (NFI) biedt een organisatorische beveiligingslaag. De exacte beschermingsmaatregelen bij DBS zijn nog niet bevestigd (zie Openstaande acties, punt 2).

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## NIET RELEVANT  B12: Jailbreak-detectie

*M8: Bescherming jailbreak-aanvallen | Grondslag: Art. 15.5*

Hansken bevat een copiloot-component. Jailbreaking kan ertoe leiden dat het systeem buiten zijn bedoelde grenzen wordt gebruikt. Vraag: welke maatregelen worden getroffen om jailbreaking te voorkomen en te detecteren?

* Op eigen hardware worden softwareproducten ingezet voor de detectie van jailbreaking.

Chosen option: "B12: Jailbreak-detectie op eigen hardware", omdat op eigen hardware softwareproducten zijn ingezet voor jailbreak-detectie. Of OpenHansken en de copiloot hier inherent in voorzien is nog niet nagegaan (zie Openstaande acties, punt 3).

* Good, because: *niet gedocumenteerd — nader in te vullen*
* Bad, because: *niet gedocumenteerd — nader in te vullen*

---

## NIET RELEVANT B13: Social engineering operators

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
