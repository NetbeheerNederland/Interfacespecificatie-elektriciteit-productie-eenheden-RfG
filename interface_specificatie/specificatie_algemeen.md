## Algemene zaken m.b.t. interface specificatie

Inleiding

Aan elektriciteitproductie-eenheden die een grotere impact op het energienet hebben (bijvoorbeeld RfG Type B), kunnen meer eisen worden gesteld. Daarom worden eisen gesteld per [interface-klasse](https://netbeheernederland.gitbooks.io/interfacespecificatie-elektriciteit/content/samenvatting.html). De interfaces voor de eenheden met een grotere impact op het energienet benoemen we hier een "Klasse 2" interface. De meest eenvoudige interface noemen we een "Klasse 1" interface. In de onderstaande specificatie wordt duidelijk aangegeven indien dit alleen geldt voor een "Klasse 2" interface.

### Primaire specificaties
Deze specificaties hebben direct betrekking op technische aspecten van de interface.
*	Gebruik van – door de markt aangeboden – IP connectiviteit. 
* (Alleen Klasse 2): Bij grotere vermogens kan geëist worden dat de IP connectiviteit alsnog via de Netbeheerder loopt. Er geldt daarom en fysieke eis voor een Ethernetaansluiting.
* Gebruik van delen van IEC 61850 waaronder:

|Standaard|Naam|
|:--|:--|
|IEC 61850-7-1 | Basic communication structure – Principles and models |
|IEC 61850-7-2 | Basic communication structure – Abstract communication service interface (ACSI)|Description of Abstract communication service interface|
|IEC 61850-7-3 | Basic communication structure – Common data classes | 
|IEC 61850-7-4 | Basic communication structure – Compatible logical node classes and data classes | 
|IEC 61850-7-6 DRAFT | Guideline for definition of Basic Application Profiles (BAPs) using IEC 61850 | 
|IEC 61850-7-420| Communication systems for distributed energy resources (DER) – logical nodes|
|IEC 61850-8-2 DRAFT| Specific communication service mapping (SCSM) - Mapping to Extensible Messaging Presence Protocol (XMPP) | 
|IEC 61850-80-3 | Mapping to Web Services - Requirement Analysis and Technology Assessment |
|IEC 61850 90-7| Object models for power converters in distributed energy resources (DER) systems |
|IEC 61850 90-10| IEC 61850 objects for scheduling |

* Eigen uitbreidingen voor zaken die niet in de 61850 Abstract communication service interface (ACSI) zijn beschreven maar wel noodzakelijk voor bijvoorbeeld het aanmelden en vervangen van certificaten.
 

### Secundaire specificaties
Non-functionele specificaties gerelateerd aan de interface.
*	Recht om 1x per jaar te testen in een operationele situatie (dus niet in een aparte testmodus).
*	Recht om het BAP maximaal 1 x per jaar aan te passen.
*	Eigenaren/Leveranciers van elektriciteitproductie-eenheid verantwoordelijk voor firmware upgrades en security patches
*	Voorlopige vrijstelling
  *	T.e.m. aansluiting AC4 (tot 160kVA bij Liander).
  *	T.e.m. datum (b.v. 12 maanden na publicatie van detailspecificatie v1 in het Engels), maar niet later dan december 2019.

