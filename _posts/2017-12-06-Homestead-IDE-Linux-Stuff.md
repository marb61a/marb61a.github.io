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
        
        Setup an apt repository(In this case Ubuntu 17.04) by editing/etc/apt/sources.list file and adding the following line
        
        
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
    
    
    7 -
    
 
 
  
**Linux** 
  I really do enjoy using Linux far more than I have ever done on Windows. I have a Windows OS at all times since the days
  of Windows 3.11 and Linux since 2004, I had Warty Warthog from Ubuntu running as well as Slackware and Mandriva all of 
  which I loved using.
  
  I have been reading through some old notes on security challenges and capture the flag wargames and some commands I
  think I could certainly make more use of now including the z commands. Essentially the z flag is added to commands to
  enable working with compressed files without having to go through the whole extraction procedure
  
    Zcat
    
      zcat filename.gz  
 
 
 **IDE's**
  I seem to be accumulating a great many IDE's and Code Editors on my system of late, I have installed
  
    Android Studio - For Android, React Native & PWA apps
    
    Netbeans - For Wordpress development
    
    Sublime & Visual Studio Code - For Web and other development
    
    MonoDevelop - For experimenting with C# on Linux and Xamarin for Android
    
  
  This is without the Cloud9, JSBin, Plunkr and StackBlitz accounts I have. I enjoy the idiosyncracies of each
  but I do wonder about whether there is a magic tool that would let me use all in one or maybe I just like being able
  to switch back and forth.
    

**Good Reads**
  - 
