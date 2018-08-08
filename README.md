# This has been discontinued in favor of Adaway version 4 which now has proper magisk systemless hosts support. Check out the [Support thread](https://forum.xda-developers.com/apps/magisk/magisk-unified-hosts-adblocker-t3559019) for more information

# Unified Hosts Adblock
Small adblock magisk module using unified host files from Steven Black [(Check out his github for more information)](https://github.com/StevenBlack/hosts)  
##Usage: 
#### First Enable Systemless Hosts in Magisk Manager
 - Open terminal then type:  
 `su`  
 `hosts`
 - Then follow the prompts to install host file of choice
##### OR
 - Open terminal and type:
 `su -c hosts arg1 arg2 arg3`
 - The script will apply your arguments all at once and close. Useful for automation purposes
 - For example: `su -c hosts m wr b`
 - Script will apply the master filter, then your regex whitelist, then your blacklist

#### Whitelist Instructions:
 - Create a text file on sdcard called "whitelist"
 - Either add exact lines you want remove to it -> Run hosts script and choose whitelist option
 - Or add regex for lines you want removed -> Run hosts script and choose whitelist regex option

#### Blacklist Instructions:
 - Create a text file on sdcard called "blacklist"
 - Add exact lines you want to remove it (do not include the 0.0.0.0 -> so for example: "facebook.com")
 - Run hosts script and choose blacklist option
 
#### To Remove Whitelist/Blacklist:
 - Just run hosts script and reinstall host file of choice

## Changelog
v3.7
  - EOF fix, should fix weird script errors. Thanks to Simon Dellenbach

v3.6
  - Put app in vendor if oreo
  - Have wget check certificates now since magisk busybox supports it
  - Attempt fix of weird busybox issues

v3.5
  - Updated app to v1.3

v3.4
  - Added app! (Thanks to @Megakaban_ at xda-developers)
  - Aliasing magisk busybox applets is glitchy, alias to actual busybox binary instead

v3.3
 - Use magisk busybox for hosts script (thanks to @Didgeridoohan at xda-developers for the idea)

v3.2
 - Update to magisk 15.0 template - all backwards compatibility now removed

v3.1
 - Remove old cache img support. All magisk installs are now located in /data. If your recovery doesn't have access to data, install via magisk manager
 - Fix uninstall
 - Add support for installing immediately after flashing magisk
 
v3.0
 - Update to template 1410 (magisk 14.2 compatibility) while maintaining backwards compatibility with 14.0

v2.9
 - Bug fixes (thanks to @Didgeridoohan at xda-developers)

v2.8
 - Updated to template v1400 for magisk v14

v2.7
 - Module will now uninstall if installer detects that the same version is already installed (thanks to @Didgeridoohan at xda-developers for the idea)

v2.6
 - Added argument capability to the script for easy automation (thanks to @Didgeridoohan at xda-developers for the idea)
 - Moved all temporary files to /cache, added unique prefix to all to prevent errors due to already existing files/folders

v2.5
 - Added fixes for samsung stock kernel users. Thanks to @jenslody at xda-developers for the fix
 - Fixed versioncode for magisk manager (thanks to @Nomelas on github for pointing it out)
 - Script now won't throw error if user inputs 'm' with other options (for example, inputting 'mfp' instead of 'fp' won't thrown an error) (thanks to @Didgeridoohan at xda-developers for the idea)

v2.4
 - Added cache workaround (oddly absent from magisk module template v4). Thanks to @g40q90 at xda-developers for troubleshooting

v2.3
 - Bug fixes for pixels

v2.2
 - Added blacklist feature

v2.1
 - Update for magisk 13.1 (NOTE: previous versions of magisk are no longer compatible)

v2.0
 - Moved included wget to out of system completely, hosts script is only file that will use it (prevents potential conflicts). Thanks to @rignfool and @veez21
 - Added wildcard support to whitelist
 
v1.9
 - Fixed last updated date change
 - Fixed whitelist option

v1.8
 - Added all possible letter combinations (order no longer matters)
 - Fixed up pixel support - still WIP (thanks to @ahrion at xda-developers)
 - Fixed Last Updated date change
 - Added update check notification at beginning of script

v1.7
 - Added pixel support

v1.6
 - Updated to magisk 11.6 (template v3)
 
v1.5
 - Updated to magisk 11.5 (template v2)
 
v1.4
 - Added date hosts were last updated (so you can determine if yours need updated)
 - Added whitelist feature
 - Minor restructuring of hosts script header

v1.3
 - Removed broken disable option and added directions for disabling hosts mod
 
v1.2
 - Made minor changes to Readme, removed support and donate links from module.prop, and removed changelog to meet standards of magisk manager 4.2 update

v1.1 
 - Changed from using curl to wget and built in wget (not all roms have curl apparently)

v1.0
 - Initial release
