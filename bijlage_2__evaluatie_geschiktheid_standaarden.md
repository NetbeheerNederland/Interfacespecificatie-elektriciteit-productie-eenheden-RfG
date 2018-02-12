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

*   XMPP (Extensible Messaging and Presence Protocol)
    *   Pro's:
        *  In lijn met final-draft IEC 61850-8-2 (Approved for Final Draft International Standard).
        *  Beoogde technologie in Duitsland i.c.m. FNN Steuerbox.
        *  Open standaard met mogelijkheid om flexibiliteit "on-top" te bouwen.
        *  In de basis web-services, standaard IT technologie.
        *  Beproefde technologie met millioenen instanties.
        *  Bi-directioneel.
    *   Con's: 
        *  QoS is expirimenteel.
        *  Nog geen XMPP implementaties in aansturing energiesector bekend.
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
