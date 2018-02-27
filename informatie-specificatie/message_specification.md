## 61850 profile {#message-specification}

IEC61850 interface profile to meet the RfG guidelines. This profile is inspired by BAP (Basic application profile/61850-7-6).

## Functional description
Due to an increasing adoption of renewable energy sources, electricity production moves slowly form big production plants to local electricity production. Think of solar panels for example. This can lead to local problems in the grid. To deal with these problems the local system operator needs to switch off or reduce the amount of electricity production (only when needed). Besides reducing load it also needs to know things about the electricity production (e.g. actual electricty production). This profile will be used for controlling and monitoring distributed energy resources.

## Description of Use Case and associated roles/actors

## Use Case

### Logialnodes used
All field descriped in the tables are mandatory (form the 61850 standard or required to meet this RfG specification)

**DRCT**

|Data object name |Common data class | Default value | Comment |
|:--|:--|:--|:--|
|DERNum| ING|
|DERTyp| ENG|
|Wmax|ASG|
|Vref| ASG|
|OutPFSet|ASG|
	
	
**LPHD**

|Data object name| Common data class|Default value | Comment |
|:--|:--|:--|:--|
|PhyNam| DPL|||
|PhyHealth| ENS|||
|Proxy|	SPS| False | Proxy is not allowed (?)|
	
	
**LLN0**

|Data object name|Common data class| Default value | Comment |
|:--|:--|:--|:--|	
|NamPlt	|LPL|	


**FSCH**
Todo: Number of schedules?

|Data object name|Common data class| Default value | Comment |
|:--|:--|:--|:--|
|SchdSt	|ENS|
|Beh| ENS|
|VldReq| SPC|
|EnAReq| SPC|
|EdtReq	|SPC|
|DsaReq| SPC|
|SchdPrio| ING|
|NumEntr| ING|
|SchdIntv| ING|
|ValASG| ASG||Number of Values allowed?|
|StrTm|	TSG|
|IntvPer| ING|
|IntvTyp| ENG|
|EvTrg|	SPG|
|InSyn|	ORG|
|SchdReuse|SPG|
	
	
**FSCC**

|Data object name|Common data class| Default value | Comment |
|:--|:--|:--|:--|
|ActSchdRef| ORS|||
|CrlEnt| ORG|||




