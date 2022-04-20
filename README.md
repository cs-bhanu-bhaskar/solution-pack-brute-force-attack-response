# solution-pack-brute-force-attack-response

## Release Information
- Solution Pack Version: 1.0.0
- FortiSOAR™ Version Tested on: 7.2.0
- Authored By: Fortinet
- Certified: No

## Overview
### Introduction
*Brute Force Attack Response Solution Pack* is designed to provide a set of investigation and utility playbooks to respond to suspicious Repeated login failure.

Configure ingestion using Connectors such as FortiSIEM, Syslog. Ingestion process creates an alert of type 'Brute Force Attempts', and then triggers the response workflow.

Refer to Simulation Scenarion - Brute Force Attempt to experience the use case without any Ingestion configuration.

### Usage 

This Solution Pack ships with following simulation scenarios. [Refer](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/docs/solution-pack-guide.md) to Simulate Scenario documentation to undersand how to Simulate and Reset Scenario.

#### 1. Scenario - Brute Force Attempt

The scenario generates a demo alert of Type 'Brute Force Attempt' from Syslog.

Goto generated alert and observe the following:
- Alert created with Type Brute Force Attempts
- Reported Alert contains Source and Destination IP 
- Targeted Assets details and other related source Data


#### 2. Scenario - Brute Force Attempt (FortiSIEM)
The scenario generates a demo alert of Type 'Brute Force Attempt' from FortiSIEM

Goto generated alert and observe the following:
- Alert created with Type Brute Force Attempts
- Reported Alert contains Source and Destination IP 
- hostname details and other related source Data


**Investigate Brute Force Attempt**:  Launch "Investigate Brute Force" and "Investigate Brute Force(FortiSIEM)"Playbook and observe various investigation activities such as
- Source IP is external or internal
- Reputation of Source IP (using Virustotal Threat intel connector)
- retrieve More details of Source IP from Splunk or Active Directory 
- Block IP as a part of BFA remediation Process

## Prerequisites
**Solution Pack Name**|**Purpose**|**Doc Link**|
| :- | :- | :- |
|SOAR Framework 1.0.0|Require for Incident Response modules|[Click here](https://github.com/fortinet-fortisoar/solution-pack-soar-framework/blob/develop/README.md)|
|SOC Simulator 1.0.1|Require for Scenario Module and SOC Simulator connector| [Click here](https://github.com/fortinet-fortisoar/solution-pack-soc-simulator/blob/develop/README.md)|

## Contents
1. Global Variable(s)
    - Demo_mode
2. Record Set(s)
    - Scenario: 
3. Playbook Collection(s)
    - 02 - Use Case - Brute Force Attack (3): 
    
    **SN**|**Playbook Name**|**Description**|
    | :- | :- | :- |
    |1|Investigate Brute Force Attempt|Investigates login failures and also identifies other impacted assets that have been victims of the brute force attempts from a particular source of attack|
    |2|Investigate Brute Force Attempt (FortiSIEM)|Investigates login failures from FortiSIEM and also identifies other impacted assets that have been victims of the brute force attempts from a particular source of attack|
    |5|Generate > FortiSIEM (Brute Force Attack)|Playbook will generate a demo record - Brute Force Attack|