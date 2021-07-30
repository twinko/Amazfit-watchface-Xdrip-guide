# Welcome to the custom watchface tutorial / guide for Artems xdrip version for GRT 2e!

This guide will lead you throught all steps needed to adapt a watchface to fit xdrip. I'm not a nativ speaker, so feel free to suggest changes.
This guide focus on adapting an existing watchface to our need. If you are creative and skilled enough to create your own watchface, this tutorial will help you with the technical adaptions to use it in xdrip.

Please remember this guide is only for **GTR 2e**! A lot of things are similiar for different watches especially the GTR 2 and GTS 2(e). If you using this guide to create watchfaces for different watches please send text snipets via issue to help this guide suite different watches aswell. 

Main credit goes to **Artem Kovalenko** who made Amazfit GTR2, GTR2e, GTS2, GTS2e, GTR42, Bip, BIP S and GTR 47 possible! Moreover he helped me a lot to create my first own watchface.
#### Please support him here: https://www.patreon.com/xdrip_miband
You can read more about his projects regarding xdrip here: https://bigdigital.home.blog/

Moreover thanks to:

 - [**SashaCX75**](https://amazfitwatchfaces.com/forum/memberlist.php?mode=viewprofile&u=113690) helped creating the watchfaceditor 
 - all watchface creator

## Things you need

I'll use the following tools. You will need all of them. All of the tools below are free for personl use.

1. Windows OS
2. **WFE**: [AmazFit WatchFace editor 2 for Windows](https://amazfitwatchfaces.com/forum/viewtopic.php?p=8392#p8392)
3. **PS**: Photoshop (Version CS2 is available for free) https://archive.fo/255q5#selection-1663.0-1663.29
4. **WF**: A watchface. (next chapter)

## Look for a watchface you would like to use

If you are not creating your own watchface, you can have alook for watchfaces here: https://amazfitwatchfaces.com/gtr/top?compatible=GTR_2
Donwload the desired file. Please watch care about the watch the watchface was made for.

**Something very important:** 

 - The smaller the watchface the better. We'll come to this later but all pictures inlcuding the json file should'nt be bigger than 50kb. 
 - 50kb watchface size (raw pictures and the json) will result in a uploadtime of about 10 seconds and you dont want it to take it longer, because of battery life and you dont want to wait untill tomorrow.
 - That means less icons, less changing things (excluding numbers, and yes only numbers). 
 - Avoide watchfaces with gradients (when one color shifts to another). 
 - Remember we want to be able to easily read our Blood Glucose (BG), so we need to make some free space somewhere. I would calculate at least 1/3 of the watchface dedicated to all xdrip related information

# Guide / Tutorial

1. Download the whole folder of the latest version of the WFE (watchface editor), linked above. 
2. You can find the "download" buttom in the top right, we need the whole folder! 
3. After clicking download choose "direct download". It will download a file like "AmazFit_Watchface_Editor_2_v5.1.zip".
4. Extract the file
5. Open (in my case) "AmazFit_Watchface_Editor_2"
6. start "AmazFit_Watchface_Editor_2.exe"
7. Buttom right, choose "Unpack compressed bin"
8. Choose the watchface you downloaded earlier
9. Now you need to get familiar with the WFE.
10. I'll explane only the absolut basics. To learn more about the watchface editor and its possibilities, have a look here: https://amazfitwatchfaces.com/forum/viewtopic.php?f=14&t=1571
Direct link to english translation:  https://translate.google.com/translate?hl=ru&sl=ru&tl=en&u=https%3A%2F%2Fowagner.ru%2Famazfitgtr%2Fwfcreator%2Fwatchfaces_creator_lesson%2F
11. Go to the "Edit" tab and click throught the different options on the right side. 
12. Choose "Layer order" to define things like the date order (dd-mm-yy or mm-dd-yy).

Important hint:
Our most important goal is to reduce size. As written above we want to get below 50kb raw png files (inlcuding .json) .

Best way to reduce size:
- less pictures
- less colors (makes smaller picture files)
- use system font (a setting in the edit tab of WFE wherever it shows numbers.)

13. When you are done with your changes, save the watchface ("Edit" tab, bottom in the middel "save Json")

Things thet helped me a lot:
- have a look at the unpacked pictures, delete all the ones you dont need.
- You need to rename the files from 0001- xxxx You will have problems later if the files are not in a row. Its not possible to have one number in between missing. It should look like: 0001, 0002, ...... 0015.) You can use https://www.bulkrenameutility.co.uk/Download.php to bulk rename files.

14. Go to the folder including the json and all needed files on your computer.
15. Make a backup of th existing files and json
16. Open every file, one after another with PS.
17. Klick on Data--> Save for Web
18. In the new Window you should choose the following on the right side:
	- png-8
	- You can tinker a little bit and delete specific colors, that will reduce the size of the image even more. You can see the new file size in the bottem right
19. Save the file by overwriting (you made a backup earlier)
20. 

