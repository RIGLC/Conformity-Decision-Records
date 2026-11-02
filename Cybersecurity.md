## Samenvatting

| Veld | Waarde |
|---|---|
| **Versie** | |
| **Status** | PROPOSED / ACCEPTED / REJECTED |
| **Laatste aanpasdatum** | |
| **Aanpasser** | |

---

## Maatregelen

### Nauwkeurigheid

**Hoe zijn de cybersecurityrisico's van dit AI-systeem integraal beoordeeld — inclusief risico's die specifiek zijn voor AI zoals modelmanipulatie en data poisoning — en welke normen of frameworks zijn hierbij gehanteerd?**

> Bijv.: een penetratietest is uitgevoerd door een externe partij conform het PTES-framework; bevindingen zijn gecategoriseerd naar ernst (kritiek, hoog, middel, laag); alle kritieke bevindingen zijn binnen 30 dagen verholpen en gedocumenteerd in het securitydossier.

`▸ AIV Art. 15.1 · AIV Art. 15.3`

**Antwoord:**

_Vul hier je antwoord in._

---

**Welke beveiligingsmaatregelen zijn getroffen om ongeoorloofde wijzigingen en integriteitsschendingen van het systeem en zijn configuratie te detecteren en te voorkomen?**

> Bijv.: een integrity check vergelijkt modelgewichten dagelijks met de cryptografische hash van de goedgekeurde versie; elke configuratiewijziging vereist goedkeuring van twee beheerders; afwijkingen triggeren automatisch een beveiligingsalert aan de CISO.

`▸ AIV Art. 15.1`

**Antwoord:**

_Vul hier je antwoord in._

---

### Ongeoorloofd gebruik en datamanipulatie

**Welke mechanismen zijn ingebouwd om ongeoorloofd of afwijkend gebruik van het systeem te detecteren en te voorkomen, en hoe zijn integriteitscontroles opgezet?**

> Bijv.: het systeem controleert bij elke aanroep of de gebruiker een actieve, geautoriseerde sessie heeft; afwijkend gebruik (ongebruikelijke uren, hoog volume, onbekend IP-adres) triggert een automatische blokkade en alert aan de beveiligingsofficier.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe zijn de trainingsdata en het model beschermd tegen data poisoning en manipulatie — inclusief toegangscontroles, versleuteling, anomaliedetectie en logging?**

> Bijv.: toegang tot de trainingsdata vereist twee-factor-authenticatie en is beperkt tot drie data-engineers; data is versleuteld opgeslagen (AES-256); een anomaliedetectiesysteem signaleert ongebruikelijke wijzigingspatronen; alle wijzigingen worden gelogd in een audittrail.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

**Zijn de bronnen van dataverzameling in kaart gebracht, en welke beveiligingscontroles waarborgen de betrouwbaarheid van data uit externe bronnen?**

> Bijv.: een dataleveranciersregister beschrijft voor elke databron de herkomst, het verificatieproces en de beveiligingsafspraken; data uit externe bronnen wordt altijd geverifieerd via een checksumcontrole vóór opname in de trainingsset.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

### Aanvalsbescherming

**Hoe is het systeem getest en gehardend tegen adversariële aanvallen, en welke detectie- en mitigatiemechanismen zijn ingebouwd om manipulatie van invoer te signaleren?**

> Bijv.: maandelijks voert het security-team een adversarial attack simulatie uit; invoer met statistische kenmerken die sterk afwijken van de trainingsdistributie wordt automatisch gemarkeerd als 'verdacht' en doorgestuurd naar een analist voor beoordeling.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

**Worden er regelmatig adversariële aanvalsoefeningen of red-teaming sessies uitgevoerd om de weerbaarheid van het systeem te testen, en hoe zijn bevindingen verwerkt?**

> Bijv.: elk kwartaal voert een intern red team een gecontroleerde aanvalssimulatie uit; bevindingen worden gecategoriseerd en verwerkt in de volgende patchcyclus; resultaten worden besproken in het maandelijkse securityoverleg.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

**Welke mechanismen zijn geïmplementeerd om ontwijkingsaanvallen te detecteren — pogingen om via aangepaste invoer de AI-beslissing te omzeilen — en hoe effectief zijn deze gebleken?**

