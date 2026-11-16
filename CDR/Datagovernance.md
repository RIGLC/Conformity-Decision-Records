# Conformity Assistance Record  

# Datasheet

### 1. Wat is de herkomst van de dataset en wat is de juridische grondslag voor het gebruik ervan?

Bijv.: de dataset bestaat uit 50.000 geanonimiseerde zaken van 2010–2023; herkomst is vastgelegd in een data-lineagedocument; juridische grondslag is 'uitvoering van een taak van algemeen belang' conform AVG art. 6(1)(e).

`▸ Art. 10.2 · Art. 10.3`

**Antwoord:**

---

### 2. Is de dataset representatief voor de beoogde populatie en het beoogde gebruik, en welke aannames zijn daarbij gemaakt?

Bijv.: een representativiteitsanalyse toonde aan dat de leeftijdsverdeling in de dataset overeenkomt met de Nederlandse bevolkingsopbouw (±3%); de aanname dat de dataset toekomstige casussen dekt is expliciet gedocumenteerd als risico.

`▸ Art. 10.2 · Art. 10.3`

**Antwoord:**

---

### 3. Wat zijn de eigenschappen van de dataset?

Bijv.: 133.533 gelabelde afbeeldingen; data type: afbeeldingen (JPEG); verzameld in Nederland in de periode 2015–2023; geografische reikwijdte: Nederland; gelabeld in 17 forensisch relevante categorieën.

`▸ Art. 10.2`

| Eigenschap | Waarde |
|---|---|
| Data type | |
| Grootte (GB) | |
| Hoeveelheid (instances) | |
| Datum van verzameling | |
| Geografische reikwijdte | |
| Label informatie | |
| Aantal features / velden | |

**Antwoord / toelichting:**

---

### 4. Welke datakwaliteitsdimensies zijn gedefinieerd en hoe worden kwaliteitscontroles per dimensie uitgevoerd?

Bijv.: kwaliteitsdimensies zijn volledigheid (>99,5%), juistheid (gevalideerd door domeinexperts), consistentie (geen conflicterende records) en actualiteit (data niet ouder dan 5 jaar); elke nieuwe dataset doorloopt een geautomatiseerde kwaliteitscheck vóór gebruik.

`▸ Art. 10.2`

**Antwoord:**

---

### 5. Hoe zijn geconstateerde afwijkingen in datakwaliteit gedocumenteerd en welke verbetermaatregelen zijn getroffen?

Bijv.: bij de kwaliteitscheck zijn 312 records met missende waarden geïdentificeerd; na analyse zijn 280 records verwijderd en 32 aangevuld op basis van domeinexpertise; dit is vastgelegd in het datakwaliteitslogboek.

`▸ Art. 10.2`

**Antwoord:**

---

### 6. Hoe is de data verzameld en op basis van welke selectiecriteria?

Bijv.: de data is verzameld via inbeslagname door het DJIT-team; selectiecriterium is dat het bewijsmateriaal betrekking heeft op een lopende zaak; data met een opnamedatum van vóór 2010 is uitgesloten.

`▸ Art. 10.2`

**Antwoord:**

---

### 7. Welke datatransformaties hebben plaatsgevonden en hoe zijn deze keuzes onderbouwd?

Bijv.: afbeeldingen zijn geresized naar 299×299 pixels voor invoer in het model; JPEG-kwaliteit is genormaliseerd naar 85%; alle transformaties zijn vastgelegd in een reproduceerbaar preprocessing-script met versienummer.

`▸ Art. 10.2`

**Antwoord:**

---

### 8. Hoe is datalabeling uitgevoerd en in welke mate heeft menselijk toezicht plaatsgevonden bij geautomatiseerde annotatie?

Bijv.: 80% van de labels is handmatig aangebracht door gecertificeerde analisten; 20% is automatisch gegenereerd en steekproefsgewijs (5%) gecontroleerd door een senior analist; inter-annotator agreement is gemeten op κ = 0,87.

`▸ Art. 10.2 · Art. 14.1`

**Antwoord:**

---

### 9. Welke bronnen van bias zijn geïdentificeerd in de data en hoe zijn deze geanalyseerd?

Bijv.: een fairness-audit toonde aan dat het model een 8% hogere fout-positiefrate had voor afbeeldingen van vrouwen in de categorie pornography; dit is geanalyseerd als gevolg van onevenwichtige vertegenwoordiging in de trainingsdata.

`▸ Art. 10.2 · Art. 10.4`

**Antwoord:**

---

### 10. Welke mitigatiemaatregelen zijn getroffen om bias te reduceren en hoe is de effectiviteit hiervan gemeten?

Bijv.: als mitigatie zijn gerichte tegenvoorbeelden toegevoegd (foto's van vrouwen zonder pornografische inhoud, factor 1,5 oversampling); na hertraining is de fout-positiefrate gedaald van 8% naar 2,1% voor deze groep; resultaten zijn vastgelegd in het fairness-rapport v2.0.

`▸ Art. 10.2 · Art. 10.4`

**Antwoord:**

---

### 11. Hoe is omgegaan met persoonsgegevens en bijzondere persoonsgegevens, inclusief de AVG-grondslag, toegepaste anonimisering en meldingen aan betrokkenen?

Bijv.: persoonsgegevens zijn gepseudonimiseerd via SHA-256 hashing; de DPIA is goedgekeurd door de Functionaris Gegevensbescherming op 15 maart 2024; betrokkenen zijn geïnformeerd via een privacy notice in het zaakdossier.

`▸ Art. 10.5`

**Antwoord:**

---

### 12. Is het risico op heridentificatie beoordeeld en welke maatregelen zijn hiervoor ingericht?

Bijv.: het risico van heridentificatie via linkage-aanvallen is beoordeeld als 'laag' op basis van een k-anonimiteitsanalyse (k=5); toegang tot ruwe data is beperkt tot twee data-engineers met een geheimhoudingsverklaring.

`▸ Art. 10.5`

**Antwoord:**

---

### 13. Hoe is de toegang tot de dataset ingericht en wie is verantwoordelijk voor toestemmingsbeheer?

Bijv.: de dataset staat op de project-/zakenschijf onder `/data/raw/FIRE/`; toegang vereist een VGB en goedkeuring van de dataseigenaar; bij gebruik voor een nieuw project dient toestemming te worden gevraagd aan de dataseigenaar of, bij afwezigheid, aan het teamhoofd.

`▸ Art. 10.5`

**Antwoord:**

---

### 14. Hoe verloopt de data-overdracht of -verwijdering aan het einde van de levenscyclus?

Bijv.: na het verstrijken van de bewaartermijn (10 jaar) worden data overschreven conform de DoD 5220.22-M standaard; verwijdering wordt gelogd in het auditsysteem met tijdstempel, verantwoordelijke en bevestiging; het effect op afhankelijke modellen is vooraf beoordeeld en vastgelegd.

`▸ Art. 10.5`

**Antwoord:**
