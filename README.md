mac-setup
=========

Wipe & Install instructions
* [OS X Mavericks: Erase and reinstall OS X](http://support.apple.com/kb/PH14243)
* http://www.thesafemac.com/how-to-reinstall-mac-os-x-from-scratch/

Install
* Work through the various options
* Sign-in to Apple

Setup
* Apply Full Disk Encryption - note it will take 1 hour + on a new MacBook Air
* Access Github and setup your Github SSH key
* Install XCode from the Mac Store - note it's a 2GB+ download so will take a while
* Install XCode Command Line Tools from the Mac Store
* 


symlink http://gigaom.com/2011/04/27/how-to-create-and-use-symlinks-on-a-mac/

- `cd /Volumes/Files/`
- `mkdir Downloads`
- `mkdir Documents`
- `mkdir Desktop`
- `mkdir Users`
- `cd users`
- `mkdir mikerkeating`
- `sudo rm -rf ~/Downloads/`
- `ln -s /Volumes/Files/Dropbox/Downloads/ ~/Downloads`
- `ln -f -s /Volumes/Files/Users/mikerkeating/Dropbox/Downloads/ ~/Downloads`
- `sudo rm -rf ~/Documents/`
- `ln -s /Volumes/Files/Dropbox/Documents/ ~/Documents`
- `sudo rm -rf ~/Desktop/`
- `ln -s /Volumes/Files/Dropbox/Desktop/ ~/Desktop`
