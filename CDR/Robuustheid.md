

## Conformity Assistance Records   

Deze CDR wordt gedeeltelijk ondervangen door de modelcard. 

**Welke waarschuwingstechnieken zijn geconfigureerd om te activeren wanneer de robuustheid onder een drempelwaarde zakt, en hoe zijn de bijbehorende protocollen voor veilig falen vastgelegd?**

> Bijv.: bij overschrijding van de robuustheidsdrempel (foutmarge >3%) genereert het systeem een oranje alert; bij twee opeenvolgende overschrijdingen schakelt het systeem automatisch naar 'veilige modus' waarbij alleen uitkomsten met hoge zekerheid worden geaccepteerd.

`▸ AIV Art. 15.2`

**Antwoord:**

_Vul hier je antwoord in._

---

**Zijn er specifieke commissies, teams of procedures ingesteld om inconsistenties, storingen of verslechterde robuustheid proactief te signaleren vóórdat ze operationele impact hebben?**

> Bijv.: maandelijks beoordeelt een technisch reviewteam (producteigenaar, data-engineer, analist) de robuustheidsstatistieken; bevindingen worden vastgelegd in het reviewregister en escaleren bij twijfel naar de CTO.

`▸ AIV Art. 15.2`

**Antwoord:**

_Vul hier je antwoord in._

---

**Welke automatische mechanismen zijn geïmplementeerd voor systeemherstel na storingen, en hoe is de effectiviteit hiervan getest?**

> Bijv.: bij een kritieke fout herstart het systeem automatisch binnen 60 seconden; bij een aanhoudende storing schakelt het over op een fallback-versie van het model; herstelmechanismen zijn getest in een jaarlijkse failover-oefening waarbij geen dataverlies mocht optreden.

`▸ AIV Art. 15.2`

**Antwoord:**

_Vul hier je antwoord in._

---

**Welke tools en procedures zijn geïmplementeerd om geo-redundantie (zie voorbeeld), versiebeheer en schaalbaarheid van het systeem te waarborgen, en hoe is de beschikbaarheid bij incidenten geborgd?**

> Bijv.: het systeem draait op twee servers in geografisch gescheiden datacenters; bij uitval van één server neemt de andere binnen 30 seconden automatisch over; alle modelversies worden bewaard in een Git-repository met terugrolmogelijkheid naar elke vorige stabiele versie.

`▸ AIV Art. 15.2`

**Antwoord:**

_Vul hier je antwoord in._

---

**Voor systemen die blijven leren: hoe wordt gemonitord dat robuustheid, nauwkeurigheid en prestaties niet degraderen naarmate het systeem meer data verwerkt?**

> Bijv.: wekelijks worden robuustheidsmetrieken vergeleken met de baseline bij oplevering; bij een afwijking van meer dan 5% wordt automatisch een review geïnitieerd; het systeem wordt pas opnieuw in productie genomen na validatie door de producteigenaar.

`▸ AIV Art. 15.2`

**Antwoord:**

_Vul hier je antwoord in._

---

**Welke monitoring- en beheersplannen zijn opgesteld om modelafwijking en bias bij systemen die blijven leren te detecteren en te mitigeren?**

> Bijv.: een wekelijkse drift-detectietest vergelijkt de actuele inputdistributie met de trainingsdistributie via de Population Stability Index (PSI); bij PSI > 0,2 wordt een hertraining geïnitieerd; na hertraining wordt een fairness-audit uitgevoerd vóór heringebruikname.

`▸ AIV Art. 15.2 · AIV Art. 10.4`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe worden interacties, interoperabiliteit met andere systemen of mensen, en ontvangen feedback gedurende de levenscyclus formeel vastgelegd en verwerkt?**

> Bijv.: alle analisten-overrides (gevallen waarbij de analist de AI-uitkomst verwerpt) worden gelogd met reden; maandelijks analyseert de producteigenaar de override-statistieken om patronen te identificeren die kunnen wijzen op modelzwakheden; bevindingen worden meegenomen in het volgende hertrainingscyclus.

`▸ AIV Art. 15.2 · AIV Art. 12.1`

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
