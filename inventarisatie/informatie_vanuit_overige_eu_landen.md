## Informatie vanuit overige EU landen {#informatie-vanuit-overige-eu-landen}

### Duitsland, FNN steuerbox {#duitsland-fnn-steuerbox}

De uitgangssituatie in Duitsland is anders. In het EEG (Erneuerbare-Energien-Gesetz, de Duitse wetgeving rondom duurzame energie) is het volgende vastgelegd [(bron)](https://www.netze-bw.de/z%C3%A4hler/grid-modul).
* 0 tot 30 kWp:	installaties, die na 1 januari 2012 geïnstalleerd zijn, moeten ofwel verreregelbaar zijn of continue op 70% worden gereduceerd.
* 30 tot 100 kWp:	Verreregelbaarheid van de invoeding voor alle installaties vanaf 1 januari 2009. 
* 100 kWp of meer: Verregegelbaarheid en communiceren van stroominvoeding bij netbeheerder. 

Doordat de nationale wetgeving voorloopt zijn de grenzen in Duitsland anders. Voor de EU-grenzen (type RFG A, B, etc) wordt het volgende verwacht: de grens van RfG Type A en Type B elektriciteitproductie-eenheden ligt niet op 1MW (zoals in Nederland), maar op 130kW. Dit betekent dat de relatief kleine installaties (bijvoorbeeld een middelgroot boeren-schuurdak) in categorie B zullen vallen. Daarmee heeft RfG Type A in zijn geheel weinig significantie heeft op het Elektriciteitsnet. In Duitsland is vooral een technologische oplossing gezocht die de Netbeheerders in staat stelden om zelf de afschakeling te kunnen uitvoeren. Er is ten tijde van het oplossen van de ontstane congesties destijds geen grote focus geweest op marktwerking. Het toepassen van bekende OT technologie (zoals RTU's) heeft voorrang gekregen t.o.v. het toepassen van (meer) IT technologieën (zoals software stacks). Het doel was immers congesties op te lossen vanuit DNO perspectief, met daarnaast ook te kunnen bijdragen aan stabiliteit op TSO niveau.

De kosten van deze steuerboxen worden gedragen door de netbeheerders en verrekend in de nettarieven. In onze beleving worden de aanschafkosten relatief hoog (paar honderd euro) ten opzichte van technologie wat door de markt kan worden aangeboden. Daarnaast ontstaan er extra kosten voor het operationaliseren en het beheer door de netbeheerders zelf (zoals het aansluiten van de elektriciteitproductie-eenheid met DSO gateway-steuerbox en het onderhoud ervan). 

De FNN steuerbox is gespecificeerd, maar er is op het moment van schrijven nog geen melding van een gecertificeerde oplossing waarmee de uitlevering kan plaatsvinden. De gekozen protocollen (voor de opbouw van de verbinding en de datamodellen) zijn nog niet op grote schaal aangetoond. Een deel van de standaarden is pas in 2017 vrijgegeven. Tot slot wordt er gebruik gemaakt van een diversiteit aan communicatietechnologieën om de Steuerboxen aan te sluiten (GPRS, Funk, LAN, etc). Hiermee is zeer onzeker dat vereiste functies (zoals software updates) überhaupt kunnen plaatsvinden. Rollen voor bijvoorbeeld software-updates zijn bijvoorbeeld toegewezen aan de 'Gateway-administrator', echter wie dit concreet gaat invullen is nog niet gedefinieerd.

Wat ook meegenomen is, maar nog niet volledig uitgewerkt, is dat een consument zelf kan bepalen welke partij welke data mag zien en wie welke bevoegdheden heeft (bijvoorbeeld schakelen). Dit is gedaan om a) de consument controle te geven over de eigen data en b) om het mogelijk te maken voor consumenten om zich te verenigen in een partij die energie verkoopt. Hiermee kan een derde partij de mogelijkheid krijgen om opwek aan en af te schakelen als het economisch gunstig is. 

Desalniettemin geeft de FNN Steuerbox goede handvatten voor de interfacespecificatie in Nederland welke vooral in de eigen requirements (zie vervolghoofdstukken) zijn verwerkt. Extra noemenswaardig zijn de:

**Primaire Functies:**

*   Systemreserve (System)
*   Schaltprogramm (EMT)
*   Wischerbefehl (EMT)
*   Direktbefehl (EMT)
*   Softstart (System)
*   Wischerbefehl (VNB)
*   Direktbefehl (VNB)
*   Kommunikationsausfall
*   Notbefehl (VNB)

**Secundaire Functies:**

*   Firmware-Update
*   Parameterierung
*   Diagnose
*   Tijdsynchronisatie

**Informatie:**

*   Sturingsfuncties in CLS-Datamodel volgens IEC 61850
*   Prioriteiten van sturingsfuncties: IEC TR 61850-90-10
*   Eigen 61850 gemodelleerd datamodel voor Firmware-Update, Parameter-aanpassingen en Diagnose voor duidelijke scheiding in datamodel onafhankelijk van leverancier; een standaard die nog in ontwikkeling is binnen IEC61850.

**Communicatie:**

*   IEC 61850-8-1 (MMS)
*   IEC 61850-8-2 (XMPP)
*   Ondersteuning IPv4 en IPv6 (Dual Stack)

### België {#belgi}

In België hebben we de volgende oplossingen waargenomen:

Voor Type A is op het moment van schrijven nog geen specificatie voorhanden. Dit heeft ermee te maken (zoals in Duitsland) dat de grens tussen Type A en Type B naar verwachting lager zal liggen dan in Nederland, namelijk 250kW. Hiermee is de populatie Type A in België (nog) minder relevant dan in Nederland.

Voor Type B wordt vooral gebruik gemaakt van ervaringen van een telecontrolkast die al bij opwek met een vermogen &gt;1MW wordt toegepast.

In Belgie wordt gepleit om het recht te hebben om de interface 1x per jaar te mogen testen.

### UK {#uk}

RfG bekend, maar geen reactie hoe men dit oplost.
