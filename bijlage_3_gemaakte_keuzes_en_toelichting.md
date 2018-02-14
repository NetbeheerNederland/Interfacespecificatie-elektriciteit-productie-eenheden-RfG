# Bijlage 3 – Gemaakte keuzes en toelichting

De keuzes die in deze interface specificatie zijn gemaakt zijn opgedeeld in 

## Componenten

## Communcatie

Keuze: Publieke netwerken (internet) en private netwerken. Technologie: Ethernet met TCP/IP.

Motivatie: Om de maatschappelijke kosten zo laag mogelijk te maken is de keuze gevallen op bestaande telecom infrastructuren en technolgie. Internet is op veel plekken beschikbaar en TCP/IP is hiervoor een gangbaar protocol. 

(in te vullen) onderscheid in typen A,B etc?

### Syntactisch

(in te vullen) XMPP,DDS, SOAP, etc

## Informatie

(in te vullen) IEC CIM of (delen van) IEC 61850

(in te vullen) gebruikte profiel

## Functies
Keuze: RfG Type B biedt de mogelijkheid tot ontvangen signaal voor terugregeling maximaal vermogen naar momentaan gespecificeerde limiet (in kW).

Motivatie: RfG artikel 14.2. Het sturen op kW-setpoint past bij toekomstige regelvraagstukken. Het resultaat van sturen op %-setpoint is afhankelijk van het maximale vermogen converter, het momentane maximaal vermogen (b.v. zonnestand), en de installatiekarakteristieken (b.v. grote converter met maar één paneel).

Keuze: RfG Type A biedt de mogelijkheid tot het ontvangen van een signaal voor terugregeling van maximaal vermogen naar geen vermogen. De implementatie zoals beschreven bij Type B is niet verplicht voor Type A.

Motivatie: RfG artikel 13.6. 

Keuze: RfG Type A en B sturen, indien verbonden, meetwaarden en status over het functioneren die in lijn zijn met RfG en GL SO om hiermee "Real-time" beschikbare gegevens voor geaggregeerde productie per primaire energiebron in het DSB-gebied te kunnen aanbieden.

Motivatie: GL-SO artikel 44.

## Business
Keuze: De keuze om geen keuze te maken over de invulling van rollen voor het verwerken, aggregeren van data en het primair of als noodbevel uitvoeren van opdrachten.

Motivatie: Buiten scope van vraagstuk. De oplossing van de interface onafhankelijk en flexibel specificeren; flexibel maken voor wijzigingen in de energiemarkt. 
