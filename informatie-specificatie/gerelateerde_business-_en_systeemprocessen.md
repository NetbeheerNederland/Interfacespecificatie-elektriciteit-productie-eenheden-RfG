## Gerelateerde Business- en Systeemprocessen {#gerelateerde-business-en-systeemprocessen}

Om een goede interfacespecificatie te maken is het handig om een overzicht te maken van de verschillende actors en de verschillende processen. Op basis van deze processen/activiteiten en requirements kan worden achterhaald welke informatie moet worden uitgewisseld. Let er op dat de getekende processen verder gaan dan de interface met de elektriciteitsproductie-eenheid. Dit om er zeker van te zijn dat er een werkbaar proces kan ontstaan met de gespecifieerde interface. Dit betekent niet dat hiermee de (verdere)processen zijn gedefinieerd. Het dient ter validatie. De tekenwijze is gebaseerd op UML (niet helemaal volgens de UML specs).

### Actors
Tot nu toe is er in de afbeeldingen onderscheid gemaakt tussen DSO of relevante netbeheerder (rood) en alle overige partijen (groen). Het onderstaande figuur geeft een completer overzicht van de verschillende actoren en aan welke categorie ze kunnen worden gerelateerd (DSO rood, of overig groen).
![Figuur: Actoren](/assets/Actors.png)
https://netbeheernederland.gitbooks.io/interfacespecificatie-elektriciteit/content/assets/Actors.png

### Aanmeldproces
Onderstaand aanmeldproces is opgetekend om te definiëren welke communicatie moet worden opgebouwd vanuit de interface, hoe en wanneer beveiligd in het proces en met welke informatie. Dit is voldoende voor de interfacespecificatie waarbij het definitieve proces officieel nog moet worden vastgesteld. 
![Figuur: aanmeld procedure](/assets/Aanmeld-flow.png)
https://netbeheernederland.gitbooks.io/interfacespecificatie-elektriciteit/content/assets/Aanmeld-flow.png

Het bovenstaande proces geeft duidelijk weer welke eisen er minimaal moeten gelden aan de interfacespecficatie van de elektriciteitsproducie-eenheid. De interface moet:
1. zich zelfstandig verbinden en aanmelden bij een centraal aansluitregister
2. verbonden blijven tot en met de ontvangst van (nieuwe)verbindinggegevens van de relevante systeembeheerder, inclusief een token voor veilige verbindingsopbouw  en al deze informatie opslaan.
3. de verbinding met het centraal aansluitregister verbreken.
4. op basis van de nieuwe verbindinggegevens verbinden met de relevante systeembeheerder. Hierbij wordt een beveiligde verbinding gebruikt.
5. een operating license kunnen ontvangen van de relevante systeembeheerder en deze opslaan. 
6. na opslag van de operating license de verbinding verbreken ter afsluiting van de installatie en registratieve processen.
7. met een operating license zelfstandig verbinden met van de relevante systeembeheerder zoals beschreven bij paragraaf "Operationele aansturing".

Voor specifieke en detaileisen zie ook hoofdstukken "Message specification", "Conformiteitseisen" en "Registratieprocotol".

### Afmeldproces
Onderstaand afmeldproces is opgetekend om te definiëren welke communicatie moet plaatsvinden met de interface, hoe en wanneer beveiligd  in het proces en met welke informatie. Dit is voldoende voor de interfacespecificatie waarbij het definitieve proces officieel nog moet worden vastgesteld. 

![Figuur: afmeld procedure](/assets/Afmelden-elektriciteitsproductie-eenheid.png)
https://netbeheernederland.gitbooks.io/interfacespecificatie-elektriciteit/content/assets/Afmelden-elektriciteitsproductie-eenheid.png

