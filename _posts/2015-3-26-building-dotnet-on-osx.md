---
layout: post
title: building .NET on OS X, part 2
---
###### Let me elaborate on what I'm trying to do: create an environment where I can work on my MacBook and develop .NET websites. As a frontend developer I can rely on processes like gulp to compile my CSS and JavaScript, that's no problem. My challenge lays in the fact that I need to do an occasional build of the .NET code and use TFS to "get latest version" and "check in" my changes. ######

Also, the backend devs work on Windows machines so the basic environment settings need to be the same in order to make sure everything keeps working.

So what I did first was install VMWare Fusion and set up an image consisting of Windows 8.1, SQL Express, Visual Studio, IIS. Setup TFS in Visual Studio, create IIS instances for my .dev websites and build a solution. Check, I can work again ;). Time for an image snapshot!

The second step was to make sure I could also access the .dev url on my OS X. So in my host file on OS X (/private/etc/hosts) I added the line:
``domainname.dev	<ip-address>``<br />
Where you would put the correct values of course. That didn't work but I realised I needed to disable the firewall on my Windows VM. That did the trick! Ok, at this point I could, build the website in my VM and view the result inside my OS X.

Now I wanted to change my files, the SCSS and JS residing inside my VM, from my OS X. So, in my VM, I shared the Workspaces folder. This is the folder which is mapped to my TFS collection. Simply right click the folder, properties and in the "sharing" tab click the "share" button. Then you have a network path which you can use to connect to in finder on OS X. I was surprised to see that when I change a file in OS X (using Sublime Text), Visual Studio still automatically checks out that file from TFS. Which is nice.

At this time I simply set up a
``$ sass --watch <css folder>``<br/>
command in order to be able to get some work done. But by now I could do most of my front-end work in OS X. Make changes in my SCSS files, which are being compiled into CSS, change JS files and see the results in my browsers on OS X.

Shortly after I set up my Gulp tasks to do all of the minifying, concatenation, renaming and relocating I wanted it to do. But still I needed to "GLV", "check in" and Build the project in my VM. Those would need to be ported next. I made some explorations using SSH to access my VM to be able to run commands, using "TF Everywhere" on OS X to be able to use Terminal  ('couse when it works in Terminal I can Gulp /*the crap out of*/ it...), I had some successes and some failures, but then I came accross __VMRUN__! THE thing I was looking for. Vmrun is a command line utility to control specific VM's. So using vmrun I could run scripts inside my VM and open programs. Just what I needed!

In the next part I'll go into using vmrun and the process of getting it all to work. It was a lot of trial and error becouse when you Google on this topic there isn't a lot to be found, but I'm managing quite well at the moment ;)

Stay tuned...
