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
1) zich zelfstandig verbinden en aanmelden bij een centraal aansluitregister
2) verbonden blijven tot en met de ontvangst van (nieuwe)verbindinggegevens van de relevante systeembeheerder, inclusief een token voor veilige verbindingsopbouw  en al deze informatie opslaan.
3) de verbinding met het centraal aansluitregister verbreken.
4) op basis van de nieuwe verbindinggegevens verbinden met de relevante systeembeheerder. Hierbij wordt een beveiligde verbinding gebruikt.
5) een operating license kunnen ontvangen van de relevante systeembeheerder en deze opslaan. 
6) na opslag van de operating license de verbinding verbreken ter afsluiting van de installatie en registratieve processen.
7) met een operating license zelfstandig verbinden met van de relevante systeembeheerder zoals beschreven bij paragraaf "Operationele aansturing".

Voor specifieke en detaileisen zie ook hoofdstukken "Message specification", "Conformiteitseisen" en "Registratieprocotol".

### Afmeldproces
Onderstaand afmeldproces is opgetekend om te definiëren welke communicatie moet plaatsvinden met de interface, hoe beveiligd wanneer in het proces en met welke informatie. Dit is voldoende voor de interfacespecificatie waarbij het definitieve proces officieel nog moet worden vastgesteld. 

![Figuur: afmeld procedure](/assets/Afmelden-elektriciteitsproductie-eenheid.png)
https://netbeheernederland.gitbooks.io/interfacespecificatie-elektriciteit/content/assets/Afmelden-elektriciteitsproductie-eenheid.png

### Operationele aansturing
Type A
* Productie vermogen reductie naar 0
* Productie vermogen reductie opheffen
Type B
* Werkzame vermogen te verminderen/uitzetten
* Werkzame vermogen te vermeederen/aanzetten

### Rapportage
Informatie uitwisselen
* Near-Real-time i.g.v. storing
* Rapportage t.b.v. prognoses.

