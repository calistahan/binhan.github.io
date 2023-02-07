---
title: "Open Source Intelligence"
layout: post
date: 2022-10-08
feature_image: images/open_source.jpg
tags: [cyberskyline, osint, basics]
---

Open Source Intelligence is the act of finding and gathering information from public sources on a target. You'll probably be surprised by the amount of information that can be found online with a bit of prodding! OSINT is great because it's typically not very expensive and and can reveal a lot of information about a target. Even something as simple as checking a company's posted job requirements for an open position can reveal what technologies and systems they use, which can help in finding a vulnerability. Something to watch out for, however, is fake information that may be posted.

<!--more-->

Some OSINT strategies:
- [**Google Dorking**](#google-dorking) - *a method of fine-tuning Google searches through advanced query searches*
- [**Metadata**](#metadata) - *looking at data about the data*
- [**Reverse Image Searching**](#reverse-image-searching) - *searching an image against online databases*
- [**Repositories**](#osint-common-tools) - *online code repositories*
- [**Internet Archive**](#osint-common-tools) - *a digital library of the Internet*
- [**Profiles**](#osint-common-tools) - *looking up information about people*

### Google Dorking
Google dorking, also called Google Hacking, is a method of fine-tuning Google searches thorugh advanced query searches in order to filter out fluff. Here are some common commands: 

##### Intext & allintext
```
Intext:usernames
allintext:"username" "password"
```
This command finds specific text. <span style = "color:aqua;">allintext</span> is used to search multiple keywords. 

##### Intitle & allintitle
```
intitle:"snapchat"
allintitle:"ip camera" "dvr"
```
This command filters results based off their HTML page title. 

##### Inurl & allinurl
```
inurl:capitalone
allinurl:
```
This filters results based off the URL.
<br>! Live cameras that aren't IP address access restricted can be found by searching 
<span style = "color:blue;">inurl:"view.shtml" "Network Camera"</span>
<br>! Zoom Bombs was a huge problem when the COVID-19 pandemic first hit, where users would go into random rooms (usually classrooms) 
and flood them with profanity, trash, etc. This search query can be used: 
<span style = "color:blue;">inurl: zoom.us/j intext: scheduled for</span>
It should be noted, however, that the FBI put out a public warning regarding zoom bombing! Don't do it.

##### Filetype 
```
filetype:log
filetype:txt
```
This command filters files by their filetype. An easy way to find email lists would be to search <span style = "color:blue;">filetype:
txt inurl:"email.txt"</span> or <span style = "color:blue;">Site: .com filetype: csv inurl: email.csv</span>

##### Ext
```
site: https://rit.edu ext:pdf
```
The extension command is similar to filetype and allows users to narrow down searches to a specific extension type. 

##### Site
```
site: https://rit.edu
```
The site command allows users to narrow down searches to a specific website.


In addition, commands can be combined. 

For example, this command searches for "admin_password" in all three types TXT, LOG, and CFG: 
```
"admin_password" ext:txt |ext:log | ext:cfg
```
<br>
### Metadata
Metadata is essentially data about data. It's information that gives additional information about a file such as the author, date created, GPS coordinates, phone model, etc. Metadata can be found in most file types and can be viewed using a third party program, viewing properties from file manager, or the *strings* command in Linux.
<br>
### Reverse Image Searching
Ever had an image file and wanted to know where it's from, what exactly it is, or find similar ones? I know I have. You can perform a reverse image search where your image will be searched against online databases to find similar ones. [Google Images](images.google.com) supports reverse image searching.
<br>
### OSINT: Common Tools
Open source intelligence has many common tools that are helpful. Here's a consolidated list from [Cyber Skyline Live - Open Source Intelligence Basics](https://youtu.be/PfUiZQD_PLU):
- [exif.regex.info](exif.regex.info) - a third-party metadata viewer
- [images.google.com](images.google.com) - reverse image searching
- [github.com](github.com) - code repository
- [shodan.io](shodan.io) - search engine for web services
- [greynoise.io](greynoise.io) - IP reputation search
- [maxmind.com](maxmind.com) - GeoIP lookup
- [web.archive.org](web.archive.org) - Internet archive
