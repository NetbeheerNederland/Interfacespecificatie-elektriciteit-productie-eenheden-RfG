# 3.5 Energy System Security by design \(EN\)

Specifying a communication interface does not mean that this part has to be secure on its own only. The communication interface is part of a complete system: the total European energy system. This energy system is built on physical laws and their limits, supported with local automation and a layer of remote influencing. Furthermore the energy system consists of natural and automated actors reacting to market prices or other behavior influencing mechanisms. This chapter describes the basics of the energy grid security at the DSO grid and focuses on the role of the electricity production unit protection and automation that is requested by the [RfG Connection code](https://electricity.network-codes.eu/network_codes/rfg/). The chapter was written from the perspective that the relevant system operators has to secure the energy grid on stability and continuity as their main task.

## Summary

For DSO operations, controlling decentralized energy production is not completely dependent on the availability of remote influencing. If remote influencing is not available, there are fall-back solutions in embedded automation \(production unit\), embedded protection \(production unit or grid\) or there is enough time in advance to act. However, the fall-back solutions are sometimes harsh and equal to the situation not having remote influencing at all. It is increasingly important being able to rely on a properly functioning of the embedded automation and protection of production units and of grid automation. This may not fail. [RfG Connection code](https://electricity.network-codes.eu/network_codes/rfg/) describes the role of the owners of electricity production units to comply with the specifications. It also describes the role of the DSO and TSO to demand compliancy of the decentralized energy production units.

| Operational situation under DSO responsibility | Remote influencing to reduce impact | Backup: Time for manual action | Backup: Embedded automation/ protection |
| :--- | :--- | :--- | :--- |
| Local voltage is too high | Yes, detect and act | Not always | `RfG overvoltage protection` |
| Local voltage is too low | n/a for productionlimit | n/a for productionlimit | n/a for productionlimit |
| High load on assets \(N-1 -&gt; N due to maintenance\) | Yes, plan reduction | `Yes, maintenance is planned` | Not possible |
| High load on assets \(N-1 -&gt; N due to failure\) | Yes, send reduction | `Yes, temporary N situation` | Not possible |
| Overload on assets \(N -&gt; I&gt; due to maintenance\) | Yes, plan reduction | `Yes, maintenance is planned` | `Yes, but only DSO grid` |
| Overload on assets \(N -&gt; I&gt; due to failure\) | Yes, avoid outage | Not possible | `Yes, but only DSO grid` |

## Physical behavior of the grid

Related to Distributed Energy Resources \(DER\) **main concerns** of the DSO are: 1. Local voltage is becoming too high, risk on production units to trip; 2. Local voltage is becoming too low, risk on production units to trip; 3. Due to maintenance the currents are too high to keep up the redundancy \(N-1\), increased risk outage 4. Due to disturbance the currents are too high to keep up the redundancy \(N-1\), increased risk outage 5. Due to maintenance the currents are too high to keep up normal operation \(N\), risk of overload 6. Due to disturbance the currents are too high to keep up normal operation \(N\), risk of overload

Frequency isn't primary managed by the DSO and therefore not mentioned as a main concern although the DSO cooperates with the TSO to keep it stable any time.

Except fuses in the grid, there are no physical means to mitigate the main concerns at a natural way. Therefore local automation and protection or external signals should contribute to mitigation.

> To the concerns above, optimization is possible in other ways which won’t be elaborated on in this document. Just in short: too high voltage \(1\) can be managed by fine-tuning the upper limits depending on characteristics of the grid area; too low voltage \(2\) can also be a symptom of local reactive power problems; with maintenance \(3\) and \(5\) attention should be paid to delayed works in relation to planned remote signals; backup protection can be optimized, e.g. situational tripping of feeders in case of congestion instead of general protection functions; overload on assets \(5\) and \(6\) can take place at higher grid levels. This means that tripping a field with energy production can make the situation worse. Therefore protection and local automation needs attention anyway, independent of remote influencing.

## Local or regional automation and protection

Local automation and protection is used to protect all assets and to keep the grid into the frequency-limits, voltage-limits and current-limits. Let's evaluate how this embedded automation adds a layer of security on the physical grid deployed with high number of DERs. [RfG Connection code](https://electricity.network-codes.eu/network_codes/rfg/) demands technical requirements to electricity production units from 800W upwards. These requirements vary from frequency and voltage protection up to reactive-power-control. The table below gives an overview of the requirements for each category production-unit \(x = mandatory from RfG\). The table includes general Dutch requirements and a sub-category for RfG type A. RfG type D is not shown due to high level customization to the grid.

| **Automated control or protection at DER** | General Dutch req. | RfG A small | RfG A large | RfG B | RfG C |
| :--- | :---: | :---: | :---: | :---: | :---: |
| Undervoltage protection \(80% Un\) | x | x | x | x | x |
| Undervoltage protection including fault-ride-through |  |  |  | x | x |
| Overvoltage protection \(110% Un\) | x | x | x | x | x |
| Low frequency protection  \(48Hz\) | x | x | x | x | x |
| High frequency protection \(51Hz\) | x | x | x | x | x |
| I&gt;, I&gt;&gt; protection | - | - | x | x | x |
| LFSM-O \(frequency sensitive mode for overvoltage\) | - | x | x | x | x |
| LFSM-U \(frequency sensitive mode for undervoltage\) | - | - | - | - | x |
| Automatic grid connection \(after auto inspection\) | - | x | x | x | - |
| Automatic voltage control | - | - | x \(MV/HV\) | x | x |
| Reactive Power \(Q\) control \(as long as type of generator can supply\) | - | - | x \(MV/HV\) | x | x |

To main concern 1 \(Local voltage is too high\), the overvoltage protection as a requirement for electricity production units is offering protection. To main concern 6 \(risk of overload due to disturbances\) the secondary substations or in worst case the primary substations contributes with their overload protection to switch off this part of the grid in a selective way. This does imply updated measurement and protection schemes due to higher level DER's in the grid, even at low voltage levels. Concern 2 is related to load-shedding and no part of this description yet, although protection demands should be required. Concerns left are 3, 4 and 5 which are not time critical as the concerns described as first. In case of maintenance which applies to concern 3 and concern 5 it is possible to manage reduction of DERs in advance to avoid non-redundancy or overload. Concern 4 demands restoration of the N-1 situation. This allows some time to manage reduction of DERs if necessary.

The local or regional control and protection does secure many situations but can be improved from DSO perspective with remote control signals for less time critical \(read as: not being within few seconds\). This will avoid that parts of the distribution grid will be switched off completely \(tripped\) due to protection.

## Remote DER influencing facilities

As requirements are demanded to electricity production units in general within [RfG Connection code](https://electricity.network-codes.eu/network_codes/rfg/), also requirements may be demanded by the relevant system operator according to this RfG. These requirements are related to facilities to influence the energy production of the production unit. These functions are defined in RfG as follows \(where x = mandatory from RfG and o = possible from RfG\):

| Remote control functions | General Dutch req. | RfG A small | RfG A large | RfG B | RfG C |
| :--- | :---: | :---: | :---: | :---: | :---: |
| Remote trip commands \(on-off interface\) | - | o | o | - | - |
| Remote reduce comands \(0-100% interface\) | - | - | - | o | o |

The implementation of these requirements do offer an additional layer of energy system stability, especially for concern 1 to 6, with the exception of concern 2. If the remote DER influencing does not work, there is fallback on embedded automation or there is time to solve it manually in specific cases as described above. TSO's conclusion may be a bit different as it is frequency responsible, and the RfG Grid code was intended to contribute to frequency stability in the end.

> A combination between Remote DER influencing facilities and local automation gives an interesting combination. By using pre-programmable schedules in the local automation, a remote facility can pre-program the local automation. This mechanism makes the embedded automation aware of the external situation like forecasts and planned work. It will act on those schedules as long as it is in the limits which are stored locally. This mechanism lowers the dependency on telecom availability at the precise moment of command execution and improves the predictability of the grid behavior.

## Managing unrequested controls

This chapter described at a high to medium level the layered security design of the energy system with its embedded \(local\) and remote automation and protection. This chapter did not describe other means of control, e.g. via a vendor support interface. It is obvious but relevant to mention that these remote controls will influence the stability of the grid as well. Requirements should be agreed to mitigate this risk.

## Roles

To build this secured and layered grid it is essential to understand each others roles. In most comprehensive summary the Dutch implementation of the RfG and GLSO may be described as follows: each party is responsible to fulfill the requirement of the grid he/she is connected to. This means that owners of production facilities has to fulfill the demands of the grid operator / system operator it is electrically connected to. The DSO has to fulfill the requirements to the TSO. The requirements are based on both legal code, cooperation and non-discriminatory implementations, grid safety first and support to enable the market.

## Requirements

Based on stated above requirements can be formulated at a later point in time. This paragraph is a placeholder for these requirements. E.g. 1: Overcurrent detection or -protection functionality should \(also\) be available caused at low voltage level \(Dutch AC5 connection categories\). E.g. 2: Functionality to plan or schedule reduction of energy production in advance in order to plan maintenance activities without causing redundancy issues or overload risk. ...

