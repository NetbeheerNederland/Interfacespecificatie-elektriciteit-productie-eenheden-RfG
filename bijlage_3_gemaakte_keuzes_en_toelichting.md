# Bijlage 3 – Gemaakte keuzes en toelichting

De (voorlopige) keuzes die in deze interface specificatie zijn opgedeeld in de verschillende lagen van SGAM. De keuzes staan ter review van allen.

## Componenten
|**Keuze:**| **De mogelijkheid om de interface te integreren in bestaande elektriciteitsproductie-eenheden, met daarnaast de mogelijkheid voor het toepassen van extra gateways.**|
|:--|:--|
|Motivatie:| Het ombouwen van bestaande elektriciteitproductie-eenheden kan kostbaar zijn hoewel sturing ervan functioneel al aanwezig is. Het gebruik van gateways als extra levering voor de eenheden kan hier een oplossing bieden. Daarnaast kunnen gateways een bijdrage leveren in een betere lifecycle van de oplossing. Bijvoorbeeld: indien er strengere encryptie-eisen gaan gelden en er meer processorcapaciteit gevraag wordt is een re-design en vervanging van een gateway goedkoper van een gehele converter of sturing.|

|**Keuze:**| **Bij gebruik van een gateway, dient de combinatie elektriciteitsproductie-eenheid met gateway aan de conformiteitseisen te voldoen.**|
|:--|:--|
|Motivatie:|Indien een gateway wordt gebruikt die niet (meer) aan de conformiteitseist voldoet, kan de certificering worden ingetrokken.|

|**Keuze:**| **De (eind)leverancier van de elektriciteitsproductie-eenheden is verplicht een conformiteitsverklaring met de hardware te leveren. Met de conformiteitsverklaring is aangetoond dat fraude of manipulatie van aansturing zeer onwaarschijnlijk is.**|
|:--|:--|
|Motivatie:| Fraude zoveel mogelijk voorkomen door het ontwerp van de eenheid (eventueel i.c.m. gateway) of tijdens de installatie hiervan of door achteraf wijzigingen door te voeren in de elektriciteitproductie-eenheid. Verplichting voor leverancier zodat er vanuit de markt een overtuigende en marktconforme oplossing wordt aangedragen i.p.v. een standaard verplichting met hoge modificatiekosten voor leveranciers.|

|**Keuze:**| **Advies: verberg optionele QR codes voor registratie**|
|:--|:--|
|Motivatie:| In het document wordt de optie voorgesteld om registratie met een QR code te laten verlopen. Aangezien iedereen die toegang heeft tot de QR code ook toegang heeft tot registratie, geldt een sterk advies naar alle partijen om QR codes te verbergen voor publieke toegang (zicht erop).|

## Communicatie

|**Keuze:**| **Zoveel mogelijk gebruik maken van bestaande publieke netwerken (internet) en private netwerken. Technologie: TCP/IP. Beschikbaarheid: >99% beschikbaarheid wordt verwacht, een langere response dan 15 seconden wordt gezien als offline**|
|:--|:--|
|Motivatie:| 1) Om de maatschappelijke kosten zo laag mogelijk te maken is de keuze gevallen op bestaande telecominfrastructuren en -technolgie. Internet is op veel plekken beschikbaar en TCP/IP is hiervoor een gangbaar protocol. Er wordt zowel over publieke als private netten gesproken, zodat er achteraf, indien noodzakelijk geacht, er geëist kan worden de verbindingen over een specifiek netwerk te laten verlopen. De Nederlandse internetproviders leveren een vele hogere mate van beschikbaarheid. Met het verschil kan onbeschikbaarheid in huisinstallaties (b.v. Wifi, repeaters) worden opgevangen. 2) De vraag of systeembeheerders eventueel gebruik willen maken van eigen telecomnetten voor grotere elektriciteitproductie-eenheden is denkbaar, maar nog niet bepaald. Welke technologie hiervoor gebruikt wordt, wordt nog opengelaten. Op het moment van schrijven, begin 2018, is er nog veel ongedefinieerd is op telecomdiensen als LTE-M en Narrowband IoT wat betreft beschikbare functies (zoals gedrag van de sleep-modus bepalen) en services. De keuze is daarom geen telecomkeuzes te maken. Een ethernetpoort voor grotere type productie-eenheden biedt voorlopig de flexibiliteit om deze later met een specifiek telecomnetwerk te verbinden (indien noodzakelijk).