> Bijv.: het systeem vergelijkt elk inkomend datapunt met een statistische baseline; afwijkingen boven een drempelwaarde worden geblokkeerd en gelogd; in de afgelopen zes maanden zijn vier echte ontwijkingspogingen gedetecteerd en tegengehouden.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

**Welke maatregelen zijn ontwikkeld om jailbreaking te voorkomen — pogingen om beperkingen of veiligheidsmechanismen van het systeem te omzeilen — en hoe is de effectiviteit hiervan getest?**

> Bijv.: het systeem heeft een inputvalidatielaag die bekende jailbreak-patronen filtert; verificatiemechanismen controleren bij elke aanroep of de output binnen de gedefinieerde veiligheidsgrenzen valt; effectiviteit is getest via red-teaming oefeningen.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

### Privacy-aanvallen en side-channel risico's

**Is beoordeeld of het systeem zelf specifieke cybersecurityrisico's introduceert, en hoe zijn inversieaanvallen en modeldiefstal voorkomen via maskering, versleuteling of componentscheiding?**

> Bijv.: modelgewichten zijn versleuteld en alleen benaderbaar via een beveiligde API; directe toegang tot het model is onmogelijk; componentscheiding voorkomt dat een aanvaller via één gecompromitteerd onderdeel het volledige model kan reconstrueren.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

**In hoeverre is het systeem kwetsbaar voor membership inference-aanvallen — waarbij een aanvaller probeert te achterhalen of een specifiek datapunt in de trainingsset zat — en welke privacybeschermingstechnieken zijn toegepast?**

> Bijv.: een membership inference attack test toonde aan dat het model met 53% kans (near-random, dus acceptabel) kon voorspellen of een datapunt in de trainingsset zat; ter aanvullende bescherming is differential privacy toegepast met ε = 1,0 bij de modeltraining.

`▸ AIV Art. 15.5 · AIV Art. 10.5`

**Antwoord:**

_Vul hier je antwoord in._

---

**Zijn de functies, tools en externe bibliotheken die het systeem gebruikt geanalyseerd op side-channel kwetsbaarheden, en hoe zijn deze beheersmatig of technisch gemitigeerd?**

> Bijv.: een inventaris van alle externe bibliotheken toont welke onbeheerde of verouderde componenten risico's introduceren; kwetsbare bibliotheken zijn vervangen of geïsoleerd; timing-side-channels zijn gemitigeerd door constante-tijd implementaties te gebruiken.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

### Social engineering en incidentrespons

**Is beoordeeld of het systeem kwetsbaar is voor social engineering — pogingen om via misleiding van menselijke operators ongeautoriseerde acties te bewerkstelligen — en welke maatregelen zijn getroffen?**

> Bijv.: operators zijn getraind om verdachte verzoeken via het systeem te herkennen; het systeem vraagt altijd een tweede autorisatie bij acties buiten de normale workflow; een communicatieprotocol beschrijft welke verzoeken nooit via automatische berichten worden gedaan.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe is veilige en betrouwbare communicatie gewaarborgd tussen het systeem en zijn gebruikers, beheerders en externe systemen — inclusief encryptie, authenticatie en integriteitscontrole van berichten?**

> Bijv.: alle communicatie verloopt via TLS 1.3; API-aanroepen worden geauthenticeerd via OAuth 2.0 met korte tokenlevensduur (15 minuten); de integriteit van berichten wordt gewaarborgd via HMAC-signing.

`▸ AIV Art. 15.5`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe zijn toegangscontroles, authenticatie en sessiebeheer ingericht om modeldiefstal en reverse engineering te voorkomen, en welke responsprotocollen zijn er voor specifieke cybersecurity-incidenten?**

> Bijv.: alleen gecertificeerde onderzoekers met NFI-badge en MFA kunnen inloggen; sessies verlopen na 30 minuten inactiviteit; procedure 'SEC-03' beschrijft drie escalatieniveaus: bij kritieke incidenten wordt het systeem direct offline gehaald en start de Art. 73-meldingsprocedure.

`▸ AIV Art. 15.5 · AIV Art. 73.1`

**Antwoord:**

_Vul hier je antwoord in._

---

## Beslissing

| Veld | Waarde |
|---|---|
| **Oordeel** | ☐ COMPLIANT · ☐ GEDEELTELIJK · ☐ NON-COMPLIANT |
| **Rationale** | |
| **Openstaande acties** | |
| **Beoordelaar** | |
| **Datum beoordeling** | |
