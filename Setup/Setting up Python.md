# Setting up Python

## Introduction

This part is the most fundamental aspect of this exercise, but it not necessarily trivial. There are multiple ways of going about it. We are going to keep it as simple as possible and use Anaconda on Windows and the Spyder IDE that comes with Anaconda. I am not the most familiar with this environment as I am more familiar with WSL and Ubuntu. 

I personally advocate that you should set-up the WSL on your windows system with Ubuntu for linux in the future. This gives you so much more power to perform other computational tasks. If you are interested, please reach out to me or google it. Googling it and figuring it out for yourself is an important step for learning. 

## Premise of Anaconda

Anaconda can be installed in a variety of combinations. There is the heavy-weight installation which comes with many packages that are useful for getting you started. Another option is miniconda which is a much more lightweight installation (doesnt come with the extra packages). The version of python is also something that needs to be considered. We will be sticking to Python3 as that is the most current version. However, there are packages that you might use in the future that rely on Python2. As far as I am aware, there is no more support for Python2 from the main developers. 

One of the main value propositions of Anaconda is that we can create reproducible environments. In days of yore, people used to waste so so much time trying to get code working when their code was perfectly fine, but the libraries they had were not the correct ones.  As such, in Anaconda, we can create distinct environments that have the packages and libraries we want, and toggle between different environments for different projects. We can also export the environment for others to replicate. 

## Installing Anaconda

Go the following link and download the appropriate Anaconda installation for your machine:  https://www.anaconda.com/products/individual#Links

Click the executable to start the installation process. Proceed as normal with the default options. 

![Python_1](C:\Users\Pavan\Desktop\Python_1.PNG)

Proceed with the default installation if this is the first time you are installing python. If you already have a way of running python scripts, go with that, no need to set-up Anaconda. 

## Setting up Anaconda and the environment

Launch the Anaconda navigator. You can find this in Windows explorer. 

![Python_2](C:\Users\Pavan\Desktop\Python_2.png)

We can create a new environment in a few ways. I shall present one way of doing so that lets you use the environment configuration file that is available in the exercise file. For windows, the configuration file should be `fipy34_windows.yml`. This file contains information about the packages needed for this course. 

Launch the CMD.exe Promt: 

![Python_3](C:\Users\Pavan\Desktop\Python_3.PNG)

Here are a few basic commands to get started: 

```
dir --> Lists all the files present in your current location
cd .. --> Move the the folder one level up. 
cd foo --> Move into the folder named foo in the current location
```

Suppose you have your the files on your desktop. When you type `dir` in the current directory, you will see many of the folders you are familiar with e.g. `Desktop`, `Downloads` etc etc:

```
Directory of C:\Users\Pavan

07/02/2020  09:16 PM    <DIR>          .
07/02/2020  09:16 PM    <DIR>          ..
07/02/2020  09:28 PM    <DIR>          .conda
07/02/2020  09:20 PM                43 .condarc
07/02/2020  07:06 PM    <DIR>          .ipython
07/02/2020  07:04 PM    <DIR>          .matplotlib
07/02/2020  08:18 PM    <DIR>          .spyder-py3
07/01/2020  08:23 PM    <DIR>          3D Objects
07/02/2020  09:18 PM    <DIR>          anaconda3
07/01/2020  08:23 PM    <DIR>          Contacts
07/02/2020  09:26 PM    <DIR>          Desktop
07/02/2020  06:45 PM    <DIR>          Documents
07/02/2020  08:29 PM    <DIR>          Downloads
07/01/2020  08:23 PM    <DIR>          Favorites
07/01/2020  08:23 PM    <DIR>          Links
07/01/2020  08:23 PM    <DIR>          Music
07/01/2020  08:25 PM    <DIR>          OneDrive
07/01/2020  08:24 PM    <DIR>          Pictures
07/01/2020  08:23 PM    <DIR>          Saved Games
07/01/2020  08:24 PM    <DIR>          Searches
07/01/2020  08:23 PM    <DIR>          Videos
               1 File(s)             43 bytes
              20 Dir(s)  132,774,273,024 bytes free
```

Change into the Desktop directory by typing `cd Desktop` . We shall now create the necessary environment using the `fipy34_windows.yml` file that you should have. Type the following command into the shell: 

```powershell
conda env create --file fipy34_windows.yml
```

You will see a bunch of text showing you that the installation is going on. At this point, the installation should be complete. It is possible to run the python scripts using this terminal. But we also want to see the actual text of the code. So let us close the window. 

## Getting started with Spyder

Go to the Anaconda Navigator and change your environment to the new `fipy34` environment. 

![Python_4](C:\Users\Pavan\Desktop\Python_4.png)

![Python_5](C:\Users\Pavan\Desktop\Python_5.png)

When you launch Spyder, it should look something like as follows. However, you may have many more windows open with introductory material. You can close then and do as you please. 

![Python_6](C:\Users\Pavan\Desktop\Python_6.png)

We need three components to run our simulation: 

1. Editor
2. iPython Console
3. Plots

The editor is needed to see our code before we run it, the console is used to run the actual code and the plots is used to see our results. Click `View` -> `Panes` and check these three components:

![Python_7](C:\Users\Pavan\Desktop\Python_7.png)

Once you check all three components, your screen should look like this:

![Python_8](C:\Users\Pavan\Desktop\Python_8.png)

We can test a trivial script e.g. Hello World. 

We do this by editing the file open on the editor: 

```python
# -*- coding: utf-8 -*-
"""
Created on Thu Jul  2 21:46:36 2020

@author: Pavan
"""

print ("Hello world")
```

There is a play button at the top. You can use that to run the script. The output will be in the iPython console:

![Python_10](C:\Users\Pavan\Desktop\Python_10.png)



## Running our simulation

To run our simulation, we first need to open our python script into Spyder: 

![Python_11](C:\Users\Pavan\Desktop\Python_11.png)

If you have uploaded `ex1.py` properly, it should look like this: 

![Python_12](C:\Users\Pavan\Desktop\Python_12.png)

At this point, if you have selected the right environment (`fipy34`) and uploaded the script properly, you should be able to run it by clicking the play button. Since we are visualizing the results, we will see it in the plots window: 

![Python_13](C:\Users\Pavan\Desktop\Python_13.png)

You need to keep track of the output in the iPython console. 

At this point, you are able to run the rest of the cases and modify them in the editor as you desire. Please explore the environment and familiarize yourself with the features of Spyder. This is a decent opportunity to get familiar with python. 