|**Keuze:**| **Interfaces van elektriciteitsproductie-eenheden verbinden met “centrale” infrastructuur voor verbindingsverzoek, vervolgens verbinden de interfaces van de elektriciteitsproductie-eenheden opnieuw met “centrale” infrastructuur voor operationele verbinding. /(Zie 3.3./)**|
|:--|:--|
|Motivatie:| Interfaces verbinden automatisch met “centrale” infrastructuur zonder extra configuraties in routers. Het verbinden in twee trappen draagt bij aan de robuustheid en geeft een extra mogelijkheid om operationele verbindingen met de juiste partij / infrastructuur op te bouwen. |

|**Keuze:**| **Encryptie en tijdreferentie via TLS**|
|:--|:--|
|Motivatie:| TLS is in staat om de encryptie in de toekomst te wijzigen en zo mee te gaan met gangbare encryptie niveau. Daarnaast is TLS bewezen technologie. TLS bevat tevens een tijdssynchronisatie die als referentie wordt gebruikt in het gehele systeem, zie hiervoor ook besluit over maximale tijdsafwijking.  |

|**Keuze:**| **End-to-end encryptie tot device OF gateway.**|
|:--|:--|
|Motivatie:| Om bestaande elektriciteitproducite-eenheden geschikt te maken om aan deze interfacespecificatie te voldoen is het toegestaan om de encryptie op een gateway te laten termineren. Dit is een afweging tussen kosten en risico. Het toevoegen van encryptie aan een bestaand product (zoals invertor) kan kostbaar zijn. Dit betekent automatisch dat de connectie tussen gateway en elektriciteitsproductie-eenheid niet automatisch encrypted is, echter aangezien dit een directe fysieke connectie is, bestaat hier alleen een security risico onder verantwoordelijkheid van eigenaar installatie.|

|**Keuze:**| **Interface ondersteuning voor IPv4 en IPv6**|
|:--|:--|
|Motivatie:| Gezien de brede adoptie van IPv4 en IPv6 is de eis om beide te ondersteunen. Dit ligt volledig in lijn met de Duitse FNN steuerbox specificaties. |

### Syntactisch

|**Keuze:**|**Het gebruik van XMPP**|
|:--|:--|
|Motivatie:| 1.	XMPP is gekozen door de IEC: IEC 61850-8-2/3. 2.	XMPP is uitbreidbaar, Er zijn voorbeelden van spraak en spelletjes die gebruik maken van het XMPP protocol dmv XMPP uitbreidingen. 3.	Door het XMPP presence protocol is het helder welke productie eenheden verbonden zijn. 4.	XMPP biedt de mogelijkheid voor schema validatie 5. XMPP biedt de mogelijkheid voor message encryption. 6. De XMPP ondersteunt een verbinding opzetten van binnenuit naar de server. 7. Het is aantoonbaar goed schaalbaar, waardoor een miljoen aangesloten installatie geen onredelijke infrastructuur nodig heeft om draaiend te houden. 8. Klein nadeel: XMPP maakt standaard niet gebruik van standaarden pooren zoals http en https. Dit is mogelijk iets meer configureer werk voor geadvanceerde TCP/IP netwerkconfiguraties met een uitgaande firewall.   |

## Informatie
|**Keuze:**|**Toepassen van digitaal Certificaat van de elektriciteitproductie-eenheid _Producent_ t.b.v. registratietoken als ook bij firmeware updates**|
|:--|:--|
|Motivatie:| 1. Voor het registeren (op de website) van een eenheid, mag geen informatie van overige installaties en "procumenten" worden gezocht door onberechtigde gebruikers. Naast het sturen van een ID van het device, beschermt het extra sturen van een token hiertegen (bijvoorbeeld samen verwerkt in QR code zoals beproefd in implementaties bij Netbeheerder). De public key van de producent is bij het registratieproces bekend, hiertegen wordt getoetst. 2. Het certificaat is bruikbaar om software-updates te valideren. In lijn met Duitse specificatie voor Steuerbox en in lijn met stand van de techniek en beveiligingseisen.  |

