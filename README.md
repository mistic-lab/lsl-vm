# lsl-vm
A Debian (stretch) VM which can be run in VirtualBox and comes pre-loaded with lsl (LWA Software Library).


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


## Notes
Atlas was installed via apt. There are some pretty involved instructions on getting it installed manually but I couldn't figure out CPU unthrottling on the VM. If anyone knows how to get that working let me know (github.com/nsbruce).

## Author
[Nicholas Bruce](https://github.com/nsbruce)