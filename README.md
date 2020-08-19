# keyboard-layouts

Wide layouts for ABNT2 keyboards.
Tested on Microsoft® Wireless Multimedia Keyboard 1.1

## Instructions
1. Add the contents of one or more of the xkb keyboard layouts found in this repo to the appropriate file(s) in /usr/share/X11/xkb/symbols/

For example:
to use "English (US, wide, intl., with dead keys)", add the contents of us-intl-with-dead-keys-wide to /usr/share/X11/xkb/symbols/us
to use "Portuguese (Brazil, wide)" add the contents of br-wide to /usr/share/X11/xkb/symbols/br
to use "English (Colemak Mod-DH, wide)" add the contents of colemak-mod-dh-wide to /usr/share/X11/xkb/symbols/us

2. Add keyboard layout to /usr/share/X11/xkb/rules/xfree86.lst

For exambple one or more of the following lines depending on what keyboard layout(s) you want.
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
