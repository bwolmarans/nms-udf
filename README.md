# Welcome to the ADM UDF Lab.
=======
Do everything from the jumpbox.  

You are playing the role of the App Delivery Team.
In this role, the only boxes you should ever be logging in to are the Kali jumpbox, and from Kali, you will then login to NMS itself.


Documentation is here: https://adm-release-4-0-0--nms-docs-private.netlify.app/adm/

## Description of the VMs in this Lab
1. NMS - this is your NMS and ADM management platform. creds are shown in the UDF deployment->NMS component->details
2. WEST-GW - this is one of your NGINX+ and NGINX-AGENT instances.
3. EAST-GW - this is another
4. WWW - this is a box of web servers, with one listening on port 80
5. KALI - this is simply a jumpbox. creds are creds are shown in the UDF deployment->Kali component->details.  Access if via RDP, and then do all your work from the jumpbox. This box is faster, smoother, more fun and easier than a Windows Jumpbox. Don't worry it has Firefox on it.  Pro Tip: When you download the RDP file, r-click and edit the file and set the resolution to 1920x1080, color depth to 24bit, username to kali, and enable saving username. Use Ctrl-Shift-V to paste. 

## DNS - READ THIS PART
The domain used for DNS in this lab is bigtechdojo.com, but that only exists within this lab, with a private (dynamic) DNS server that runs on one of the machines, and DNS resolution is already configured on all the boxes. This is a legit domain in the real world which the lab creators own purely to avoid any potential domain conflicts. 

## Lab diagram:
You can see the domain names for each box here:

<img src="https://github.com/bwolmarans/nms-udf/blob/main/images/lab.png" width="800" title="hover text">

## Your Challenge
In this scenario, PlatOps team has done all the hard work of installing everything for you, now you just need to do some clickops.

There is a Coffee application which lives on the www box.  

The application FQDN is http://www.bigtechdojo.com (don't click on this, but if you do, I've put guardrails in place)
It is also available, with proper SSL certs, on https://www.bigtechdojo.com.
There are also 4 instances of juiceshop running on 3000,3001,3002,and 3003 (cleartext) so for bonus points, get those working as well.

### Your Task
Use ADM to deploy this application using end-to-end SSL encryption on the west gateway. That's it. A one sentence task, you figure it out. You'll know you have succeeded when you can fire up firefox in your Kali jumpbox and browse to the front half of the proxy, and see the application web site being proxied all the way through. Without any Cert warnings, the SSL has to work without any warnings in the browser.

You can find the certs and keys that you will need for the West and East Gateways in the Kali user home directory on the jumpbox, all in one file named certs.txt, so open a terminal to see those, and with some judicious copy and pasting you can add them via the ADM UI. These are real LE certs. Try to experiment to see if you need the fullchain, cert, and key or just the cert and key.

