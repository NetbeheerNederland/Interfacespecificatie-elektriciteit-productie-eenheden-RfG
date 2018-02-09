## Businesskader {#businesskader}

Het businesskader wordt beschreven a.d.v. een SGAM plane waarbij de verantwoordelijkheden van de DSO en de overige partijen is gevisualiseerd \(zie Figuur 5\). In het rood zijn de verantwoordelijkheden aangegeven van de DSO en in het groen van de “Overige partijen”. Op dit moment is het nog irrelevant om te definiëren wie deze “Overige partijen” precies zijn; bijvoorbeeld leveranciers van hardware, aggregator, etc. De TSO is hier vanwege de tekenwijze en overzichtelijkheid weggelaten, maar de uitkomsten zullen voor TSO en DSO hetzelfde zijn m.b.t. de interfacespecificatie.

De informatie-en-opdrachten-infrastructuur \(witte vlek in Figuur 5\) waarmee de interfaces straks gaan verbinden is op dit moment voor een groot gedeelte irrelevant. Vragen of deze systemen centraal of decentraal zijn, of deze de TSO/DSO of een marktpartij toebehoren is voor de interface \(nog\) irrelevant. Wel zullen een aantal eigenschappen van deze toekomstige centrale of decentrale informatie-en-opdrachten-infrastructuur nu al duidelijk moeten worden om te kunnen interacteren met de interfaces. Er moet bijvoorbeeld duidelijkheid zijn over bepalingen zoals encryptie, tijdsynchronisatie, etc.

![](/assets/180123_EUDevicesSGAM_UCs_git_2.png)

Figuur 5

De uitdaging bij RfG Type A zit voornamelijk in de aantallen devices, de uitdaging bij Type B zit voornamelijk in de mogelijke impact in de stabiliteit het Elektriciteitsnet \(zie Figuur 1\). RfG Type C en Type D zijn van aantallen beperkt waarvoor maatwerk-aansluitingen zullen worden uitgevoerd. Hoewel de technologie van A en B kan hiervoor worden gebruikt, is het expliciet specificeren van Type C en D buiten scope. Daarnaast zal er ook voor DCC een interface beschikbaar moeten komen. Eenduidigheid tussen de RfG en de DCC interface wordt wel nagestreefd maar is niet de primaire doelstelling van de RfG interfacespecificatie.

Praktisch geldt dat met de huidige vermogensgrenzen, Type B al vaak vanuit een DSO onderstation of middenspannigsruimte elektrisch is aangesloten en dus schakelbaar is \(al dan niet op afstand\). Ze zijn niet regelbaar zoal wèl binnen de RfG voor type B is vereist. Binnen Type A bestaan er varianten waarbij de elektrische aansluiting op een middenspanningsruimte plaatsvindt \(ongeveer &gt;300 of &gt;400kVA\) en dus schakelbaar. Daarnaast zijn er varianten met een lager vermogen die niet schakelbaar zijn door lagere positionering in het elektriciteitsnet.

Tot slot geldt bij het businesskader dat er de mogelijkheid bestaat dat de vermogensgrens tussen Type A en Type B in de toekomst zal wijzigen \(verlagen\). Het is van belang dat het ontwerp hiermee rekening houdt. Concreet: een Type A zal \(met name voor leveranciers van hardware\) gemakkelijk geüpgraded moeten kunnen worden tot een Type B.

