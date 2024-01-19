# Bienvenue sur le tutoriel / guide de customisation de watchface pour la version xdrip d'Artems pour GRT 2e !

Ce guide est traduit automatiquement en :
- Chinois (CHN) 
- Allemand (DE)
- Espagnol (ES)
- Français (FR)
- Italien (IT)
- Russe (RU)
Je ne parle que DE et EN, donc s'il vous plaît si vous entrez en contact, faites-le en anglais !

Ce guide vous guidera à travers toutes les étapes nécessaires pour adapter un watchface à xdrip. Je ne suis pas un locuteur natif, donc n'hésitez pas à suggérer des changements.
Ce guide se concentre sur l'adaptation d'un watchface existant à nos besoins. Si vous êtes assez créatif et compétent pour créer votre propre watchface, ce tutoriel vous aidera avec les adaptations techniques pour l'utiliser dans xdrip.

S'il vous plaît rappelez-vous que ce guide est seulement pour **GTR 2e** ! Beaucoup de choses sont similaires pour les différentes montres, en particulier pour les GTR 2 et GTS 2(e). Si vous utilisez ce guide pour créer des watchfaces pour différentes montres, veuillez envoyer des snipets de texte via issue pour aider ce guide à s'adapter aux différentes montres. 

Le crédit principal va à **Artem Kovalenko** qui a rendu possible Amazfit GTR2, GTR2e, GTS2, GTS2e, GTR42, Bip, BIP S et GTR 47 ! De plus, il m'a beaucoup aidé à créer ma première surface de montre personnelle.
#### Soutenez-le ici : https://www.patreon.com/xdrip_miband
Vous pouvez lire plus sur ses projets concernant xdrip ici : https://bigdigital.home.blog/

