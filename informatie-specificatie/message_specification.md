## 61850 profile {#message-specification}

IEC61850 interface profile to meet the RfG guidelines. This profile is inspired by BAP (Basic application profile).


### Logialnodes used
All field descriped in the tables are mandatory (form the 61850 standard of required to meet the RfG guideline)

**DRCT**
|Data object name|Common data class|
|:--|:--|
|DERNum| ING|
|DERTyp|	ENG|
|Wmax|ASG|
|Vref|	ASG|
|OutPFSet|	ASG|
	
	
**LPHD**

|Data object name| Common data class|
|:--|:--|
|PhyNam|	DPL|
|PhyHealth|	ENS|
|Proxy|	SPS|
	
	
**LLN0**	
|Data object name|Common data class|
|:--|:--|	
|dummy	|dummy|	
	
**FSCH**
|Data object name|Common data class|
|:--|:--|
|SchdSt	|ENS|
|Beh|	ENS|
|VldReq|	SPC|
|EnAReq|	SPC|
|EdtReq	|SPC|
|DsaReq|	SPC|
|SchdPrio|	ING|
|NumEntr|	ING|
|SchdIntv|	ING|
|ValASG|	ASG|
|StrTm|	TSG|
|IntvPer|	ING|
|IntvTyp|	ENG|
|EvTrg|	SPG|
|InSyn|	ORG|
|SchdReuse|SPG|
	
	
**FSCC**
|Data object name|Common data class|
|:--|:--|
|ActSchdRef|	ORS|
|CrlEnt|	ORG|




