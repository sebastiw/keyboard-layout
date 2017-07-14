About
===
This keyboard layout is based on the US layout, but with some special keys:
Swedish åäö on altgr+[';
German üß on altgr+us
UK £ on altgr+3
EU € on altgr+e


How to install
===
1. Add the file "seba" to `/usr/share/X11/xkb/symbols/`

        $   sudo cp seba /usr/share/X11/xkb/symbols/

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

4. Choose Seba from "text entry settings"/keyboard layouts
   or do something like `setxkbmap -layout seba -option ctrl:nocaps -option lv3:ralt_switch`
   from terminal
