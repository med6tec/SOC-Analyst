## Introduction
This guide will walk you through the process of building a home lab using Active Directory (AD) and Splunk Security Information and Event Management (SIEM). By the end of this tutorial, you will have a functional lab environment where you can practice threat detection, incident response, and security monitoring.

## Overview
In this home lab today we will learn how to setup Active directory & how to create users & add machines to the Domain. We will also setup sysmon & splunk for log collection & analysis. Finally we will use Kali linux & ART (Atomic Red Team) to create telemetry which we can analyse in splunk.

## Lab Setup
Using VMWare Workstation 17 Pro, set up the following virtual machines:

* _1 x Windows Server 2019 (Domain controller)_

* _1 x Windows 10 Enterprise — User-machine 1_

* _1 x Ubuntu Machine (Splunk)_

## 1- Install & setup Windows 10 & Windows Server for Active Directory
* Open VMware select File (left corner) -> New virtual machine -> Typical -> Disc image : select path where you downloaded above file for windows 10 -> location : default -> storage : default -> Customize hardware : RAM 2GB -> Finish
* Select windows 10 -> edit virtual machine settings -> Options -> Advanced -> Firmware type : change to BIOS close ->Power On windows 10 -> Language, Time : Default -> Install now -> I dont have product key -> Windows 10 pro -> accept license terms -> Custom install -> Next -> Finish
* Setup & give credentials which you can remember.

## _Windows 10 Screenshots_

![Capture12](https://github.com/user-attachments/assets/c37d3b60-6211-4621-b509-f5da4a4495f3)

![Capture13](https://github.com/user-attachments/assets/d45a6951-c5b8-4e78-bb8f-c6ec286184a8)

![Capture14](https://github.com/user-attachments/assets/b43dbf25-163c-4559-9b87-f8abc20ba33f)

![Capture](https://github.com/user-attachments/assets/0479cad7-5381-438d-8139-8515b5c33b60)

![Capture15](https://github.com/user-attachments/assets/ed1b9bde-2918-4fc7-afe1-74ad2959b377)

![credent](https://github.com/user-attachments/assets/bb7ed3a1-48b5-4c10-ba5a-568ff3835a2a)

## _Windows Server 2019 Screenshots_

![Capture 5](https://github.com/user-attachments/assets/5246970f-d660-48ab-a3ae-f7176a88b04c)

![Capture 7](https://github.com/user-attachments/assets/12a44309-f472-4840-a9fb-59464b56d0de)

![Capture9](https://github.com/user-attachments/assets/0c926237-0c13-4c0b-949a-1c1bcc07dc4b)

![Capture10](https://github.com/user-attachments/assets/1cf866f3-681b-44cf-b04b-00823d9318ee)

![credent](https://github.com/user-attachments/assets/8c9f5c02-75f5-4c44-afd8-85675d5cef14)

## 2- Configure Active Directory & Join Windows 10 to Domain
