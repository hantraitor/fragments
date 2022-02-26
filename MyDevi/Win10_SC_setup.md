[Pre-OSD]  
(optional){}:  

[System]  
{Settings} Region: log in with local admW..., and change "Country or region" to US and "Regional format" to Recommended English (US)  
{Settings} Language: (with admW...) move English (US) to top of "Preferred languages"  
{CP} Region: (with admW...) copy the international settings to system and new user accounts  
{CP} Region: change system locale to English (US)  
{CP} Power Options - Choose what closing the lid does: select "Do nothing" if plugged in when closing the lid  
{Settings} Wi-Fi: enable "Use random hardware addresses"  
{LANDesk Agent}: disable LANDesk Software Monitoring by changing service startup type to Disabled and rebooting the computer  
{"Default" profile}: some activities e.g. software deployment cause undesired Jump Lists cache, so check at times and delete them i.e. items in Recent also in AutomaticDestinations and CustomDestinations subfolders  

[User]  
{Settings} Display: change Scale size to suitable one like 125% _**#the very first job after waiting sometime during initial login**_  
{Settings} Date & time: show additional calendar "Traditional Chinese (Lunar)"  
{CP} File Explorer Options - View: enable "Show hidden files..."; disable "Hide empty drives"  
{NTFS for profile folder}: for security purpose, replace Administrators with "Local account and member of Administrators group" having Full control, and add user own adm... having Full control  
{SEP}: check subkeys of HKLM\SOFTWARE\Wow6432Node\Symantec\Symantec Endpoint Protection\AV\Exclusions\ScanningEngines\Directory\Admin to find excepted path suitable for use, under user profile for the best e.g. %[USER_PROFILE]%\AS_Prod\, and create that folder (%USERPROFILE%\AS_Prod\) being hidden  

[WSL]  
{CP} Windows Features: enable "Windows Subsystem for Linux"  
{Microsoft Store}: set "HKLM\SOFTWARE\Policies\Microsoft\WindowsStore /v RequirePrivateStoreOnly /t REG_DWORD /d 0" to get back public store temporarily _#immediately effective_  
{Kali Linux}: to escape AV scan which prevents some Kali tools, redirect Kali installation to an excepted folder by "mklink /j %LOCALAPPDATA%\Packages\KaliLinux.54290C8133FEE_ey8k8hqnwqnmg %USERPROFILE%\AS_Prod\AppData.Local.Packages.KaliLinux"  
{Kali Linux} Microsoft Store: install Kali Linux from public store  
