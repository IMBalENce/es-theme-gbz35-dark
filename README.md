# Gameboy Zero 3.5" Dark Theme for EmulationStation

[Click here for the original Light Theme](https://github.com/rxbrad/es-theme-gbz35)

![System Select Screen](http://i.imgur.com/Ijk4hZw.png) ![Detailed Game List](http://i.imgur.com/bf5fAgd.png) ![Basic Game List](http://i.imgur.com/xnpbati.png) ![Detailed Game List #2](http://i.imgur.com/7lOMjn0.png)

This theme pulls heavily from the [Carbon](https://github.com/RetroPie/es-theme-carbon), [Spare](https://github.com/mattrixk/es-theme-spare), and [SimpleBigArt](https://github.com/robertybob/es-theme-simplebigart) themes.  It is optimized for resolutions up to 640x480 on small 4:3 screens (like the 3.5" screens commonly used in Gameboy Zero builds).  It also works on 16:9 screens but you will notice that the background art is stretched when viewing in this aspect.

Changelog
-----------

- Update #3 - Jul 18, 2017: Fixed clipping at the bottom of the gamelist at certain resolutions
- Update #2 - Jul 18, 2017: Added c64, colecovision, intellivision, kodi, & ti99
- Update Jul 18, 2017: Added favorite, all games, recently played and custom-collections functionality
- Update Jul 17, 2017: Added support for video previews (be sure you're on the latest version of RetroPie, and note that the Pi Zero apparently struggles with video previews in RetroPie, so you may only want to scrape videos if you have a Pi2 or Pi3 in your GBZ); fixed Retropie menu screen theme
- Update Feb 9, 2017: Added dark theme and Dosbox section to theme
- Update Dec 16, 2016: Added Child-friendly EmulationStation Icon support in the detailed view
- Update Oct 4, 2016: I tweaked the Basic View to show an 8th game on the screen, and colorized the selected game on the list to match the current system's theme.

Installation (using Samba share & Windows PC)
-----------

Use the green button at the top of this Git to download the theme as a ZIP file.

You will need to connect the Pi Zero to Wifi.  Then, from another computer on the same WiFi network, SSH in (use Putty on PCs).  The default username is 'pi' and default password is 'raspberry'.

Now modify the permissions on the themes folder so you can copy themes to it over Wifi.
```
sudo chmod 0777 /etc/emulationstation/themes
```

Next, add the themes folder to the list of Samba shares
```
sudo nano /etc/samba/smb.conf
```
Scroll to the end of the file and add the following lines:
```
[themes]
comment = themes
path = "/etc/emulationstation/themes/"
writeable = yes
guest ok = yes
create mask = 0644
directory mask = 0755
force user = pi
```

Hit Ctrl-X, and overwrite the original file.

Once you're out of nano, reboot your Pi.
```
sudo reboot
```

After you've rebooted, you should be able to access the themes folder on your RETROPIE machine in Windows through File Explorer.  If asked for a username and password, the defaults are 'pi' & 'raspberry'.

![alt tag](http://i.imgur.com/B3IsFFW.png)

Open the ZIP that you downloaded here, and copy the 'es-theme-gbz35-dark' folder inside that ZIP over to the 'themes' folder on RETROPIE.

![alt tag](http://i.imgur.com/G7YTaMe.png)

The name of the folder you just copied is how it's listed in RetroPie.  Once it's copied over, I like to rename the folder to 'gbz-35-dark', but that's just me.

Restart EmulationStation on your Pi, and you should be able to switch to this theme in the UI Settings.

![alt tag](http://i.imgur.com/vbATdHH.png)