Het bovenstaande proces geeft weer dat er voor het afmelden maar beperkte eisen gelden aan de interface, namelijk dat de interface herkent dat door het intrekken van het certificaat, en daardoor een certificaatfout, opnieuw de registratie doorlopen moet worden. Zie hiervoor ook [gedrag productie-eenheden](https://netbeheernederland.gitbooks.io/interfacespecificatie-elektriciteit/content/assets/Gedrag-productie-eenheden.png).


### Operationele aansturing
**Dit wordt momenteel verder uitgewerkt:** Het momentele standpunt is dat het mechanisme van IEC 61850-90-10 (scheduling) **uiteindelijk** kan worden toegepast naar de Duitse FNN Steuerbox specificatie. Echter is deze standaard vrij nieuw (relatief onbeproefd) en is scheduling een extra complicatie om in software om te zetten voor marktpartijen. Deze complicatie is ook aanwezig op testen hiervan voor  conformiteit. Er wordt een oplossing gevonden waarbij het scheduling wordt gereduceerd tot maximaal één week vooruit waarbij tijdens conformiteit op x aantal punten steekproefmatig het gedrag wordt getoetst. De informatie-uitwisseling op de interface zal het liefst IEC 61850-90-10 conform zijn, maar minimaal in opéénvolgende versies groeien naar het volledige IEC 61850-90-10 mechanisme. 

Naast de monitoring van de elektriciteitsproductie eenheid is het ook wenselijk om te sturen, parameters te versturen en ad-hoc vragen de stellen aan de elektriciteitsproductie-eenheid. Dit zal een request-response mechanisme zijn.

![Figuur: Aansturen elektrictiteitsproductie eenheid](/assets/sequence-Aansturen-elektriciteitsproductie-eenheid.png)

Klasse 1 (voorzien in Type A)
* Productie vermogen reductie naar 0 aanzetten
* Productie vermogen reductie opheffen
* Bijwerken schema's voor autonome gedrag
* Opvragen interface versie (dit document)
* Opvragen interface (software) versie elektriciteitsproductie eenheid


Klasse 2 (voorzien in Type B), aanvullend aan klasse 1:
* Opvragen regelbaar werkelijk/blind vermogen
* Regelstappen elektriciteitsproductie eenheden
* Werkzame vermogen te verminderen/uitzetten
* Werkzame vermogen te vermeerderen/aanzetten
* Melden van terugregeling productie eenheid aan systeembeheerder

De schema's zijn vrij de defineren door de systeembeheerder. De prioriteiten zouden er zo uit kunnen zien (voorbeeld):

|Prio |Gebruik | Commentaar |
|:--|:--|:--|
|250| Emergency| Voor noodgevallen |
|210| Opstart schema | Wordt getriggerd bij het opstarten.|
|200| Schema per dag| Wordt actief bijgewerkt door systeembeheerder|
|100| Baseline op basis van lokale netconfiguratie | vast patroon om congestie te voorkomen|
|50| Markt | kan gebruikt worden voor handel op de markt|
|0| Geen reductie| Elektriciteitsproductie eenheid mag 100% leveren|



### Rapportage/monitoring
Hoog over zal de rapportage functie een publisch-subscribe mechanisme zijn waarbij de elektriciteitsproductie-eenheid zelfstandig zijn eigen status rapporteerd. De exacte informatie die uitgewisseld moet worden is per type verschillend en zal later uitgewerkt moeten worden.

![Figuur: Monitoren elektrictiteitsproductie eenheid](/assets/sequence-Monitoren-elektriciteitsproductie-eenheid.png)
Near-Real-time informatie kan gebruikt worden voor storingen en prognoses.

Klasse 1 (voorzien in Type A):
* Tijdsynchronisatie fout melding/status
* Keepalive om de verbinding open te houden<sup>1</sup>
* Werkelijk momententaan vermogen (MW) wat terug geleverd wordt door de elektriciteitsproductie eenheid

Update frequentie monitoring signalen (configureerdbaar door systeembeheerder): 15 minuten

Klasse 2 (voorzien in Type B), aanvullend aan klasse 1:
* Minimal Power (P) during measurement interval 15 minuten
* Maximal Power (P) during measurement interval 15 minuten
* Average Power (P) in each 24 hours
* Momentane frequentie
* Momentane spanning
* Minimale/maximale spanning/frequentie van een piek/dal met tijdstip. 8 waarden totdat deze worden uitgelezen.
* Status elektriciteitsproductie eenheid (is hij instaat om te acteren op bestuur commando's van de systeembeheerder)
* Werkelijk blindvermogen (MVar) wat terug geleverd wordt door de elektriciteitsproductie eenheid

Update frequentie monitoring signalen (configureerdbaar door systeembeheerder): 30 seconden

<sup>1</sup>
Een productieeenheid is in basis verantwoordelijk voor de verbinding met de relevante systeembeheerder.
Om deze verbinding actief te maken en te houden en om ervoor te zorgen dat het dataverbruik beperkt blijft zijn er een aantal aandachtspunten:
* Ondersteuning voor TLS session resumption.
        Resumption is niet noodzakelijk na een stroomuitval, maar gedurende de dag wel.
* Keepalive tijd van een verbinding wordt door de productieeenheid bepaald.
        Hierbij moet het apparaat zelf bepalen wat de optimale keepalive tijd is.
        Keepalives zijn in basis de standaard keepalives in tcp of tls.
