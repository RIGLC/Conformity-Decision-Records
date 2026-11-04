## Bijlage IV checklist

Verifieer per element van Bijlage IV of het aanwezig is in het technisch dossier. Noteer de vindplaats en stel de status in.

| Bijlage IV-element | Vindplaats | Status |
|---|---|---|
| Systeembeschrijving — naam, versie, doel, distributiewijze, hardware-eisen | Bijv.: CDR Tech doc, Modelcard | ☐ Aanwezig · ☐ Ontbreekt · ☐ n.v.t. |
| Architectuur, algoritmen, trainingsdata en computerbronnen | Bijv.: Modelcard, CDR Art. 10 | ☐ Aanwezig · ☐ Ontbreekt · ☐ n.v.t. |
| Monitoring en prestatiedrempels (KPI's, anomaliedetectie) | Bijv.: CDR Art. 15, CDR Art. 72 | ☐ Aanwezig · ☐ Ontbreekt · ☐ n.v.t. |
| Geschiktheid van de gedefinieerde prestatieparameters | Bijv.: CDR Art. 15 | ☐ Aanwezig · ☐ Ontbreekt · ☐ n.v.t. |
| Risicobeheersysteem conform Art. 9 | Bijv.: CDR Art. 9 | ☐ Aanwezig · ☐ Ontbreekt · ☐ n.v.t. |
| Wijzigingen gedurende de levenscyclus na ingebruikstelling | Bijv.: Versiebeheer (Git?) | ☐ Aanwezig · ☐ Ontbreekt · ☐ n.v.t. |
| Lijst van gehanteerde geharmoniseerde normen | Bijv.: Inception | ☐ Aanwezig · ☐ Ontbreekt · ☐ n.v.t. |
| EU-conformiteitsverklaring conform Art. 47 | Bijv.: NFI-CONF-001 | ☐ Aanwezig · ☐ Ontbreekt · ☐ n.v.t. |
| Post-market monitoringplan conform Art. 72 lid 3 | Bijv.: CDR Art. 72 | ☐ Aanwezig · ☐ Ontbreekt · ☐ n.v.t. |

---

### Conformity Assistance Records

**Hoe is de strategie voor technische documentatie vastgelegd, incl. mijlpalen, verantwoordelijke partijen per domein en het bijwerkingsproces?**

> Bijv.: een RACI-matrix toont per documentatiedomein (data, risicobeheer, cybersecurity, menselijk toezicht) wie verantwoordelijk, raadpleegbaar, geïnformeerd en aansprakelijk is; de technisch verantwoordelijke heeft 20% FTE gereserveerd voor documentatiebeheer.

`▸ AIV Art. 11.1`

**Antwoord:**

_Vul hier je antwoord in._

---

**Wie is formeel aangesteld als verantwoordelijke voor de technische documentatie, en beschikt deze persoon over voldoende middelen en bevoegdheden?**

> Bijv.: de AI Governance Officer is bij besluit van de directie aangesteld als documentatieverantwoordelijke; deze heeft schrijftoegang tot het technisch documentatiesysteem, een jaarlijks budget voor externe audits, en rapporteert rechtstreeks aan de CTO.

`▸ AIV Art. 11.1 · AIV Art. 17.1`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe is de centrale opslagplaats voor technische documentatie ingericht, met versiebeheer, gedifferentieerde toegangsrechten, audittrail, back-ups en redundantie?**

> Bijv.: alle technische documentatie is opgeslagen in een DMS met versiebeheer (major.minor.patch-nummering); schrijftoegang is beperkt tot twee documenteigenaren; alle wijzigingen worden vastgelegd in een audittrail; dagelijkse back-ups worden bewaard op een geografisch gescheiden server.

`▸ AIV Art. 11.1 · AIV Art. 12.3`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe zijn het beoogde doel, de naam, de versie en de relatie tot eerdere versies van het systeem gedocumenteerd, inclusief interoperabiliteit met externe systemen?**

> Bijv.: het systeem is gedocumenteerd als 'NFI-DNA-Match v2.1', een opvolger van v1.8; de documentatie beschrijft de gewijzigde architectuur ten opzichte van v1.8, de interoperabiliteit met het NFI-zaakbeheersysteem (via REST API v3), en de vereiste hardware-specificaties.

`▸ AIV Art. 11.2`

**Antwoord:**

_Vul hier je antwoord in._

---

**Op welke manier zijn de architectuur, algoritmekeuzes, gehanteerde normen en de gebruikte trainings-, validatie- en testdata gedocumenteerd?**

> Bijv.: de architectuurdocumentatie bevat een dataflowdiagram, een beschrijving van het transformer-gebaseerde modelontwerp, de keuze voor het PTES-framework voor cybersecurity, en een verwijzing naar de datagovernancedocumentatie conform Art. 10.

`▸ AIV Art. 11.2 · AIV Art. 10.2`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe zijn voorzienbare onbedoelde uitkomsten, risico's voor grondrechten en non-discriminatie gedocumenteerd, en welke maatregelen voor menselijk toezicht zijn beschreven?**

> Bijv.: de technische documentatie bevat een expliciete sectie over grondrechtenrisico's, waaronder het recht op een eerlijk proces (Art. 47 EU Handvest) en non-discriminatie (Art. 21); per risico is beschreven welke toezichtmaatregel van toepassing is en wie verantwoordelijk is voor de uitvoering.

`▸ AIV Art. 11.3 · AIV Art. 9.2 · AIV Art. 14.1`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe zijn de prestatieparameters van het systeem gedefinieerd en gevalideerd, en hoe wordt de documentatie bijgehouden bij relevante wijzigingen?**

> Bijv.: prestatieparameters (precisie ≥97%, recall ≥95%) zijn gedocumenteerd in het technisch validatierapport; bij een modelupdate wordt het rapport bijgewerkt vóór ingebruikname; de documentatieverantwoordelijke controleert actualiteit bij elke releasegoedkeuring.

`▸ AIV Art. 11.3 · AIV Art. 15.1`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe is geborgd dat alle wijzigingen aan het AI-systeem na ingebruikstelling worden vastgelegd, beoordeeld op conformiteitsimpact en verwerkt in de technische documentatie?**

> Bijv.: elke modelupdate doorloopt een change request-procedure; de documentatieverantwoordelijke beoordeelt of de wijziging een nieuwe conformiteitsbeoordeling vereist; alle wijzigingen worden bijgehouden in een wijzigingsregister met datum, omschrijving en goedkeurende functionaris.

`▸ AIV Art. 11.1`

**Antwoord:**

_Vul hier je antwoord in._

---

**Welke geharmoniseerde normen of technische specificaties zijn toegepast op dit systeem, en hoe is vastgelegd dat aan de eisen van elk van deze normen is voldaan?**

> Bijv.: ISO 31000 (risicobeheer), NEN-ISO/IEC 25010 (softwarekwaliteit) en ETSI EN 303 645 (cybersecurity) zijn gehanteerd; per norm is een concordantietabel opgesteld die aantoont welke eisen aantoonbaar zijn nageleefd en waar de bewijzen zijn opgeslagen.

`▸ AIV Art. 11.1`

**Antwoord:**

_Vul hier je antwoord in._

---

**Is de EU-conformiteitsverklaring conform Art. 47 opgesteld, ondertekend door de bevoegde persoon en opgenomen in het technisch dossier, inclusief verwijzing naar de relevante bijlagen van de AI-verordening?**

> Bijv.: de conformiteitsverklaring is ondertekend door de directeur op [datum], verwijst naar Art. 6 lid 2 jo. Bijlage III (hoog-risico classificatie) en Bijlage IV (technische documentatie), en is gearchiveerd onder documentnummer NFI-CONF-001 in het DMS.

`▸ AIV Art. 11.1 · AIV Art. 47.1`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe is de bewaring van technische documentatie, QMS-documentatie en conformiteitsverklaringen voor ten minste 10 jaar geborgd, incl. toegankelijkheid voor toezichthouders en continuïteit bij opheffing?**

> Bijv.: de documentatie wordt bewaard in een gecertificeerd archiefsysteem conform NEN 2082; een jaarlijkse archiefcontrole verifieert toegankelijkheid en integriteit; bij opheffing van het NFI is een bewaarsprotocol overeengekomen met de Rijksdienst voor het Cultureel Erfgoed.

`▸ AIV Art. 18.1 · AIV Art. 18.1.a`

**Antwoord:**

_Vul hier je antwoord in._

---

**Hoe wordt het bewaarmechanisme regelmatig gecontroleerd op correcte werking, naleving van de bewaarplicht en toegankelijkheid?**

> Bijv.: elk kwartaal voert de documentatieverantwoordelijke een steekproef uit waarbij vijf willekeurige documenten worden opgehaald en op leesbaarheid en compleetheid gecontroleerd; bevindingen worden gerapporteerd in het kwaliteitsoverleg.

`▸ AIV Art. 18.1`

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
