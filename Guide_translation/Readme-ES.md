# ¡Bienvenido al tutorial/guía de personalización de watchface para la versión xdrip de Artems para GRT 2e!

Esta guía está traducida automáticamente a:
- Chino (CHN) 
- Alemán (DE)
- Español (ES)
- Francés (FR)
- Italiano (IT)
- Ruso (RU)
Sólo hablo DE y EN, así que por favor, si te pones en contacto, hazlo en inglés.

Esta guía le llevará a través de todos los pasos necesarios para adaptar un watchface para adaptarse a xdrip. No soy un hablante nativo, así que siéntase libre de sugerir cambios.
Esta guía se centra en la adaptación de un watchface existente a nuestras necesidades. Si eres lo suficientemente creativo y hábil como para crear tu propio watchface, este tutorial te ayudará con las adaptaciones técnicas para utilizarlo en xdrip.

¡Por favor, recuerda que esta guía es sólo para **GTR 2e**! Muchas cosas son similares para diferentes relojes, especialmente el GTR 2 y el GTS 2(e). Si usted utiliza esta guía para crear watchfaces para diferentes relojes por favor envíe fragmentos de texto a través de la cuestión para ayudar a esta guía suite diferentes relojes aswell. 

El mérito principal es de **Artem Kovalenko** que hizo posible Amazfit GTR2, GTR2e, GTS2, GTS2e, GTR42, Bip, BIP S y GTR 47. Además, me ayudó mucho a crear mi primer watchface propio.
#### Por favor, apóyalo aquí: https://www.patreon.com/xdrip_miband
Puedes leer más sobre sus proyectos con respecto a xdrip aquí: https://bigdigital.home.blog/

