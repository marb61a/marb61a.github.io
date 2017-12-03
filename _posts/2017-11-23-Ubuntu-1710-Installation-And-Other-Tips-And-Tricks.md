---
layout: post
title: "Ubuntu 17-10 Intstallation And Other Bits"
date: 2017-11-23
---


**Some Links, Tips & Thoughts for the day**
  I finally decide to give into to the persistent update available notice that Ubuntu 17.04 has been showing me for the
  past few weeks, so I clicked the update now button and set the process in motion.
  
  The process itself was relatively painless and took about an hour from beginning download to reboot so all in all not too
  bad. No OS update or upgrade is ever smooth so I knew that there would be trouble ahead as there would be settings changed
  which would be incovenient. There are some good and bad things about the update
  
  - The screen rotate is enabled unless switched off in the drop-down task bar
    
    
  - Caribou has a bug which means that the virtual keyboard appears everytime I touch the screen on my touchscreen
    laptop which does get annoying after a while.
      
      
  - By far my biggest annoyance is what the OS tells you can be removed, towards the end of the installation the installer
    told me that there were about 200 or so files which were no longer of use and could be removed, I told the installer
    to remove them which is where my frustration comes from as among these files are installation files for PHP7 and             others. This led to some frustration as I could reinstall PHP and MYSQL etc as well as Phpmyadmin but I had a lot of         connection problems due to a missing mbstring. Eventually I managed to find the solution
      
      
          sudo apt-get install libapache2-mod-php7.0
          sudo apt-get install php7.0-mbstring
        
        
    And then restart the apache service using
        
          
          sudo service apache2 restart
        
        
  - Also on the annoyance list is the opening of an unknown icon which is something to do with an OpenGL renderer


  - On the other hand I really like the visual effect of Ubuntu and the user interface has been sharpened up as well as 
    switching the show applications button being moved from top to bottom and the whole menu has had a bit of a revamp. 
  
  On the whole the OS looks good, performs reasonably well and after a few updates hopefully should be a great OS to work
  on as I have a lot of different applications that I use and switch so that sharpness of performance is needed
  
  
  
  **IDE'S and Code Editors**
  I am a big fan of trying out various different IDE and Code Editors, my current development environment which is both
  installations and cloud based are
  
    - Android Studio
    - Monodevelop
    - Eclipse
    - VSCode
    - Sublime
    - Cloud9
    - Stackblitz
  
  I use them all for a variety of projects and each has their own vagaries and idiosyncracies, for instance I am finding
  VSCode to be immensely usable on Ubuntu. Two shortcuts I have been using a lot are
  
      - For open up the cli
          ctrl-~

      - For opening a search box to find plugins
          ctrl-shift-x
  
  
  I also have just install sublime-linter which will do syntax checking as part of its linting process in JS so I am 
  looking forward to trying that out.
  
  
  **Good Reads**
  
    - https://blog.prototypr.io/5-secrets-to-design-an-excellent-ux-designer-resume-and-get-hired-981628826946
    
    - https://medium.com/swlh/i-have-an-idea-for-an-app-now-what-5bfe9e95148f
    
    - https://medium.com/@preethikasireddy/why-im-leaving-silicon-valley-72919edb3297
    
    - https://hackernoon.com/practical-guide-to-saas-security-e6b8b76d50a2
