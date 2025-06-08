# DKwerty
DKwerty is a modified version of Johan E. Gustaffssons 'Swerty' which making typing is swedish on an ANSI keyboard not be an absolute hellscape. I've adapted this for a danish layout as well by allowing for æøå, while keeping most of the ANSI standards.

## Personal layout (DKwerty - Classic)
As well as the direct fork of the original Swerty, the repo also features my own personal setup which i use from day to day. This layout leans more towards the Nordic ISO layout, with `<` and `>` being near the left shift, `"` being under `2`, and a few other tweaks for those who are used to using the classic ISO layout, but have found themselves needing to use ANSI for what ever reason.

## Installation
1. Clone the repo to your preferred location and copy the contents of 'dk' into the the bottom of the file at `/usr/share/X11/xkb/symbols/dk`

2. Go to 'usr/share/X11/xkb/rules/evdev.xml', locate `<name>dk</name>` and paste the following after `<variantList>`
```
<variant>
  <configItem>
    <name>dkwerty</name>
    <description>DKwerty</description>
  </configItem>
</variant>
```
1. In the same folder, open 'evdev.lst', locate `! variant` and paste the following underneath:
'''
dkwerty         dk: DKwerty
'''

4. You can now switch to the layout, either through your system settings, or by running the following command:

`setxkbmap -layout danish -variant dkwerty`
