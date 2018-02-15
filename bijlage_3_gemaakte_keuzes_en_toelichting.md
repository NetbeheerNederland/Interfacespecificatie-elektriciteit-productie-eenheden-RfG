# Bijlage 3 – Gemaakte keuzes en toelichting

De keuzes die in deze interface specificatie zijn opgedeeld in de verschillende lagen van SGAM.

## Componenten

## Communcatie

Keuze: Publieke netwerken (internet) en private netwerken. Technologie: Ethernet met TCP/IP.

Motivatie: Om de maatschappelijke kosten zo laag mogelijk te maken is de keuze gevallen op bestaande telecom infrastructuren en technolgie. Internet is op veel plekken beschikbaar en TCP/IP is hiervoor een gangbaar protocol. 



Keuze: Encryptie via TLS

Motivatie: TLS is in staat om de encryptie in de toekomst te wijzigen en zo mee te gaan met gangbare encryptie niveau. Daarnaast is TLS bewezen technologie. TLS bevat tevens een tijdssynchronisatie mogelijkheid.


Keuze: End-to-end encryptie tot device of dongle, De dongle-productie interface is een punt-punt verbinding die niet gedeeld is op alle communicatie lagen. Dit betekend een directe fysieke connectie zonder routing functies etc. Voorbeeld is een seriele poort (RS232).

Motivatie: Om bestaande invertors geschikte te maken om aan deze interface specificatie te voldoen is het toegestaan een punt-punt verbidingen te hebben met de invertor en de interface dongle. Het toevoegen van encryptie aan een bestaand product kan kostbaar zijn.

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

Keuze: Een productie eenheid kan zicht in 3 toestanden bevinden.
![Figuur: gedrag productie-eenheden](/assets/Gedrag-productie-eenheden.png)

* Ongepland autonoom gedrag: De productie-eenheid waarvan de interface niet is aangesloten. De productie eenheid voldoet aan de overige netcodes en gedrag.
* Gecontroleerd gedrag: De productie-eenheid is geregisteerd en heeft een werkende connectie met de lokale netbeheerder.
* Gepland autonoom gedrag: De productie-eenheid handeld op basis van vooraf opgestuurde schema's/planning.

Motivatie: Conform 3.2; Het toevoegen van schedules in de eenheden naar Duits voorbeeld kunnen het autonome gedrag en daardoor robuustheid van het elektriciteitsnet versterken.

## Business
Keuze: De keuze om geen keuze te maken over de invulling van rollen voor het verwerken, aggregeren van data en het primair of als noodbevel uitvoeren van opdrachten.

Motivatie: Buiten scope van vraagstuk. De oplossing van de interface onafhankelijk en flexibel specificeren; flexibel maken voor wijzigingen in de energiemarkt. 

Keuze: Er wordt 1 centraal register aangewezen waar het registratie van de productie-eenheden plaats vind.

Motivatie: Om complexiteit te voorkomen bij het registratie proces is het handig als de registratie via een centraal register verloopt. Productie-eenheden leveranciers hebben dan een eenduidige ingang waar het registratie proces kan plaats kan vinden. Via dit centrale register kan worden doorvewezen naar 3de partijen.


Keuze: Productie-eenheden zijn direct verbonden met de lokale netbeheerder

Motivatie: Om de afhankelijkheid van 3de partijen te verminderen en de de verantwoordelijkheid van de netbeheerder maximaal te kunnen nemen is gekozen om de apparaten direct te laten communiceren met de lokale netbeheerder.
