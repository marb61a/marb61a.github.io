---
layout: post
title: "GNS3, Fedora and Python"
date: 2018-01-26
---


**Some Links, Tips & Thoughts for the day**

**GNS3 -**
I finally got around to installing GNS3 on my computer. This will help me a great deal with setting up my training
laboratory for both security related material but also for development projects. The procedure for installing on my Ubuntu
17.10 system is very straight forward 

- Start an elevated privilige session
  
  - sudo -s

- Add the repository

  - add-apt-repository ppa:gns3/unstable

- Do perform a system update

    - sudo apt-get update

- Install the GUi application

    - apt-get install gns3-gui

- To run simply the following at a command prompt

  - gns3

This will start up a server and then you can add some projects. To download preconfigured images visit

  - https://www.gns3.com/marketplace/appliances



**Fedora -**
It has been a while since I used the Fedora version of Linux. I have been looking at some IPTables stuff which seems to be 
getting phased out (at least being eased out) with Firewalld being the newer and apparently better application. There were
a few things that caught my eye but most strikingly I found out Yum has apparently already gone in favour of the dnf package 
manager.

More about the application is available here

- https://fedoraproject.org/wiki/DNF?rd=Dnf

I was installing Firewalld which went as follows

- Start an elevated privilige session
  
  - sudo -s

- Use dnf to install the firewalld package

  - dnf install firewalld

- The firewall-config utility is needed but is not installed by default

  - dnf install firewall-config

- The Firewalld utility comes with some default zones installed by default, to check these

  - firewall-cmd --get-zones

- To run the firewall-config gui utility, at the command prompt type

  - firewall-config

From this point the configuration will depend on the network. In subsequent articles there will be tutorials on the best
way to configure the various firewall zones.


**Python -**
I have not being doing much with Python of late as I have been concentrating on JS and Java but it still remains my favourite
language. I am learning some proper in-depth security material such as exploit development and the language of choice is of
course Python. I have done several projects with Django but it did not work for me, I did like Flask for web development and
it played very well with the MeteorJS framework but I think that Python will remain a niche player in the Web and Mobile
development arenas which is a shame.

I do think that Python has an amazing future though in areas such as 
- Security Tools such as Firewalld metioned above

- Other Tools such as ScaPy 

- AI & Machine Learning

- Big Data

These are huge growth areas which means that any time spent learning Python is potentially very rewarding and is sure 
to keep growing over the coming years.

  

**Good Reads**
 - https://medium.com/dailyjs/how-to-use-javascript-proxies-for-fun-and-profit-365579d4a9f8
 
 - https://blog.prototypr.io/why-you-need-to-learn-the-difference-between-urgency-and-importance-bc9ae4d8612e
 
 - https://medium.freecodecamp.org/js-type-coercion-explained-27ba3d9a2839
 
 - https://medium.com/swlh/the-ultimate-guide-to-chatbots-for-lead-generation-7dac67f8296b
 
 - https://proandroiddev.com/building-an-autocompleting-edittext-using-rxjava-f69c5c3f5a40
 
 - https://medium.com/dailyjs/react-and-visual-automata-based-programming-c1d13e153cde
 
 


