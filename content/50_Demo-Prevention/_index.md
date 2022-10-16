---
title: "Prevention Mode"
chapter: false
weight: 50
pre: "<b>5. </b>"
---
## Demo Prevention Mode 
In this lab, all the Security Controls available on Cloud One Workload Security and Vision One XDR Agent are configured to prevent attacks and detect and block malicious files. You will note that some of the instructions executed using the Mitre Caldera will not be stopped by default by the platform (C1WS+V1). That happens because they are not necessarily malicious, they can be malicious depending on the context and other risk factors that can be detected by Vision One. 

With this demo you will learn how C1WS and V1 can work together to stop all the known threats and attacks, and at the same same enable the detection and response against 0-day malwares and attacks.

### Attacking Phase
In this demo, we are using the Mitre Caldera tool, to help us following the normal/expected attack sequence. The Mitre Caldera helps to deploy instructions based on the Mitre ATT&CK Framework, allowing us to evaluate security solutions based on real-world use cases.

#### What are Tactics in the ATT&CK Framework?
ATT&CK stands for adversarial tactics, techniques, and common knowledge. The tactics are a modern way of looking at cyberattacks. Rather than looking at the results of an attack, aka an indicator of compromise (IoC), it identifies tactics that indicate an attack is in progress. Tactics are the “why” of an attack technique.

The Enterprise ATT&CK matrix has 14 tactics. In this demo, we are covering the following highlighted tactics.

- Reconnaissance
- Resource Development
- Initial Access
- Execution
- Persistence
- Privilege Escalation
- Defense Evasion
- Credential Access
- Discovery
- Lateral Movement
- Command & Control
- Collection
- Exfiltration
- Impact