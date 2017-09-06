About
===
This keyboard layout is based on the US layout, but with some special keys:

- Swedish åäö on `Lv3+[';`
- German üß on `Lv3+us`
- UK £ on `Lv3+3`
- EU € on `Lv3+e`
- Cyrillic alphabet on `Lv5`
- Caps Lock as Control (`ctrl`)


- Level 3 chooser is Alt-Gr (`ralt_switch`)
- Level 5 chooser is Lesser/Greater than (`lsgt_switch`)


How to install
===
1. Add the file "seba" to `/usr/share/X11/xkb/symbols/`

        $  sudo ln -s seba /usr/share/X11/xkb/symbols/

2. There is a number of files to modify in `/usr/share/X11/xkb/rules/`
   in file `base.lst`
   after the line where it says: `! layout`
   add a line `seba Seba`

   in file `base.xml`
   where `<layoutList>` begins
   add
```
       <layout>
          <configItem>
            <name>seba</name>
            <shortDescription>seba</shortDescription>
            <description>Seba</description>
            <languageList>
              <iso639Id>eng</iso639Id>
            </languageList>
          </configItem>
        </layout>"
```

3. Logout + login.

4. Set Seba keyboard layout

        $  setxkbmap -layout seba
