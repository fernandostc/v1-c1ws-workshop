---
title: "Lab Preparation"
chapter: false
weight: 30
pre: "<b>3. </b>"
---
## Lab Preparation Guide

### Lab Architecture
To simulate a real customer environment, we will use a pre-built CloudFormation template that will create the following resources all in the same Availibility Zone (AZ):

The CFT will create 1 VPC. On this VPC, you will find one attacker computer (Mitre Caldera), one Windows computer (Windows Client - Target 1) and one Linux Computer (Linux Client - Target 2).

With this three components, you will be able to demonstrate all the Cloud One Workload Security and Vision One XDR Agent features. The Mitre Caldera is our attacking tool. It simulates an Command and Control Server, that can be used to create malicious payloads and execute malicious commands on the affected computers.

NETWORK DIAGRAM HERE

---
### Importing the Security Policies to C1WS
Before deploying the Cloud Formation Template, its important to have all the C1WS and V1 base configurations ready.

Following you will find two C1WS policies that must be imported into C1WS. These policies will later be used to test the C1WS Platform.

> <b>[C1WS_DetectionMode](https://raw.githubusercontent.com/andrefernandes86/demo-v1-c1ws/main/DetectionMode.xml)</b>

> <b>[C1WS_PreventionMode](https://raw.githubusercontent.com/andrefernandes86/demo-v1-c1ws/main/PreventionMode.xml)</b>

After you download these policies, import them into C1WS.

{{< youtube id="miCCYM1Zv1k" >}}

---
### Enabling the Vision One XDR Agent (Automatic Activation)
The following instructions will guide you on how to enable the Vision One XDR Agent automatic activation.

{{< youtube id="5k7QyaBSZ6U" >}}

---

### Creating the base AWS environment using AWS CloudFormation Template
Using your AWS Account, deploy the Cloud Formation Template “[demo-aws-c1ws.yaml](https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=ZTSAWorkshop&templateURL=https://visionone.s3.us-west-1.amazonaws.com/demo-aws-c1ws.yaml)” and follow the next instructions. 

<a href="https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=V1-C1WS-Workshop&templateURL=https://visionone.s3.us-west-1.amazonaws.com/demo-aws-c1ws.yaml" target="_blank"><img src="https://cdn.rawgit.com/buildkite/cloudformation-launch-stack-button-svg/master/launch-stack.svg" /></a>

{{< youtube id="QgYiRZLhbyk" >}}

