## Informatie- en communicatiekader {#informatie-en-communicatiekader}

In Figuur 6 is zichtbaar dat RfG type A is uitgevoerd met een logische interface \(conform RfG artikel 13.6\). Tevens is in het figuur te zien dat bij RfG type B de systeembeheerder \(in dit geval de DSO\) eisen mag stellen aan extra apparatuur \(RfG artikel 14.2.d\). Voor DCC wordt een soortelijke situatie verwacht. 

Om de maatschappelijke kosten van de implementatie te beperken wordt in het ontwerp vooral gestreefd naar het gebruik van bestaande telecom- en data-infrastructuren, dus beschikbaar op de markt of beschikbaar bij de systeembeheerders. Ten behoeve van een toekomstvast ontwerp wordt er expliciet gekozen om geen beperkingen op te leggen aan de te gebruiken communicatietechnologie. Er wordt alleen gekozen voor IP-connectiviteit met minimaalvereisten op bijvoorbeeld bandbreedte en latency. De keuze voor de drager \(DLS, LTE, …\) wordt opengelaten. Deze verbindingen worden gevisualiseerd in Figuur 6 tussen de groene-device-interfaces en de infrastructuur. 

De plaatsing van extra apparatuur bij RfG Type B, is een afweging tussen het garanderen van de systeemveiligheid \(lees: stabiliteit\) en de extra kosten die hierdoor in de markt ontstaan. Vanuit een totaal maatschappelijke kostenperspectief is het gewenst dat de groene, algemene interface dermate voldoet dat extra apparatuur onnodig is. Op basis van het laatste inzicht is geconcludeerd dat de RfG ook bij Type B eisen stelt aan de (extra) apparatuur. Hiermee zou "DSO Hardware" bij de elektriciteitproductie-eenheid moeten worden vermeden. Dit staat echter nog wel zo getekend in figuur 6 met verbindingen voor apparatuur van de DSO zelf tussen de rode-device-interface en de DSO’s systemen. **Er wordt dus vanuit gegaan dat ook de DSO's zoveel mogelijk gebruik maken van de algemene interfaces (groen in figuur 6) en de optie houden om voor net-kritische elektriciteitproductie-eenheden gebruik te maken van eigen (DSO/TSO) communicatienetwerken.** 

![](/assets/180123_EUDevicesSGAM_UCs_git_6.png)

Figuur 6

### Initiatief voor opbouwen dataverbindingen {#initiatief-voor-opbouwen-dataverbindingen}
Voor de interface-specificatie ontkomen we er niet aan om toch een stuk interactie met de centrale of decentrale elementen te benoemen. In het onderstaande figuur is een draft zichtbaar waarin het initiatief tot het opbouwen van verbindingen is weergegeven (links) i.v.m. dynamische IP adressen bij huis-internetaansluitingen. Vervolgens is weergegeven dat daarna de operationele verbinding vanuit het de interface van de elektriciteitproductie-eenheid wordt opgebouwd met het Operational-DER-Control wordt opgebouwd. Een verdere detaillering en uitwerking is hier noodzakelijk in de vervolghoofdstukken en later in de detailspecificatie. Het bovenstaande wordt als uitgangspunt gehanteerd voor verdere keuzes in standaarden.

![](/assets/180123_EUDevicesResponsibilitySGAM_UCs_8.png)

Figuur 7
