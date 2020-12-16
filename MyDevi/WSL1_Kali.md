[Upgrade at first use]  
sudo apt-get update  
sudo apt-get dist-upgrade  

[Basic commands, Kali core]  
sudo apt-get install man-db  
sudo apt-get install kali-linux-core  
sudo apt-get install kali-desktop-core  

[DE - Xfce]  
sudo apt-get install kali-desktop-xfce  

sudo apt-get install xfce4  

[Access to DE - xrdp]  
sudo apt-get install dbus-x11 xrdp  
sudo sed -i -e 's|^port=3389$|port=tcp://.:13389|g' /etc/xrdp/xrdp.ini  
sudo /etc/init.d/xrdp start  
