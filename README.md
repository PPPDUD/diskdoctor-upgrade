# diskdoctor-upgrade
The Disk Doctor Upgrade Utility is a simple utility used to upgrade Disk Doctor 1.0 and 2.0 flash drives to Disk Doctor 2.1 using a Windows machine.

Some non-Mojavesoft approved modifications that have been applied under earlier Disk Doctor versions might get deleted or broken during the upgrade to Disk Doctor 2.1. If this occurs, ask the creators of your modification for help.

Disclaimer: We are NOT responsible for any damages caused by misusage of this utility.

# Using the Disk Doctor Upgrade Utility
Download the Disk Doctor Upgrade Utility from the Releases tab, and decompress the downloaded ZIP archive.

Afterwards, run `upgrade.bat` as an administrator on a Windows machine (Windows S mode is not currently supported).

Then, press any key to begin the upgrade wizard.

Type in the drive letter for your Disk Doctor flash drive, followed by a colon (no spaces), and then press `ENTER` or `RETURN` on your keyboard. For example, drive letter D would be typed as `D:` in the wizard.

Next, sit back and relax while the utility performs the upgrade to Disk Doctor 2.1. This should take less than a minute.

Finally, press any key to close the wizard. Your Disk Doctor flash drive has been upgraded successfully.

# When things go wrong
<h2>Fixing Error 740</h2>
Error 740 is caused by not running the Disk Doctor Upgrade Utility as an admin. Carefully reread the prior section and try again.

<h2>Fixing  and Error: 0xc1420114</h2>
Go to your root directory (usually C:/ on Windows) and delete the folder named diskdoctor_temp.

<h2>Fixing Error 3</h2>
Error 3 occurs whenever you mistype the path to your flash drive. Carefully reread the prior section and try again.

<h2>Fixing Error 0xc1420117</h2>
Try closing all running programs.
After you do that, run the following command in the Command Prompt as an admin: dism /Unmount-Wim /MountDir:"%HOMEDRIVE%/diskdoctor_temp/" /discard & rmdir "%HOMEDRIVE%/diskdoctor_temp"

# To-do list
- Add better WIM compression to save space (medium-priority)
- Add cross-platform support (low-priority)
