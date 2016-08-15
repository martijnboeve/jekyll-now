---
layout: post
title: Moving your .NET frontend development to OS X...
---
__Sure, you'll say: "Nope! Can't be done, you need Microsoft to build .NET..." I know, you do, but imagine a VM running Windows with Visual Studio and IIS. And just that, have it running and don't ever, EVER open that window. Ever.__

I work at a classical technical development agency, we develop .NET websites and use TFS for our source control. Sure, we can transfer to Git since VS2013, but we haven't yet and - I suspect - won't any time soon.

So me and my frontend comrades are bound to having a Windows machine to develop on. And, as you all know, this is getting more and more of a problem as the entire frontend community is running on OS X. So most of the documentation is written for OS X, answers to questions on stackoverflow, but most importantly: __Doing frontend these days includes working the command line (terminal) and using build processes (gulp)! A lot...__

And those two main things, well, __suck balls__ when you need to do them on MS Windows. CMD is crap; commands suck, tabbing will make you wanna kill someone. And gulp is slow, or plugins  are not working at all.

But luckily, the terminal and Gulp are also our way out! Team Explorer Everywhere gives us a command line interface (cli) to use TFS from the terminal. And we can use 'vmrun' or ssh to run .exe files on our VMWare Windows machine, like, I don't know, maybe a little file called: msbuild.exe...

So, in theory, using just the Terminal I can "Get Latest Version" of a solution, make changes and call the msbuild.exe to build the code. And then check in those files. While never looking at a Windows dialog once. And the best part; with Gulp I can create tasks to specifically call these commands, Me gusta!

So instead of calling:
```bash
tf get "$/[our product/branch/project]" /force /recursive [/login:username,[password]]
```
I can simply call:
```bash
gulp GLV
```
And gulp will run the terminal command in the background using the right credentials. Like I said: Me gusta! Muchas!

I say "in theory" because currently I'm setting this up, it is going to work but, as with all things new, I'm hitting bumps in the road which need smoothing. From simple things like firewall settings in Windows to things a little more difficult like Application Pool Identity settings in IIS and their security settings in the NTFS file system.

I'll keep you updated on the progress I'm making!
