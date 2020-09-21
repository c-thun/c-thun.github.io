---
layout: post
title:  "Linux Distribution Recommendations"
author: aakash
categories: [ Blog ]
tags: [ Linux ]
image: assets/images/laptop.png
---

It comes as a shock to nobody that Linux distributions tend to be a dime a dozen. As I have discussed in my article, [The Confusion of Choice](../confusion-by-choice), anarchy and chaos is often a side effect of complete freedom. Not that it’s a bad thing by any means. 

Thanks to a number of projects like Linux From Scratch, freely available base distribution source code and easily available guides, not to mention video tutorials on YouTube by experts like Chris Titus Tech, it’s really not a hassle to take a base distribution and produce a spin off of it. It’s such an easy task that even kids can produce their own distribution spin offs. 

With all this choice available, there are also a hundred different online blogs that’ll tell you which distribution they recommend. The thing is, though, most of these major tutorials  are written by people who have cursory knowledge of using Linux and have their main skills cantered around SEOs and clickbait to get more viewers to their websites. Popular guides usually follow the policy of “ad revenue first, passion for the subject material second”. 

However, I digress. Getting on to the subject matter, I have organised the following discussion based on a number of crucial aspects linked with each distribution. In addition, I shall be directly making use of some background knowledge of distributions. If you don’t have the necessary background, I would highly recommend you to read this concise article on what Linux distributions actually are.

If you can’t be bothered to read up, just note these points -

* There are 3 major Linux distro families *(Arch, Debian and Fedora)*,  each with their own package managers, binary package formats, software repositories, and release schedule. 
* Most of these projects contribute to upstream and, thus, end up sharing a lot of features. This is an “everyone is a winner” model, *and really where open source shines,* because the more everyone focuses on upstream, the faster features get added and bugs get fixed. 
* The user in most cases will interact with their distribution mainly through the graphical interface. As such, the choice of the default Desktop Environment matters a lot more than the choice of the distribution itself. *I have prepared a succinct summary of Desktop Environments which you may read by clicking here.* 
* Distribution spins, thus, mainly aim to provide different defaults, out of the box desktop environments, themes and tweaks to make life easier.  In most cases, though, unless heavily supported by the community or the official developers, spins tend to be rocky in terms of stability and viability. This needs to be kept in mind.

So, where do I stand on distributions? Well, I’ve divided major distributions into three lists : Recommended, Neutral and Not Recommended. Each distribution will have a justification for why they belong to said category as well as the desktop environments of the distribution that I recommend *(not all distributions work well with every desktop environment and so my picks here are what I’ve found to be the best combination)*. I have also tried to keep a member from each distribution family in each category so as to provide you with options based on your software needs.


