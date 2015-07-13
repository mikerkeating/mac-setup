mac-setup
=========

Wipe & Install instructions
- [] [OS X Mavericks: Erase and reinstall OS X](http://support.apple.com/kb/PH14243)
- [] http://www.thesafemac.com/how-to-reinstall-mac-os-x-from-scratch/

Install
- [] Work through the various options
- [] Sign-in to Apple

Setup
- [] Apply Full Disk Encryption - note it will take 1 hour + on a new MacBook Air
- [] Access Github and setup your Github SSH key
- [] Install XCode from the Mac Store - note it's a 2GB+ download so will take a while
- [] Install XCode Command Line Tools from the Mac Store

Notes
- [] symlink http://gigaom.com/2011/04/27/how-to-create-and-use-symlinks-on-a-mac/
- [] http://www.scrubly.com/blog/how-to-mac/move-system-folders-another-drive-mac/

Folders and Files

- `cd /Volumes/Files/`
- `mkdir users`
- `cd users`
- `mkdir mikerkeating`
- `cd mikerkeating`
- `mkdir Dropbox`
- `cd Dropbox`
- `mkdir Desktop`
- `mkdir Downloads`
- `mkdir Documents`
- System Folders
  - `sudo rm -rf ~/Desktop/ ; ln -s /Volumes/Files/users/mikerkeating/Dropbox/Desktop/ ~/Desktop`
  - `sudo rm -rf ~/Downloads/ ; ln -s /Volumes/Files/users/mikerkeating/Dropbox/Downloads/ ~/Downloads`
  - `sudo rm -rf ~/Documents/ ; ln -s /Volumes/Files/users/mikerkeating/Dropbox/Documents/ ~/Documents`
  - `sudo rm -rf ~/Public/ ; ln -s /Volumes/Files/users/mikerkeating/Dropbox/Public/ ~/Public`
- Non System Folders
  - `mkdir Pictures`
  - `sudo rm -rf ~/Pictures/ ; ln -s /Volumes/Files/users/mikerkeating/Dropbox/Pictures/ ~/Pictures`
  - `sudo rm -rf ~/Movies/ ; ln -s /Volumes/Files/users/mikerkeating/Dropbox/Movies/ ~/Movies `
  - `sudo rm -rf ~/Music/ ; ln -s /Volumes/Files/users/mikerkeating/Dropbox/Music/ ~/Music`

Terminal Setup
- Terminal
  - Already downloaded iTerm2; may need to update 
  - install XCode Command Line tools via `xcode-select --install`
  - check via `xcode-select -p`
  - check via `gcc --version`
- ZSH
  - Install oh my zsh via `curl -L http://install.ohmyz.sh | sh`
  - Symlink into dropbox via `sudo rm ~/.zshrc ; ln -s /Volumes/Files/users/mikerkeating/Dropbox/shared-config/.zshrc ~/.zshrc`
- Add to `.zshrc` `export HOMEBREW_CASK_OPTS="--appdir=/Applications"`

App Setup
- Install Homebrew via `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
- Setup brewfile
- via https://mattstauffer.co/blog/setting-up-a-new-os-x-development-machine-part-2-global-package-managers
- "Now, once I've installed Homebrew, I can just navigate to the directory with my Brewfile and run `brew bundle`"
