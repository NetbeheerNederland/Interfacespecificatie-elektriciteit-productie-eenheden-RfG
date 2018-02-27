## 61850 profile {#message-specification}

IEC61850 interface profile to meet the RfG guidelines. This profile is inspired by BAP (Basic application profile/61850-7-6).

## Functional description
Due to an increasing adoption of renewable energy sources, electricity production moves slowly form big production plants to local electricity production. Think of solar panels for example. This can lead to local problems in the grid. To deal with these problems the local system operator needs to switch off or reduce the amount of electricity production (only when needed). Besides reducing load it also needs to know things about the electricity production (e.g. actual electricty production). This profile will be used for controlling and monitoring distributed energy resources.

## Description of Use Case and associated roles/actors
![Actor overview](/assets/61850Actors-overview.png)

## Use Case
![use case overview](/assets/61850Monitor-and-control-DER.png)

## Sequence diagram
![sequence](/assets/61850Sequence-diagram-typical-interactions.png)

## Logical Architecture


### Logicalnodes used
All field descriped in the tables are mandatory (form the 61850 standard or required to meet this RfG specification)

**DRCT for local DER control function**

|Data object name |Common data class | Attributes |Default value | Comment |
|:--|:--|:--|:--|:--|
|DERNum| ING|stVal
|DERTyp| ENG|steVal
|Wmax|ASG|setMag
|Vref| ASG|setMag
|OutPFSet|ASG|setMag
	
	
**LPHD**

|Data object name| Common data class| Attributes |Default value | Comment |
|:--|:--|:--|:--|:--|
|PhyNam| DPL|vendor, swRev, model,mRID||
|PhyHealth| ENS|stVal,q,t|||
|Proxy|	SPS| stVal,q,t | False | Proxy is not allowed (?)|
	
	
**LLN0**

|Data object name|Common data class|Attributes | Default value | Comment |
|:--|:--|:--|:--|:--|	
|NamPlt	|LPL|vendor,swRev,configRef,paramRev	


**FSCH for Schedule function**
Todo: Number of schedules?

|Data object name|Common data class|Attributes | Default value | Comment |
|:--|:--|:--|:--|:--|
|SchdSt	|ENS|stVal,q,t|
|SchdEntr |INS|stVal,q,t|
|Beh| ENS|stVal,q,t|
|VldReq| SPC|ctlModel
|EnaReq| SPC|ctlModel
|EdtReq	|SPC|ctlModel
|DsaReq| SPC|ctlModel
|SchdPrio| ING|setVal
|NumEntr| ING|setVal
|SchdIntv| ING|setVal
|ValASG| ASG|setMag|Number of Values allowed?|
|StrTm|	TSG|setTm,setCal
|IntvPer| ING|setVal
|IntvTyp| ENG|stVAl
|EvTrg|	SPG|setVal
|InSyn|	ORG|setSrcRef
|SchdReuse|SPG|setVal
	
	
**FSCC for Schedule control function**

|Data object name|Common data class| Attributes | Default value | Comment |
|:--|:--|:--|:--|:--|
|ActSchdRef| ORS|stVal, q,t|||
|CrlEnt| ORG|setSrcRef||

**MMXU for DER monitor function**

|Data object name|Common data class| Attributes |Default value | Comment |
|:--|:--|:--|:--|:--|
|TotW| MV|mag,q,t||
|TotVAr| MV|mag,q,t||


|PhV| MV||Not a requirement|
|TotPF| MV||Not a requirement|

Cannot be found in IEC61850 (so far):
Minimal Power (P) during measurement interval t
Maximal Power (P) during measurement interval t
Average Power (P) in each 24 hours
Average Power (P) during the day*
Average Power (P) during the night*
Average Power in total during interval t, measured in a resolution of 30 minute values**.


