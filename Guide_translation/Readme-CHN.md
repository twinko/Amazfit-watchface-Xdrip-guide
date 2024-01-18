# 欢迎来到Artems xdrip版本的GRT 2e的自定义手表界面教程/指南!

本指南被自动翻译成。
- 中文(CHN) 
- 德文 (DE)
- 西班牙语 (ES)
- 法语 (FR)
- 意大利语 (IT)
- 俄语(RU)
我只讲德文和英文，所以如果你要联系，请用英文。

本指南将引导你完成所有的步骤，以适应xdrip的手表界面。我不是一个本地人，所以请随时提出修改意见。
本指南的重点是根据我们的需要改编现有的手表界面。如果你有足够的创造力和技能来创建你自己的手表界面，本教程将帮助你进行技术调整，以便在xdrip中使用它。

请记住本指南只适用于**GTR 2e**! 对于不同的手表，尤其是GTR 2和GTS 2(e)，很多东西是相似的。如果你使用本指南为不同的手表创建手表表面，请通过问题发送文本剪贴，以帮助本指南也适用于不同的手表。

主要归功于**Artem Kovalenko**，是他使Amazfit GTR2, GTR2e, GTS2, GTS2e, GTR42, Bip, BIP S和GTR 47成为可能！此外，他还帮助我创建了很多的手表。此外，他还帮助我创建了我的第一个自己的手表表面。
#### 请在这里支持他：https://www.patreon.com/xdrip_miband
你可以在这里阅读更多关于他在xdrip方面的项目：https://bigdigital.home.blog/