Merci également à :

 - **SashaCX75**](https://amazfitwatchfaces.com/forum/memberlist.php?mode=viewprofile&u=113690) qui a aidé à créer le watchfaceditor. 
 - tous les créateurs de watchface


> 

### Exemple de Watchface


Dans le dossier [01-WF-MD225-Version3-xdrip-ready](https://github.com/twinko/GTR-2-WF-Xdrip-EN/tree/main/01-WF-MD225-Version3-xdrip-ready
"01-WF-MD225-Version3-xdrip-ready") vous trouverez le produit final d'un watchface personnalisé. Je vais lier un autre dépôt ici avec un autre watchface que j'ai créé plus tard. 

**Si vous avez créé votre propre watchface, merci de le partager avec les autres. Nous pourrions les rassembler dans un repo, n'hésitez pas à me contacter via issue.**


## Choses dont vous avez besoin

Je vais utiliser les outils suivants. Vous aurez besoin de tous ces outils. Tous les outils ci-dessous sont libres pour une utilisation personnelle.

1. Système d'exploitation Windows
2. **WFE** : [AmazFit WatchFace editor 2 for Windows] (https://amazfitwatchfaces.com/forum/viewtopic.php?p=8392#p8392)
3. **PS** : Photoshop (la version CS2 est disponible gratuitement) https://archive.fo/255q5#selection-1663.0-1663.29
5. **WF** : Un watchface. (chapitre suivant)
6. Téléchargez le dépôt complet, nous aurons besoin de certains fichiers plus tard dans le dossier "Guide". Vous pouvez télécharger ce dépôt en cliquant sur le bouton "code" en haut de cette page et choisir "Télécharger ZIP".

## Recherchez un watchface que vous souhaitez utiliser

Si vous ne créez pas votre propre watchface, vous pouvez chercher des watchfaces ici : https://amazfitwatchfaces.com/gtr/top?compatible=GTR_2
Téléchargez le fichier désiré. Veuillez faire attention à la montre pour laquelle le cadran a été créé.

**Quelque chose de très important:** 

 - Plus le cadran est petit, mieux c'est. Nous y reviendrons plus tard mais toutes les images, y compris le fichier json, ne doivent pas dépasser 50kb. 
 - 50kb watchface taille (images brutes et le json) se traduira par un temps de téléchargement d'environ 10 secondes et vous ne voulez pas qu'il prenne plus longtemps, en raison de la vie de la batterie et vous ne voulez pas attendre jusqu'à demain.
 - Cela signifie moins d'icônes, moins de choses changeantes (à l'exception des chiffres, et oui seulement des chiffres). 
 - Évitez les interfaces de montres avec des gradients (lorsqu'une couleur passe à une autre). 
 - Rappelez-vous que nous voulons être en mesure de lire facilement notre glycémie (BG), nous devons donc laisser de l'espace libre quelque part. Je calculerais au moins 1/3 de la surface de la montre dédiée à toutes les informations relatives à xdrip.

# 1. Guide / Tutoriel

1. Téléchargez le dossier complet de la dernière version du WFE (éditeur watchface), lié ci-dessus. 
2. Vous pouvez trouver le bouton "download" en haut à droite, nous avons besoin du dossier entier ! 
3. Après avoir cliqué sur "download", choisissez "direct download". Cela va télécharger un fichier comme "AmazFit_Watchface_Editor_2_v5.1.zip".
4. Extraire le fichier
5. Ouvrez (dans mon cas) "AmazFit_Watchface_Editor_2".
6. lancez "AmazFit_Watchface_Editor_2.exe".
7. Bouton droit, choisir "Unpack compressed bin".
8. Choisissez le watchface que vous avez téléchargé plus tôt
9. Le watchface décompressé peut être trouvé ici : ...\AmazFit_Watchface_Editor_2\Watch_face
10. Maintenant, vous devez vous familiariser avec le WFE.
11. Je n'expliquerai que les bases absolues. Pour en savoir plus sur l'éditeur watchface et ses possibilités, jetez un coup d'oeil ici : https://amazfitwatchfaces.com/forum/viewtopic.php?f=14&t=1571
Lien direct vers la traduction anglaise : https://translate.google.com/translate?hl=ru&sl=ru&tl=en&u=https%3A%2F%2Fowagner.ru%2Famazfitgtr%2Fwfcreator%2Fwatchfaces_creator_lesson%2F
12. Allez dans l'onglet "Edit" et cliquez sur les différentes options sur le côté droit. 
13. Choisissez "Ordre des couches" pour définir des choses comme l'ordre des dates (dd-mm-yy ou mm-dd-yy).

> **Introduction importante:** 
> Notre objectif le plus important est de réduire la taille. Comme écrit
> ci-dessus, nous voulons obtenir moins de 50kb de fichiers png bruts (y compris .json).
> 
> La meilleure façon de réduire la taille :
> - moins d'images
> Moins de couleurs (pour des fichiers images plus petits)
La meilleure façon de réduire la taille : > - moins d'images > - moins de couleurs (pour réduire la taille des fichiers d'images) > - utiliser la police système (un paramètre dans l'onglet d'édition de WFE où les chiffres sont affichés)


14. Lorsque vous avez terminé vos modifications, sauvegardez le watchface (onglet "Edit", en bas au milieu "save Json").

> **Les choses qui m'ont beaucoup aidé:**
> - L'image 0001.png est toujours le fond. Normalement, il est nécessaire d'adapter le fond à un graphique de glucose et à toutes les données nécessaires. Utilisez Photoshop pour cela ou un autre programme
> Jetez un coup d'oeil aux images déballées, supprimez toutes celles dont vous n'avez pas besoin.
> - Vous devez renommer les fichiers de 0001 à xxxx Vous aurez des problèmes plus tard si les fichiers ne sont pas alignés. Il n'est pas possible d'avoir un
> Il n'est pas possible d'avoir un numéro entre deux fichiers manquants. Cela devrait ressembler à : 0001, 0002, ......
> 0015.) Vous pouvez utiliser https://www.bulkrenameutility.co.uk/Download.php pour renommer des fichiers en masse.

15. Allez dans le dossier comprenant le json et tous les fichiers nécessaires sur votre ordinateur.
16. Faites une sauvegarde des fichiers existants et de json.

## 1.1 Modification de l'arrière-plan du cadran de votre montre
Si votre cadran a une couleur unie, modifiez-la dans le WFE. Mais vous aurez besoin de créer une image, où toute la date xdrip est placée, donc créez une image de couleur assortie dans PS et sautez la partie suivante, où je décris comment couper l'image.

