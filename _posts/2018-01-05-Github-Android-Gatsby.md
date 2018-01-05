---
layout: post
title: "Github, Android and Gatsby "
date: 2018-01-05
---


**Some Links, Tips & Thoughts for the day**

**Github -**
  I am a big fan of Git and in particular Github, I have also used Bitbucket but was not that enthused by it for some
  reason, I think that it was the UI that I did not like but the Github UI despite being plain is very easy to navigate
  through and that is the only real difference I can see. 
  
  Every so often though Git throws you an issue which will cause you to scratch your head. This time it was when I was
  setting up a repository for a small Spring 5 project this time though when I ran
  
    $ git status
  
  I got a rather disconcerting error, disconcerting because it was a new one on me, it was 
  
    $ git head points to an unborn branch (master)
  
  I thought that this might be an error from initialising a repo using the Spring Tool Suite. To check to see if the HEAD
  which must exist in a repo is damaged or non-existent
  
    git rev-parse HEAD --
    
  I discovered that the folders where I had cloned a repo and then setup in STS had been different which caused the issue
  so rather than mess about with many different ideas I decided to remove the exsting origin and start again which is very
  straight forward to do
  
    git remote rm origin
    
  Sometimes stepping back is the best and most productive thing to do.
  
  
**Android -** 
  I have been getting back into Android and have managed to get everything up and running, I got the Genymotion plugin
  working, unfortunately I ran into a problem at building time. I was getting a java.nio.file.accessdeniedexception error.
  Then it became an IDE error where I was getting a Unable to read anonymization settings error related to Analytics.
  I had a look at a few different solutions but as it turned out using some folders on Ubuntu requires a change to 
  default priviliges as the IDE will need read and write access to folders. A very simple command worked
  
  
    $ sudo chmod 777 /home/folder_owner/.android
  
  
  This command worked to take care of both errors and the app was built and running on the emulator very quickly. I am
  still amazed at how good the Genymotion emulator is 4 years after I first tried it, I think it compares very well to
  anything Microsoft or Mac users have, now I just have to get React Native apps running properly on it :)


**Gatsby -**
  I have been reading about Gatsby for a while, its site is at
  
    https://www.gatsbyjs.org
  
  It is a React based static site generator and supports all the usual components eg Webpack, I decided to check out the
  CMS on a free version of Netlify
  
    https://app.netlify.com
  
  This comes with login from Github, Bitbucket and Gitlab and upon registration will generate a repository in your account
  this comes with a lot of stuff built in including continuous integration and deployment as simple as found on Heroku.
  I have only begun to use it and will investigate much more about how it performs with adding content.
  

**Good Reads**
 - https://medium.freecodecamp.org/inspirational-success-stories-from-self-taught-web-developers-4f6f375cf17d
 
 - https://medium.com/swlh/how-you-can-quickly-become-a-genius-and-why-most-people-arent-e01cc912abd9
 
 - https://medium.com/swlh/the-only-3-ways-to-reinvent-yourself-in-2018-a0a064d79235
 
 - https://hackernoon.com/the-top-javascript-trends-to-watch-in-2018-a8437dd94425


