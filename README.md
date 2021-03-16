### https://github.com/Tho#re-Krug/Flash-CHIP
### https://medium.com/@0x1231/nextthingco-pocket-c-h-i-p-flashing-guide-3445492639e
# flashpocketchip

![image1](https://d500.epimg.net/cincodias/imagenes/2015/05/08/gadgets/1431080878_711283_1431081013_noticia_normal.jpg)

Flashing Process for the C.H.I.P and PocketC.H.I.P Computer

Must be used Ubuntu I tested with Kali and dont works best option Ubuntu 16

- Install some apps
> apt-get -y install git android-tools-fastboot sunxi-tools u-boot-tools make gcc curl wget
- Clone repository https://github.com/linux-sunxi/sunxi-tools.git
> git clone --branch v1.4.1  https://github.com/linux-sunxi/sunxi-tools.git && cd sunxi-tool && make install-all install-misc && cd ../ && ./Flash.sh
- Choose an option and wait
> I choose gnf

# On Pocket C.H.I.P
![image1](https://www.home-assistant.io/images/blog/2016-07-pocketchip/pocketchip-logo.png)
- Change obsolete sources
> nano /etc/sources.list
- Comment nexthing.co repo and add new repos
> #deb http://opensource.nextthing.co/chip/debian/repo jessie main
>
> deb http://chip.jfpossibilities.com/chip/debian/repo jessie main
> deb http://chip.jfpossibilities.com/chip/debian/pocketchip jessie main
> deb http://archive.raspbian.org/raspbian jessie main contrib non-free
- Download other needed apps for touch screen and other stuff.
> apt-get upgrade --force-yes && apt-get install wget curl git htop net-tools vala-terminal xfce4-genmon-plugin xinput-calibrator software-properties-common apt-transport-https --force-yes && wget https://raw.githubusercontent.com/ALLGray/PocketDesk/master/Scripts/keyboard.sh && chmod +x keyboard.sh && ./keyboard.sh && wget https://raw.githubusercontent.com/ALLGray/PocketDesk/master/Scripts/touchscreen.sh && chmod +x touchscreen.sh && ./touchscreen.sh && git clone https://github.com/editkid/chip-battery-status && cd chip-battery-status && ./install.sh

- Note: Follow the instructions from here [ https://github.com/editkid/chip-battery-status/blob/master/README.md ]

- Right-click (or Ctrl-click) on an existing panel item, e.g your clock. Choose Panel > Add New Items...
![image1](https://miro.medium.com/max/353/1*MNH44UcNhoHMk-DbKLT6QA.png)
- Select Generic Monitor from the list and hit Add
![image2](https://miro.medium.com/max/356/0*nJ0VnvGAe3xQsFt8.png)
- You’ll see (genmon) xxx appear in your panel. Right-click (or Ctrl-click) it and choose Properties
![image3](https://miro.medium.com/max/205/0*8vuHNnsiv1rB9Yws.png)
- In the Command field enter chip-battery-xfce-genmon and for the Period (s) enter 5. Hit Close
![image4](https://miro.medium.com/max/348/0*F_J3FMwO1lue58IY.png)
- All Done.



