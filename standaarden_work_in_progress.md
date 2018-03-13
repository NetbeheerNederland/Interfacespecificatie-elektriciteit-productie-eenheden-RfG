# Inventarisatie van toepasbare standaarden {#standaarden-work-in-progress}


In de onderstaande tabel is een samenvatting te vinden voor de geschiktheid van standaarden voor het vraagstuk. De detailuitwerkingen zijn te vinden in [_Bijlage 2 – Evaluatie geschiktheid Standaarden._](https://netbeheernederland.gitbooks.io/interfacespecificatie-elektriciteit/content/bijlage_2__evaluatie_geschiktheid_standaarden.html)

De vorige hoofdstukken hebben in de architectuurbeschrijving al de onderwerpen informatie, communicatie en impact op fysieke componenten benoemd. De koppen in de tabel zijn overeenkomstig opgebouwd volgens de [SGAM lagen](http://ec.europa.eu/energy/sites/ener/files/documents/xpert_group1_reference_architecture.pdf): Informatie, Communicatie en Componenten. In de koppen zijn deze benoemd als Informatiedefinitie, Communicatie/Transport en Fysiek. Een standaard beschrijft soms maar één deel \(bijvoorbeeld IEC CIM beschrijft alleen de Informatie-definitie en vertelt niets over het gebruik van fysieke connectoren voor interfaces\). Tot slot wordt er geïnventariseerd of de standaard geschikt is als algemene interface, waarvan we zoveel mogelijk gebruik willen maken en als specifieke DSO of TSO-interface indien noodzakelijk; zie hiervoor ook de beschrijving in hoofdstuk 3.3).

Legenda van waarden: 

'-'   = negatief

'0'   = neutraal

'+'   = positief

'?'   = oordeel nog te geven

'nvt' = niet van toepassing bij deze standaard.

Uiteindelijk zal de definitieve evaluatie van deze standaarden resulteren in de keuze van het communicatie & transport protocol en de het gebruikte informatiemodel wat wordt toegepast.

| Standaard | Informatie def | Com & Transport  | Fysiek | Geschiktheid alg[^1] | Geschiktheid xSO [^2]|
| :---      | :---           | :---             | :---   | :---             | :---             |
| EF-Pi     |                |                  |        | -                | 0                |
| openADR   | -              |                  |        | -                | -                |
| MQTT      | nvt            | +                | nvt    | 0                | 0                |
| Webservices | nvt          | +                | nvt    | +                | 0                |
| XMPP      | nvt            | +                | nvt    | +                | + ?              |
| DLMS Cosem |       0       | +                | +      | 0                | -                |
| IEC 60870-x-104 |    -     | 0                |        | 0                | 0                |
| Modbus    |         -      | -                |        | -                | 0                |
| IEC 61850 algemeen [^3] |  |                  |        |                  |                  |
| IEC 61850-8-1 (MMS) | -    | 0                | nvt    |                  |                  |
| IEC 61850-8-2 (XMPP)| -    | +                | nvt    |                  |                  |
| IEC 61850-90-7 (object models DER)| + | nvt   | nvt    | +                | +                |
| IEC CIM   |       +        | -                | nvt    | +                | +                |


**Conclusie**

Gegeven het massale gebruik van het TCP/IP en de volwassenheid/bekendheid gaat de voorkeur uit naar webservices. Dit wordt ingevuld  XMPP in combinatie met IEC 61850 gebaseerde berichten. IEC 61850-90-10 scheduling logical nodes en 61850-90-7 DER logical nodes wordt hier ingezet. Dit zal verder worden uitgewerkt in de detail specificatie.

De keuze is gevallen op IEC61850 met de volgende redenen:
* Sluit aan bij de IEC TC57 doelarchitectuur
* IEC 61850-90-7 sluit goed aan bij gestelde requirements
* IEC 61850 beschrijft soms ook gedrag (zoals bij schedules)
* Bestaande Elektriciteitsproductie eenheden hebben soms al een IEC61850 interface (zoals windmolens)
* IEC61850 wordt ook gebruikt in Duitsland voor het aansturen van elektriciteits productie eenheden
* IEC61850 wordt prominent genoemd in EU mandaat [M490 (bijvoorbeeld figuur 30)](https://ec.europa.eu/energy/sites/ener/files/documents/xpert_group1_reference_architecture.pdf)

[^1]: Interface gespecificeerd in de scope van dit document die als eis geldt voor fabrikanten.


[^2]: Optionele interface niet gerealiseerd door markt maar door systembeheerder.


[^3]: De selectie van de beoordeelde delen van IEC61850 is op basis van grotere keuzes die voor dit vraagstuk, als eerste stap gemaakt moeten worden. Daarom wordt bijvoorbeeld MMS en XMPP  met elkaar vergeleken. IEC61850 beschrijft echter zoveel, dat de selectie van delen helaas nog een arbitrair proces is. Details zoals common data-classes is op dit moment voor de eenvoud nog weggelaten en zal onderdeel zijn van detailspecificaties. 
