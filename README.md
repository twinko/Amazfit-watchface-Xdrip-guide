# Welcome to the custom watchface tutorial / guide for Artems xdrip version for GRT 2e!

This guide will lead you throught all steps needed to adapt a watchface to fit xdrip. I'm not a nativ speaker, so feel free to suggest changes.
This guide focus on adapting an existing watchface to our needs. If you are creative and skilled enough to create your own watchface, this tutorial will help you with the technical adaptions to use it in xdrip.

If you have questions, feel free to open an issue. Please do your own research in advance, I'm also only a normal guy who does this in his freetime.

Please remember this guide is only for **GTR 2e**! A lot of things are similiar for different watches especially the GTR 2 and GTS 2(e). If you using this guide to create watchfaces for different watches please send text snipets via issue to help this guide suite different watches aswell. 

Main credit goes to **Artem Kovalenko** who made Amazfit GTR2, GTR2e, GTS2, GTS2e, GTR42, Bip, BIP S, GTR 47 and a lot of MiBands possible! Moreover he helped me a lot to create my first own watchface.
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

If you are not creating your own watchface, you can have a look for watchfaces here: https://amazfitwatchfaces.com/gtr/top?compatible=GTR_2
Donwload the desired file. Please care about the watch the watchface was made for.

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
9. The unpacked watchface can be found here: ...\AmazFit_Watchface_Editor_2\Watch_face
10. Now you need to get familiar with the WFE.
11. I'll explane only the absolut basics. To learn more about the watchface editor and its possibilities, have a look here: https://amazfitwatchfaces.com/forum/viewtopic.php?f=14&t=1571
Direct link to english translation:  https://translate.google.com/translate?hl=ru&sl=ru&tl=en&u=https%3A%2F%2Fowagner.ru%2Famazfitgtr%2Fwfcreator%2Fwatchfaces_creator_lesson%2F
12. Go to the "Edit" tab and click throught the different options on the right side. 
13. Choose "Layer order" to define things like the date order (dd-mm-yy or mm-dd-yy).

> **Important hint:** 
> Our most important goal is to reduce size. As written
> above we want to get below 50kb raw png files (inlcuding .json) .
> 
> Best way to reduce size:
> - less pictures
> - less colors (makes smaller picture files)
> - use system font (a setting in the edit tab of WFE wherever it shows numbers.)

13. When you are done with your changes, save the watchface ("Edit" tab, bottom in the middel "save Json")

> **Things thet helped me a lot:**
> - picture 0001.png is always the background. Normally it'S neccessary to adapt the background to fit a glucose graph and al the needed data. Use Photoshop for that or a different program
> - have a look at the unpacked pictures, delete all the ones you dont need.
> - You need to rename the files from 0001- xxxx You will have problems later if the files are not in a row. Its not possible to have one
> number in between missing. It should look like: 0001, 0002, ......
> 0015.) You can use https://www.bulkrenameutility.co.uk/Download.php to bulk rename files.

14. Go to the folder including the json and all needed files on your computer.
15. Make a backup of th existing files and json

### Editing your watchface background (only needed if its not a plain color)
If your watchface has a plain color, edit it in the WFE. But you'll need to create a picture, where all the xdrip date is placed on, so create a colormatching image in PS and skip the following part, where i describe how to cut the picture.

17. Open 0001.png (your background image) in PS
18. ddd
19. ddd
20. ddd
21. ddd
22. dd
23. dddd
24. d
25. d
26. d
27. d
28. d
29. d
30. d
31. 
32. Open every file, one after another with PS.
33. Klick on Data--> Save for Web
34. In the new Window you should choose the following on the right side:
	- png-8
	- You can tinker a little bit and delete specific colors, that will reduce the size of the image even more. You can see the new file size in the bottem right
	- Files need to be png! 
	- If you encounter a weird border around your images:
		-  go picture, Mode and change it to "indexed colors" before saving it for web
35. Save the file by overwriting (you made a backup earlier). I didnt found a way to do it to all files at once, let me know if you know how.
36. Now open up WFE again, see if everthing still works out.

## Preparing the final watchface

21. Navigate to ....\AmazFit_Watchface_Editor_2\Tools
22. hold shift+rightclick in this folder
23. Choose "Open Powershell Window here"
24. To pack your json you only need to navigate to tools folder and execute command like this  
`main.exe --gtr2 47 --file config-file.json` where config-file.json is a location to your json.
	- i had some trouble with that and needed to add to whole path infront of the main.exe so it was something liek this:
		- `C:\Users\twinko\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Tools\main.exe --gtr2 47 --file C:\Users\TwinkosTower\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Watch_face\gtr2-g7en-colormix03-346659-994092c337\Small\WF_2_V01.json`
25. As a result, you should receive a unpacked bin file. This file you would need to use in the xdrip. Xdrip will inject the required resource into this file, compress it and sent it to the watch.

## Putting everything together

26. Create a seperate folder
27. put in the following files and rename like shown below
- config.json 
- the image where the xdrip data should be displayed on --> my_image.png
- the uncompressed .bin we created with Powershell --> my_watchface.bin
28.  insert these 3 files into the xdrip folder on your smartphone 
- Needed xdrip folder is found here:
-   Internat storage/xdrip or
-   root/storage/emulated/0/xdrip
30. Enable custom watchface in xdrip settings.
