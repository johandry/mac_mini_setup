# Mac Mini Setup

This is my guide and collection of scripts to setup from scratch my Mac Mini. I use it as a Media Server and Development Server so it will have all kind of software required for such functions and maybe more.

## Requirements

* Mac Mini  
* Internet Access

## Usage

In a Mac (could the the Mac Mini to restore or other Mac), clone/download this repository

  $ git clone git@github.com:johandry/mac_mini_setup.git

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

4. Join to a wireless network, then use the arrow key to highlight the USB drive (could be named 'OS X Base System' or 'Yosemite Installer'), press enter and you will see the Yosemite Installer Welcome screen. Follow the instructions to install the OS X in Macintosh HD disk.

WARNING: The next step is to erase your hard drive. I have a Time Machine to backup my disks but if you don't have it, make sure you backup your data before erase the disk.

5. Follow the structions as desired, then select Disk Utility to Erase the Macintosh HD disk. Make sure you select the 'Mac OS Extended (Journaled)' format.

6. Select Quit Disk Utility and select Install OS X. Follow the instructions to install Yosemite OS X

  Source: http://macs.about.com/od/OS-X-Yosemite/ss/Perform-a-Clean-Install-of-OS-X-Yosemite-on-Your-Macs-Startup-Drive_3.htm#step-heading

  If you need more information or details to install Yosemite read to the source.

7. Update the OS X Yosemite to the latest version.

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
* 