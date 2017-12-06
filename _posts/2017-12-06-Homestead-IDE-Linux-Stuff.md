---
layout: post
title: "Homestead, IDE's and Linux Stuff"
date: 2017-12-06
---


**Some Links, Tips & Thoughts for the day**

**Laravel**
  I decided to give Homestead a whirl for my Laravel experiments. For the uninitiated Homestead is a pre-packaged Vagrant
  box. It runs on any OS and most virtual machine software in my case as I am running Ubuntu I installed Virtual Box.
    
    1 - Install VirtualBox on Ubuntu (from the terminal)
      
            sudo apt-get update
            sudo apt-get install virtualbox-5.2

        
        !!! You may need to do some preliminary work prior to these commands
        
        Setup an apt repository(In this case Ubuntu 17.04) by editing/etc/apt/sources.list file and adding the following
        
        
            deb http://download.virtualbox.org/virtualbox/debian zesty contrib
        
        
        Import the Virtualbox package sign key
        
        
            wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
            wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
    
    
    2 - Install Vagrant on the system
    
        
            sudo apt-get install vagrant
    
    
    3 - Install Homestead on the system
    
    
            vagrant box add laravel/homestead
          
    
    4 - Setup Homestead on the system by cloning the GitHub repo into a Homestead directory
    
         
          git clone https://github.com/laravel/homestead.git ~/Homestead
    
    
    5 - Configure the Homestead.yaml file, in order to generate these files you have to run
    
          cd Homestead
          
          bash init.sh
    
        
        You can configure this file with IP address, CPU's, Memory etc
    
    
    6 - The next thing to configure is Folder Mapping which will allow you to code on your local machine but 
    serve them on Homestead. To do this you will set the folders directive in the Homestead.yaml file like below
    
        folders:
          - map: ~/directory_name
            to: /home/vagrant/directory_name
    
    
    7 - Setup Composer
    
    
        sudo composer global require "laravel/installer"
    
    
    8 - Start a new Laravel project
    
        laravel new project_name
    
    
    9 - Fire up the Vagrant box
    
        vagrant up
    
  This was pretty much the process that I followed with a few extra bits
    - I was able to boot the vagrant box up directly from Virtual Box right to the command line, this asks for a password
    and login, in both cases the word vagrant got everything up and running smoothly
    
    - You can have a folder mapping scheme that has one for each project or one for all projects, the former is apparently
    the preferred methodology
    
    - In order to have a specific domain eg example.dev you will have to edit the /etc/hosts file and add an entry which
    points to the virtual machine address for example
    
        sudo gedit /etc/hosts
     
    Then add
    
        192.168.10.10
   
   
   After that I was running smoothly, I think it is a lengthy enough process but I do think that it is probably only
   because it was the first time and if I need that machine to be portable then putting in an extra few moments at the
   start could have huge benefits. 
  
  
**Linux -** 
  I really do enjoy using Linux far more than I have ever done on Windows. I have a Windows OS at all times since the days
  of Windows 3.11 and Linux since 2004, I had Warty Warthog from Ubuntu running as well as Slackware and Mandriva all of 
  which I loved using.
  
 
 **IDE's -**
  I seem to be accumulating a great many IDE's and Code Editors on my system of late, I have installed
  
    Android Studio - For Android, React Native & PWA apps
    
    Netbeans - For Wordpress development
    
    Sublime & Visual Studio Code - For Web and other development
    
    MonoDevelop - For experimenting with C# on Linux and Xamarin for Android
    
  
  This is without the Cloud9, JSBin, Plunkr and StackBlitz accounts I have. I enjoy the idiosyncracies of each
  but I do wonder about whether there is a magic tool that would let me use all in one or maybe I just like being able
  to switch back and forth.
    

**Good Reads**
  - https://thinkgrowth.org/building-tools-can-provide-better-roi-than-blogging-ec87e304c47d
  
  - https://medium.com/personal-growth/self-improvement-has-made-me-worse-a4cc23e93e7a
  
  - https://medium.com/dev-channel/a-pinterest-progressive-web-app-performance-case-study-3bd6ed2e6154
  
  - https://codeburst.io/the-2-types-of-software-engineering-interviews-and-how-to-prepare-for-them-2e7bd4daa0b
