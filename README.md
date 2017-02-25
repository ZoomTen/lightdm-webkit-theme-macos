# lightdm-webkit-theme-macos
LightDM Webkit (&amp; WebKit2) greeter theme which is deliberately made to be macOS-esque.

##Source
This LightDM webkit greeter theme is based on [LightDM-Webkit-MacOSX-Theme](https://github.com/Wattos/LightDM-Webkit-MacOSX-Theme), with the visuals changed to approximate the more recent releases of macOS.

It can be applied on pretty much any Linux distro which includes LightDM and the WebKit / WebKit2 greeter either in the repositories or installed with distro.

##Installation
You will need to set LightDM as your display manager and you will need either of the LightDM WebKit greeters. (For Arch Linux that's `lightdm-webkit-greeter` or `lightdm-webkit2-greeter` from the AUR)

Then modify the LightDM configuration file in:

     /etc/lightdm/lightdm.conf
     
Change the `greeter-session` to `lightdm-webkit-greeter` or `lightdm-webkit2-greeter`, depending on which one you have installed.

You should have something similar to this on your config:

     [SeatDefaults]
     greeter-session=lightdm-webkit-greeter
     allow-guest=false

Next, install the theme by copying all the files in this repository to:

     /usr/share/lightdm-webkit/themes/macos

To apply the theme, modify `/etc/lightdm/lightdm-webkit-greeter.conf` or `/etc/lightdm/lightdm-webkit2-greeter.conf` so that it contains a line similar to this:

     webkit-theme = macos

Enjoy your aesthetic login screen :D

##Modifications
Among the modifications I've made include:
 - Restyled svg icons
 - Updated style
 - Added clock and title on header
 - A new font (based on Liberation Sans)

##Customizing
###Text on the greeter###
To add your own text, like "Welcome to your computer", you can open `index.html` in a text editor and modifying line 10, e.g.

    <div class="headertext"></div> <!-- you can change this to whatever -->
to

    <div class="headertext">Welcome to your computer</div>

###Custom background###
Simply replace `logon.png` in the `resources/img/` folder with a background of your choice. A sample background (made by me) is included.

##Demo
A demo of this theme can be viewed [here](https://zoomten.github.io/lightdm/macos/index.html)