## Introduction
This guide will walk you through the process of building a home lab using Active Directory (AD) and Splunk Security Information and Event Management (SIEM). By the end of this tutorial, you will have a functional lab environment where you can practice threat detection, incident response, and security monitoring.

## Overview
In this home lab today we will learn how to setup Active directory & how to create users & add machines to the Domain. We will also setup sysmon & splunk for log collection & analysis. Finally we will use Kali linux & ART (Atomic Red Team) to create telemetry which we can analyse in splunk.

## Lab Setup
Using VMWare Workstation 15 Player, set up the following virtual machines:

* _1 x Windows Server 2019 (Domain controller)_

* _1 x Windows 10 Enterprise — User-machine 1_

* _1 x Ubuntu Machine (Splunk)_

## 1- Install & setup Windows 10 
* Open VMware select File (left corner) -> New virtual machine -> Typical -> Disc image : select path where you downloaded above file for windows 10 -> location : default -> storage : default -> Customize hardware : RAM 2GB -> Finish
* Select windows 10 -> edit virtual machine settings -> Options -> Advanced -> Firmware type : change to BIOS close ->Power On windows 10 -> Language, Time : Default -> Install now -> I dont have product key -> Windows 10 pro -> accept license terms -> Custom install -> Next -> Finish
* Setup & give credentials which you can remember.
