## Informatie vanuit overige EU landen {#informatie-vanuit-overige-eu-landen}

### Duitsland, FNN steuerbox {#duitsland-fnn-steuerbox}

De uitgangssituatie in Duitsland is anders. Ten eerste ligt de grens van Type A en Type B productie-installaties niet op 1MW (zoals in Nederland), maar op 130kW. Dit betekent dat er relatief kleinere installaties (middelgroot boeren-schuurdak) in categorie B zullen vallen en de Type A in zijn geheel weinig significantie heeft op het Elektriciteitsnet. Daarnaast is in Duitsland vooral een technologische oplossing gezocht die de Netbeheerders in staat stelden om zelf de afschakeling te kunnen uitvoeren. Er is ten tijde van het oplossen van destijds ontstane congesties nog niet gekeken naar marktwerking en bekende IT technologieën die wat meer onbekend zijn in OT landschappen. Het doel was immers congesties op te lossen vanuit DNO perspectief.

De kosten van deze steuerboxen worden gedragen door de netbeheerders en verrekend in de tarieven. In onze beleving worden de aanschafkosten relatief hoog (paar honderd euro) ten opzichte van technologie wat door de markt kan worden gedreven.

De FNN steuerbox is gespecificeerd, maar er is op het moment van schrijven nog geen bericht ontvangen dat een leverancier is gecertificeerd en de uitlevering kan plaatsvinden. De gekozen protocollen (opbouw verbinding en datamodellen) zijn nog niet op grote schaal aangetoond. Een deel van de standaarden pas in 2017 vrijgegeven. Tot slot wordt er gebruik gemaakt van een diversiteit aan communicatietechnologieën om de Steuerboxen aan te sluiten (GPRS, Funk, LAN, etc). Hiermee is zeer onzeker dat vereiste functies (zoals software updates) überhaupt kunnen plaatsvinden. Rollen voor bijvoorbeeld software-updates zijn nog niet gedefinieerd.

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

Voor Type A is op het moment van schrijven nog geen specificatie voorhanden. Dit heeft ermee te maken (zoals in Duitsland) dat de grens tussen Type A en Type B lager zal liggen dan in Nederland, namelijk 250kW. Hiermee is de populatie Type A in België (nog) minder relevant dan in Nederland.

Voor Type B wordt vooral gebruik gemaakt van ervaringen van een telecontrolkast die al bij opwek met een vermogen &gt;1MW wordt toegepast.

In Belgie wordt gepleit om het recht te hebben om de interface 1x per jaar te mogen testen.

### UK {#uk}

RfG bekend, maar geen reactie hoe men dit oplost.