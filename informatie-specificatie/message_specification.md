## 61850 profile {#message-specification}

IEC61850 interface profile to meet the RfG guidelines. This profile is inspired by BAP (Basic application profile/61850-7-6).

## Functional description
Due to an increasing adoption of renewable energy sources, electricity production moves slowly from big production plants to local electricity production. Think of solar panels for example. This can lead to local problems in the grid. To deal with these problems the local system operator needs to switch off or reduce the amount of electricity production (only when needed). Besides reducing load it also needs to know things about the electricity production (e.g. actual electricty production) to predict congestion. This 61850 profile will be used for controlling and monitoring distributed energy resources.

## Description of Use Case and associated roles/actors
![Actor overview](/assets/61850Actors-overview.png)

## Use Case
![use case overview](/assets/61850Monitor-and-control-DER.png)

## Sequence diagram
![sequence](/assets/61850Sequence-diagram-typical-interactions.png)

## Logical Architecture

Logical architecture monitoring function
![Logical architecture monitoring function](/assets/Logical_Architecture_DERmonitoringfunction.png)

Logical architecture control function
![Logical architecture control function](/assets/Logical_Architecture_DERcontrolfunction.png)



### Description of data model per actor
All field descriped in the tables are mandatory where the M is shown (by the IEC61850 standard if you want to certificate your device) . All IEC61850 required fields (R) should be included in the device to meet this RfG implementation. All parameters should be changeable by 61850 services except stated otherwise.

**DRCT for local DER control function**

|Data object name |Common data class | Attribute(s) |Default value | Comment | R/M|
|:--|:--|:--|:--|:--|:--|
|DERNum| ING|stVal||Number of electricity production (DER) units connected to controller. 1 of only 1 production unit is connected or is fysical .|M|
|DERTyp| ENG|steVal|| Type of DER unit managed by controller.|M|
|MaxWLim| ASG|setMag||Nominal max output power at controller. |M|
|MaxVArLim| ASG|setMag||Nominal max output reactive power at controller. The Electricity production unit should not exceed this setting.|M|
|Wmax|ASG|setMag||Maximal output of the electricity production unit. Assumption: internal control system finds a setpoint below this value. |R|
|Vref| ASG|setMag||Reference voltage for functions using grid voltage as input|M|
|OutPFSet|ASG|setMag||Setpoint for maintaining fixed power factor.|M|
	
	
**LPHD**

|Data object name| Common data class| Attribute |Default value | Comment |R/M|
|:--|:--|:--|:--|:--|:--|
|PhyNam| DPL|vendor||Vendor of the physical device.|R|
| | |swRev||Software revision of the physical device. Should be changed by manufacture.|R|
| | |model||Software revision of the physical device. Should be changed by manufacture.|R|
| | |mRID||mRID of the physical device.|R|
| | |serNum||Serialnumber of de physical device. Should be changed by manufacture.|R|
| | |primeOper||Primary operator of device. STRING256(can we use this for the QR URL?)|R|
|PhyHealth| ENS|stVal||Physical device health|M|
| | |q||Quality|M|
| | |t||Timestamp|M|
|Proxy|	SPS| stVal | False | Proxy |M|
| | |q||Quality|M|
| | |t||Timestamp|M|
|PwrUp| SPS| stVal | | Power-up detected |R|
| | |q||Quality|M|
| | |t||Timestamp|M|
	
**LLN0**

|Data object name|Common data class|Attribute | Default value | Comment |R/M|
|:--|:--|:--|:--|:--|:--|
|NamPlt	|LPL|vendor||Vendor of the LN. Mandatory by IEC61850. | M|
| | |swRev||Software revision of the LN.|M|


**FSCH for Schedule function**
Number of schedules is limited by memory size and the way of consuming the schdules (number of values in a schedule).

|Data object name|Common data class|Attribute | Default value | Comment |R/M|
|:--|:--|:--|:--|:--|:--|
|SchdSt	|ENS|stVal||State of this schedule|R|
| | |q||Quality|M|
| | |t||Timestamp|R|
|SchdEntr |INS|stVal||The current schedule entry of a running schedule.|R|
| | |q||Quality|M|
| | |t||Timestamp|R|
|Beh| ENS|stVal|||M|
| | |q||Quality|M|
| | |t||Timestamp|M|
|VldReq| SPC|ctlModel||Operating with value true initiates validate transition request|R|
|EnaReq| SPC|ctlModel||Operating with value true enable validate transition request.|R|
|EdtReq	|SPC|ctlModel||Operating with value true edit validate transition request.|R|
|DsaReq| SPC|ctlModel||Operating with value true disable validate transition request.|R|
|SchdPrio| ING|setVal||The priority of this schedule.|R|
|NumEntr| ING|setVal||The number of schedule entries that are valid.|R|
|SchdIntv| ING|setVal||The schedule interval duration in time entities as specified in the SchdIntv.units.SIUnit.|R|
|ValASG| ASG|setMag||current value output as MV: Number of Values allowed?|R|
|StrTm|	TSG|setTm||Start time of the schedule in UTC time.|R|
|||setCal|||R|
|IntvPer| ING|setVal||The periodicity interval duration in entities as specified in IntvTyp; if the value is 0, the schedule shall not be repeated periodically.|R|
|IntvTyp| ENG|stVAl||Interval type to define the periodicity.|R|
|EvTrg|	SPG|setVal||If true, the change of the schedule to the running and activated state is triggered by an external event and not by the start time.|R|
|InSyn|	ORG|setSrcRef||Object reference of the external trigger if the schedule is triggered by an event.|R|
|SchdReuse|SPG|setVal||If true, once terminated or disabled, the schedule will change to the validated state, otherwise it will change to the not ready state.|R|
	
	
**FSCC for Schedule control function**

