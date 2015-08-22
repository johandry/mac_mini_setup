# Mac Mini Setup

This is my guide and collection of scripts to setup from scratch my Mac Mini. I use it as a Media Server and Development Server so it will have all kind of software required for such functions and maybe more.

## Requirements

* Mac Mini  
* Internet Access

## Usage

In a Mac (could the the Mac Mini to restore or other Mac), clone/download this repository

  ```
  $ git clone git@github.com:johandry/mac_mini_setup.git
  ```

There are 2 options: Setup and Provision a Mac from scratch or a Mac with OS X already installed.

### Setup a USB drive to install OS X Yosemite from scratch

1. Execute the init script

  ```
  $ cd mac_mini_setup
  $ ./USB_Setup
  ```

  The init script will download OSX 10.10 Yosemite and setup a USB drive for a clean install of OSX Yosemite.

  **_Source_**: http://www.macworld.com/article/2367748/how-to-make-a-bootable-os-x-10-10-yosemite-install-drive.html

2. Remove the USB drive when the script finish, shutdown the Mac Mini and plug the USB drive.

3. Start up the Mac Mini while holding the Option key (Alt key if it is a Windows keyboard)

4. Join to a wireless network, then use the arrow key to highlight the USB drive (could be named 'OS X Base System' or 'Yosemite Installer'), press enter and you will see the Yosemite Installer screen.

5. **WARNING** This step is to erase your hard drive, make sure you backup your data before erase the disk or have Time Machine with your backups.
  In the top menu select Tools -> Disk Utility. Select the Macintosh HD disk and go to Erase tab then click on Erase botton. When the erase is completed I also go to First Aid tab and select Repair Disk, just in case there are some disk errors.

6. Select Quit Disk Utility in the top menu and select Install OS X. Follow the instructions to install Yosemite OS X

  **_Source_**: http://macs.about.com/od/OS-X-Yosemite/ss/Perform-a-Clean-Install-of-OS-X-Yosemite-on-Your-Macs-Startup-Drive_3.htm#step-heading

  If you need more information or details to install Yosemite read to the source.

7. Connect the keyboard, trackpad and/or mouse and configure them in System Preferences

8. Update the OS X Yosemite to the latest version, if needed. Open App Store -> Updates

### Setup and Provision a Mac with OS X already installed.

1. Execute the script

  ```
  $ cd mac_mini_setup
  $ ./setup
  ```

## What will I get in the Mac?

This provision script may change from time to time but there are some base software that will be installed:

* [Homebrew](http://brew.sh/): Required to install all the software.
* [Homebrew Cask](http://caskroom.io/): Extension to Homebrew to install OS X Applications and large binaries.
* [rbenv](http://rbenv.org/): Ruby environment manager
* Browsers: Chrome, Firefox and Tor
* Cloud Storage Managers: Dropbox, Box Sync and Google Drive
* Media Tools: HandBrake, Subler, VLC, Transmission, Spotify
* Development & DevOps Tools: Sublime Text, Visual Studio Code, Github, VirtualBox, Boot2Docker, Kitematic, Packer and Vagrant
* Other Applications such as: Skype, Caffeine and UnRar