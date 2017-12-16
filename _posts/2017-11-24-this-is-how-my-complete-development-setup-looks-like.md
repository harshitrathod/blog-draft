---
title: This is how my complete development setup looks like
date: 2017-11-24T18:03:19+00:00
author: Harshit Rathod
layout: post
feature-img: "assets/img/my-dev-setup/IMG_20171124_155729-01.jpeg"
---
It's been almost 2 years since my Professional career started. In these years, I always have some struggle to decide stable development setup which works for me. I went through many blogs to decide stable setup but didn't work for me. The main reason for this is my custom workflow. I have my preferences which may not work for others. This post will give some clarification of tools which are on my laptop.

### Operating System (OS)

There is no doubt about OS which is currently on my laptop. It's Linux. Linux will never disappoint any developer. I started programming on the windows machine. With time when stuff gets complex and windows didn't sustain. I was spending more time to solve windows problem rather than my actual problem. The amount of my productivity eaten by windows machine is so high that I finally decided to format my laptop and Installed Linux

{: .center}
![windows vs mac vs Linux]({{ "/assets/img/my-dev-setup/image1.jpg" }})

One can argue about which flavor is better than other. One can choose CentOs over Ubuntu or Fedora on their preference. I used Ubuntu only and since then didn't face any situation to change. The biggest benefit of Ubuntu is their support. There is a huge community out there to support any of your system problems.

### Browser

There are two browsers on my laptop, [Chromium](https://www.chromium.org/) and [Firefox.](https://www.mozilla.org/en-US/firefox/) I am using Chromium because of the interface which I am using for many years. I know most of the shortcut keys on Chromium which increase my productivity. Chrome web store has many good plugins which I am using for a long time. I only open Firefox to test UI because the project on which I am working support these two browsers. 

#### Pinned tab vs Bookmarks

I have many websites which are used frequently in my day to day life. I prefer to have pinned tab over bookmarks because

  * You can access these sites by chrome tab shortcut keys ( Ctrl + 'tab number' ) rather than opening it from bookmarks
  * If there is any notification, you can see from tab header. In bookmarks, you can't know about notification until opening it

{: .center}
![Pinned tab]({{ "/assets/img/my-dev-setup/image2.png" }})

I have following websites in my tab list

  * LinkedIn
  * Twitter
  * Gmail
  * Evernote
  * Stack overflow
  * Google Calander
  * WordPress Dashboard of this site

### **Terminal**

#### [Terminator](https://apps.ubuntu.com/cat/applications/quantal/terminator/)

First thing I do when I start my laptop is open terminal. I have a habit of opening any tool from command line even though it is in my sidebar. I use [Terminator](https://apps.ubuntu.com/cat/applications/quantal/terminator/) instead of default terminal. The main reason to use Terminator is you can open many terminals in one window. Also, it is providing many shortcuts to switch between tabs. Most of the time I am on terminal debugging server by logs. By having many terminals I can run the command in one and watch for logs in other.

#### [Oh My ZSH!](http://ohmyz.sh/)

Sometimes it is frustrating to write entire command to default bash. This open source project will provide you many functions and plugin which you can use to increase your productivity. As far as I know, this contains aliases and wrapper function of all command which I use in day to day life. If you don't find command in this you can also create your own aliases and function. Next time onward rather than typing entire command you can call aliases or a function.

  * You can install ZSH by following [this steps](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH)
  * [List of ZSH plugins](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins)
      * I am using following plugins
      * plugins=(git history mvn lol last-working-dir jira common-aliases vagrant zsh-autosuggestions)
  * [Enable ZSH in your Terminator](https://askubuntu.com/questions/253812/change-default-shell-for-terminator)

My Custom Aliases:

{% highlight sh %}
# Git Push current branch and create remote branch
alias gpn='git push -u origin $(git branch | grep \* | cut -d '\'' '\'' -f2)'
#Force push current branch
alias gpf='git push -f origin $(git branch | grep \* | cut -d '\'' '\'' -f2)'
# Git push current branch
alias gpc='git push origin $(git branch | grep \* | cut -d '\'' '\'' -f2)'
{% endhighlight %}

I am using this extra 3 aliases for Git. By doing this I did not need to write entire command again and again. [Please refer this to set aliases in zsh](https://askubuntu.com/questions/31216/setting-up-aliases-in-zsh)

### Vagrant

2 years ago when I needed to install Oracle and MySQL on my laptop. It took me 2 days to just install this two stuff. After doing all this I found out that I installed an older version of MySQL. While removing MySQL, I had done something wrong that I am not able to install new MySQL. This should not be acceptable. Then I spend the entire weekend to find the alternative solution to this problem. I need a solution that is quick and doesn't screw my laptop. This is How I found **[Vagrant](https://www.vagrantup.com/). **It took only 2 hours to install both databases on my laptop. with vagrant, I can remove or add stuff without changing anything on my Host machine.

### IntelliJ

IDE is a weapon to any developer without it, you can not survive. One can write a simple program in notepad without IDE but when we talk about large-scale application, IDE is key for fast delivery. When someone solving a bug or adding new feature in project having hundreds of files, One can not succeed with simple notepad

{: .center}
![Life without IDE]({{ "/assets/img/my-dev-setup/612022.png" }})

From last 2 years, I am using IntelliJ IDEA. I am so happy with it that I didn't try any other IDE. I don't have a comparison of IDEA with other IDE but after using it so long I know shortcuts for all the action which frequently occur in developer's life. I can code in many languages without changing IDE every time. I have modified default setting according to my need which I will share in a future post.

With this post, I tried to share my experience and difficulty which I faced while coding. I also tried to find a solution to these problems. Something might be done differently to get a better result and I am happy to try new things.