### Recommended Distributions
1. **Fedora *(GNOME)* -** *Score : 10/10*
    * Usually the **quickest to adopt new features in a stable way**. This makes the most innovative distribution with loads of new functionality every update. *Stability is important here as new features will be quicker on rolling releases but won't be as thoroughly tested*
    * Worked on by a lot of RedHat employed developers and forms the foundation for Red Hat Enterprise Linux. This leads to **high stability, polish and software availability**.
    * GNOME, systemd, Wayland, and a lot many technologies in the Linux desktop space are developed, supported and pushed primarily by Red Hat. As Fedora is also made by the same guys, it tends to be **tested very well**.
    * While it does not ship by support of non-free software by default, that is easily remedied by opening the Software app and selecting RPMFusion as an enabled repository. The benefit? RPMFusion contains almost all the packages you will ever need with **very easy installations from the Software app**. No more adding PPAs and fumbling around with third party repos needed.
    * NVIDIA Optimus is supported out of the box and proprietary **NVIDIA drivers are just one click install away** from the Software app *(provided you have enabled RPMFusion first)*. Fedora does everything for you and I find this much easier than even Windows.
    * [Amazing Battery life](https://www.omgubuntu.co.uk/2018/02/better-battery-life-on-fedora-linux) out of the box thanks to customised tweaks to the power management features. Fedora has been the only Linux experience that gives me battery life as good or even better than Windows without installing additional software like ```tlp``` or ```powertop```  
    * Flatpak integration out of the box 
2. **PopOS! -** *Score : 9.5/10*
    * Based on Ubuntu and so has all the software available on it that is present on Ubuntu. However, it uses a near vanilla GNOME desktop experience, unlike Ubuntu, while feels faster, smoother and has lesser glitches.
    * System76, the creator of PopOS, also applies battery life tweaks similar to Fedora. This causes PopOS to have **amazing battery life out of the box**, equaling Fedora and Windows. 
    * PopOS ships with a custom software app called Pop Shop which also has Flatpak integration out of the box. In addition, it allows **easy one click installation of NVIDIA drivers**.
    * Ships with an amazing tiling extension out of the box which, frankly speaking, is very well made for basic users and will be appreciated by people who use wide screens
3. **Manjaro *(KDE/XFCE)* -** *Score : 9/10*
    * Their **graphical package management utility** is one of the most polished and functional utilities I have ever used. It is extremely powerful for installing and updating apps, enabling the Arch User Repository (AUR), enabling Flatpak/Snap support, and configuring updates.
    * Ships with a **built in Kernel Manager** which helps manage, update and install kernel versions with a very nice graphical utility.
    * They spend a lot of time configuring the looks and shortcuts of their KDE and XFCE versions, both of which are officially supported, making them feel like **extremely polished and premium** experiences.
    * Manjaro is based on Arch and so has **amazing software availability** thanks to the Official Repositories and AUR. 
    * While a rolling release distribution, Manjaro benefits from testing of updates before they actually release. Thanks to this, while Manjaro may lag behind Arch *(when it comes to new system updates)* for 1-2 weeks but has quite **stable updates with significantly lower risks of bugs**.  


### Neutral Distributions
1. **openSUSE *(KDE)* -** *Score : 8.5/10*
    * Has the amazing tool called **YaST which makes configuring the system extremely easy** without the need to go into the terminal. Definitely a big plus for a lot of new users who are not comfortable with the command line
    * openSUSE Tumbleweed is a rolling release edition which gets the latest software as it comes. On the other hand, openSUSE Leap is a fixed time-spaced release distro suited better for enterprise users rather than regular desktop users.
    * An amazing advantage of using openSUSE is that it **allows you to also use Fedora repositories** to install software in addition to its own repositories. 
    * The reason I am unable to recommend this distribution is that it **can sometimes have weird configurations** which may confuse new users. An example for this is packaging Synaptic touchpad drivers by default rather than libinput, leading to quite an extremely disappointing touchpad experience. 
    * Despite all this, it still is **one of the best Linux experiences especially if you have some experience with Linux** or if you are using it in enterprise deplyments. 
2. **Linux Mint *(Cinnamon)* -** *Score : 8/10*
    * The Cinnamon desktop environment made by Linux Mint is often touted to be **user friendly for users coming from Windows**. However, the same also goes for the KDE Desktop and so Cinnamon doesn't have much of an advantage here.
    * The problem here is that Cinnamon **does not have as much development support and funding** going into it that KDE and GNOME have. Thanks to this, Cinnamon **misses out on a lot of optimizations** that go into other desktops. Take for example the performance improvements that GNOME has received from versions 3.28 to 3.36 : While Cinnamon branched off of GNOME 3 originally, it doesn't rebase itself on new GNOME versions and so will not get all these performance improvements. 
    * In addition, new technologies like Wayland are nowhere to be seen on the Linux Mint timeline while GNOME already ships with it and KDE is shipping with it very soon. 
3. **elementaryOS *(Pantheon)* -** *Score : 7.5/10*
    * **One of the best and most well designed distributions with an actual vision for good design**. Mac users will find themselves right at home with elementaryOS thanks to the similarities. 
    * This similarity, however, turns into a disadvantage for users coming from a non-Mac background as they will find themselves with **unusual out of the box defauls**, keyboard shortcuts and touchpad/mouse click behaviours.
    * In addition, elementaryOS is **not customisable** and if you find yourself missing a feature, you can just hope and pray to the elementaryOS developers that they implement it later on. 
4. **Arch Linux -** *Score : 8/10*
    * If you are a power user who is extremely comfortable with the command line, you would love Arch Linux. In addition, it is **one of the best ways to learn Linux** and is an extremely rewarding experience.  
    * **Everything can be customised** from scratch and you can choose whatever you want to install and leave everything else, leading to a leaner and faster system.    
    * However, this is **not recommended at all for a new or inexperienced user** as it demands a basic level of knowledge, dedication and desire to learn.
5. **Debian Stable *(GNOME)* -** *Score : 8/10*
    * **Extremely stable** and very resistant to breakage 
    * Often has **outdated software in its repositories**. While this is not a problem for software that is available as Flatpak, it is still an issue because a lot of software still isn't available as a Flatpak. In addition, command line software does not get packaged as Flatpak and so that will stay outdated with Debian.
    * **Installing Debian can be a hassle on certain hardware**, especially laptops, because Debian by default does not package non-free software/drivers in their ISOs or repositories. Workarounds like unoffical install images exist but they tend to be huge (4.5 GB).
    * Default installations of Debian package in a lot of unnecessary software which can be considered **bloat**.
    * In addition, Debian **only enables free repositories by default** which do not contain non-free software. This needs to be manually enabled and so can be a hassle for inexperienced users.  

### Not Recommended Distributions 
1. **Ubuntu *(GNOME/KDE)* :**
2. **Zorin OS :**
3. **Gentoo :**
4. **Debian Sid :**
