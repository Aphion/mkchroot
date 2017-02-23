#Readme
================

This is a modified script to create a Debian Jessie x86/i386 chroot environment on your Raspberry Pi forked & based on the original [script](https://github.com/socialdefect/mkraspbian-chroot) released by [socialdefect](https://github.com/socialdefect). 


All credit should go to [socialdefect](https://github.com/socialdefect)! Im still learning Linux and you should consider this still very much a WIP by a Linux newbie! 

#####Still on the TO-DO list:

- [x] Rename mkraspbian-chroot to mkchroot to avoid conflicts
- [x] Modify arch in mkchroot
- [ ] Fix gpg jessie public key
- [ ] Add script to install Dependencies
- [ ] Fix README.md
- [ ] Script cleanup


###Dependencies
=================

>####debootstrap <> qemu <> qemu-user-static <> qemu-debootstrap

###Installation:
=================

>WIP!





##mkchroot Readme:
==================================

Script for setting-up a Debian chroot directory for developing software for the [Raspberry Pi](http://raspberrypi.org) on your Linux desktop computer.
The script can also help you bind-mount /dev, /proc and /sys filesystems to enable device
access and networking inside your chroot, unmount bind-mounts and start a chrooted shell or
execute a chrooted command.

####Usage:
       
* mkchroot (with no arguments will create a chroot in the working directory)
*       mkchroot [workdir] [chroot name] [distribution] [mirror] - (name, distrib and mirror are not mandatory for they get default values)
*       mkchroot mount [/path/to/chroot/dir]
*       mkchroot unmount [/path/to/chroot/dir]
*       mkchroot chroot [/path/to/chroot/dir] [command] - (if [command] is not passed it will default to a bash shell)

####Examples:
    
	When you run mkchroot without any arguments a Debian jessie
    chroot will be created in your current directory ($PWD). The chroot
    directory will be named 'chroot-debian-i386'.
    If this directory exists you can choose to overwrite or auto-rename it.

    Create a new Debian jessie chroot in directory: /home/username/raspi
        named: jessie-i386

                mkchroot /home/username/raspi jessie-i386 jessie






######mkraspbian-chroot Original Readme:
======

>Script for setting-up a Raspbian chroot directory for developing software for the Raspberry Pi 
>(http://raspberrypi.org) on your Linux desktop computer.  
>The script can also help you bind-mount /dev, /proc and /sys filesystems to enable device 
>access and networking inside your chroot, unmount bind-mounts and start a chrooted shell or 
>execute a chrooted command.
>
>Usage:
>       mkraspbian-chroot
>		(with no arguments will create a chroot in the working directory)
>       mkraspbian-chroot [workdir] [chroot name] [distribution] [mirror]
>		(name, distrib and mirror are not mandatory for they get default values)
>       mkraspbian-chroot mount [/path/to/chroot/dir]
>       mkraspbian-chroot unmount [/path/to/chroot/dir]
>       mkraspbian-chroot chroot [/path/to/chroot/dir] [command] 
>		(if [command] is not passed it will default to a bash shell)

######Examples:
>    When you run mkraspbian-chroot without any arguments a raspbian wheezy
>    chroot will be created in your current directory ($PWD). The chroot
>    directory will be named 'chroot-raspbian-armhf'.
>    If this directory exists you can choose to overwrite or auto-rename it.
>
>    Create a new raspbian wheezy chroot in directory: /home/username/raspi 
>	named: wheezy-armhf
>
>		mkraspbian-chroot /home/username/raspi wheezy-armhf wheezy
>
>   Create a
