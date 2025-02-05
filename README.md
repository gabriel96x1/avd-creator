# avd-creator

This script ONLY work for MacOS for now...

This repo contains a script to install and Run Android Emulator without have to install Android Studio the advantages we have installing it by this tool are the following:

- One command to launch the emulator, without have to run Android Studio.
- APK installation from your Mac to the Emulator using a simple drag & drop.
- Is possible use other Android Studio utils (like logcat using adb toolset) without the big CPU usage of have the IDE opened.

The steps to use this tool are the following:

1. git clone this repo where you want to install it.

2. Run the following in the same terminal:

```
  chmod +x $PWD/avd_creator/cravd
  export PATH=$PWD/avd_creator:$PATH  
  echo "export PATH=${PWD}/avd_creator:$PATH" >> ~/.zshrc
``` 

3 . If you dont have Java installed run the following command:
```
  brew install --cask adoptopenjdk/openjdk/adoptopenjdk8
```
4. Go to https://developer.android.com/studio#command-tools and download Command line tools only.

5. Extract the .zip and move the resultant cmdline-tools directory to the place you want to install it.

6. Open a terminal and go to the path where cmdline-tools is now.
```  
  cd <path_where_cmdline-tools_is>
``` 
7. Once there run:
```  
  cravd buid-emulator
```
8. Follow the installation steps that will be prompted in your terminal to complete the installation.

Only for the first time boot run the commands:
```
  adb kill-server && emulator @Android_Emulator_Api_33
```  
Any time after first boot could be used:
```
  emulator @Android_Emulator_Api_33
```  
  
To remove the complete emulator installation run the following command:
```
  cravd remove-emulator
```  
  
  
  
