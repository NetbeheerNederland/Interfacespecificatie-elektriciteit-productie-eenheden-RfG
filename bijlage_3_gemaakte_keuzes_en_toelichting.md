# Bijlage 3 – Gemaakte keuzes en toelichting

De (voorlopige) keuzes die in deze interface specificatie zijn opgedeeld in de verschillende lagen van SGAM. De keuzes staan ter review van allen.

## Componenten
|Keuze:| De mogelijkheid om de interface te integreren in bestaande elektriciteitsproductie-eenheden, als ook het toepassen van gateways.|
|:--|:--|
|Motivatie:| Het ombouwen van bestaande elektriciteitproductie-eenheden kan kostbaar zijn hoewel sturing ervan functioneel al aanwezig is. Het gebruik van gateways als extra levering voor de eenheden kan hier een oplossing bieden. Daarnaast kunnen gateways een bijdrage leveren in een betere lifecycle van de oplossing. Bijvoorbeeld: indien er strengere encryptie-eisen gaan gelden en er meer processorcapaciteit gevraag wordt is een re-design en vervanging van een gateway goedkoper van een gehele PV converter|

|Keuze:| Indien een extra gateway wordt toegepast, dient de verbinding tussen gateway en de elektriciteitsproductie-eenheid via één van de volgende methodes te verlopen: serieële communicatie of stuursignalen als 4-20mA, 0-100V, e.d. of gebruike maken van binaire contacten of mapping naar IEC communicatieprotocollen met goedkeuring van de relevante systeembeheerder.|
|:--|:--|
|Motivatie:| Bovenstaande methodes zijn generiek genoeg en in lijn met huidig beschikbare interfaces van elektriciteitproductie-eenheden. Daarnaast is het opbouwen van een nieuwe IP verbinding, anders dan bovenstaande implementaties, tijdens conformiteitstesten niet te beoordelen tegen standaarden. |

|Keuze:| Bij gebruik van gateways ligt bij de leverancier van de elektriciteitsproductie-eenheden de verplichting om aan te tonen dat de gateway zich alleen maar met één dezelfde productie-eenheid kan verbinden of dat fraude met deze verbinding betrouwbaar kan worden aangetoont.|
|:--|:--|
|**Keuze:**| **Bij de leverancier van de elektriciteitsproductie-eenheden ligt de verplichting om aan te tonen dat fraude op manipulatie van sturing van de electriciteitsproducite-eenheden betrouwbaar kan worden aangetoont.**|
|Motivatie:| Fraude voorkomen door wijzigingen in de elektriciteitproductie-eenheid of in de verbinding tussen gateway en electriciteitproductie-eenheden door te voeren na conformiteitstest of installatie. Verplichting voor leverancier zodat er vanuit de markt een overtuigende en marktconforme oplossing wordt aangedragen i.p.v. een standaard verplichting met hoge modificatiekosten voor leveranciers.|

|Keuze:| Bij gebruik van een gateway, dient de combinatie elektriciteitsproductie-eenheid met gateway aan de conformiteitseisen te voldoen.|
|:--|:--|
|Motivatie:| |

## Communcatie

|Keuze:| Zoveel mogelijk gebruik maken van bestaande publieke netwerken (internet) en private netwerken. Technologie: TCP/IP. Beschikbaarheid: -definieer-|
|:--|:--|
|Motivatie:| Om de maatschappelijke kosten zo laag mogelijk te maken is de keuze gevallen op bestaande telecominfrastructuren en -technolgie. Internet is op veel plekken beschikbaar en TCP/IP is hiervoor een gangbaar protocol. Er wordt zowel over publieke als private netten gesproken, zodat er achteraf, indien noodzakelijk geacht, er geëist kan worden de verbindingen over een specifiek netwerk te laten verlopen.| 

(in te vullen) communicatie voor operationele verbinden, van "Centraal" naar devices...

|Keuze:| Encryptie via TLS|
|:--|:--|
|Motivatie:| TLS is in staat om de encryptie in de toekomst te wijzigen en zo mee te gaan met gangbare encryptie niveau. Daarnaast is TLS bewezen technologie. TLS bevat tevens een tijdssynchronisatie mogelijkheid. (check: hoe kan deze tijdsync vervolgens worden gebruikt?)|

|Keuze:| End-to-end encryptie tot device OF gateway.
|:--|:--|
|Motivatie:| Om bestaande elektriciteitproducite-eenheden geschikt te maken om aan deze interfacespecificatie te voldoen is het toegestaan om de encryptie op een gateway te laten termineren. Dit is een afweging tussen kosten en risico. Het toevoegen van encryptie aan een bestaand product (zoals invertor) kan kostbaar zijn. De directe fysieke connectie zorgt er voor dat de security is beperkt tot locale en fysieke toegang. De combinatie van component-besissingen zoals hierboven gestelt, werken mitigerend op restrisico.|

