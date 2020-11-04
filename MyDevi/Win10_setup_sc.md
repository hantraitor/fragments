[Pre-OSD]  
(optional){SEP}: prevent **managed** SEP from OSD by renaming sep_pkginstaller.vbs on bootstick (after OSD, manually install SEP unmanaged) or by renaming SyLink.xml of the actual SEP package on bootstick

[System]  
{Settings} Region: log in with local admW..., and change "Region" to US and "Regional format" to English (US)  
{Settings} Language: (with admW...) move English (US) to top of "Preferred languages"  
{CP} Region: (with admW...) copy the international settings to system and new user accounts _#issue (true on 1709): "Switch account" always sets Chinese input as default on welcome screen_  
{CP} Region: change system locale to English (US)  
{CP} Power Options - Choose what closing the lid does: select "Do nothing" if plugged in when closing the lid  
{Settings} Wi-Fi: enable "Use random hardware addresses"  
{LANDesk Agent}: disable LANDesk Software Monitoring by changing service startup type to Disabled and rebooting the computer  
(for unmanaged SEP){SEP}: add wanted exceptions, then import Sylink.xml from OSD bootstick  
{"Default" profile}: some activities e.g. software deployment cause undesired Jump Lists cache, so check at times and delete them i.e. items in Recent also in AutomaticDestinations and CustomDestinations subfolders  

[User]  
{Settings} Display: change Scale size to suitable one like 125% _**#the very first job after waiting sometime during initial login**_  
{Settings} Date & time: show additional calendar Traditional Chinese (Lunar)  
{CP} File Explorer Options - View: enable "Show hidden files..."; disable "Hide empty drives"  
{NTFS for profile folder}: for security purpose, replace Administrators with "Local account and member of Administrators group" having Full control, and add user own adm... having Full control  
{SEP}: check subkeys of HKLM\SOFTWARE\Wow6432Node\Symantec\Symantec Endpoint Protection\AV\Exclusions\ScanningEngines\Directory\Admin to find excepted path suitable for use, under user profile for the best e.g. %[USER_PROFILE]%\AS_Prod\, and create that folder (%USERPROFILE%\AS_Prod\) being hidden  