|Data object name|Common data class| Attribute | Default value | Comment |R/M|
|:--|:--|:--|:--|:--|:--|
|ActSchdRef| ORS|stVal||Indication of which schedule is active as an object reference.|R|
| | |q||Quality|M|
| | |t||Timestamp|M|
|CrlEnt| ORG|setSrcRef||Object reference to the entity controlled by the schedule.|R|
|Schd| ORG|||Object reference of schedule n (an LN reference to the LN of class FSCH). (maximal numer of schedules?)|R|

**MMXU for DER monitor function**
This logical node measures the actual output of the electricity production unit.

|Data object name|Common data class| Attribute |Default value | Comment |R/M|
|:--|:--|:--|:--|:--|:--|
|TotW| MV|mag|||R|
| | |q||Quality|M|
| | |t||Timestamp|R|
|TotVAr| MV|mag|||M|
| | |q||Quality|M|
| | |t||Timestamp|M|

**MMXU for Measurement calculation function**

These Logical nodes can be used to calculate the averages etc. These LN's should connect to the actual MMXU who does the non-calculated measurements.

|Data object name|Common data class| Attribute |Default value | Comment |R/M|
|:--|:--|:--|:--|:--|:--|
|ClcMth | ENG|mag|MAX| Calculation Method of statistical data|R|
| | |q||Quality|M|
| | |t||Timestamp|M|
|ClcMod | ENG |mag|PERIOD|Calculation mode|R|
| | |q||Quality|M|
| | |t||Timestamp|M|
|ClcIntvTyp |ING| || Calculation interval type. |R|
|ClcIntvPer|ING| || In case ClcIntvTyp equals to MS, PER-CYCLE, CYCLE, DAY, WEEK, MONTH, YEAR, number of units to consider to calculate the calculation interval duration | R|
|InSyn|ORG|||Object reference to the source of the external synchronization signal for the calculation interval |R|
|CLCSrc|ORG|||Object reference to source logical node |R|
|ClcExp|SPS|||Calculation period expired |R|
|TotW| MV |mag||Active power value|R|
| | |q||Quality|M|
| | |t||Timestamp|R|



**MMTR for DER monitor function**

|Data object name|Common data class| Attribute |Default value | Comment |R/M|
|:--|:--|:--|:--|:--|:--|
|TotWh| BCR |ActVal||Sending the kWh every X minutes allow the system operator to calcuate the de daily average etc |R|
| | |q||Quality|M|
| | |t||Timestamp|R|
| | |PulsQty||Timestamp|M|

## Communication Services
The following services should be supported by the electricity production unit.

Association
* Associate
* Release
* Abort

Server
* GetServerDirectory

Locigal Device
* GetLogicalDeivceDirectory

Logical Node
* GetLogicalNodeDirectory

Data
* GetDataValues
* SetDataValues
* GetDataDefinition

Data set
* GetDataSetValues
* SetDataSetValues

Reporting
* Report
* GetURCBValues
* SetURCBValues
* SetBRCBValues
* SetBRCBValues

Control
* Operate

**keepalive**
According 61850-8-2, XEP 0199 can be used to build a keep alive signal.

**XMPP**
IEC 61850-8-2 should be used for communication: Communication networks and systems for power utility automation - Part 8-2: Specific communication service mapping (SCSM) - Mapping to Extensible Messaging Presence Protocol (XMPP).

**Persistence**
The following items need to be persistance on the device (saved when the device has no power):
* Schedules
* Report buffer
* Measurement settings

## Standards used

An overview of the standards used in this Profile.

|Standard|Name| Used for |
|:--|:--|:--|
|IEC 61850-7-1 | Basic communication structure – Principles and models | Description of the logical nodes |
|IEC 61850-7-2 | Basic communication structure – Abstract communication service interface (ACSI)|Description of Abstract communication service interface|
|IEC 61850-7-3 | Basic communication structure – Common data classes | Description of the common data classes |
|IEC 61850-7-4 | Basic communication structure – Compatible logical node classes and data classes | Description of the logical nodes | 
|IEC 61850-7-6 DRAFT | Guideline for definition of Basic Application Profiles (BAPs) using IEC 61850 | Inspration for this BAP |
|IEC 61850-7-420| Communication systems for distributed energy resources (DER) – logical nodes|Overview of the DER LN's|
|IEC 61850-80-2| Mapping to Web Services - Requirement Analysis and Technology Assessment | Motivation for using XMPP and use-cases (annex)|
|IEC 61850-80-3 DRAFT| Specific communication service mapping (SCSM) - Mapping to Extensible Messaging Presence Protocol (XMPP) | ACSI mapping on XMPP|
|IEC 61850 90-10| IEC 61850 objects for scheduling | Descripton of the schedule nodes |
