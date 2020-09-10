---
layout: post
title:  "Choosing a Linux Distribution (Distro)"
author: aakash
categories: [ Blog ]
tags: [ Linux ]
image: assets/images/tux.png
---

Barry Schwartz in his book, [The Paradox of Choice](https://amzn.to/33uNZcT), mentioned *(very wisely indeed)* that : 
> Learning to choose is hard. Learning to choose well is harder. And learning to choose well in a world of unlimited possibilities is harder still, perhaps too hard.

This is one of the biggest problems that users venturing into the free software landscape face almost immediately. Without the lock-in of proprietary software and decisions made by monetary or strategic reasons, developers are free to create whatever they wish to create. In spirit, this is an extremely liberating and empowering thought. In practice, however, it turns out to be quite restrictive and debilitating. This is, however, quite an extended discussion and is covered well by [this post](../confusion-by-choice) of mine. 

Skipping over to the main topic of discussion, let's have a talk about the vast universe of Linux Distributions that leave us spoilt for choice. It can get a bit daunting when it comes to choosing one of these excellent options but, with the right approach, one can make an informed decision quite easily. Let's begin, shall we?

## What Makes A Distro Special?
All Linux distros, at their core, run the Linux Kernel *(duh)* and so share a lot of common features. However, there are a few distinguishing features that make a distro unique. These are : **Package Management Systems**, **User Experience Defaults**, **Base Distribution** and **Release Frequency**. Let's have a look into each of these three in detail. 

#### Package Management Systems
Most Linux users would have used a package manager, knowingly or unknowingly. Package managers allow you to install, modify, or remove packages (programs, command line tools, etc) and repositories (which eventually host these packages). I will name a few and my comments on them if I have used them. I shall not be listing the standard copy paste that is present on third-grade blogs as a means to increase their article length and ad clicks. Now, a few of the most popular package managers on various distros include :
* **apt** : Advanced Packing Tool (APT) is one of the most used package managers in the Linux universe. It gets this position from being the package manager of Debian and its derivatives, especially Ubuntu. It has also become quite popular in the more geeky circles of pop culture and you will frequently hear it being called out in universities. Personally, I have never been impressed with it. Things like requiring two steps for updates, no easy way to revert group installed packages, and extremely risky autoremoval of unused dependencies makes it really unattractive for me. However, it powers millions of servers and computers so should be good enough, I guess.
* **dnf** : Dandified yum, as can be clear from the name, is an upgraded package manager replacing the ```yum``` package manager. This is once again very frequently used because it ships with RedHat, SUSE and RedHat based systems. This is the package manager I have used for the longest time and although its Tab-autocompletion could be made faster, it is extremely solid everywhere else. Finding packages in all your repositories, undoing any ```dnf``` command from your history of ```dnf``` commands, and sensible autoremove of unused dependencies make it far for reliable and convenient for me as compared to ```apt```. It also has built in quick aliases so updates are as simple as ```sudo dnf -y up```.
* **pacman** : Now, this is one package manager I have never used simply becaused I could not be bothered with Arch and its derivatives. From what I hear, though, it is quite fast and powerful but has quite a complicated instruction manual and so isn't the easiest or the most convenient thing to use. Fortunately, a lot of alternative frontends like ```yay``` exist for ```pacman``` which make life easy while still having the power of ```pacman```.  
* **zypper** : This is one powerful package manager, especially because of its amazing integration with YaST *(one of the most distinguishing features of openSUSE)* and RPMs as well. It does everything that the other package managers do with similar fast performance but with the added bonuses mentioned above. No personal comments because I have not personally used it. 

*Niche Package Managers (pun intended, npm?) are sure to exist but in the spirit of having a civil discussion, let us limit ourselves to the Big 4.*

#### User Experience Defaults
Apart from the software availability, which is mostly dependent on the other two aspects, user experience defaults are what give a distro its unique look and feel. This includes things like -
* What should the UI look like? What Desktop Environment to use? What customizations to the default Desktop Environment need to be done? Should it have a dock, a panel or what? *(I'll have a post on Desktop Environments [here soon]())*
* What drivers to include by default? What hardware to support?
* What should the power management settings be like? 

Things like these have immense impact on the choice of our Linux distro. For example, a distro with outdated drivers would not work with our brand new hardware and thus be practically useless. This is especially important for gamers and laptops as they often need the latest features by default. *It should be important to mention, though, that drivers are more dependent on the Linux kernel version than just the distro. It, however, remains the distro's choice of what version of the Linux kernel to package.* Manjaro is perferred by gamers because they always have the latest kernel and so have the best compatibility for the newest hardware. 

Fedora, for example, has amazing power management buil-in and so I find it to be great for laptops. Even PopOS has this sorted out very well. Ubuntu, however, does not and unless you install power management tools manually and configure them correctly, you will have worse battery life than other distros *(or Windows)*. 

#### Base Distribution
There are three major families in the universe of Linux distros. They form the basis for installation format, package manager, software repositories and features. These families are - 
* **The Debian Family :** This consists of Debian and its derivatives. They use ```apt``` as their package manager and support the installation of ```deb``` executables. The Debian repository is one of the largest and most Linux software can be found within it. If something isn't in the Debian repositories, one may always find the software in Ubuntu's repositories. The app ecosystem is pretty rich.
    * Famous distros : Debian, Ubuntu, Linux Mint, elementaryOS, PopOS
* **The RedHat Family :** This consists of RedHat and its derivatives. They use ```dnf``` as their package manager and support the installation of ```rpm``` executables. Thanks to the high usage of RedHat and centOS in enterprise, they have a large collection of software in their repositories (on par with the Debian family). Some specialised engineering tools would also be exclusive to the RedHat family because of their wide usage in enterprise. 
    * Famous distros : Fedora, RedHat Enterprise Linux, centOS, openSUSE
* **The Arch Family :** This consists of Arch and its derivatives. They use ```pacman``` as their package manager and most software is installed from the **Arch User Repository (AUR)**, which consists of a huge amount of software. The AUR is an amazing source of software and an indispensable tool for anyone who uses Arch or its derivates. There is, however, the issue that Arch fails to be officially supported by companies and proprietary software. This can be a disadvantage for casual users and that's why I usually steer clear of recommending Arch and its derivatives to casual users. 
    * Famous distros : Arch Linux, Manjaro

*Other minor families exist but I am glossing over them here just to keep the discussion of a sane length.*

#### Release Frequency
Distributions have a fixed release frequency model that they approach. There are broadly three types of distros here -
* **Rolling Release :** This sort of release model leads to a distro that doesn't really need to have any discrete versions or releases. Packages are updated almost as soon as they are updated upstream *(by the developer of the package)* and this ensures you always have the latest and greatest running on your machine. While this model is amazing for getting new features and supporting new hardware, it faces a major problem in that a few buggy updates can bring the entire system down. Some of the most famous distros of this category are **Arch**, **Manjaro**, **openSUSE Tumbleweed** and **Debian Sid** *(well, maybe not Sid technically because it was never meant that way)*. 
* **Cutting Edge :** Such distros have fixed release schedules, usually six months, but keep up to date softwares in their repositories. Unlike rolling releases, however, they do not continuously roll through updates for the entire OS but provide latest third party packages. A good example for such distros are **Fedora** and **Ubuntu Non-LTS**.
* **Stable :** Such distros are mainly used for servers and enterprises where stability is of paramount importance. They rarely have major updates and mostly receive security and bug fixes. A side effect of this is that they tend to have extremely outdated software in their repositories. However, they won't break easily at all. Good examples of such distros are **Debian**, **RedHat Enterprise Linux**, **centOS** and **Ubuntu LTS**. 

 
## So, What Should You Choose?
This section will be quick. The fundamental details have already been covered earlier. Keeping those in mind, here are my recommendations summed up pretty briefly *(quite an anti-climactic ending, isn't it?)* - 
* **For servers**, I would recommend either **Debian** or **centOS**. If you want additional, excellent, paid support, look no further than **RedHat Enterprise Linux** or **Ubuntu LTS**.
* **For desktop/laptop users** who want stable, fixed versions of softwares *(you'll know if you need it)*, go with **Ubuntu LTS** or any of its derivatives like **elementaryOS**, **Linux Mint**, etc. Do not go for non-LTS variants of either.

**For most other users**, the general person, simply use the cutting edge distros. I would highly recommend **Fedora** or **PopOS**. *If you do not have a need for Ubuntu LTS, then opting for the non-LTS Ubuntu is a bad idea and you would be better served with PopOS!* Honestly, just go with Fedora. 

**Fedora** is a unique distro in that it is one of the quickest to receive all the newest features with some of the best defaults coupled with a lot of testing by the RedHat developers who maintain Fedora. In addition, many popular softwares in Fedora *(like Chromium)* receive a lot of additional features that no other distros have. It is one of the most refined and polished Linux desktop experience and is my official recommendation. I have tried breaking my Fedora install by doing so many methods but it has refused to break. On the other hand, a simple update has often killed my Ubuntu installs, even LTS versions *(quite ironical)*. In conclusion, 
>My overall recommendations are **Fedora** in the first place, followed by **PopOS** in the second. Anything else would have to be a far away and distant third place in my personal opinion.