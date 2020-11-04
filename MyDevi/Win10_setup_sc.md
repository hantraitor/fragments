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
