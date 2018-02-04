---
layout: post
title: "Web Development Security, Kali Linux and React VR"
date: 2018-02-04
---


**Some Links, Tips & Thoughts for the day**

**Web Development Security -**
I know that a lot of the time that Web development and in particular Javascript does not seem to put security at the top
of any agenda. I did come across this repository which looks very interesting, it is the JavaScript Web Application Secure 
Coding Practices repository

  https://github.com/Checkmarx/JS-SCP

It can be read online or downloaded from Gitbook in several formats

  https://www.gitbook.com/download/pdf/book/checkmarx/JS-SCP

This is an excellent resource as JavaScript has like every other language a set of quirks and there are few quality
resources dealing with secure and secure development issues.


**Kali Linux -**
Anybody interested in security will know what Kali Linux is, the downloads page is at

  https://www.kali.org/downloads/

I came across a free Kali training course 

  https://www.opentechinfo.com/learn-use-kali-linux/#

A lot of security tutorials seem to be like software development tutorials and go from average to very poor and
completely unhelpful so I am hoping that this one is better. A really excellent resource is located at

  https://www.hackingtutorials.org

I am also a fan of a competitor distro to Kali called Parrot Linux which can be downloaded from

  https://www.parrotsec.org/download.fx

I have used both and find them both to be excellent, which is better? it seems to be only opinions like here

  https://null-byte.wonderhowto.com/forum/kali-vs-parrotos-0170083/
  
why not try them both and decide for yourself.


**ReactVR -**
Virtual Reality and Augmented Reality are subjects that have always fascinated me and in the last few years have gained
traction with the explosive growth of both gaming platforms but also the increased power of mobile devices. I managed to
have a quick look at React VR which is from Facebook too and uses React and React Native syntax so cuts down on some of the
learning time.

To get started you will need to install the ReactVR CLI (globally) using npm. Depending on the OS it may need
elevated user privilege levels

  npm install -g react-vr-cli  


The next step is to generate a project

  react-vr init project_name


Change into the project directory

  cd project_name


The first thing to notice is how similar the structure is to other React platform projects. The main entry point
in this case though is index.vr.js


To start up the project

  npm start


Then open up a web browser window ( I have recently started using Firefox developer edition and is highly recommended)

Navigate to the following url to see the default virtual reality image

  http://localhost:8081/vr/


From this point is the point where you start putting together your own app and as it is built on React Native you will
be able to use a lot of what was learned previously.
  

**Good Reads**
 - https://medium.com/swlh/how-you-can-but-shouldnt-patent-an-app-idea-cf68b1ef4e70
 
 - https://medium.com/swlh/how-technology-quality-issues-can-ruin-careers-and-how-to-prevent-that-part-1-59c8164f31ef
 
 - https://medium.com/coding-artist/learn-react-vr-chapter-8-building-a-vr-video-app-a7ce2dfc4e2f
 
 - https://betterhumans.coach.me/the-complete-guide-to-understanding-and-dealing-with-online-trolls-4a606ae25c2c
 
 - https://moz.com/blog/write-for-seo-2018
 
 - https://mobilemoxie.com/blog/mobile-first-indexing-whole-new-google-voice-first-article-1-3/

 - https://medium.com/swlh/minimum-viable-product-define-the-best-fit-type-method-and-follow-simple-building-stages-3bd0b0d66607 
