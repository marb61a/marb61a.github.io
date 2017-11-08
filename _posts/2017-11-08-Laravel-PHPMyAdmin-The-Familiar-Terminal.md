---
layout: post
title: "Laravel, PHPMyAdmin"
date: 2017-11-08
---


**Some Links, Tips & Thoughts for the day**
**Laravel**
  I had originally decided to install and tryout Laravel on my Cloud9 account but I decided to take the plunge on
  my Ubuntu system. I will stick with my Linux systems installation (Ubuntu & Mint) and will leave Windows 10 well
  enough alone. The installation of laravel itself was really quick, there are a few different installation options
  
    - Install Composer & PHP and then install Laravel, creating a project is then just a matter of a couple of commands
        
        - composer create-project --prefer-dist laravel/laravel project-name "5.4.*" 
          - This creates a project using the Laravel 5.4 version
        
        - php artisan serve 
          - This will run the project on http://localhost:8000
          - This will need to be added to your path or you will have to go into the project folder each time
    
    
    - Homestead
      - Basically a prebuilt VM to avoid the installation of multiple software apps and dependencies on your system
      - https://laravel.com/docs/5.5/homestead
      - Because the project is based on Vagrant, it will be immensely portable and should be easier to manage.
      
    - Laragon
      - Another project similar to Homestead but a bit more lightweight
      - https://laragon.org
      - I have not had the chance to use this but plan to very quickly as it is getting very good reviews 


  
  **PHPMYADMIN**
  After getting my Laravel setup and running far too smoothly it was the turn of PHPMyAdmin to cause an issue and it did not
  disappoint, after the installation of the application there was no connection so I went back to basics
      
        Install the needed software            - sudo apt-get install apache2 php mysql-server
        Install the phpmyadmin apackage        - sudo apt-get install phpmyadmin
 
 
  Normally you will accept Apache2 and dbconfig-common during the installation process, unfortunately this is where
  things started to cause an issue, there was no connection to the localhost url. I decided to tackle it by doing
  a few basics
      
        sudo apt-get purge phpmyadmin*         
        - This resets and there is no space between the n and the asterisk
 
 
  This did not have the desired effect so I tried this 
  
        sudo gedit /etc/apache2/apache2.conf    
        - Needs elevated permissions to edit this file
        
        Include /etc/phpmyadmin/apache.conf     
        - Added at file's end 
        
        /etc/init.d/apache2 restart             
        - To restart your Apache server, have root password handy
 
 
  Again no dice but then a single command helped
      
      
      sudo dpkg-reconfigure phpmyadmin          - You will be given an option to get rid of existing stuff, getting rid
                                                  of it worked for me.


  Once again command line 1 gui based tools 0 when it comes to clearing up isues
  

**Good Reads**
  - https://medium.com/@mikeal/modern-modules-d99b6867b8f1
  - https://medium.freecodecamp.org/scaling-node-js-applications-8492bd8afadc
  - https://blog.risingstack.com/measuring-http-timings-node-js/
  - https://www.twilio.com/blog/2017/10/chat-interfaces-react-javascript.html
  - https://hackernoon.com/a-crash-course-on-serverless-with-node-js-632b37d58b44
  - https://nodesource.com/blog/how-massive-companies-use-node-js-at-scale