17. Ouvrez 0001.png (votre image de fond) dans PS.
18. Allez dans Picture-->Mode et changez-le en RGB.
19. Sélectionnez l'outil Angle droit en appuyant sur "M" et choisissez la partie où vous voulez que vos données xdrip soient affichées.
![##**PS_cut_xdrip_part_01.PNG**](https://raw.githubusercontent.com/twinko/GTR-2-WF-Xdrip-EN/main/Guide/PS_cut_xdrip_part_01.PNG)

20. Faites un clic droit à l'intérieur et choisissez "Couche par découpe".
21. Enregistrez ce fichier comme un fichier PS (.psd)
22. Cachez le reste de l'image en cliquant sur l'icône de l'œil sur le côté droit (Calques) sur le Calque 1
![## **PS_cut_xdrip_part_02.PNG**](https://raw.githubusercontent.com/twinko/GTR-2-WF-Xdrip-EN/main/Guide/PS_cut_xdrip_part_02.PNG)
23. Appuyez sur "c" pour utiliser l'outil de découpe
24. Découpez l'image à la taille de la partie visuelle de votre cadran de montre.
25. Appuyez sur la touche entrée pour confirmer ou sur la case à cocher en haut de la page.
26. Maintenant, enregistrez cette image comme **mon_image.png**.
27. Ouvrez le fichier psd sauvegardé et faites la même chose pour le reste du cadran de la montre, de sorte que nous avons l'image de fond, divisée en 2 fichiers.


### 1.1.1 Réduire la taille de l'image
28. Ouvrez chaque fichier, l'un après l'autre avec PS.
29. Cliquez sur Données--> Enregistrer pour le Web
30. Dans la nouvelle fenêtre, vous devriez choisir ce qui suit sur le côté droit :
	- png-8
	- Vous pouvez bricoler un peu et supprimer certaines couleurs, ce qui réduira encore plus la taille de l'image. Vous pouvez voir la nouvelle taille du fichier en bas à droite.
	- Les fichiers doivent être en png ! 
	- Si vous rencontrez une bordure bizarre autour de vos images :
		- allez dans Image, Mode et changez-la en "couleurs indexées" avant de la sauvegarder pour le web.
31. Sauvegarder le fichier en l'écrasant (vous avez fait une sauvegarde plus tôt). Je n'ai pas trouvé de moyen de le faire pour tous les fichiers à la fois, faites-moi savoir si vous savez comment.

### 1.1.2 Placez mon_image.png au bon endroit dans le WF.
32. Maintenant ouvrez WFE à nouveau, vous devriez remarquer, que nous avons une découpe au milieu de notre cadran. (si ce n'est pas le cas, enregistrez votre image découpée comme image de fond).
33. naviguez vers Edit--> Activity -->Fat-burning-->Icon
34. Copiez l'image suivante située ici : ## GTR-2-WF-Xdrip-FR/[Guide](https://github.com/twinko/GTR-2-WF-Xdrip-EN/tree/main/Guide)/**0099.png** elle ne fait que 1 pixel. Nous la remplacerons plus tard par mon_image.png via le code. Mais cela nous fait gagner beaucoup de taille de watchface.
35. Maintenant il faut le mettre dans le coin supérieur gauche de notre découpe. Pour trouver les bonnes coordonnées, lisez la rubrique suivante (Comment trouver les bonnes coordonnées dans PS)

## 1.2 Préparer le watchface final
Ce que vous devriez avoir jusqu'à présent dans 1 dossier :
- un json que vous avez créé avec WFE
- tous les fichiers WF nécessaires, de taille réduite au maximum
- mon_image.png, taille réduite au maximum.
--> nous nous rapprochons de votre WF final :)

36. Allez sur ....\AmazFit_Watchface_Editor_2\Tools
37. maintenez shift+clic droit dans ce dossier
38. Choisissez "Ouvrir la fenêtre Powershell ici".
39. Pour emballer votre json, il vous suffit de naviguer dans le dossier tools et d'exécuter la commande suivante  
`main.exe --gtr2 47 --file config-file.json` où config-file.json est l'emplacement de votre json.
	- J'ai eu quelques problèmes avec ça et j'ai eu besoin d'ajouter tout le chemin devant le main.exe donc c'était quelque chose comme ça :
		- `C:\Users\twinko\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Tools\main. exe --gtr2 47 --file C:\Users\TwinkosTower\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Watch_face\gtr2-g7en-colormix03-346659-994092c337\Small\WF_2_V01.json`
40. En conséquence, vous devriez recevoir un fichier bin décompressé. Vous devrez utiliser ce fichier dans xdrip. Xdrip injectera la ressource requise dans ce fichier, le compressera et l'enverra à la montre.
41. renommez le fichier bin en : my_watchface.bin
42. Créez un nouveau dossier, en mettant les fichiers suivants :
- le my_watchface.bin que nous avons créé
- mon_image.png

## 1.3 Édition du config.json

Le config.json définit, où sur mon_image.png, quelles données xdrip sont affichées et comment. Il est différent du json créé par le WFE, ne les confondez pas !

Le config.json original créé par Artem est lié ici :
https://github.com/twinko/GTR-2-WF-Xdrip-EN/blob/main/Guide/config.json
Vous avez téléchargé le référentiel plus tôt, récupérez le fichier dans le dossier Guide !



> **Choses générales à savoir:**
> - ce config.json est uniquement lié à mon_image.png
> - donc si nous parlons de coordonnées (x et y), c'est basé sur my_image.png et sa taille totale, pas sur l'ensemble du watchface.
> - lisez le post d'Artems sur l'alignement ici : https://github.com/bigdigital/xDrip-miband/issues/5#issuecomment-878008056
> - text_align : "right" (alignement du texte) 
> - vous devez compter les pixels en commençant par le côté droit
> - donc si on lit : x : 100 et que l'alignement du texte est à droite, il faut compter 100 pixels à partir du côté droit de l'image pour savoir où l'élément est placé.

### 1.3.1 Comment trouver les bonnes coordonnées dans PS ?
43. Ouvrez mon_image.png dans PS
44. Appuyez sur F8, une petite fenêtre d'information s'affiche.
45. Si vous déplacez votre souris sur l'image, vous verrez les nombres X et Y bouger. 

### 1.3.2 config.json expliqué
46. Ouvrez le fichier config.json avec le bloc-notes.
47. Vous voyez de petits groupes, qui s'expliquent d'eux-mêmes.
48. Nous avons seulement besoin d'éditer resource_to_replace, X, Y font_size peut-être bg_color du graphique.

#### 1.3.2.1 ressource_à_remplacer
49. mettez le numéro de l'image que nous choisissons pour Fat-burning-->Icon (si votre image de départ s'appelle 0001.png) réduisez le numéro par un. L'algorithme commence à compter avec 0)

#### 1.3.2.2 "x" , "y" et "text_align" : "right",
50. Comme décrit dans "Comment trouver les bonnes coordonnées dans PS", vous pouvez trouver la bonne position pour placer vos données xdrip. 

> **Introduction** : La police de caractères du système est "Segoe UI", donc appuyez sur t dans PS pour écrire du texte et > mettez du texte défuelt dans la police.
> pour écrire du texte, mettez du texte défectueux dans votre my_image.png et cherchez les bonnes coordonnées.
> coordonnées. Rappelez-vous que *x et y sont en bas à gauche de la première > lettre/chiffre*.
> lettre/chiffre*. Ne sauvegardez pas mon_image.png avec les nombres que vous avez
> Ne sauvegardez pas mon_image.png avec les chiffres que vous avez notés, cela sera fait plus tard par la magie d'Artems, nous le faisons dans PS.
> pour trouver les bonnes coordonnées, pas autre chose.

51. Maintenant, changez toutes les coordonnées selon vos besoins.
52. Attention : il y a des valeurs qui ont la ligne suivante : `"text_align" : "right",` pour celles-ci nous avons une règle différente pour les coordonnées. *Mettez la coordonnée Buttom droite de la dernière lettre/du dernier chiffre.*

#### 1.3.2.3 "font_size" (taille de la police)
53. mettez la même taille de police que vous avez choisie dans PS.

### 1.3.3 Sauvegarder le config.json
54. Sauvegardez le config.json dans le dossier comprenant mon_image.png et mon_watchface.bin (config.json et non mon_config.json !).


## 1.4 Téléchargement et test de l'application

55. Nous devrions maintenant avoir un dossier avec les fichiers suivants :
- config.json 
- mon_image.png 
- my_watchface.bin  
56. Insérez ces 3 fichiers dans le dossier xdrip de votre smartphone. 
- Le dossier xdrip nécessaire se trouve ici :
	- Internat storage/xdrip ou
	- root/storage/emulated/0/xdrip
57. Activez le watchface personnalisé dans les paramètres xdrip.
58. Terminé !

# 2. Note de bas de page

S'il vous plaît ouvrir un problème ici si vous rencontrez des problèmes. Veuillez faire vos propres recherches à l'avance, je ne suis aussi qu'un gars normal qui fait ça pendant son temps libre. 
https://github.com/twinko/GTR-2-WF-Xdrip-EN/issues

Si vous avez des suggestions sur la façon d'améliorer le guide ou de l'adapter à d'autres watchfaces, écrivez également un problème :)

J'espère que ce guide a été utile :)