|**Keuze:**|**Gebruik van UTC tijd**|
|:--|:--|
|Motivatie:| In lijn met IEC 61850, overeenstemmend met Duitse FNN Steuerbox specificatie, geen implementatie en management noodzakelijk voor zomer/wintertijd aanpassingen in decentrale devices. |

|**Keuze:**|**Geen privacy-gevoelige data in uitwisseling interface<->"centrale" systemen**|
|:--|:--|
|Motivatie:| De interface van de elektriciteitproductie-eenheid wisselt geen data uit waarin informatie is af te leiden over klant / aansluiting. De uitwisseling vindt plaats op basis van annonieme sleutels. De koppeling naar de positie in het elektriciteitsnet wordt in een "centrale" veilige omgeving gemaakt indien nodig. |

(in te vullen) IEC CIM of (delen van) IEC 61850

(in te vullen) gebruikte profiel

(in te vullen) electriciteitproductie-eenheden of gateways sturen geen data over de interfaces waarmee identificatie van gebruikers of aansluitingen mogelijk is. Dit betekent ook dat er geen EAN codes over de interfaces van deze apparaten wordt gestuurd. 

## Functies
|**Keuze:**| **RfG Type B biedt de mogelijkheid tot ontvangen signaal voor terugregeling maximaal vermogen naar momentaan gespecificeerde limiet (in kW).**|
|:--|:--|
|Motivatie:| RfG artikel 14.2. Het sturen op kW-setpoint past bij toekomstige regelvraagstukken. Het resultaat van sturen op %-setpoint is afhankelijk van het maximale vermogen converter, het momentane maximaal vermogen (b.v. zonnestand), en de installatiekarakteristieken (b.v. grote converter met maar één paneel).|

|**Keuze:**| **RfG Type A biedt de mogelijkheid tot het ontvangen van een signaal voor terugregeling van maximaal vermogen naar geen vermogen. De implementatie zoals beschreven bij Type B is niet verplicht voor Type A.**|
|:--|:--|
|Motivatie:| RfG artikel 13.6. |

|**Keuze:**| **RfG Type A en B sturen, indien verbonden, meetwaarden en status over het functioneren die in lijn zijn met RfG en GL SO om hiermee "Real-time" beschikbare gegevens voor geaggregeerde productie per primaire energiebron in het DSB-gebied te kunnen aanbieden.**|
|:--|:--|
|Motivatie:| GL-SO artikel 44.|

|**Keuze:**| **Een productie eenheid kan zich in meerdere toestanden bevinden. ![Figuur: gedrag productie-eenheden](/assets/Gedrag-productie-eenheden.png)**  |
|:--|:--|
|Motivatie:| Conform 3.2; Het toevoegen van schedules in de eenheden naar Duits voorbeeld kunnen het autonome gedrag en daardoor robuustheid van het elektriciteitsnet versterken.|

|**Keuze:**| **Aanmelden/Afmelden van een elektriciteitsproductie-eenheid kan via een centrale website of API**|
|:--|:--|
|Motivatie:| Om het aanmelden van elektriciteitsproductie-eenheiden zo makkelijk mogelijk te maken kan dit via een website of API. Via de API kunnen derden partijen integreren met bijvoorbeeld hun invertor of klantportaal.|

|**Keuze:**| **Detectie en mitigatie bij tijdsafwijking groter dan 2 seconden (klasse 1 interface voor RfG Type A) en groter dan 1 seconde (klasse 2 interface voor RfG Type B)**|
|:--|:--|
|Motivatie:| Voor de sturing en het loggen van acties op het energiesysteem is een integere tijd noodzakelijk. De referentietijd vanuit de TLS is geldend als maatstaf. Het mitigeren van de afwijking wordt naar inzicht van de leverancier geïmplementeerd, zoals (opnieuw)synchroniseren, melding van tijdsafwijking volgens gespecificeerd datapunt. Het doel is om niet meer dan 1x per dag opnieuw te synchroniseren. Ongecalibeerde hardware met een maximale afwijking van ca. 1,7 seconden blijkt beschikbaar tegen lage kosten. Voor de betere klasse interfaces is dus betere hardware noodzakelijk, of calibratie om aan de 1 seconde te voldoen. |

