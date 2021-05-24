---
title: Using raspberry pi and cloud to control a remote display
layout: post-right-sidebar
categories: []
image: assets/images/post/kloudtise.jpg
featured: false
---

This was done as part of our Bachelors Technology project in 2014. The Project was named as Kloudtise - Cloud and Advertise.
# Introduction 
A simple platform for the advertiser to display advertisements in any location where these advertisement terminals are setup.

Advertisements  are displayed anywhere without any direct link between the advertiser and the advertisement !
A cloud server is built which directs advertisements from the advertiser to the desired display using the internet. 

This project consists of a website that can be used by both admins and advertisers. Admins have elevated permissions on the website. They can accept advertisements submitted by advertisers, process payments and check advertisement content. If the advertisement violates any advertisement terms or conditions, admins can reject ad’s or else they can forward the ad to the cloud server. 

Advertisers can signup for an account in the website using which they can upload advertisements and purchase advertising space on the corresponding terminal.

![]({{ 'assets/images/kloudtise-flow.jpg' | relative_url }})

Each advertising terminal consists of a large display and a single board microcomputer (Raspberry Pi). A server program runs in the Pi which is connected to the cloud server via the internet. Advertisements pushed by the cloud server are accepted by the server program running on the Pi and is displayed in the large screen. Each advertisement is displayed in the screen for a predetermined period of time after which the next ad is displayed. Also if display terminal is moving, then location of display terminal is identified using GPS satellites and advertisements corresponding to the particular location are displayed.
# Existing System

In our cities we can see advertisement display boards on top of buildings and other structures.
These systems consists of a display terminal which is already preloaded with a set of advertisements that are displayed repeatedly. 
The time and duration for which the advertisements is to be displayed is manually controlled at this location.
Loading of advertisements in the terminal  is also done at this location itself.
# Kloudtise Model
Our system consists of a display terminal which is remotely controlled by administrator.
An Interface is provided for interaction between stakeholders and the server.

Our system is divided into three modules namely
Interface
Servers
Terminal

**Interface**

Users can :
* Create Account
* Login
* Upload advertisements	 

Admin can
* Admin login
* Approve uploaded advertisements
* View registered user details

**Server**

Our project mainly consists of two servers:
* Cloud server
* FTP server
FTP server mainly deals with uploaded advertisements.
Users upload advertisements to FTP server.
Cloud server is deployed with the help of Redhat’s OpenShift Engine
Once the advertisement is approved by the Admin ,the Cloud server helps in redirecting it to the respective display terminals.
Advertisements are filtered based on terminal location.

**Terminal**

The terminal consist of a display screen or a panel which is connected to a Raspberry Pi board.
The Raspberry Pi board controls displaying of advertisements.
Advertisements are downloaded  from ftp server to raspberry pi using an internet connection based on terminal location. 
Raspberry pi executes functions such as looping of advertisements, duration for which the advertisements is to be displayed etc.

![]({{ 'assets/images/kloudtise-ss2.jpg' | relative_url }})
**Requirnments**

* Software Requirements
1. Eclipse
2. JDK 
3. Openshift
4. Filezilla
5. Omx player


* Hardware Requirements
1. Raspberry pi board
2. Display Monitors
3. Power Source
4. GPS module