### Syntactisch

(in te vullen) XMPP,DDS, SOAP, etc

## Informatie

(in te vullen) IEC CIM of (delen van) IEC 61850

(in te vullen) gebruikte profiel

(in te vullen) electriciteitproductie-eenheden of gateways sturen geen data over de interfaces waarmee identificatie van gebruikers of aansluitingen mogelijk is. Dit betekent ook dat er geen EAN codes over de interfaces van deze apparaten wordt gestuurd. 

## Functies
|Keuze:| RfG Type B biedt de mogelijkheid tot ontvangen signaal voor terugregeling maximaal vermogen naar momentaan gespecificeerde limiet (in kW).|
|:--|:--|
|Motivatie:| RfG artikel 14.2. Het sturen op kW-setpoint past bij toekomstige regelvraagstukken. Het resultaat van sturen op %-setpoint is afhankelijk van het maximale vermogen converter, het momentane maximaal vermogen (b.v. zonnestand), en de installatiekarakteristieken (b.v. grote converter met maar één paneel).|

|Keuze:| RfG Type A biedt de mogelijkheid tot het ontvangen van een signaal voor terugregeling van maximaal vermogen naar geen vermogen. De implementatie zoals beschreven bij Type B is niet verplicht voor Type A.|
|:--|:--|
|Motivatie:| RfG artikel 13.6. |

|Keuze:| RfG Type A en B sturen, indien verbonden, meetwaarden en status over het functioneren die in lijn zijn met RfG en GL SO om hiermee "Real-time" beschikbare gegevens voor geaggregeerde productie per primaire energiebron in het DSB-gebied te kunnen aanbieden.|
|:--|:--|
|Motivatie:| GL-SO artikel 44.|

|Keuze:| Een productie eenheid kan zicht in 3 toestanden bevinden. ![Figuur: gedrag productie-eenheden](/assets/Gedrag-productie-eenheden.png) (1) Ongepland autonoom gedrag: De productie-eenheid waarvan de interface zoals gespecificeerd in dit document niet is aangesloten. De productie eenheid voldoet aan de overige netcodes en vertoon bijbehorend gedrag. (2) Gecontroleerd gedrag: De productie-eenheid is geregisteerd en heeft een werkende connectie/interface met de lokale netbeheerder. (3) Gepland autonoom gedrag: De productie-eenheid handeld op basis van vooraf opgestuurde schema's/planning van de systeembeheerder of TSB. |
|:--|:--|
|Motivatie:| Conform 3.2; Het toevoegen van schedules in de eenheden naar Duits voorbeeld kunnen het autonome gedrag en daardoor robuustheid van het elektriciteitsnet versterken.|

|Keuze:| Aanmelden/Afmelden van een elektriciteitsproductie-eenheid kan via een centrale website of API|
|:--|:--|
|Motivatie:| Om het aanmelden van elektriciteitsproductie-eenheiden zo makkelijk mogelijk te maken kan dit via een website of API. Via de API kunnen derden partijen integreren met bijvoorbeeld hun invertor of klantportaal.|

## Business
|Keuze:| De keuze om geen keuze te maken over de invulling van rollen voor het verwerken, aggregeren van data en het primair of als noodbevel uitvoeren van opdrachten.|
|:--|:--|
|Motivatie:| Buiten scope van vraagstuk. De oplossing van de interface onafhankelijk en flexibel specificeren; flexibel maken voor wijzigingen in de energiemarkt. |

|Keuze:| Er wordt 1 centraal register aangewezen waar het registratie van de productie-eenheden plaatsvind.|
|:--|:--|
|Motivatie:| Om complexiteit te voorkomen bij het registratie proces is het handig als de registratie via een centraal register verloopt. Productie-eenheden leveranciers hebben dan een eenduidige ingang waar het registratie proces kan plaats kan vinden. Via dit centrale register kan worden doorvewezen naar 3de partijen.|


|Keuze:| Productie-eenheden zijn direct verbonden met de lokale netbeheerder|
|:--|:--|
|Motivatie:| Om de afhankelijkheid van 3de partijen te verminderen en de de verantwoordelijkheid van de netbeheerder maximaal te kunnen nemen is gekozen om de apparaten direct te laten communiceren met de lokale netbeheerder. Dit zorgt er tevens voor dat in het geval van noodzakeljk ingrijpen de vertraging minimaal is.|
