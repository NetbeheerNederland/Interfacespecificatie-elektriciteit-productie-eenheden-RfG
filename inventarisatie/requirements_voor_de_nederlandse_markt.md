## Requirements voor de Nederlandse markt {#requirements-voor-de-nederlandse-markt}

Momenteel zijn er circa 20 requirements beschreven die het doel hebben om de belangrijkste zaken te noemen. Het doel is niet uitputtend te zijn, maar vooral de focus op de belangrijkste zaken te stellen. We stellen daarom een limiet van maximaal 40 requirements. De onderstaande lijst met requirements is een totaaloverzicht van requirements:

* die direct voortkomen uit RfG, DCC en GL SO,
* die voortkomen uit inventarisaties van de oplossingen in het buitenland
* die aansluiten op TSO/DSO generieke requirements m.b.t. beheerbaarheid, veiligheid en beschikbaarheid van IT en OT oplossingen.

De requirements zijn functioneel en kwalitatief van aard en niet uitputtend. De deliverables van deze specificatie zullen hieraan moeten voldoen en geven invulling aan de interfaces.

#### Requirements {#requirements}

| ID | Requirement | Type | Type | [Prioriteit \(MoSCoW\)](https://duckduckgo.com/l/?kh=-1&uddg=https%3A%2F%2Fnl.wikipedia.org%2Fwiki%2FMoSCoW-methode) | [Prioriteit \(MoSCoW\)](https://duckduckgo.com/l/?kh=-1&uddg=https%3A%2F%2Fnl.wikipedia.org%2Fwiki%2FMoSCoW-methode) | [Prioriteit \(MoSCoW\)](https://duckduckgo.com/l/?kh=-1&uddg=https%3A%2F%2Fnl.wikipedia.org%2Fwiki%2FMoSCoW-methode) | Bron |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
|  | Rationale | F | NF | RfG | DCC | GL SO |  |
| 1 | Het afluisteren van één datastroom mag nooit leiden tot het verkrijgen van interpreteerbare data. |  | NF | Must | Must | Must | Alliander IT / Enexis. |
|  | Bescherming van privacy op aansluitgegevens, meet- en instelwaardes. Dit is een extra beveiliging aangezien er niet geleund wordt op één beveiligingsmaatregel zoals encryptie. |  |  |  |  |  |  |
| 2 | “De administratieve lasten en kosten waarmee het verstrekken van vraagsturing gepaard gaat, moeten binnen redelijke grenzen blijven” |  | NF | Must | Must | Must | Verordening DCC, Beleid Alliander Enexis en vanuit Regulering |
|  | Eis in DCC verordeningen. En in lijn met de doelstellingen netbeheerders betreffende maatschappelijke kosten te beperken. |  |  |  |  |  |  |
| 3 | De beschikbaarheid van minimaal één logische interface ten tijde van het terugleveren \(RfG\) of opnemen \(DCC\) van energie en waarmee het vermogen gestuurd kan worden is minimaal 99,90% per jaar voor elke stuurbare-installatie. Dit is alleen van toepassing op stuurbare installaties met een potentieel significante impact op de energiehuishouding van het elektriciteitsnetwerk \(RfG Type B-D en DCC\) gedurende dat deze parallel aan het net gekoppeld zijn. Deze requirement is bindend, echter afhankelijk van een kosten/risico optimalisatie. |  | NF | Must | Must |  | Alliander IT / Enexis. |
|  | Beschikbaarheid hoog genoeg voor dynamische regelsystemen met beïnvloeding op het net \(8,8 uur onvoorziene onbeschikbaarheid\). Beschikbaarheid lager dan klassieke stationsautomatisering vanwege verspreid risico over verschillende installaties. Updates en onderhoud kan worden toegepast wanneer geen opwek \(RfG\) of belasting \(DCC\) verwacht is, bijvoorbeeld nacht of wind-stilte. |  |  |  |  |  |  |
| 4 | Het werkbare \(uitgangs\)vermogen kan binnen vijf seconden naar nul kan worden gereduceerd nadat een instructie daartoe is ontvangen door de ingangspoort | F | NF | Must | Must |  | RfG 13.6 |
|  | Eis Verordening RfG. Daarnaast is het onlogisch andere eisten te stellen aan verbruiksinstallaties |  |  |  |  |  |  |
| 5 | Geïmplementeerde interfacetechnologie moet eenduidig zijn voor alle verschillende devices. |  | NF | Could | Could | Could | Verzoek Netbeheer Nederland werkgroep IEC. |
|  | Standaardisatie waardoor lagere OPEX. Minder implementatievarianten waardoor lagere CAPEX voor zowel Netbeheerder als Marktpartijen. Als grens binnen RfG Type A en B verandert blijft de technologische basis hetzelfde. |  |  |  |  |  |  |
| 6 | Het wijzigen \(verlagen\) van de grens tussen Type A en Type B in de RfG mag niet leiden tot hardware aanpassingen voor marktpartijen. |  | NF | Should |  |  | Verzoek Netbeheer Nederland werkgroep IEC. |
|  | Laagste maatschappelijke kosten op \(middel\)langere termijn |  |  |  |  |  |  |
| 7 | Zoveel mogelijk gebruik van internationale en open Energie- en IT-marktstandaarden. |  | NF | Should | Should | Should | Alliander IT / Enexis. |
|  | Faciliteert markt voor omzetten benodigdheden, lagere kosten door breder beschikbare marktkennis. |  |  |  |  |  |  |
| 8 | Met gebruik van beschikbare technologie en marktstandaarden is aangetoond dat het gespecificeerde en de gestelde requirements voldoet als informatie- en opdrachen-uitwisseling systeem op een schaal met minimaal 200.000 decentrale devices. |  | NF | Should | Should |  | Alliander IT / Enexis. |
|  | Aangetoonde werking van gespecificeerde interface bij grotere getallen. |  |  |  |  |  |  |
| 9 | Het is aantoonbaar dat de data-uitwisseling \("data transfer protocollen"\) en het gebruik van de informatie die daarmee beschikbaar komt, optimaal beheerbaar is voor zowel de systeem instandhouding als ook direct bruikbaar is in andere informatiebehoevende systemen. |  | NF | Should | Shoud | Should | Alliander IT / Enexis. |
|  | Vanwege de grote aantallen devices en de daarmee verbonden data, streven we vanuit operationele kosten ernaar om dataconversies en mapping van datapunten zoveel mogelijk te vermijden. Aan de andere kant moeten de datastromen en de ontstane informatie goed beheerbaar blijven en daardoor begrijpelijk zijn opgebouwd. |  |  |  |  |  |  |
| 10 | Bi-directionele communicatie | F | NF | Should | n.t.b. | Must | RfG A-D: Controll-system \(Should\).RfG vanaf Type B: Waarden: \(Could\), Type C \(Must\). GL SO \(Must\). |
|  | Naast het versturen van opdrachten het ook kunnen ontvangen van bevestigingen \(Acknowlegements\) typische eigenschap regelsystemen. Daarnaast ontvangen van waarden en statussignalen vanuit GL SO vereisten t.b.v. real-time beste inschatting productie en verbruik. |  |  |  |  |  |  |
| 11 | Backwards compatibility van protocollen en informatie-configuraties. |  | NF | Should | Should | Should | Alliander IT / Enexis. |
|  | Toekomstige wijzigingen in het protocol in devices en IT systemen kunnen implementeren. Zelfs goed gedefinieerde protocollen en informatieberichten zijn in de praktijk achteraf ge-upgrade. |  |  |  |  |  |  |
| 12 | Koste efficiëntie vanuit totaal maatschappelijke kosten. |  | NF | Must | Must | Must | Alliander IT / Enexis. |
|  | Eis vanuit verordening en in lijn met doelstellingen Netbeheerders. Sterke overweging in de extra operationele kosten die ontstaan door het wél of niet invullen van requirements. |  |  |  |  |  |  |
| 13 | End-to-End encryption |  | NF | Must | Must | Must | Alliander IT / Enexis. |
|  | Voorkomen man-in-the-middle attacks, voorkom data-manipulatie, extra laag Back-up beveiliging tegen privacy incidenten, gebruik van huidige stand van beveiligingstechniek. |  |  |  |  |  |  |
| 14 | Compatibility met buurlanden |  | NF | Could | Could | Could | Alliander IT / Enexis. |
|  | Zoveel mogelijk gebruik van dezelfde technologische oplossing. Minder risico dat een volgende EU standaardisatie leidt tot refurbishment van al geïnstalleerde devices. |  |  |  |  |  |  |
| 15 | De interfaces moeten faciliteren dat security-gerelateerde aanvallen \(zoals Ddos aanvallen\) i.c.m. andere systemen volgens de huidige stand van de techniek kunnen worden gemitigeerd. |  | NF | Must | Must | Must | Alliander IT / Enexis. |
|  | Zekerstellen van continuïteit en beschikbaarheid gehele systeem. |  |  |  |  |  |  |
| 16 | De interface specificatie moet geschikt zijn voor opschaling tot enkele miljoenen devices op zowel communicatie-niveau als op informatie-model niveau |  | NF | Should | Should | Should | Alliander IT / Enexis. |
|  | Toekomstvast ontwerp, voorkomen van toekomstige migratiekosten. |  |  |  |  |  |  |
| 17 | Data dat op de interface ontvangen wordt en relevant is voor direct stuurgedrag of tot 7 dagen vooruit, wordt gepersisteerd op het device. \[Nog verder uitzoeken schedules in device\]. | F |  | Could | ? | ? | Alliander IT |
|  | Grotere onafhankelijkheid communicatie en naar voorbeeld Duitse invulling. Langere opslag dan 7 dagen wordt als onwaarschijnlijk geacht aangezien dan een E-systeem aanpassing meer op zijn plaats zou zijn. |  |  |  |  |  |  |
| 18 | De interfaces van het RfG/DCC device moeten in staat zijn om naast de productieve host, ook een andere host te kunnen verbinden. Indien de eerste verbinding beschikbaar is, wordt er geen data uitgewisseld over de tweede verbinding. | F |  | Should |  |  | Alliander IT / Enexis. |
|  | Indien "centrale" IT infrastructuur wijzigt blijft het systeem beschikbaar door een back-up lijn. Toekomstig landschap is flexibel en maakt migratie mogelijk naar meer decentrale IT systemen. Redundancy in communicatiepaden. |  |  |  |  |  |  |
| 19 | Betrouwbare tijdsynchronisatie | F | NF | Must |  |  | Afgeleid van DCC en GL SO |
|  | Bijdrage aan de eisen time-stamping en altijd een actueel beeld van de net-situatie hebben in geval van storingen. |  |  |  |  |  |  |
| 20 | De interface moet in staat zijn om berichten van Netbeheerders met een hogere prioriteit te behandelen dan die van marktpartijen. | F |  | Must | Must | - | VDE FNN |
|  | Naar voorbeeld Duitsland om schakelopdrachten te kunnen prioriseren. |  |  |  |  |  |  |
| 21 | Alle interface moeten voorspelbaar reageren op onverwacht, niet gepland, gedrag van zijn omgeving (Dynamic Behavior). | NF |  | Should | Should | - | Alliander IT |
|  | Naar 2nd DC IEC TR 61850-7-6 - Interchangeability; Niet alleen competabiliteit bereiken op gepland gedrag, maar ook uitzonderlijke situaties, zoals haperende communicatieverbindingen. Hiermee kan de uitwisselbaarheid van de apparaten beter worden gegarandeerd zonder fine-tuning van configuraties. |  |  |  |  |  |  |


