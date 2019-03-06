# lsl-vm
A Debian (stretch) VM which can be run in VirtualBox and comes pre-loaded with lsl (LWA Software Library).

## Cloning this repo
The vm virtual hard drive files are managed using Git LFS (they amount to several GB). You'll need to consider that when cloning/forking so you don't end up with only the pointer files.

Another option is just just build your own image using the install instructions [below](#building-your-own).

## Accounts
__Username__: root
__Password__: misticlsl

__Username__: mistic *(in sudoers group)*
__Password__: lslvm


## Links
[__UViip__](htps://github.com/mistic-lab/UViip): The project being worked on at UVic which requires this VM.

[__VirtualBox__](https://www.virtualbox.org/): Run this VM in it.

[__LWA__](http://www.phys.unm.edu/~lwa/index.html): The group that created lsl. If you don't know who they are, you're in the wrong repo.

[__lsl__](https://fornax.phys.unm.edu/lwa/trac/wiki): The software needed for working with LWA data and setting up SDFs.

## Building your own
These worked on Debian 9.0 "stretch".
### Setup a sudo account
```bash
your-user-name@host$ su -
root@host$ apt install sudo
root@host$ usermod -aG sudo your-user-name
root@host$ reboot
```
### Install dependencies
```$ sudo apt install libatlas-base-dev liblapack-dev libatlas-dev fftw3 fftw3-dev libgdbm-dev libgdbm3 python-pip python-matplotlib```
```$ pip install pyephem numpy scipy pyfits aipy pytz```
### Install lsl
```$ pip install lsl```
### Optional - install/download the SDF GUI
``` $ sudo apt install subversion```
```svn export http://fornax.phys.unm.edu/lwa/subversion/trunk/SessionSchedules```

## Notes
Atlas was installed via apt. There are some pretty involved instructions on getting it installed manually but I couldn't figure out CPU unthrottling on the VM. If anyone knows how to get that working let me know (https://github.com/nsbruce).

## Author
[Nicholas Bruce](https://github.com/nsbruce)