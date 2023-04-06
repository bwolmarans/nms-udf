# Welcome to the ADM UDF Lab.

## Description of the VMs in this Lab
1. NMS - this is your NMS and ADM management platform
2. WEST-GW - this is one of your NGINX+ and NGINX-AGENT instances
3. EAST-GW - this is another
4. WWW - this is a box of web servers, with one listening on port 80

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


