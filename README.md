---
title: "Trend Micro Vision One™ - Move faster than your adversaries with powerful purpose-built XDR, attack surface risk management, and zero trust capabilities"
chapter: true
weight: 2
---

## Trend Micro Vision One™
### Move faster than your adversaries with powerful purpose-built XDR, attack surface risk management, and zero trust capabilities
![TrendMicro](/images/logo.png)

With this guide, you’ll learn how to use Trend Micro Vision One and Trend Micro Cloud One Workload Security to detect and prevent attacks, even when they don’t rely on malicious code (0-day malware), like, for example, using Powershell or shell scripts, or other OS commands to compromise, do lateral movement, data exfiltration, and others.

Cloud One Workload Security will be initially deployed to detect (not taking actions), in this way allowing the attacker to execute all the malicious instructions they want. Using Vision One, you will find that some of the activities that were not detected/considered malicious by Cloud One Workload Security were detected and reported by Vision One. This will happen because of the nature of the instructions used by the attacker, which are not necessarily malicious (they are just Windows or Linux instructions/commands). Still, when found or identified in specific contexts, they could be part of attacks.

The second phase of this demo will require the Cloud One Workload Security policy to be changed. The new policy will activate and enable the protection, so you can expect some of the tests you have done in the initial phase of this demo to be detected and stopped by Cloud One Workload Security and the others (non-malicious instructions), detected by Vision One.

--------
## Use Cases Covered in this Workshop
With this workshop, you can simulate Real World uses cases like:

<b>- Use Case A - A Windows Server (EC2 Instance)</b>

An administrator accidentally compromised a Windows Server, when the administrator download a compromised version of Mozilla Firefox.will download and run a 0-day malware that will give the control of the affected computer to attackers. We will show in this demo how C1WS in conjunction with Vision One can help detecting suspicious behaviors related to 0-day attacks, and mitigate/remediate them as soon as they are detected by the Trend Micro components in place.

--------
## Demo Structure
The demo is divided into the sections listed below. Plan on setting aside 2 hours to complete the full workshop.

<b>1. Introduction (5 minutes)</b>

<b>2. Prerequisites (5 minutes)</b>

<b>3. Lab Preparation (10 minutes)</b>

<b>4. Detection Mode (20 minutes)</b>

<b>5. Prevention Mode (20 minutes)</b>

<b>6. CleanUp (10 minutes)</b>

---------
### **Additional Help**
For any additional help please reach out to: 

- Fernando Cardoso - Email: fernando_cardoso@trendmicro.com
- Andre Fernandes - Email: andre_fernandes@trendmicro.com

<p>
<a  href="mailto:fernando_cardoso@trendmicro.com;andre_fernandes@trendmicro.com?subject=Vision One - C1WS Workshop"  target="_blank" rel="noopener noreferrer"  class="btn btn-default">  
  Talk to us
  <i class="fas fa-paper-plane"></i>
</a>

<a  href="https://github.com/fernandostc/v1-c1ws-workshop/issues/new" target="_blank" rel="noopener noreferrer"  class="btn btn-default">  
  <i class="fas fa-bug"></i>
  Report an issue or feature request
</a>
</p>
</li>
</ul>
<p>Built with <i class="far fa-heart" style="color: red;"></i> by Trend Micro Team</p>

