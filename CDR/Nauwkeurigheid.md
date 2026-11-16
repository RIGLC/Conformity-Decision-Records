# Conformity Assistance Records
# Modelcard

## Beschrijving

*Korte beschrijving van wat het model doet, voor welke taak het is ontwikkeld en in welke context het wordt ingezet.*

**Categorieën / output:**

**Architectuur:**

---

## Gebruik

*Waarvoor is het model bedoeld? Wat zijn de aanbevolen en niet-aanbevolen toepassingen?*

**Aanbevolen gebruik:**

**Niet aanbevolen gebruik:**

---

## Data

*Beschrijving van de trainings- en validatiedata: herkomst, samenstelling, aantallen per klasse.*

| Label | Training set | Validation set |
|---|---|---|
| | | |

---

## Training

*Beschrijving van de trainingsprocedure: optimiser, learning rate, verliesfunctie, batch-samenstelling, data-augmentatie.*

### 1. Welke nauwkeurigheidseisen en prestatiedoelstellingen zijn vastgesteld voor dit systeem, uitgedrukt in meetbare statistieken, en hoe zijn deze afgeleid uit het beoogde gebruik en de risicoanalyse?

Bijv.: de vereiste nauwkeurigheid is ≥97% recall en ≤2% false positive rate, afgeleid uit de acceptatiegrens die in overleg met deployers en de risicoanalyse is bepaald; deze drempels zijn opgenomen in de gebruiksinstructies conform Art. 13.

`▸ Art. 15.1 · Art. 15.2`

**Antwoord:**

---

### 2. Welke evaluatiemetrieken zijn gehanteerd en waarom passen deze bij het beoogde gebruik van het model?

Bijv.: het model is geëvalueerd op precision@20 omdat het primair bedoeld is om afbeeldingen te rangschikken, niet te filteren; aanvullend is recall gemeten om te beoordelen hoeveel relevante afbeeldingen het model mist, wat cruciaal is in forensische toepassingen waarbij volledigheid telt.

`▸ Art. 15.1`

**Antwoord:**

**Resultaten per klasse:**

| Label | Precision@20 | Recall | F1 |
|---|---|---|---|
| | | | |
| **Gemiddelde** | | | |
| **Minimum** | | | |

---

### 3. Hoe zijn betrokken medewerkers opgeleid om de output van het model correct te interpreteren en toe te passen?

Bijv.: medewerkers volgen een verplichte training van twee uur over de betekenis van de scores en de beperkingen van het model vóór ingebruikname; training wordt herhaald bij elke nieuwe modelversie; de gebruiksinstructies zijn beschikbaar via [link].

`▸ Art. 15.1`

**Antwoord:**

---

### 4. Hoe is geborgd dat de test- en validatieomgeving de productieomgeving nauwkeurig repliceren?

Bijv.: de testomgeving draait op identieke hardware als productie (zelfde GPU-type, geheugen en OS-versie); equivalentie wordt halfjaarlijks gecontroleerd door het infra-team en vastgelegd in een omgevingsverklaring.

`▸ Art. 15.1`

**Antwoord:**

---

### 5. Is het model gevalideerd op echte data onder productieomstandigheden, en welk bewijs is beschikbaar van de nauwkeurigheid in de praktijk?

Bijv.: gedurende een pilotperiode van drie maanden is de nauwkeurigheid gemeten op 1.200 echte zaken; resultaten (precision@20 gemiddeld 0,91) zijn vergeleken met de doelstellingen en gedocumenteerd in het acceptatierapport.

`▸ Art. 15.1`

**Antwoord:**

---

### 6. Hoe worden degradatie in nauwkeurigheid gedurende de operationele fase gedetecteerd en gerapporteerd, en welke waarschuwings- en herstelprotocollen zijn ingericht?

Bijv.: als de precision@20 voor een kritieke klasse drie opeenvolgende weken onder 0,80 zakt, genereert het systeem automatisch een melding aan de producteigenaar; bij overschrijding van de 0,70-drempel wordt het model in 'review mode' gezet en kan het niet worden gebruikt totdat herbeoordeling heeft plaatsgevonden.

