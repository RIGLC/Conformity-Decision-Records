

## Conformity Assistance Records
Deze CAR wordt waarschijnlijk vervangen door de modelcard. 

**Welke nauwkeurigheidseisen en prestatiedoelstellingen zijn vastgesteld voor dit systeem, uitgedrukt in meetbare statistieken, en hoe zijn deze afgeleid uit het beoogde gebruik en de risicoanalyse?**

> Bijv.: de vereiste nauwkeurigheid is ≥97% recall en ≤2% false positive rate, afgeleid uit de acceptatiegrens die in overleg met deployers en de risicoanalyse is bepaald; deze drempels zijn opgenomen in de gebruiksinstructies conform art. 13.

`▸ AIV Art. 15.1 · AIV Art. 15.2`
`▸ Zie modelcard voor de waarden dat het model heeft behaald`

**Antwoord:**

_Vul hier je antwoord in._

---

**Welke kritieke systeemkenmerken zijn geïdentificeerd die bepalend zijn voor de nauwkeurigheid, en welke prestatie- en complexiteitsmetrieken zijn voor elk kenmerk gedefinieerd?**

> Bijv.: voor een DNA-vergelijkingssysteem zijn 'matchingscore' en 'zekerheidsinterval' als kritieke kenmerken geïdentificeerd; per kenmerk zijn drempelwaarden bepaald (matchingscore ≥0,95, zekerheidsinterval ≤0,05) en opgenomen in het validatierapport.

`▸ AIV Art. 15.1`
`▸ Zie modelcard (feature importance)`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe zijn betrokken medewerkers opgeleid om nauwkeurigheidsdoelstellingen te begrijpen, correct te interpreteren en toe te passen in hun dagelijkse werk?**

> Bijv.: forensisch analisten volgen een verplichte training van twee uur over de betekenis van prestatiestatistieken (precisie, recall, F1) vóór ingebruikname; training wordt herhaald bij elke nieuwe modelversie.

`▸ AIV Art. 15.1`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe is geborgd dat de validatie- en testomgevingen de productieomgeving nauwkeurig repliceren, inclusief hardware-equivalentie, en hoe worden eventuele afwijkingen gedocumenteerd?**

> Bijv.: de testomgeving draait op identieke hardware als productie (zelfde GPU-type, geheugen en OS-versie); equivalentie wordt halfjaarlijks gecontroleerd door het infra-team en vastgelegd in een omgevingsverklaring; afwijkingen worden bijgehouden in het testregister.

`▸ AIV Art. 15.1`

**Antwoord:**

_Vul hier je antwoord in._

---

**Welke experimenten zijn ontworpen en uitgevoerd om de nauwkeurigheid van het systeem aan te tonen, en hoe zijn de resultaten geanalyseerd, gedocumenteerd en gevalideerd?**

> Bijv.: een experimentenplan beschrijft tests op vijf scenario's (standaard gebruik, randgevallen, ontbrekende data, hoog volume, verschoven populatie); resultaten zijn opgenomen in het technisch validatierapport v2.3 en goedgekeurd door de producteigenaar.

`▸ AIV Art. 15.1`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe is het systeem gevalideerd op echte data onder productie-omstandigheden, en welk aantoonbaar bewijs is beschikbaar van de nauwkeurigheid in de praktijk?**

> Bijv.: gedurende een pilotperiode van drie maanden is de nauwkeurigheid gemeten op 1.200 echte zaken; resultaten (precisie 97,3%, recall 95,8%) zijn vergeleken met de doelstellingen en gedocumenteerd in het acceptatierapport.

`▸ AIV Art. 15.1`
`▸ Zie modelcard (performance van het model)`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe worden degradatie in nauwkeurigheid gedurende de operationele fase gedetecteerd en gerapporteerd, en welke waarschuwings- en herstelprotocollen zijn ingericht?**

> Bijv.: als de precisie drie opeenvolgende weken onder de 95% zakt, genereert het systeem automatisch een melding aan de producteigenaar; bij overschrijding van de 90%-drempel wordt het systeem in 'review mode' gezet en kan het niet worden gebruikt totdat herbeoordeling heeft plaatsgevonden.

`▸ AIV Art. 15.1 · AIV Art. 72.2`

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
