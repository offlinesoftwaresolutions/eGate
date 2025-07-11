# eGate
Offline MDM for Android

Current version: 1.32

Click on [here](https://github.com/offlinesoftwaresolutions/eGate/releases/latest) to get the latest version

Buy your license [here](https://payhip.com/b/vxf1i)


Need help installing, here's a great guide written up by [@DonBot](https://forums.jtechforums.org/u/DonBot). Original post [here](https://forums.jtechforums.org/t/how-to-install-egate-guide/689).
This guide will walk you through installing and activating eGate on your Android device using ADB.

What You’ll Need
Android Device: Running Android 6.0 or later.
eGate APK: Download the latest version from the GitHub repository.
ADB Tools:
Install platform-tools on your computer, or use a browser-based ADB tool like WebADB.
Activation License Key: Purchase from PayHip or use one you got from a reseller.
USB Debugging Enabled:
Enable Developer Options on your device by going to:
Settings > About Phone > Tap “Build Number” 7 times.
Enable USB Debugging in Developer Options.
Installation Steps
Step 1: Install the APK via ADB
Option 1: Local ADB Installation
Connect your Android device to your computer via USB.
Open a terminal/command prompt on your computer and navigate to the folder containing ADB tools.
Place the eGate APK in the same folder for easier access.
Run the following command to install the APK:
adb install app-general-release.apk
Replace app-general-release.apk with the exact name of the APK file.
If this is the first time you are connecting this device to your computer, a popup may come up on the device asking you to Allow permission. Press allow and run the command again.
Option 2: Install via WebADB
Go to WebADB in your browser.
Connect your Android device via USB or Wi-Fi following the on-screen instructions.
Select the Install APK option, upload the eGate APK file, and install it.
If this is the first time you are connecting this device to your computer, a popup may come up on the device asking you to Allow permission. Press allow and run the command again.
Step 2: Set eGate as the Device Owner
Ensure the eGate app is installed.

Run the following command to set eGate as the device owner:

adb shell dpm set-device-owner com.oss.egate/.a
If the device is the LG Classic, run the following ADB command instead:

dpm set-device-owner com.android.cts.egate/com.oss.egate.a
This grants the app device management permissions, necessary for full functionality.
Read more about setting the device owner and how to fix issues setting the device owner at this topic I wrote:
https://www.jtechforums.org/t/setting-the-device-owner-information/674?u=donbot

Step 3: Grant Accessibility Permissions
To allow eGate to set some features like blocking WebView and other app-related settings, run this ADB command:
adb shell pm grant com.oss.egate android.permission.WRITE_SECURE_SETTINGS
Step 4: Activate the App
Open the eGate app on your device.
Enter the license key you received at the time of purchase.
Step 5: Configure eGate Settings
View all the settings and what each does at this topic that I wrote:
https://www.jtechforums.org/t/egate-settings-explained/679?u=donbot

I hope this helps you installing eGate! Feel free to let me know if any modifications/changes should be made to add/correct information.