`▸ Art. 15.1 · Art. 72.2`

**Antwoord:**

---

### 7. Welke waarschuwingstechnieken zijn geconfigureerd om te activeren wanneer de robuustheid onder een drempelwaarde zakt, en hoe zijn de bijbehorende protocollen voor veilig falen vastgelegd?

Bijv.: bij invoer van afbeeldingen kleiner dan 256×256 pixels geeft het systeem een expliciete waarschuwing aan de gebruiker en sluit de afbeelding uit van de ranking; de onderzoeker legt in het dossier vast waarom de afbeelding toch is bekeken of uitgesloten.

`▸ Art. 15.2`

**Antwoord:**

---

### 8. Zijn er procedures ingesteld om inconsistenties of verslechterde robuustheid proactief te signaleren vóórdat ze operationele impact hebben?

Bijv.: maandelijks beoordeelt een technisch reviewteam (producteigenaar, data-engineer, analist) de robuustheidsstatistieken op basis van productielogs; bevindingen worden vastgelegd in het reviewregister en escaleren bij twijfel naar de CTO.

`▸ Art. 15.2`

**Antwoord:**

---

### 9. Welke mechanismen zijn geïmplementeerd voor systeemherstel na storingen, en hoe is de effectiviteit hiervan getest?

Bijv.: bij een kritieke fout herstart het systeem automatisch; bij een aanhoudende storing schakelt het over op een fallback-werkwijze waarbij de onderzoeker de afbeeldingen handmatig doorzoekt; herstelmechanismen zijn getest in een jaarlijkse failover-oefening.

`▸ Art. 15.2`

**Antwoord:**

---

### 10. Welke procedures zijn geïmplementeerd voor versiebeheer en hoe is de beschikbaarheid bij incidenten geborgd?

Bijv.: alle modelversies worden bewaard in een Git-repository met terugrolmogelijkheid naar elke vorige stabiele versie; bij uitval van het systeem valt de onderzoeker terug op handmatige doorzoeking; de producteigenaar besluit over terugrol.

`▸ Art. 15.2`

**Antwoord:**

---

### 11. Voor systemen die blijven leren: hoe wordt gemonitord dat robuustheid en prestaties niet degraderen naarmate het systeem meer data verwerkt?

Bijv.: wekelijks worden robuustheidsmetrieken vergeleken met de baseline bij oplevering; bij een afwijking van meer dan 5% wordt automatisch een review geïnitieerd; het systeem wordt pas opnieuw in productie genomen na validatie door de producteigenaar. Indien niet van toepassing: vermeld waarom (bijv. het model heeft een vast voorgetraind gewicht en wordt niet bijgewerkt op basis van zaaksdata).

`▸ Art. 15.2`

**Antwoord:**

---

### 12. Hoe worden interacties met medewerkers en ontvangen feedback gedurende de levenscyclus vastgelegd en verwerkt?

Bijv.: gevallen waarbij een onderzoeker de ranking van het model negeert of bijstelt worden gelogd met reden; maandelijks analyseert de producteigenaar de override-statistieken om patronen te identificeren; bevindingen worden meegenomen in de volgende hertrainingscyclus.

`▸ Art. 15.2 · Art. 12.1`

**Antwoord:**

---

## Beperkingen

*Beschrijving van bekende beperkingen van het model: use cases waarvoor het niet geschikt is, invoervereisten, randgevallen.*

---

## Bias

*Beschrijving van bekende bias in het model en de mogelijke impact op grondrechten.*

**Fairness-analyse per subgroep:** *Is de prestatie van het model systematisch geanalyseerd per relevante subgroep, bijv. geslacht, leeftijd, etniciteit of geografische herkomst van het materiaal? Wat waren de gevonden prestatieverschillen?*

**Mitigatiemaatregelen:**

---

## Beslissing

| Veld | Waarde |
|---|---|
| **Oordeel** | ☐ COMPLIANT · ☐ GEDEELTELIJK · ☐ NON-COMPLIANT |
| **Rationale** | |
| **Openstaande acties** | |
| **Beoordelaar** | |
| **Datum beoordeling** | |
