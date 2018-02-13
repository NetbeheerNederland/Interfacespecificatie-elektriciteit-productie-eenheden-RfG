# Standaarden \(Work in Progress\) {#standaarden-work-in-progress}

In de onderstaande tabel is een voorlopige samenvatting te vinden voor de geschiktheid van standaarden voor het vraagstuk. De detailuitwerkingen zijn te vinden in _Bijlage 2 – Evaluatie geschiktheid Standaarden._

De koppen in de tabel zijn opgebouwd volgens de SGAM lagen: Informatie, Communicatie en Componenten. In de koppen zijn deze benoemd als Informatiedefinitie, Communicatie/Transport en Fysiek. Daarnaast wordt er een algemene evaluatie gedaan of de standaard geschikt is voor de algemene interface of de DSO/TSO interface. Een standaard beschrijft soms maar één deel \(bijvoorbeeld IEC CIM beschrijft alleen de Informatie-definitie en vertelt niets over het gebruik van fysieke connectoren voor interfaces\).

Waarden: 

'-'   = negatief

'0'   = neutraal

'+'   = positief

'?'   = oordeel nog te geven

'nvt' = niet van toepassing bij deze standaard.

Uiteindelijk zal de definitieve evaluatie van deze standaarden resulteren in de keuze van het communicatie & transport protocol en de het gebruikte informatiemodel wat wordt toegepast.

| Standaard | Informatie def | Com & Transport  | Fysiek | Geschiktheid alg | Geschiktheid xSO |
| :---      | :---           | :---             | :---   | :---             | :---             |
| EF-Pi     |                |                  |        | -                | 0                |
| openADR   | -              |                  |        | -                | -                |
| MQTT      | nvt            | +                | nvt    | 0                | 0                |
| Webservices | nvt          | +                | nvt    | +                | 0                |
| XMPP      | nvt            | +                | nvt    | + ?              | + ?              |
| DLMS Cosem |               |                  |        |                  |                  |
| IEC 60870-x-104 |          |                  |        |                  |                  |
| Modbus    |                |                  |        |                  |                  |
| IEC 61850-6 (SCL) | +           |         -        |   nvt    |                  |                  |
| IEC 61850-8-1 (MMS) | -          |                  |   nvt    |                  |                  |
| IEC 61850-8-2 (XMMP)| -           |                  |    nvt    |                  |                  |
| IEC 61850-7-420 (DER) | +         |                  |   nvt     |                  |                  |
| IEC 61850-90-10 (scheduling)| +          |                  |    nvt   |                  |                  |
| IEC CIM   |       +        |         -        |    -   | +                | +                |
