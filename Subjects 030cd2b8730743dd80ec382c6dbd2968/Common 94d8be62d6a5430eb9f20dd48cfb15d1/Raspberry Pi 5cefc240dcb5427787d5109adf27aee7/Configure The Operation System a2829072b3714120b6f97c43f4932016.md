# Configure The Operation System

Before you can start programme, it's best to configure the Raspberry Pi with the latest software and required software.

![https_lh3.googleusercontent.com-i7JYVVAps0MWWNR85xDlaIAAAAAAAAMuk9_vub_BtBH8gYc7M48HHxJWFqgHmbX83ACLkCGAYYCws0Screenshot2Bfrom2B2017-07-102B20-05-57.png](Configure%20The%20Operation%20System%20a2829072b3714120b6f97c43f4932016/https_lh3.googleusercontent.com-i7JYVVAps0MWWNR85xDlaIAAAAAAAAMuk9_vub_BtBH8gYc7M48HHxJWFqgHmbX83ACLkCGAYYCws0Screenshot2Bfrom2B2017-07-102B20-05-57.png)

<aside>
<img src="https://www.notion.so/icons/list_orange.svg" alt="https://www.notion.so/icons/list_orange.svg" width="40px" /> $\utilde {\color{black} \fcolorbox{darkorange}{darkorange}  {Table of Contents}}$

</aside>

## **Update Software and Configuration**

Run the following commands at the terminal

```bash
mkdir Programming
cd Programming
git clone http://github.com/Lake-Tuggeranong-College/RPi
cd RPi
chmod +x rpi-setup.sh
sudo ./rpi-setup.sh
```

This may take a while. Sit back, relax.

At the end of the process, the Raspberry Pi will need to reboot.

## **If the Date & Time is not correct**

Ensure that ntpdate is installed and configured correctly.

```bash
sudo apt-get install ntpdate
sudo service ntp stop
sudo ntpdate 203.62.5.5
sudo service ntp start
```