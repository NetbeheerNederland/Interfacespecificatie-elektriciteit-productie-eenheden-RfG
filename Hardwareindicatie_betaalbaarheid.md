## Indicatieve eisen hardware t.b.v. kosten Rfg implementatie voor leveranciers.
Om de maatschappelijk kosten voor de interface implementatie betaalbaar te houden is er gerekend aan de hardware specicaties.
Deze zijn gemaakt om te controleren of de eisen voor een fabrikant redelijk blijven.

**Bij intergratie in bestaande inverter:**
- Genoeg processorkracht en/of een cryptografisch versnelde processor om TLS 1.2 met bijv ECDSA en AES.
- Genoeg opslag om logging/schedules/libaries op te slaan.
Hieronder staat de berekening, deze komt uit op ongeveer 140kilobyte.
Hier komt nog bij de opslag voor een tls stack en 61850/xmpp stack, maar dit is implementatieafhankelijk en ligt bij de fabrikant.
- Bij grotere systemen een fysieke ethernetpoort.
- 'Een' interface naar een gebruiker, bij een lcd/webpagina melding of ledje of het device verbonden is.
- Unieke QR code op het device of link in een webinterface.
- Meting van spanning/frequentie/opbrengst (zie conformiteitseisen}).
- Opbrengst moet afgeregeld kunnen worden tot 0.
- Niet eenvoudig manipuleerbaar (zie conformiteitseisen).
- Unieke identifier per apparaat.

**Voor opslag:**
Schedule:
Verwacht wordt aan schedules:
- Een weekschedule op uren specifiek.
- Een dagschedule op 5minuten specifiek.
- Een rampup schedule van een uur per minuut specifiek.
- Een marktschedule van een dag op kwartier specifiek.
Dit geeft ongeveer 600 scheduling momenten waarbij een scheduling moment geschat 64 bytes opslag kost.
Dat komt neer op ongeveer 40kbyte aan data, hier wordt ruim boven genomen voor toekomstvastheid.

Hiervoor wordt 100kbyte gereserveerd.

**Voor logging:**
Hierbij worden minimaal kwartierwaarden en events verwacht.
Bij 3-fase, vermogensmeting, tijd, etc betekend dit tot 16 meetwaardes per logvermelding.
Met een ruwe schatting van 10 events per uur (spanningpiek etc) en kwarierwaardes en een opslag vor 12 uur komt dat uit op:
12*(10+4)*16=~2700 meetpunten in logs.
Met 4 bytes voor een meetpunt is dit ruim 10 kilobyte opslag.

Hiervoor wordt 25kbyte gereserveerd.

Certificaten en instellingen:

Certificaten kunnen bestaan uit kettingen van certificaten.

Verwacht wordt dat er ongeveer 6 certificaten opgeslagen zullen moeten worden, en daarnaast een prive paar voor het apparaat.
Een certificaat neem ongeveer een 1,5kilobyte in en een prive paar 4,5kilobyte.

Instellingen zijn beperkt tot ip/poort/dns/etc en zal slecht een paar honderd bytes zijn.

Hiervoor wordt 14kilobyte gereserveerd.
