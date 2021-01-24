# edkins-shanghainese-ime
An IME for Shanghainese, using Edkins romanisation.

How to use:
IF YOU HAVEN'T ALREADY INSTALLED RIME (Windows only):
1.	Make sure RIME is installed. Here's their website: https://rime.im/ . Make sure you get the right one: Weasel is for Windows, Squirrel's for MacOS. 
2.	Download the files you want from github/#resources etc., and move them into the Rime folder in the C:\Users\[username]\AppData\Roaming\Rime branch. You'll notice that there are other yaml files there, named dict or schema files. These belong to the default IMEs that come with RIME, like Pinyin input. I think Bopomofo input is there too.
3.	Create a text file in Notepad named 'default.custom.yaml'. Copy everything here into it:
```
customization:
  distribution_code_name: Weasel
  distribution_version: 0.14.3
  generator: "Rime::SwitcherSettings"
  modified_time: "Wed Jun 24 21:23:10 2020"
  rime_version: 1.5.3
patch:
  schema_list:
    - {schema: luna_pinyin}
    - {schema: luna_pinyin_simp}
    - {schema: luna_pinyin_fluency}
    - {schema: bopomofo}
    - {schema: bopomofo_tw}
    - {schema: cangjie5}
    - {schema: stroke}
    - {schema: terra_pinyin}
    - {schema: luna_quanpin}
    - {schema: bopomofo_express}
    - {schema: cangjie5_express}
    - {schema: luna_pinyin_tw}
```
Plus:
    `- {schema: [schema_id of whatever IME you want to use – found in schema file]}`

directly underneath (omit the square brackets). Make sure to save this file and re-deploy afterwards if you change this file in any way whatsoever (see step 6)。

4. Save this in the same RIME folder (that is, the one in Appdata branch mentioned in Step 3, and ONLY this folder).

5. Switch to RIME input by changing your input language. On Windows (if you're typing in English), you click on the box which says ENG to get the list; on Mac you click on the flag or something (sorry, I've never used Mac before, the blasted thing).
 

6. Right-click on the silver button with either an A or an 中 on it, to get this menu:
 
You need to click on the second option from the bottom, the one which says '重新部署 (R)' to deploy these changes. (NB: every time you edit the files in the Appdata folder, you MUST deploy afterwards. This is necessary for Rime to acknowledge these changes.)

7. Press Ctrl + ` to get this menu:

 

Click on the option you want. The name of your desired IME will show up here in Han characters. If you don’t know what name to look for, go to the schema file of your desired IME and look for whatever comes after ‘name:	’

(8.) I think the default setting is traditional characters, but if you want simplified, click on the second option in the menu above (西/半/漢/。) to get this menu:

 
Click on the circled option to switch. If you want to return to traditional, repeat this process if you're in simplified right now.

If you don't know the romanisation for a word, look for it in the dict.yaml file of the IME you’re using in the Appdata branch, using the Find function (Ctrl + F) with 'Wrap around' ticked.

Questions? Problems? Please let me know; I'll be more than happy to help. Here's our Discord server: https://discord.gg/2qRymM7KFY
