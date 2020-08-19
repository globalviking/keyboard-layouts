# keyboard-layouts

## Wide layouts for ABNT2 keyboards.

Please note that the images do not reflect the layout exactly, it is missing a key due to a bug in the way Gnome renders the layout. It renders the keyboard as having an ISO layout. ABNT2 keybords have an extra key to the left of Right Shift, ";" on br-wide and "/" on us-wide)

Portuguese (Brazil, wide)
![Portuguese (Brazil, wide)](https://raw.githubusercontent.com/globalviking/keyboard-layouts/master/images/br-wide.png)

English (US, wide, intl., with dead keys
![English (US, wide, intl., with dead keys)](https://raw.githubusercontent.com/globalviking/keyboard-layouts/master/images/us-intl-wide.png)

The inspiration behind this came from wanting to customize my keyboard, without having to learn a completely new layout such as Dvorak, Colemak, etc. I wanted something easy to pick up and that my friends and family would be able to use without any problems.

The hands are spaced a bit further apart which helps ergonomics a tiny bit. More importantly, since the keys on the right side of the keyboard are shifted one key to the right; Backspace, Enter, Shift, CTRL and AltGr are a bit closer and the right pinky does not have to move as far.

I got inspiration to do this after reading this...
https://colemakmods.github.io/mod-dh/keyboards.html

Tested on Microsoft® Wireless Multimedia Keyboard 1.1 (Brazilian model)

### Instructions
1. Add the contents of one or more of the xkb keyboard layouts found in this repo to the appropriate file(s) in /usr/share/X11/xkb/symbols/

For example:
to use "English (US, wide, intl., with dead keys)", add the contents of us-intl-with-dead-keys-wide to /usr/share/X11/xkb/symbols/us
to use "Portuguese (Brazil, wide)" add the contents of br-wide to /usr/share/X11/xkb/symbols/br
to use "English (Colemak Mod-DH, wide)" add the contents of colemak-mod-dh-wide to /usr/share/X11/xkb/symbols/us

2. Add keyboard layout to /usr/share/X11/xkb/rules/xfree86.lst

For example one or more of the following lines depending on what keyboard layout(s) you want.
intl-wide       us: English (US, wide, intl., with dead keys)
wide            br: Portuguese (Brazil, wide)
colemak-mod-dh-wide us: English (Colemak Mod-DH, wide)

3. Add keyboard layout to /usr/share/X11/xkb/rules/evdev.xml

For example:
to add "English (US, wide, intl., with dead keys)"
<variant>
  <configItem>
    <name>intl-wide</name>
    <description>English (US, wide, intl., with dead keys)</description>
  </configItem>
</variant>

to add "Portuguese (Brazil, wide)", add the following lines to /usr/share/X11/xkb/rules/evdev.xml
<variant>
  <configItem>
    <name>wide</name>
    <description>Portuguese (Brazil, wide)</description>
  </configItem>
</variant>

to add "English (Colemak Mod-DH, wide)", add the following lines to /usr/share/X11/xkb/rules/evdev.xml
<variant>
  <configItem>
    <name>colemak-mod-dh-wide</name>
    <description>English (Colemak Mod-DH, wide)</description>
  </configItem>
</variant>
