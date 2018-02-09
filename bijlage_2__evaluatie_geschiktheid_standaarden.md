# Bijlage 2 – Evaluatie geschiktheid Standaarden {#bijlage-2-evaluatie-geschiktheid-standaarden}

*   EF-Pi ([https://fan-ci.sensorlab.tno.nl/builds/fpai-documentation/development/html/](https://fan-ci.sensorlab.tno.nl/builds/fpai-documentation/development/html/) ):
    *   Pro’s
        *   Uit Nederland afkomstig, zowel Alliander als Stedin zijn al bij dit project betrokken.
        *   Wordt al gebruikt in dynamo.
        *   Sluit nouw aan bij de specs zoals jij die aangaf
    *   Cons:
        *   Lijkt eerder een logische specificatie te zijn dan een technische.
        *   Zelf niet gebaseerd op bestaande standaarden
        *   classificaties van apparaten zijn een beetje onhandig in de spec `gehardcode’
    *   Overig en conclusie: Deze standaard is niet internationaal bekend en is strijdig met het zoveel mogelijk willen gebruiken van internationale standaarden. Daarom wordt EF-Pi niet geschikt geacht voor de markt-interface en ook minder geschikt voor de DSO/TSO interface, hoewel het iedere DSO/TSO het vrijstaat om het alsnog intern toe te passen.
*   openADR([https://fan-ci.sensorlab.tno.nl/builds/fpai-documentation/development/html/](https://fan-ci.sensorlab.tno.nl/builds/fpai-documentation/development/html/) ):
    *   Pro’s
        *   Lijkt een technische specificatie
        *   Gebaseerd op Oasis Energy Interoperation (EI)
    *   Cons:
        *   Vooral gebruikt in Noord-America
        *   Semantisch gezien konden we hier geen soep van maken
*   Steuerbox (zie mail `FNN Steurbox v1.0‘ + bijlage)
    *   Pro’s:
        *   Zeer gedetaileerd +
        *   Gebaseerd op 61850
        *   Dit is het Duitse antwoord op de zelfde wetgeving
    *   Cons:
        *   In het Duits (spreek ik zelf niet zo goed, maar jij hebt hier misschien helemaal geen moeite mee ;-)) dus ik kan het niet zo goed beoordelen
        *   Sander: Semantisch is 61850 niet zo goed uitgewerkt, ik zou hier CIM voor gebruikt hebben.
        *   Lijkt niet 1 op 1 aan te sluiten op de architectuur zoals wij die voor ogen hebben (moet een apart kastje geinstalleerd worden, maar hoe dat kastje aangesloten wordt is wél gespecificeerd, en deze ontkoppeling heeft ook zijn voordelen)
*   MQTT
    *   Pro’s:
        *   QoS standaard aanwezig
        *   Proof of concept millioenen instanties (Facebook messenger).
        *   bidirectioneel
        *   has a built-in distribution mechanism,supporting one to one,one to many,one to zero distribution models
        *   Lage bandbreedte, want data-centric
    *   Con’s:
        *   Geen informatiewaarde, want data-centric, dus mapping???
*   IEC CIM
    *   Pro’s:
        *   Informatie is opgesteld in een format dat door andere systemen (gemakkelijker) kan worden geïntegreerd.
        *   In lijn met interface specificatie alle grotere SCADA leveranciers
    *   Con’s:
        *   Niet direct toepasbaar op huidige/oude systemen.
        *   Geen communicatie-dragers gespecificeerd.
        *   Netwerkbelasting mogelijk groter.