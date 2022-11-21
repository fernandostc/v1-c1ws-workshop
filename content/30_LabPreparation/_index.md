---
title: "Lab Preparation"
chapter: false
weight: 30
pre: "<b>3. </b>"
---
## Lab Preparation Guide

### Lab Architecture
We will use a CloudFormation template to simulate a real customer environment with the following resources.

        1x VPC
            - Attacker Instance: Mitre Caldera
            - Target Instance: Windows Client

With these three components, you can demonstrate all the Cloud One Workload Security and Vision One XDR Agent features. The Mitre Caldera is our attacking tool. It acts as the Command and Control Server that will be used to create malicious payloads and execute remote commands on the affected computers.

---
### C1WS - Importing the Security Policies
Before deploying the Cloud Formation Template, it is important to have all the C1WS and V1 base configurations ready.

Following you will find two C1WS policies that must be imported into C1WS. These policies will later be used to test the C1WS Platform.

> <b>[C1WS_DetectionMode](https://raw.githubusercontent.com/andrefernandes86/demo-v1-c1ws/main/DetectionMode.xml)</b>

> <b>[C1WS_PreventionMode](https://raw.githubusercontent.com/andrefernandes86/demo-v1-c1ws/main/PreventionMode.xml)</b>

After you download these policies, import them into C1WS.

{{< youtube id="miCCYM1Zv1k" >}}

---
### Vision One - Enabling the Vision One XDR Agent Automatic Activation
The following instructions will guide you on how to enable the Vision One XDR Agent automatic activation.

{{< youtube id="5k7QyaBSZ6U" >}}

---

### AWS - Deploying the CloudFormation Template
Using your AWS Account, deploy the folliowing Cloud Formation Template based on the instructions available on the following video.

>  <b>Be sure you followed the instructions available on the video, adding the Cloud One Workload Security Activation Command and the Vision One Agent Installation URL to the CFT.</b>

<a href="https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=V1-C1WS-Workshop&templateURL=https://v1demoplatform.s3.us-west-1.amazonaws.com/v1-c1ws-demo/demo-aws-c1ws.yml" target="_blank"><img src="https://cdn.rawgit.com/buildkite/cloudformation-launch-stack-button-svg/master/launch-stack.svg" /></a>

{{< youtube id="unTn6Nas-FA" >}}

