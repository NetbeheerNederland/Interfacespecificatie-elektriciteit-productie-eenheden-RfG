## Conformiteitseisen
  * Het systeem moet niet eenvoudig oncontroleerbaar te manipuleren zijn
    *	Het eruit trekken van een stekker mag geen invloed kunnen veroorzaken.
    * Het verkeerd verbinden van stekkers mag geen invloed veroorzaken.
    * Een kortsluiting in een kabel of stekker mag geen invloed veroorzaken.
    * Contacten die invloed hebben moeten minstens achter een zegel zitten.
    * Etc.
*	Toegang tot relevante instellingen moet afdoende beveiligd zijn.
  * Interfaces met relevante instellingen moeten afgeschermd zijn van een gebruiker met minstens een unieke inlog of afdoende wijze verzegeld.

  * Onder relevante instellingen vallen onder andere:
    *	Certificaten voor de verbinding(en) met centrale systemen.
    * Calibatieinstellingen
    * Identificatieinstellingen zoals serienummer.
    * Etc.
  * Onder relevante instellingen valt niet:
    * Instellingen voor een netwerkverbinding (WIFI netwerk/wachtwoord)
    * Reset naar fabrieksinstellingen
    * Etc.

* Het systeem moet een unieke identificatie hebben
  *	Denk hierbij aan de naam van de fabrikant/product in combinatie met een serienummer.

*	De interne tijd mag niet meer dan 5 seconden afwijken van de platformtijd.
  *	Tijdsynchronisatie gebeurt bijvoorbeeld via de TLS verbinding met het platform.
  *	Afwijking van de interne klok is maximaal 2 seconden per dag.
  *	Synchronisatie met de platformtijd behoort niet vaker dan 1x per dag noodzakelijk te zijn.
  *	GPS is ook acceptabel.
  *	Bij NTP of anders is de bron hiervan onderdeel van de conformiteitstest.

*	Meetnauwkeurigheid.
  *	Tijdens de conformiteitstest wordt beoordeeld of de installatie in staat is zich aan de meeteisen te voldoen.
  *	1% afwijking op de spanningsmeting.
  *	Maximaal 0.01Hz afwijking op frequentiemeting.
  *	Maximaal 0.1 graad afwijking op fasehoekmeting (bij 3-fase systemen).

*	Security libraries en software updates.
  *	Apparaten mogen alleen generieke libraries gebruiken voor bijv TLS verbindingen en certificaten.
  *	Leveranciers wordt verwacht gedurende minimaal de economische levensduur updates hiervoor te leveren indien die noodzakelijk zijn voor het behouden van een veilige verbinding.

*	Er moet voldaan worden aan de interface-specificatie.
  * Terugschalen of uitschakelen moet binnen 5 seconden gebeuren na ontvangst van een signaal. Er staat 15 seconden in de specificatie, maar dit is inclusief communicatievertraging, de installatie moet in een testopstelling binnen 5 seconden omlaag kunnen regelen.
  * Er moet een indicatie op het device/gateway zitten van een succesvolle verbinding met het platform, denk aan een led of melding op een lcd.

Als er blijkt tijdens de conformiteitstest of na goedkeuring dat aan deze eisen niet is voldaan wordt er geen goedkeuring verleend (of indien deze verleend was, ingetrokken) waardoor een interface geen verbinding met het platform kan maken.