## Business
|**Keuze:**| **De keuze om geen keuze te maken over de invulling van rollen voor het verwerken, aggregeren van data en het primair of als noodbevel uitvoeren van opdrachten.**|
|:--|:--|
|Motivatie:| Buiten scope van vraagstuk. De oplossing van de interface onafhankelijk en flexibel specificeren; flexibel maken voor wijzigingen in de energiemarkt. |

|**Keuze:**| **Er wordt 1 centraal register aangewezen waar het registratie van de productie-eenheden plaatsvindt.**|
|:--|:--|
|Motivatie:| Om complexiteit te voorkomen bij het registratie proces is het handig als de registratie via een centraal register verloopt. Productie-eenheden leveranciers hebben dan een eenduidige ingang waar het registratie proces kan plaatsvinden. Via dit centrale register wordt doorverwezen naar de (op dat moment) relevante een systeembeheerder. Dit voorkomt dat een elektriciteitsproductie-eenheid alle netbeheerders moet kennen. Door het snelle doorverwijzen naar de relevante systeembeheerder wordt de centrale serverbelasting tot een minimum beperkt en heeft de systeembeheerder een integraalbeeld van al zijn relevante productie-eenheden.|


|**Keuze:**| **Productie-eenheden zijn direct verbonden met de lokale netbeheerder**|
|:--|:--|
|Motivatie:| Om de afhankelijkheid van 3de partijen te verminderen en de de verantwoordelijkheid van de netbeheerder maximaal te kunnen nemen is gekozen om de apparaten direct te laten communiceren met de lokale netbeheerder. Dit zorgt er tevens voor dat in het geval van noodzakeljk ingrijpen de vertraging minimaal is.|

|**Keuze:**| **Toestemming en het recht t.b.v. testen en analyse op goede werking**|
|:--|:--|
|Motivatie:| Het verifiëren van de werking van het gehele systeem /(gedrag van elektriciteitproductie-eenheid, eventueel gateway, en "centraal" systeem/) door het willekeurig testen van de afschakel of regelfunctie bij prosumenten.  Dit mag niet onredelijk bezwarend zijn voor de gebruiker. Goede werking van een specifiek merk en type eenheid wordt aangetoond o.b.v. analyse in de combinatie met overige netbeheerdermeetdata inclusief slimme-meterdata waarvoor toestemming is gegeven. Testen is in lijn met Belgische implementatie.|

|**Keuze:**| **Aanmelden  elektriciteitsproductie eenheden API geen onderdeel van interface specificatie**|
|:--|:--|
|Motivatie:| Om de eerste versie van de interface specificatie eenvoudig te houden is er voor gekozen om de API voor het registreren van de elektriciteitsproductie eenheden geen onderdeel te maken van de specificatie. Mogelijk dat in de toekomst elektriciteitsproductie eenheden zichtzelf (gedeeltelijk) kunnen registreren.|

|**Keuze:**| **Systeembeheerder stuurt op werkelijk vermogen**|
|:--|:--|
|Motivatie:| Er is er gekozen om enkel op werkelijk vermogen te gaan sturen. De discussie rondom blindvermogen is nog niet afgerond. Indien de noodzaak voor het sturen op blindvermogen wordt aan getoond kan dit worden toegevoegd aan de volgende versie van deze interfacespecificatie. Bij de keuzes voor de interfacespecificatie moet hier alvast rekening mee worden gehouden, maar hoeft de (externe) sturing op blindvermogen nog niet worden geïmplementeerd. Hetzelfde geldt elektriciteitsproductie-eenheden die elektriciteit kunnen opslaan. Dit is vooralsnog niet in de specificatie voorzien maar moet later kunnen worden toegevoegd. |