此外，还要感谢。

 - [**SashaCX75**](https://amazfitwatchfaces.com/forum/memberlist.php?mode=viewprofile&u=113690)帮助创建了watchfaceditor。
 - 所有watchface的创建者


> 

### 观察面示例


在文件夹[01-WF-MD225-Version3-xdrip-ready]（https://github.com/twinko/GTR-2-WF-Xdrip-EN/tree/main/01-WF-MD225-Version3-xdrip-ready
"01-WF-MD225-Version3-xdrip-ready"），你会发现一个自定义的watchface的最终产品。我将在这里链接一个不同的资源库，其中有我稍后创建的不同的手表界面。

**如果你创建了你自己的界面，请与其他人分享。我们可以把它们收集在一个仓库里，请随时通过问题联系我。


## 你需要的东西

我将使用以下工具。你将需要所有这些工具。以下所有的工具都是免费供个人使用的。

1. Windows操作系统
2. **WFE**。[AmazFit WatchFace editor 2 for Windows](https://amazfitwatchfaces.com/forum/viewtopic.php?p=8392#p8392)
3. **PS**: Photoshop（CS2版可免费使用） https://archive.fo/255q5#selection-1663.0-1663.29
5. **WF**: 一个手表面。(下一章)
6. 下载整个资源库，我们稍后将需要 "指南 "文件夹中的一些文件。你可以通过点击本页顶部的 "代码 "按钮，选择 "下载ZIP "来下载这个资源库。

##寻找你想使用的手表界面

如果你不创建你自己的手表界面，你可以在这里寻找手表界面：https://amazfitwatchfaces.com/gtr/top?compatible=GTR_2
下载所需的文件。请注意该表面是为哪只手表制作的。

**有一点非常重要：**。

 - 手表表面越小越好。我们稍后会讨论这个问题，但是所有的图片，包括json文件，都不应该大于50kb。
 - 50kb的界面大小（原始图片和json）将导致大约10秒的上传时间，你不希望它花费更长的时间，因为电池的寿命，你不希望等到明天。
 - 这意味着减少图标，减少变化的东西（不包括数字，是的，只有数字）。
 - 避免使用渐变色的手表表面（当一种颜色转移到另一种颜色时）。
 - 记住，我们希望能够很容易地读出我们的血糖（BG），所以我们需要在某个地方腾出一些空间。我计算了一下，至少有1/3的手表表面专门用于显示所有与xdrip有关的信息

# 1. 指南/教程

1. 下载上面链接的最新版本的WFE（watchface编辑器）的整个文件夹。
2. 你可以在右上方找到 "下载 "按钮，我们需要整个文件夹! 
3. 点击下载后，选择 "直接下载"。它将下载一个类似 "AmazFit_Watchface_Editor_2_v5.1.zip "的文件。
4. 4.提取该文件
5. 打开（在我的例子中）"AmazFit_Watchface_Editor_2"。
6.启动 "AmazFit_Watchface_Editor_2.exe"。
7. 右键，选择 "解压缩的bin"
8. 选择你之前下载的手表界面
9. 解压后的表面可以在这里找到： ...\AmazFit_Watchface_Editor_2\Watch_face
10. 现在你需要熟悉一下WFE。
11. 我将只阐述绝对的基础知识。要了解更多关于watchface编辑器和它的可能性，请看这里：https://amazfitwatchfaces.com/forum/viewtopic.php?f=14&t=1571
直接链接到英文翻译：https://translate.google.com/translate?hl=ru&sl=ru&tl=en&u=https%3A%2F%2Fowagner.ru%2Famazfitgtr%2Fwfcreator%2Fwatchfaces_creator_lesson%2F
12. 进入 "编辑 "标签，点击右侧的不同选项。
13. 13. 选择 "图层顺序 "来定义诸如日期顺序（dd-mm-yy或mm-dd-yy）的东西。

> **重要的提示：**。
> 我们最重要的目标是缩小尺寸。如上所述
> 以上我们希望得到低于50kb的原始png文件（不包括.json）。
> 
> 减少尺寸的最佳方法。
> - 更少的图片
> - 减少颜色（使图片文件更小）。
> - 使用系统字体（在WFE的编辑选项卡中，凡是显示数字的地方都有设置。


14. 当你完成了你的修改，保存手表界面（"编辑 "选项卡，在中间的底部 "保存Json"）。

> **对我帮助很大的事情是：**。
> - 图片0001.png始终是背景。通常情况下，有必要调整背景以适应葡萄糖图和所有需要的数据。用Photoshop或其他程序来做。
> - 看一下解压后的图片，删除所有你不需要的图片。
> - 你需要把文件从0001- xxxx重新命名，如果文件不在一个行里，以后会有问题。它不可能有一个
> 数字之间的缺失。它应该看起来像。0001, 0002, ......
> 0015.) 你可以使用https://www.bulkrenameutility.co.uk/Download.php 来批量重命名文件。

15. 进入包括json和你电脑上所有需要的文件的文件夹。
16. 16. 对现有的文件和json做一个备份。

## 1.1 编辑你的表脸背景
如果你的手表表面有一个普通的颜色，可以在WFE中编辑它。但你需要创建一张图片，所有的xdrip日期都放在上面，所以在PS中创建一个颜色匹配的图片，并跳过下面的部分，在那里我描述如何切割图片。

17. 在PS中打开0001.png（你的背景图片）。
18. 进入Picture-->Mode，把它改回RGB。
19. 按 "M "选择 "直角工具"，选择你想显示xdrip数据的部分。
![#**PS_cut_xdrip_part_01.PNG**](https://raw.githubusercontent.com/twinko/GTR-2-WF-Xdrip-EN/main/Guide/PS_cut_xdrip_part_01.PNG)

20. 在里面点击右键，选择 "通过切割分层"
21. 将此文件保存为PS文件(.psd)
22. 在图层1上点击右侧（图层）的眼睛图标，隐藏图片的其他部分
![## **PS_cut_xdrip_part_02.PNG**](https://raw.githubusercontent.com/twinko/GTR-2-WF-Xdrip-EN/main/Guide/PS_cut_xdrip_part_02.PNG)
23. 按 "c "键，使用切割工具
24. 把图片切成你的手表表面视觉部分的大小。
25. 按回车键确认，或按上面的复选键
26. 现在将其保存为**my_image.png**。
27. 打开保存的psd文件，对手表表面的其他部分做同样的事情，这样我们就有了背景图片，分成了两个文件。


### 1.1.1 减少图像大小
28. 用PS打开每个文件，一个接一个。
29. 点击数据-->保存为网络
30. 在新的窗口中，你应该在右边选择以下内容。
	- png-8
	- 你可以稍微修补一下，删除一些特定的颜色，这将进一步减少图片的大小。你可以在右下角看到新的文件大小
	- 文件需要是png! 
	- 如果你的图片周围出现了奇怪的边框。
		- 转到图片，模式，并在保存为网络之前将其改为 "索引的颜色"。
31. 通过覆盖来保存文件（你之前做了一个备份）。我没有找到一次对所有文件都这样做的方法，如果你知道怎么做，请告诉我。

### 1.1.2 将my_image.png放在WF的适当位置。
32. 现在再次打开WFE，你应该注意到，我们的手表表面中间有一个切口。(如果没有，请将你的切口图片保存为背景图片）。)
33.导航到编辑-->活动-->脂肪燃烧-->图标
34. 复制下面的图片到这里。## GTR-2-WF-Xdrip-EN/[指南](https://github.com/twinko/GTR-2-WF-Xdrip-EN/tree/main/Guide)/**0099.png**它只有一个像素。我们以后会通过代码用my_image.png替换它。但这为我们节省了大量的watchface尺寸。
35. 现在你需要把它放在我们切口的左上角。要找到正确的坐标，请阅读下面的主题（如何在PS中找到正确的坐标）。

## 1.2 准备好最终的手表表面
到目前为止，你应该在1个文件夹中拥有什么。
- 你用WFE创建的json文件
- 所有需要的WF文件，最大限度地缩小尺寸
- my_image.png，最大限度地缩小尺寸。
--> 我们正在接近你的最终WF:)

36. 导航到....\AmazFit_Watchface_Editor_2\Tools。
37.在这个文件夹中按住shift+右键
38. 选择 "在这里打开Powershell窗口"
39. 要打包你的json，你只需要导航到tools文件夹并执行这样的命令  
`in.exe --gtr2 47 --file config-file.json` 其中config-file.json是json的位置。
	- 我遇到了一些麻烦，需要在main.exe后面添加整个路径，所以它是这样的。
		- C:\Users\twinko\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Tools\main. exe --gtr2 47 --file C:\Users\TwinkosTower\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Watch_face\gtr2-g7en-colormix03-346659-994092c337\Small\WF_2_V01.json`
40. 因此，你应该收到一个解压的bin文件。这个文件你将需要在xdrip中使用。Xdrip将把所需的资源注入该文件，并对其进行压缩，然后将其发送给watch。
41. 将bin文件重命名为：my_watchface.bin
42. 创建一个新的文件夹，放入以下文件。
- 我们创建的my_watchface.bin
- my_image.png



## 1.3 编辑config.json

config.json定义了在my_image.png上显示哪些xdrip数据以及如何显示。它与WFE创建的json不同，不要把它们混为一谈!

Artem创建的原始config.json链接在这里。
https://github.com/twinko/GTR-2-WF-Xdrip-EN/blob/main/Guide/config.json
你之前下载了版本库，从Guide文件夹中获取文件吧



> **需要知道的一般事项：**
> - 这个config.json只与my_image.png有关。
> - 所以如果我们谈论坐标（x和y），它是基于my_image.png和它的总尺寸，而不是整个watchface。
> - 阅读Artems关于对齐的帖子：https://github.com/bigdigital/xDrip-miband/issues/5#issuecomment-878008056
> - text_align: "右" 
> - 你需要从右面开始计算像素
> - 所以如果读到：x: 100，文本对齐方式为右，从图片的右边开始计算100像素就是元素的位置

### 1.3.1 如何在PS中找到正确的坐标
43. 在PS中打开my_image.png
44. 按F8键，会出现一个小的信息窗口
45. 如果你在图片上移动鼠标，你会看到X和Y数字的移动。

### 1.3.2 config.json的解释
46. 用记事本打开config.json文件
47. 你会看到一些小的集群，这些集群是不言自明的。
48. 我们只需要编辑resource_to_replace, X, Y font_size或许bg_color的图形。

#### 1.3.2.1 resource_to_replace
49. 输入我们为Fat-burning-->Icon选择的图片的编号（如果你的第一张图片被命名为0001.png），将该编号减少1。该算法从0开始计算)

#### 1.3.2.2 "x" , "y" 和 "text_align" 。"右"。
50. 如 "如何在PS中找到正确的坐标 "中所述，你可以找到正确的位置来放置你的xdrip数据。

> **提示**。系统字体是 "Segoe UI"，所以在PS中按t来写文字，然后
> 在你的my_image.png中放上一些定义的文字，然后查找正确的
> 坐标。记住*x和y是左下角的第一个
>字母/数字*。不要用你写下的数字保存my_image.png。
> 写下的数字，这将在以后由Artems的魔法完成，我们在PS中这样做
>中找出正确的坐标，其他的就不说了。

51. 现在根据你的需要改变所有的坐标。
52. 注意：有一些值的巫师有以下一行：`"text_align": "text_align": "right", "对于这些值，我们有一个不同的坐标规则。*输入最后一个字母/数字的右座标*。

#### 1.3.2.3 "font_size"
输入你在PS中选择的相同字体大小。

### 1.3.3 保存config.json
54. 将config.json保存到包括my_image.png和my_watchface.bin的文件夹中（config.json不是my_config.json！）。


## 1.4 上传并测试它

55. 我们现在应该有一个包含以下文件的文件夹。
- config.json 
- my_image.png 
- my_watchface.bin  
56. 将这3个文件插入你智能手机上的xdrip文件夹中。
- 需要的xdrip文件夹可以在这里找到。
	- Internat storage/xdrip或
	- root/storage/emulated/0/xdrip
57. 在xdrip设置中启用自定义手表界面。
58. 完成了!

# 2. 脚注

如果你遇到了问题，请在这里开一个问题。请提前做好你自己的研究，我也只是一个在空闲时间做这个的普通人。
https://github.com/twinko/GTR-2-WF-Xdrip-EN/issues

如果你对如何改进这个指南或使它也适用于其他的watchface有建议，也可以写一个问题:)

我希望这个指南能对你有所帮助:)