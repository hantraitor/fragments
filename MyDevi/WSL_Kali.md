[Upgrade at first use]  
sudo apt-get update  
sudo apt-get dist-upgrade  

[Kali linux base]  
sudo apt-get install kali-linux-core  

[Kali GUI - Xfce]  
sudo apt-get install kali-desktop-core  

sudo apt-get install kali-desktop-xfce  

sudo apt-get install xfce4  
sudo apt-get install dbus-x11 xrdp  
sudo vi /etc/xrdp/xrdp.ini #port=3389 --> port=tcp://.:13389  
sudo /etc/init.d/xrdp start  

[Python]  
sudo apt-get install python3  
