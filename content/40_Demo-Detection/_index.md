---
title: "Detection Mode"
chapter: false
weight: 40
pre: "<b>4. </b>"
---
## Demo Detection Mode 
In this lab, all the Security Controls available on Cloud One Workload Security and Vision One XDR Agent are configured to only generate detection events for all the security incidents detected by the solutions.

The idea is to show how both solutions can together help detecting suspicious and malicious events related to Zero Day Attacks.

In the next phase of this demo (Prevention Mode), we will show how these security controls, when deployed to detect and stop the attacks, could help detecting and preventing all the stages of the attacks described on this demo.

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