Además, gracias a:

 - [**SashaCX75**](https://amazfitwatchfaces.com/forum/memberlist.php?mode=viewprofile&u=113690) ayudó a crear el watchfaceditor 
 - todo el creador de watchface


> 

### Ejemplo de Watchface


En la carpeta [01-WF-MD225-Version3-xdrip-ready](https://github.com/twinko/GTR-2-WF-Xdrip-EN/tree/main/01-WF-MD225-Version3-xdrip-ready
"01-WF-MD225-Version3-xdrip-ready") encontrarás el producto final de un watchface personalizado. Más adelante enlazaré aquí otro repositorio con otro watchface que he creado. 

**Si has creado tu propio watchface por favor compártelo con los demás. Podríamos reunirlas en un solo repositorio, no dudes en contactar conmigo a través de un issue.**


## Cosas que necesitas

Voy a utilizar las siguientes herramientas. Necesitarás todas ellas. Todas las herramientas de abajo son gratuitas para uso personal.

1. 1. Sistema operativo Windows
2. **WFE**: [AmazFit WatchFace editor 2 para Windows](https://amazfitwatchfaces.com/forum/viewtopic.php?p=8392#p8392)
3. **PS**: Photoshop (la versión CS2 está disponible de forma gratuita) https://archive.fo/255q5#selection-1663.0-1663.29
5. **WF**: Un watchface. (próximo capítulo)
6. Descarga todo el repositorio, necesitaremos algunos archivos más tarde de la carpeta "Guide". Puedes descargar este repositorio haciendo clic en el botón de "código" en la parte superior de esta página y elegir "Descargar ZIP".

## Busca un watchface que quieras utilizar

Si no vas a crear tu propio watchface, puedes buscar watchfaces aquí: https://amazfitwatchfaces.com/gtr/top?compatible=GTR_2
Descargue el archivo deseado. Por favor, ten cuidado con el reloj para el que se hizo el watchface.

**Algo muy importante:** 

 - Cuanto más pequeño sea el watchface, mejor. Ya hablaremos de esto más adelante, pero todas las imágenes, incluyendo el archivo json, no deben ser mayores de 50kb. 
 - 50kb de tamaño de watchface (imágenes en bruto y el json) dará lugar a un tiempo de carga de unos 10 segundos y no quieres que te lleve más tiempo, por la vida de la batería y no quieres esperar hasta mañana.
 - Eso significa menos iconos, menos cosas cambiantes (excluyendo los números, y sí, sólo los números). 
 - Evita los watchfaces con gradientes (cuando un color cambia a otro). 
 - Recuerde que queremos ser capaces de leer fácilmente nuestra glucosa en sangre (BG), por lo que tenemos que hacer algo de espacio libre en alguna parte. Yo calcularía al menos 1/3 del watchface dedicado a toda la información relacionada con el xdrip

# 1. Guía / Tutorial

1. Descargue toda la carpeta de la última versión del WFE (editor de watchface), enlazada arriba. 
2. Puedes encontrar el botón de "descarga" en la parte superior derecha, ¡necesitamos toda la carpeta! 
3. Después de hacer clic en la descarga, elija "descarga directa". Se descargará un archivo como "AmazFit_Watchface_Editor_2_v5.1.zip".
4. Extraiga el archivo
5. Abrir (en mi caso) "AmazFit_Watchface_Editor_2"
6. Iniciar "AmazFit_Watchface_Editor_2.exe"
7. Botón derecho, elegir "Descomprimir la papelera comprimida"
8. Elige el watchface que has descargado anteriormente
9. El watchface descomprimido se encuentra aquí: ...\NAmazFit_Watchface_Editor_2\NWatch_face
10. Ahora tienes que familiarizarte con el WFE.
11. Voy a explicar sólo los fundamentos absolutos. Para aprender más sobre el editor de watchface y sus posibilidades, echa un vistazo aquí: https://amazfitwatchfaces.com/forum/viewtopic.php?f=14&t=1571
Enlace directo a la traducción al inglés: https://translate.google.com/translate?hl=ru&sl=ru&tl=en&u=https%3A%2F%2Fowagner.ru%2Famazfitgtr%2Fwfcreator%2Fwatchfaces_creator_lesson%2F
12. Ir a la pestaña "Editar" y hacer clic a través de las diferentes opciones en el lado derecho. 
13. Elige "Orden de las capas" para definir cosas como el orden de las fechas (dd-mm-yy o mm-dd-yy).

> **Pista importante:** 
> Nuestro objetivo más importante es reducir el tamaño. Como se ha escrito
> Como se ha escrito anteriormente, queremos obtener menos de 50kb de archivos png sin procesar (incluyendo .json).
> 
> La mejor manera de reducir el tamaño:
> - menos imágenes
> - menos colores (hace que los archivos de imagen sean más pequeños)
> - utilizar la fuente del sistema (un ajuste en la pestaña de edición de WFE donde se muestran los números.)

14. Cuando hayas terminado con tus cambios, guarda el watchface (pestaña "Edit", abajo en el medio "save Json")

> **Cosas que me ayudaron mucho:**
> - La imagen 0001.png es siempre el fondo. Normalmente es necesario adaptar el fondo para que se ajuste a un gráfico de glucosa y a todos los datos necesarios. Usa Photoshop para eso o un programa diferente
> - Mira las imágenes desempaquetadas, borra todas las que no necesites.
> - Tienes que renombrar los archivos desde 0001- xxxx Tendrás problemas más adelante si los archivos no están seguidos. No es posible que falte un
> número entre los que faltan. Debería ser así: 0001, 0002, ......
> 0015.) Puedes utilizar https://www.bulkrenameutility.co.uk/Download.php para renombrar archivos de forma masiva.

15. Ve a la carpeta que incluye el json y todos los archivos necesarios en tu ordenador.
16. Haz una copia de seguridad de los archivos existentes y del json

## 1.1 Editar el fondo de tu watchface
Si su watchface tiene un color liso, edítelo en el WFE. Pero usted tendrá que crear una imagen, donde toda la fecha xdrip se coloca en, por lo que crear una imagen que coincida con el color en PS y saltar la siguiente parte, donde se describe cómo cortar la imagen.

17. Abra 0001.png (su imagen de fondo) en PS
18. Ir a Picture-->Mode y cambiar de nuevo a RGB
19. 19. Seleccione la herramienta de ángulo recto pulsando "M" y elija la parte en la que quiere que se muestren sus datos de xdrip.
![##**PS_cut_xdrip_part_01.PNG**](https://raw.githubusercontent.com/twinko/GTR-2-WF-Xdrip-EN/main/Guide/PS_cut_xdrip_part_01.PNG)

20. Haz clic con el botón derecho del ratón dentro y elige "Capa por corte"
21. Guardar este archivo como un archivo PS (.psd)
22. Ocultar el resto de la imagen haciendo clic en el icono del ojo en el lado derecho (capas) en la capa 1
![## **PS_cut_xdrip_part_02.PNG**](https://raw.githubusercontent.com/twinko/GTR-2-WF-Xdrip-EN/main/Guide/PS_cut_xdrip_part_02.PNG)
23. Pulse "c" para utilizar la herramienta de corte
24. Corta la imagen al tamaño de la parte visual de tu watchface.
25. Pulsa enter para confirmar o el check en la parte superior
26. Ahora guarda esto como **mi_imagen.png**
27. Abrir el archivo psd guardado y hacer lo mismo con el resto de la esfera del reloj, de manera que tengamos la imagen de fondo, dividida en 2 archivos.


### 1.1.1 Reducir el tamaño de la imagen
28. Abrir todos los archivos, uno tras otro con PS.
29. Pinchar en Datos--> Guardar para Web
30. En la nueva ventana debes elegir lo siguiente en el lado derecho:
	- png-8
	- Puedes juguetear un poco y eliminar colores específicos, eso reducirá aún más el tamaño de la imagen. Puedes ver el nuevo tamaño del archivo en la parte inferior derecha
	- ¡Los archivos deben ser png! 
	- Si encuentras un borde extraño alrededor de tus imágenes
		- ve a la imagen, a Mode y cámbiala a "colores indexados" antes de guardarla para la web
31. Guarda el archivo sobrescribiendo (has hecho una copia de seguridad antes). No he encontrado una manera de hacerlo a todos los archivos a la vez, hágamelo saber si usted sabe cómo.

### 31. Coloca mi_imagen.png en el lugar correcto en el WF
32. Ahora abra el WFE de nuevo, usted debe notar, que tenemos un recorte en el medio de nuestro watchface. (si no, guarde su imagen recortada como imagen de fondo)
33. navegue a Editar--> Actividad -->Quemar grasa-->Icono
34. Copiar la siguiente imagen situada aquí: ## GTR-2-WF-Xdrip-ES/[Guía](https://github.com/twinko/GTR-2-WF-Xdrip-EN/tree/main/Guide)/**0099.png** es solo 1 pixel. La sustituiremos más tarde por la imagen_mi.png a través del código. Pero esto nos ahorra mucho tamaño de watchface.
35. Ahora hay que ponerlo en la esquina superior izquierda de nuestro recorte. Para encontrar las coordenadas correctas, lea el siguiente tema (Cómo encontrar las coordenadas correctas en PS)

## 1.2 Preparación de la cara del reloj final
Lo que deberías tener hasta ahora en 1 carpeta
- un json que ha creado con WFE
- todos los archivos WF necesarios, de tamaño reducido al máximo
- mi_imagen.png, de tamaño reducido al máximo
--> nos estamos acercando a su WF final :)

36. Navegue a ....\AmazFit_Watchface_Editor_2\Tools
37. Mantenga Mayúsculas + clic derecho en esta carpeta
38. Elija "Abrir ventana de Powershell aquí"
39. Para empaquetar su json sólo tiene que navegar a la carpeta de herramientas y ejecutar el comando como este  
`main.exe --gtr2 47 --file config-file.json` donde config-file.json es una ubicación a su json.
	- Tuve algunos problemas con eso y necesitaba añadir a toda la ruta delante de la main.exe por lo que fue algo liek esta:
		- `C:\NUsers\twinko\NDesktop\NAmazFit_Watchface_Editor_2\NAmazFit_Watchface_Editor_2\NTools\Nmain. exe --gtr2 47 --file C:\Users\TwinkosTower\Desktop\AmazFit_Watchface_Editor_2\AmazFit_Watchface_Editor_2\Watch_face\gtr2-g7en-colormix03-346659-994092c337\Small\WF_2_V01.json`
40. Como resultado, debería recibir un archivo bin desempaquetado. Este archivo tendrá que utilizarlo en xdrip. Xdrip inyectará el recurso requerido en este archivo, lo comprimirá y lo enviará al reloj.
41. Cambie el nombre del archivo bin a: my_watchface.bin
42. Crear una nueva carpeta, poniendo los siguientes archivos:
- el my_watchface.bin que hemos creado
- mi_imagen.png



## 1.3 Editar el config.json

El config.json define en qué parte de my_image.png se muestran los datos de xdrip y cómo. Es diferente al json creado por el WFE, ¡no los confunda!

El config.json original creado por Artem está enlazado aquí:
https://github.com/twinko/GTR-2-WF-Xdrip-EN/blob/main/Guide/config.json
Si ha descargado el repositorio antes, obtenga el archivo de la carpeta Guide.



> **Cosas generales que hay que saber:**
> - este config.json sólo está relacionado con mi_imagen.png
> - si hablamos de coordenadas (x e y) se basa en my_image.png y su tamaño total, no en todo el watchface
> - leer el post de Artems sobre la alineación aquí: https://github.com/bigdigital/xDrip-miband/issues/5#issuecomment-878008056
> - text_align: "right" 
> - tienes que contar los píxeles a partir del lado derecho
> - así que si se lee: x: 100 y la alineación del texto es a la derecha, contando 100 píxeles desde el lado derecho de la imagen es donde se coloca el elemento

### 1.3.1 Cómo encontrar las coordenadas correctas en PS
43. Abra mi_imagen.png en PS
44. Presione F8, una pequeña ventana de información se mostrará
45. Si mueves el ratón sobre la imagen, verás que los números X e Y se mueven. 

### 1.3.2 config.json explicado
46. abre el config.json con el bloc de notas
47. Verás pequeños grupos, que se explican por sí mismos
48. Sólo tenemos que editar resource_to_replace, X, Y font_size quizás bg_color del gráfico

#### 1.3.2.1 resource_to_replace
49. poner el número de la imagen que elegimos para Fat-burning-->Icono (si su imagen fiurst se llama 0001.png) reducir el número en uno. El algoritmo empieza a contar con 0)

#### 1.3.2.2 "x" , "y" y "text_align": "right",
50. como se describe en "Cómo encontrar las coordenadas correctas en PS" puedes encontrar la posición correcta para colocar tus datos de xdrip. 

> **Pista**: El tipo de letra del sistema es "Segoe UI" así que pulsa t en PS para escribir texto y
> poner algún texto defualt en su my_image.png y buscar la derecha
> coordenadas. Recuerda que *x e y son la parte inferior izquierda de la primera
> letra/número*. No guardes el my_image.png con los números que
> anotados, esto lo hará más tarde la magia de Artems, lo hacemos en PS
> para averiguar las coordenadas correctas, no para otra cosa.

51. Ahora cambie todas las coordenadas a sus necesidades.
52. Atención: hay algunos valores que tienen la siguiente línea: `"text_align": "right",` para estos tenemos una regla diferente para las coodinadas. *Poner la coordenada Buttom derecha de la última letra/número.*

#### 1.3.2.3 "font_size"
53. Poner el mismo tamaño de letra que eliges en PS

### 1.3.3 Guardar el config.json
54. Guarda el config.json en la carpeta que incluye my_image.png y my_watchface.bin (config.json no my_config.json)


## 1.4 Subirlo y probarlo

55. Ahora deberíamos tener una carpeta con los siguientes archivos
- config.json 
- mi_imagen.png 
- my_watchface.bin  
56. inserta estos 3 archivos en la carpeta xdrip de tu smartphone 
- La carpeta xdrip necesaria se encuentra aquí:
	- Internat storage/xdrip o
	- root/storage/emulated/0/xdrip
57. Habilitar watchface personalizado en la configuración de xdrip.
58. Hecho.

# 2. Nota a pie de página

Por favor, abre un tema aquí si encuentras problemas. Por favor, haga su propia investigación de antemano, yo también soy sólo un tipo normal que hace esto en su tiempo libre. 
https://github.com/twinko/GTR-2-WF-Xdrip-EN/issues

Si tienes sugerencias sobre cómo mejorar el guiode o hacerlo adecuado para otros watchfaces también, escribe un issue también :)

Espero que esta guía haya sido de ayuda :)
