This document contains the issues I had and solutions when trying to use Android Virtual Device (AVD) or real device through USB debugging on Ubuntu environment.  
I am happy to receive any advice or opinion!  

# Common issue  
When I tried to open React Native application on AVD emulator, Genymotion, or even real device. The issues happened such as:  
```  
ADB server didn't ACK
* failed to start daemon *
error: cannot connect to daemon
```  
or  
```  
adb server is out of date. killing
```  
or client app cannot connect to backend.  

# Main reasons and solutions    
## 1
Too many instance of adb running at the same time.  
Solution: save `<PATH>/adb` to global environment variable.  
Notice:  
- There are 2 paths for adb: `/home/user/Android/Sdk/platform-tools/` and `/usr/bin/`.  
- Either is fine, but preferable the first one.  

Run:  
`adb kill-server` to kill the running server.  
`adb start-server` to restart the adb server.  
Notice: for every emulator or device running/ connecting to the computer, an adb instance will run automatically.  

## 2
The adb version of Android SDK in my local machine is older than the client adb version.  
The issue with using Linux is that version available from the Ubuntu repositories is older than the standard version.  
However, we can still get it from the latest platform tools by manually download and get it straigt from there.  
```  
wget https://dl.google.com/android/repository/platform-tools-latest-linux.zip
unzip \platform-tools-latest-linux.zip
sudo cp platform-tools/adb /usr/bin/adb
sudo cp platform-tools/fastboot /usr/bin/fastboot
```  
then run `adb version` to check the update.  

## Client app cannot connect to backend  
By default, React Native listen to default port 8081.  
Run `adb reverse <local> <remote>` to to reverse network connections from the device
to the host.
In my case, we run `adb reverse tcp:3888 tcp:3888`, with 3888 is the port our backend is listening to.  
After that, run `npm run android`.  

# Source  
https://androideputies.com/2016/12/11/linux-update-adb-fastboot-to-the-latest-version/  
https://developer.android.com/studio/releases/platform-tools.html  
https://www.reddit.com/r/reactnative/comments/5etpqw/what_do_you_call_what_adb_reverse_is_doing/  
https://gitlab.com/pbeeler/system_core/commit/252586941934d23073a8d167ec240b221062505f  
