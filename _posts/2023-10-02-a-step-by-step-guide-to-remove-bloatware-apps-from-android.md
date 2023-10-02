---
title: A Step-by-Step Guide to Remove Bloatware Apps from Android
layout: post-right-sidebar
categories:
- Windows
- Android
image: assets/images/post/bloatware.jpg
---

If you've recently purchased a new Android smartphone, you might have noticed that it comes preloaded with a bunch of apps you never asked for or may never use. These unwanted pre-installed apps (mainly in Xiaomi, Mi, Vivo, Oppo), commonly referred to as "bloatware," can slow down your device, consume precious storage space, and even compromise your privacy. Fortunately, you can reclaim control over your Android device by removing these bloatware apps. In this step-by-step guide, we will show you how to remove bloatware from your Android device.

**Disclaimer**: Removing system apps or bloatware may cause issues if done incorrectly. Proceed with caution, and be aware that some apps are essential for the proper functioning of your device. We recommend taking a backup of your data before proceeding.

**Step 1: Check for Disable Option**

Before you start removing apps, check if your Android device allows you to disable bloatware. Disabling an app will prevent it from running, but it will still occupy some storage space. To disable an app:

1. Go to **Settings** on your Android device.
2. Navigate to **Apps** or **Applications** (the exact name may vary depending on your device).
3. Scroll through the list of apps and select the bloatware app you want to disable.
4. Tap the **Disable** or **Turn Off** option if available.

**Step 2: Use ADB (Android Debug Bridge)**

If your device doesn't allow you to disable bloatware, you can use the Android Debug Bridge (ADB), a command-line tool for Android development, to remove these apps. Here's how:

1. Install ADB on your computer. You can download it from the official Android Developer website.
2. Enable USB Debugging on your Android device. Go to **Settings > About phone** and tap on the **Build number** several times until you enable Developer Options. Then, in Developer Options, enable **USB Debugging.**
3. Connect your Android device to your computer using a USB cable.
4. Open a command prompt or terminal window on your computer.
5. Navigate to the directory where ADB is installed.
6. Run the command `adb devices` to ensure your device is recognized.
![]({{ 'assets/images/post/bloatware-1.jpg' | relative_url }})
7. Run the command `adb shell` to go inside shell to write commands
8. To uninstall a bloatware app, run the command `pm uninstall -k --user 0 <package_name>` , replacing <package_name> with the package name of the app you want to remove. 
 
![]({{ 'assets/images/post/bloatware-3.jpg' | relative_url }})

You can find the package name of an app in the URL of its Google Play Store page or by using the command `pm list packages --user 0`.
![]({{ 'assets/images/post/bloatware-2.jpg' | relative_url }})

**Step 3: Use Third-Party Apps**

If you prefer a more user-friendly approach, there are several third-party apps available on the Google Play Store that can help you remove bloatware without needing root access. Some popular options include "Package Disabler Pro" and "NoBloat Free." These apps provide a list of installed apps, and you can simply select the ones you want to remove.

Download and install one of these apps from the Play Store.
Open the app and grant the necessary permissions.
Select the bloatware apps you want to uninstall.
Follow the on-screen prompts to remove the selected apps.

**Step 4: Root Your Device (Advanced)**

If you're an advanced user and willing to take more control over your device, you can root your Android phone. Rooting grants you superuser access, allowing you to uninstall any app, including system apps. However, rooting can void your warranty and potentially cause security and stability issues, so proceed with caution and at your own risk.


Removing bloatware from your Android device can free up storage space, improve performance, and enhance your overall user experience. Depending on your comfort level with technical procedures and potential risks, you can choose the method that suits you best. Remember always to be cautious when uninstalling apps, and avoid removing any critical system apps that your device relies on for proper functioning.
