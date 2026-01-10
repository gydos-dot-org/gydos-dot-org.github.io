
http://gydos-dot-org.github.io

README.md

Paul Gydos
paul@gydos.org 

January 2026

vishgit

vishgit is what we call using vim dash and git in conjunction with one another.

We try it out in an environment which I call Smellinux - A Small Environment for Learning Linux.

smell

The way to do Smellinux is by making sure there is a command line environment in your device with access to a linux kernel and with some response to well known UNIX conventions.

on android

So far I've done it this way on an very inexpensive Android device. 

I install fdroid from its own website from its downloadable .apk
I use fdroid to install Termux

Using Termux, I run a script written to do certain things. 

The Smellinux v0.13 vishgit script for Termux on Android
does the following:

By bringing in an Alpine Minirootfs, introduce a more minimal busybox based userspace to be utilized by a chroot or proot from the Terminal to the Alpine Minirootfs Userspace which fdroid installed Termux will launch utilizing Android’s preexisting Linux kernel. This will give us our dash layer and userspace

Bring in all dependencies necessary to install and run vim and git

Install the foundational repository: The King James Version Bible in database form (csv - comma separated value database) from one of the github repository sites with a version of the “Metav KJV db”. This is the metav or kjv layer. 

There should be a tutorial layer, which with development will emerge here as well in the near future. 

smell command

Once the Android device is properly configured with fdroid installed Termux and the Smellinux script has been brought in and run then,...

The Smellinux system designed to give us an environment to vishgit in and get the foundational repository: The database version of The King Version Bible (metav kjv db)

To enter the system simply, from the Termux command line (once the smellinux.sh script has been installed), one only needs to type: “smell”

on windows 11

gydos-dot-org currently endeavors to make a smellinux script for Windows 11 systems which have come off S-mode and installed the WSL environment

At this time gydos-dot-org is testing using WSL installed Debian

From there the modified Smellinux script for WSL activated Win 11 will attempt to: 

By bringing in an Alpine Minirootfs, introduce a more minimal busybox based userspace to be utilized from the Command Prompt
to the Alpine Minirootfs Userspace which WSL installed Debian will launch using WSL installed Debian's preexisting Linux kernel. This will give us our dash layer and userspace

Bring in all dependencies necessary to install and run vim and git

Install the foundational repository: The King James Version Bible in database form (csv - comma separated value database) from one of the github repository sites with a version of the “Metav KJV db”. This is the metav or kjv layer.

There should be a tutorial layer, which with development will emerge here as well in the near future. 

Shortly if all goes as planned then you should be able to get these instructions and the scripts from https://github.com/gydos-dot-org










