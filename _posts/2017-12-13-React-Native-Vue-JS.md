---
layout: post
title: "React Native and Vue JS Stuff"
date: 2017-12-06
---


**Some Links, Tips & Thoughts for the day**

**React Native -**
  It has been a while since I looked in at React Native as it was something that seemed to be aiming for iOS rather
  than my platform of choice Android. I decided to have a look in as I have some concerns about Ionic both from the
  fact of not really liking TypeScript and Angular 2+.
  
  The first step I took was to download and install Android Studio
  
    https://developer.android.com/studio/index.html
    
  
  The next thing that I did was install the React Native CLI (ensure you have Node installed)
    
    $ npm install -g react-native-cli
  
  
  
  Then I installed the latest version of Java (In this case 9)
  
  I decided to stick with the "Official" Oracle version rather than the OpenJDK version
  
    $ sudo add-apt-repository ppa:webupd8team/java
    
    $ sudo apt-get update
    
    $ sudo apt-get install oracle-java9-installer
  
  
  To check that Java is installed
  
    $ java --version
    
    
  After that it was time to configure JAVA_HOME Environment Variable, in my case its
  
    /usr/lib/jvm/java-9-oracle/bin/java 
  
  
  Copy this path and edit the /etc/environment file
    
    $ sudo gedit /etc/environment
    
  Add the following line to the file before saving and exiting
  
    JAVA_HOME="/usr/lib/jvm/java-9-oracle/bin/java"
    
    
  Download and install the Android SDK from within Android Studio, you will then have to add the path to the
  $HOME/.bash_profile file 
    
    export ANDROID_HOME=$HOME/Android/Sdk
    export PATH=$PATH:$ANDROID_HOME/tools
    export PATH=$PATH:$ANDROID_HOME/platform-tools
    
    
  Then you 
    
  
  
  
**Vue -** 
  The last couple of weeks I have been playing with Vue.js on my Cloud9 setup, it is a very clean framework and very
  very quick

    

**Good Reads**
https://thinkgrowth.org/how-to-build-a-saas-platform-3rd-party-developers-will-love-19c139ec8e72

https://medium.com/swlh/how-much-does-it-cost-to-design-an-application-a-comprehensive-guide-to-app-design-7c03e579b38



