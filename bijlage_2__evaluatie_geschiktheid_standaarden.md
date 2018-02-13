# Bijlage 2 – Evaluatie geschiktheid Standaarden {#bijlage-2-evaluatie-geschiktheid-standaarden}

*   EF-Pi ([https://fan-ci.sensorlab.tno.nl/builds/fpai-documentation/development/html/](https://fan-ci.sensorlab.tno.nl/builds/fpai-documentation/development/html/) ):
    *   Pro’s
        *   Uit Nederland afkomstig, zowel Alliander als Stedin zijn al bij dit project betrokken.
        *   Wordt al gebruikt in dynamo, er is ervaring aanwezig.
        *   Sluit nauw aan bij de specificaties m.b.t. informatiebehoefte.
    *   Cons:
        *   Lijkt eerder een logische specificatie te zijn dan een technische.
        *   Zelf niet gebaseerd op bestaande standaarden
        *   Classificaties van apparaten zijn een beetje onhandig in de spec `gehardcode’
    *   Overig en conclusie: Deze standaard is niet internationaal bekend en is strijdig met het zoveel mogelijk willen gebruiken van internationale standaarden. Daarom wordt EF-Pi niet geschikt geacht voor de markt-interface en ook minder geschikt voor de DSO/TSO interface, hoewel het iedere DSO/TSO het vrijstaat om het alsnog intern toe te passen.

*   openADR([https://fan-ci.sensorlab.tno.nl/builds/fpai-documentation/development/html/](https://fan-ci.sensorlab.tno.nl/builds/fpai-documentation/development/html/) ):
    *   Pro’s
        *   Lijkt een technische specificatie
        *   Gebaseerd op Oasis Energy Interoperation (EI)
    *   Cons:
        *   Vooral gebruikt in Noord-America
        *   Semantisch gezien onduidelijk, geen meerwaarde
    *   Overig en conclusie: Deze standaard heeft niet de volwassenheid voor een open-internationaal gebruikte standaard. Vanuit de semantische meerwaarde, informatiemodel, heeft deze standaard onvoldoende meerwaarde voor dit vraagstuk.         
        

*   MQTT
    *   Pro’s:
        *   QoS standaard aanwezig
        *   Proof of concept millioenen instanties (Facebook messenger).
        *   bi-directioneel
        *   has a built-in distribution mechanism,supporting one to one,one to many,one to zero distribution models
        *   Lage bandbreedte, want data-centric
    *   Con’s:
        *   Geen informatiewaarde, want data-centric, dus mapping?
        *   Berichtgrootte zeer beperkt, waardoor kans op onvoldoende informatieoverdracht.
        *   End-to-end-Encryptie nog onvoldoende, standaard en getest aanwezig.
    *   Overig en conclusie: MQTT is een veelbelovende standaard voor de toepassing in dit vraagstuk. Vanwege de beperkte berichtgrootte, de nog onvoldoende zekerheid op encryptie in combinatie met het feit dat er nog geen standaardisatie in de energiesector rondom opwek-sturing en vraagsturing plaatsvindt zal MQTT niet worden toegepast. In de toekomst ligt er veel potentieel voor MQTT.

*   Webservices
     *  Pro's:
        *  Zeer volwassen technologie, op grote schaal toegepast bij o.a. bank transacties en veel meer.
        *  Kennis van webservices en toepassingen is breed beschikbaar in de markt.
        *  Flexibel in architecturen in te passen (centraal/decentraal).
        *  Inhoud van berichten is flexible naar eigen inzicht in te richten. Zowel met XML, als JSON.
        *  Kan, afhankelijk van implementatie, zeer weinig traffic veroorzaken. 
     *  Con's:
        *  Vereist een continuë verbinding, of buffering en persistentie bij tijdelijke uitval.
        *  Is een standaard, maar schrijft geen specifieke zaken voor toepassing in Energiesector.
    *   Overig en conclusie: Webservices zijn een goede, flexibele basis waarop een overgroot deel van verschillende sectoren hun systemen hebben gebouwd. Door de flexibiliteit is het mogelijk de architecturen te implementeren die gewenst zijn. Anderzijds is de standaardisatie voor dit specifieke vraagstuk daarmee niet ingevuld. Naast deze standaard is er behoefte aan sector-specifieke standaarden, bijvoorbeeld over gebruik van webservices of de semantiek die wordt ingevuld.          

*   XMPP (Extensible Messaging and Presence Protocol)
    *   Pro's:
        *  In de basis web-services, standaard IT technologie.
        *  In lijn met final-draft IEC 61850-8-2 (Approved for Final Draft International Standard).
        *  Beoogde technologie in Duitsland i.c.m. FNN Steuerbox (naast de MMS optie).
        *  Open standaard met mogelijkheid om flexibiliteit "on-top" te bouwen.
        *  Beproefde technologie met millioenen instanties.
        *  Bi-directioneel.
    *   Con's: 
        *  QoS is expirimenteel.
        *  Nog geen XMPP implementaties in aansturing energiesector bekend.
        *  Vereist een continuë verbinding, of buffering en persistentie bij tijdelijke uitval, want is web-service.
    *   Overig en conclusie: XMPP heeft het potentieel om te worden toegepast bij dit vraagstuk vanwege de standaardisatie binnen IEC 61850 en i.c.m. de FNN Steuerbox. De openstaande vraag is hoe het past in de algehele architectuur met berichtenuitwisseling zoals verder in dit vraagstuk is gespecificeerd. Past dit samen?    

*   IEC CIM
    *   Pro’s:
        *   Informatie is opgesteld in een format dat door andere systemen (gemakkelijker) kan worden geïntegreerd.
        *   In lijn met interface specificatie alle grotere SCADA leveranciers
    *   Con’s:
        *   Niet direct toepasbaar op huidige/oude systemen.
        *   Geen communicatie-dragers gespecificeerd.
        *   Netwerkbelasting mogelijk groter.
    *   Overig en conclusie: IEC CIM is naast IEC 61850 één van de standaarden die in Europa de betekenis van informatieoverdracht definiëren en structureren en blijft voorlopig candidaat.
    
*   IEC 61850
   *  Pro's:
        * Reeds in gebruik bij vele onderstations en IED's
        * Hoog detail niveau voor controle en schakel functies
        * Onderdeel van de IEC doel architectuur: IEC62357
   * Con's:
        * Beperkt zich tot stations/devices, het volledigte elektriciteitsnet kan niet worden uitgedrukt in IEC61860
        * Complex: standaard kent vele pagina's en opties etc.
        * XMPP implementatie is relatief nieuw (Nog in draft, 248 pagina's)
