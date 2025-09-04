
<div align="center">
  <h1 align="center">eOSdock-themeswitcher</h1>
  <h3 align="center">Theming for the dock of elementary OS 8 and beyond</h3>
</div>

  <a href="https://elementary.io">
    <img src="https://ellie-commons.github.io/community-badge.svg" alt="Made for elementary OS">
  </a>
  

- The 2000s: A very frutiger aero spin with all the 3D<br>
- Aqua: A old nostalgic MacOS. However from playing with zoom-magnification, i wont be able to redo that<br>
- Princess Eyebleed: something flashy and pastelly and bright because why not<br>

### I dont want all this i want the Classic plank theme !

One-liner. Paste this in a terminal
```bash
wget -O - https://raw.githubusercontent.com/teamcons/eOSdock-themeswitcher/refs/heads/main/themes/Classic.css >> ~/.config/gtk-4.0/gtk.css && killall io.elementary.dock
```

By default the dock is partially transparent, if you just want it opaque you can go<br>

```bash
echo "dock {opacity: 1;}" >>  ~/.config/gtk-4.0/gtk.css && killall io.elementary.dock
```



### Usage:

To set theme.css as the current dock theme
```bash
eOSdock-themeswitcher.sh ./themes/theme.css
```

No argument, to revert to default
```bash
eOSdock-themeswitcher.sh
```

you can then run
```bash
killall io.elementary.dock
```
to restart the dock. Or log out and in again

The file doesnt overwrite gtk.css, and reverts to default without leaving anything else.<br>
This is per user, and does not require sudo

I would do the killall in the script if somehow that didnt crash my session everytime i tried

Application.css is the default. It is taken from elementaryOS source code itself and is present as example
https://github.com/elementary/dock/blob/main/data/Application.css

Feel free to submit pull requests with your themes. Im happy to host neat stuff

### I just want to set the transparency
Also i did another to set transparency. It overrides whatever value a theme may set if you call it afterward
```bash
eOSdock-set-transparency.sh
```
<br>
Give any integer between 0 and 100.<br>
Any other value just reset to default (60)<br>
<br>
<br>

By default the dock is partially transparent, if you just want it opaque you can go.<br>

```bash
echo "dock {opacity: 1;}" >>  ~/.config/gtk-4.0/gtk.css && killall io.elementary.dock
```



### THEMES

Classic</br>
Attempt at mimicking the old Plank dock. It isnt complete, but damn good looking.</br>
<img src="https://github.com/teamcons/eOSdock-themeswitcher/blob/main/assets/Classic.png"/>


Stellas Tweaks</br>
Shadows behind icons. Accent color in running indicator. Icon up on hover.</br>
<img src="https://github.com/teamcons/eOSdock-themeswitcher/blob/main/assets/Stellas%20Tweaks.png"/>

The 2000s</br>
An attempt at funky 3D.</br>
<img src="https://github.com/teamcons/eOSdock-themeswitcher/blob/main/assets/The%202000s.png"/>

Whatever</br>
I dont know. It looks neat.</br>
<img src="https://github.com/teamcons/eOSdock-themeswitcher/blob/main/assets/Whatever.png"/>

Pinstripes - By <a href="https://github.com/t3rminus" target="_blank">t3rminus</a></br>
Lots of lines, similar to early Mac OS X.</br>
<img src="https://github.com/teamcons/eOSdock-themeswitcher/blob/main/assets/Pinstripes.png"/>
