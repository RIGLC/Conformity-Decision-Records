# Wat is een Compliancy Decision Record?

De Europese AI-verordening (AIV) verplicht organisaties die AI-systemen ontwikkelen of inzetten
tot aantoonbare naleving van juridische eisen. Dit vraagt om traceerbare, gestructureerde
documentatie van keuzes die worden gemaakt gedurende de ontwikkeling van een AI-systeem.

## Waarom een CDR?

Een toezichthouder, auditor of externe partij moet kunnen vaststellen wat er is gedaan, waarom,
en waar het bewijs te vinden is. Zonder systematische aanpak raakt deze informatie verspreid over
losse documenten en wordt daarmee onvindbaar of onbetrouwbaar. Het Compliancy Decision Record
(CDR) lost dit op. Per thema uit de AI-verordening wordt vastgelegd welke maatregelen zijn
getroffen, in welke mate daaraan is voldaan, en wie daar verantwoordelijk is.

## Hoe deed aanpak; waar komt het vandaan?

Het CDR bouwt voort op het Architectural Decision Record (ADR), een bewezen werwijze uit de
softwareontwikkeling. Een ADR legt vast waarom een technische keuze is gemaakt, zodat de
redenering later nog te begrijpen en te verantwoorden is. Hetzelfde principe wordt hier toegepast
op compliance: in plaats van architectuurkeuzes worden compliancekeuzes gedocumenteerd.

## Hoe werkt het?

Compliance wordt behandeld als integraal onderdeel van de ontwikkelcyclus, niet als administratief
proces achteraf. De opzet kent één centrale structuur:

- **Inception** is de single point of truth. Hier staat per thema het toepasselijke wetsartikel,
  de vertaling naar concrete maatregelen, en de actuele stand van zaken.
- **De uitvoering** staat dichtbij de code. Het daadwerkelijke bewijs, technische implementatie,
  onderbouwingen en verantwoordingen, wordt vastgelegd in de repository van het systeem, en waar
  van toepassing in modelcards en datasheets. Zo is de documentatie altijd een actuele weergave
  van wat het systeem werkelijk doet.
- **Elke maatregel** verwijst terug naar Inception. Dit voorkomt verspreide of verouderde
  documentatie en maakt het systeem op elk moment auditeerbaar.
