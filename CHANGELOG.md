# Change Log
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)

## [1.1.0] - 2019-08-24
```Initial commit```
 -  Fixing
       - Webarchive : remove email contains on list domain.
       - Docker image : add chromium webdriver for webscreenshot.

       
## [1.1.0] - 2019-08-31
 -  Update
       - Filtering list subdomain result more specific - (subdomain.txt)

## [1.1.0] - 2019-10-21
 -  Update
       - DNSDumpster update regex for retrieving csrfMiddlewaretoken values
    
## [1.1.1] - 2020-02-12
 -  Update
       - CRTSH update regex for retrieving subdomain
   
## [1.1.2] - 2020-02-15
 -  Update
       - Added Identify technologies on websites from domain list
       - Fix Some Bug and Issues

## [1.1.3] - 2020-04-03
 - Update
	- Added Plugin IP DB_PORT
	- Explain :
		- Data Collecting/Scraping open port from 3rd party (Default::Shodan), For right now just using Shodan [Future::Censys,Zoomeye] 
		- So we do not perfom active scan, who collect the port ? Third-party sites (Shodan,Zoomeye,Censys) doing that and perfom active scan and then, we just collected the port from their result   
		- More efficient and effective to collecting port from list ip on target [[ Subdomain > IP Resolver > Crawling > ASN & Open Port ]]
		- Here we can further narrow the targeting port for checking in port scanning

		- List ASN From IP List [running auto on db_port::ip_dbasn.txt]


## [1.1.4] - 2020-04-19
 - Update
	- Added Plugin for Extract URL parameter from domain (--extract-params/-ep)
	- Explain :
		- Data Collecting & Scraping URL Parameter from Passive scan (Default::Web Archive) 
		- Regex using DFA Engine (awk,sed)
		- Support and Collecting URL with multi Parameter to Fuzzing
		- Removing Duplicate Parameter & URL
		- Passive_Collecting_URLParamter.txt : This File is original Collecting URL Parameter without Parsing 
	- Fixing Bug in statement Plugin --db-port
