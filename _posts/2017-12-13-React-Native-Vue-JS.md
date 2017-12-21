---
layout: post
title: "React Native and Vue JS Stuff"
date: 2017-12-13
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
    
    
  Then you can generate the profile using
    
    $ react-native init project
  
  
  To run the app you will do the following
    
    $ cd project
    
    $ react-native run-android.
  
  
  You can then import this project into Android Studio using the import existing project feature when
  the application starts up.
  
  I tend not to use the built in emulators that are built into Android Studio, I have been using Genymotion
  for a few years now and it has a fantastic free version available.
  
  - https://www.genymotion.com
 
  You will need to register and download the package, this comes as a .bin file so to install is
    
    $ sudo chmod +x genymotionfile.bin
    
    $ ./genymotionfile.bin
  
  
  Once the app starts up you have to register to download devices but they are very fast, the fastest that I have used.
  
  This is as far as I have gotten at this point as I am building a sample CRM app with React Native to see how it goes.
  
  
**Vue -** 
  The last couple of weeks I have been playing with Vue.js on my Cloud9 setup, it is a very clean framework and very
  very quick. There are only a few steps to getting a sample app upp and running
  
  To install the vue-cli package
  
     npm install -g vue-cli
  
  
  To then generate a project
  
    vue init webpack-simple
  
  
  Then change to the project directory
  
    cd project
  
  
  Then add the following line to the webpack.config.js file under devServer, this will differ for each user
    
    public: "https://c9.container.name"
  
  
  I also added the following to avoid header mismatch errors, again under devServer
    
    historyApiFallback: true
    
    
  In package.json add the following under scripts
  
    dev“: “cross-env NODE_ENV=development webpack-dev-server --open --inline --hot --host $IP --port $PORT”
  
  
  To run the project
  
    npm run dev
    
  
  This if working correctly will generate a link which will open a new tab with your running app and then 
  you can begin building your project with Vue.
    
    
    

**Good Reads**
https://thinkgrowth.org/how-to-build-a-saas-platform-3rd-party-developers-will-love-19c139ec8e72

https://medium.com/swlh/how-much-does-it-cost-to-design-an-application-a-comprehensive-guide-to-app-design-7c03e579b38

https://medium.com/swlh/8-reasons-most-people-arent-successful-and-8-ways-to-ensure-you-ll-succeed-7e8be17e5187

https://blog.prototypr.io/how-to-collaborate-on-design-with-developers-8aac41991194

https://medium.com/swlh/explaining-blockchain-with-coconuts-and-pineapples-e44edcbe2e0f
