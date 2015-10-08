# Animus Threat Data Repository
## Summary

This is a centralized repository for threat data collected by the Animus threat intelligence system. This repository contains reports generated by the Animus system on a daily basis. Additionally, this repository contains a set of
master files which include all data collected historically by the honeypot sensors distributed around the Internet.  

Currently, Animus threat reports only contain data on SSH threat actors and tactics. Other methods and vulnerabilities are currently being developed.  

## Stats

The following are some numbers surrounding Animus activity to date. These stats were last updated on October 08, 2015. All activity 
is fully automated.
* Attacker IP addresses collected: 27892
* Total SSH attempts observed: 36695846
* Unique malware samples captured: 1814
* Malicious domains identified: 504
* Unique passwords collected from sensors: 886064
* Unique usernames collected from sensors: 38542
* SSH library versions observed from SSH bruteforce tools: 210

## Features

Current version: ```0.1.1``` - Added malware URLs to Animus Threat Report  

##### Attacker IP address threat feed

Animus publishes daily reports containing attacker IP addresses which can be preemptively blocked in your environment  

##### Malware Artifact Reporting

Animus threat reports include a list of all URLs attackers attempted to download malware from.  

##### C2 Mass Scan

Animus mass scans the Internet once per week to locate known-malicious command and control servers which can serve as indicators of compromise (IOCs).  

##### DDOS Target Tracking

Once Animus discovers a C2 server using software it knows how to communicate with, it will connect to the C2 server and begin logging distributed denial-of-service target IP addresses. This allows Animus to track who different
adversary groups are targeting with denial-of-service attacks in real time.  

##### Threatbot

Animus collects all data in a centralized repository. This repository can be queried on a per-IP basis via a Twitter bot, [@threatbot](https://twitter.com/threatbot).  

Threatbot will parse one or more IP addresses in a tweet, query the Animus database, and response back with a summarized report of that IP address. This report includes first sighting of attacks from the IP address and most recent 
attacks from this IP address.  

Threatbot will tweet once per day with a link to the daily Animus threat report. This tweet will include the total number of attacks received, as well as the most aggresive attacker IP address of the day. 

Threatbot also will tweet once per day with a summary of malware URLs captured

#### TODO

Animus will be expanding the threat reports to include data on the following threats:
* Shellshock
* Heartbleed
* Wordpress attacks

## Version History

Current: ```0.1.1```  

* 0.1.1 - Added malware URLs to Animus Threat Report
* 0.1.0 - Initial version, publish reports on SSH attacker IP addresses and surrounding metadata.

## Contact

If you have any questions or feedback about the Animus threat intelligence system, don't hesitate to reach out to the main developer via [email](mailto:andrew@morris.guru) or [Twitter](https://twitter.com/andrew___morris).  

### License

All rights reserved by Andrew Morris under Creative Commons Non-Commercial 4.0 license, 2014-2015.  
Contact me if you'd like to use this data for commercial purposes.  
