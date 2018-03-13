## Architecturele impact op net- en marktcomponenten \(fysiek en logisch\) {#architecturele-impact-op-net-en-marktcomponenten-fysiek-en-logisch}

In de vorige hoofdstukken en paragrafen heeft de architectuurverkenning plaatsgevonden. Dit hoofdstuk beschrijft de architecturele impact op de net- en marktcomponenten. Het doel is om een impact zo klein mogelijk te houden voor wijzigingen op de componenten. Het is vooral van belang om vooral fysieke wijzigingen aan net- en marktcompontenten zo klein mogelijk te houden en R&D kosten en implementatietijd zoveel mogelijk te vermeiden. Daarom wordt er gekozen voor het alternatief: eisen te stellen aan software. Ook hier zullen R&D kosten en implementatietijd van toepassing zijn, echter veelal zonder fysieke productiegevolgen specifiek voor de Nederlandse markt.

Een korte verkenning leert, dat ook (enkele) toonaangevende zonne-converters zijn voorzien van een Linux (embedded) waardoor het aannemelijk is dat zeer compacte software-stacks hierin gehosted kunnen worden, uiteraard na intensief testen door de leveranciers. Het kan ook voorkomen dat er geen plaats is in de zonne-converters, of elektriciteitproductie-eenheden in het algemeen. Ook kan het voorkomen dat er meerdere elektriciteitproductie-eenheden tegelijkertijd worden aangestuurd met een centrale stuurinrichting van de installatie. Voor deze situaties moet de oplossing ook passend zijn. Daarom is het voor producenten van elektriciteitsproductie-eenheden en -installaties toegestaan om in plaats van een product-geïntegreerde-interface \(zie \[1\] in Figuur 8\) ook gebruikt te maken van een extra, lokaal geplaatste, gateway \(zie \[2\] in Figuur 8\). Met lokaal wordt in deze context bedoeld: achter de meter.

Hierdoor wordt er niet afgedwongen om aanpassing te maken op de hardware of software van het apparaat zelf. Tevens kan de gateway universeel worden ingezet voor verschillende brandstofsoorten \(PV, wind en nog meer zoals \[2\] en \[3\] in Figuur 8\) en beheerbaarheid software. Het zal een groot voordeel zijn als de interface als open-soure referentie-stack beschikbaar wordt gesteld in de markt, waarmee elke leverancier onder eigen verantwoordelijkheid de functionaliteit kan inbouwen.

Er zullen extra eisen gelden voor het certificeren van de hardware combinaties met apart geplaatste gateways.

![](/assets/180123_EUDevicesSGAM_UCs_git_12.png)

Figuur 7

