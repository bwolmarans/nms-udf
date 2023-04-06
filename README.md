# Welcome to the ADM UDF Lab.
A note on credential complexity: You'll notice some very simple passwords in this lab.  This is because complex passwords are not going to keep you out of anything if got into UDF, and into the lab, so we're just going to save time for everyone and skip over something that adds complexity without making anything more secure.

## Description of the VMs in this Lab
1. NMS - this is your NMS and ADM management platform. creds are admin/admin
2. WEST-GW - this is one of your NGINX+ and NGINX-AGENT instances
3. EAST-GW - this is another
4. WWW - this is a box of web servers, with one listening on port 80
5. KALI - this is simply a jumpbox. creds are kali/kali.  Access if via RDP, and then do all your work from the jumpbox. This box is more fun and easier than a Windows Jumpbox. Don't worry it has Firefox on it.  Pro Tip: When you download the RDP file, r-click and edit the file and set the resolution to 1920x1080, color depth to 24bit, username to kali, and enable saving username. 

## DNS
The domain used for DNS in this lab is udf.com, but that only exists within this lab.
The DNS server runs on 10.1.1.7, and this is already configured on all the boxes. 

## Lab diagram:
You can see the domain names for each box here:

<img src="https://github.com/bwolmarans/nms-udf/blob/main/images/lab-diagram.png" width="600" title="hover text">

## Your Challenge
In this scenario, PlatOps team has done all the hard work of installing everything for you, now you just need to do some clickops.

There is a Coffee application which lives on the www box.  

The application FQDN is http://www.udf.com

Use ADM to deploy this application on the west gateway.

The udf.com domain lives only within the blueprint

You can use your regular RDP client to RDP to the Kali box to test it, login to kali with kali/kali, then run firefox and browse to the front half of your proxy (gateway)


