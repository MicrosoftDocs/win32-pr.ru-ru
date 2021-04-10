---
title: Формат файла темы
description: В этом документе рассматривается формат файлов темы (Themes). Файл Theme — это текстовый файл. ini, разделенный на разделы, в которых указываются визуальные элементы, отображаемые на рабочем столе Windows. Имена разделов заключены в квадратные скобки (\ \) в ini-файле.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61ba97172fc5aaddb912183130941337a149536
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "103891204"
---
# <a name="theme-file-format"></a>Формат файла темы

В этом документе рассматривается формат файлов темы (Themes). Файл Theme — это текстовый файл. ini, разделенный на разделы, в которых указываются визуальные элементы, отображаемые на рабочем столе Windows. Имена разделов упаковываются в квадратные скобки ( \[ \] ) в ini-файле.

Новый формат файла,. семепакк, появился в Windows 7, чтобы помочь пользователям совместно использовать темы. Темы можно выбрать на панели управления персонализацией только в Windows 7 Домашняя расширенная или более поздней версии или только на Windows Server 2008 R2 при установке компонента Desktop.

В этой статье рассматриваются следующие темы.

-   [Создание файла темы](#creating-a-theme-file)
-   [Описание файла темы](#description-of-a-theme-file)
    -   [\[\]Раздел темы](#theme-section)
    -   [\[Раздел "цвета" панели управления \\ \]](#control-panelcolors-section)
    -   [\[\\Раздел курсоров панели \] управления](#control-panelcursors-section)
    -   [\[Раздел " \\ Рабочий стол" панели управления \]](#control-paneldesktop-section)
    -   [\[Раздел "слайды" \]](#slideshow-section)
    -   [\[Раздел метрик \]](#metrics-section)
    -   [\[Раздел стилей визуальных элементов \]](#visual-styles-section)
    -   [\[Разделы «звуки \] и \[ аппевентс \] » (звуки)](#sounds-and-appevents-sections-sounds)
    -   [\[\]Раздел загрузки](#boot-section)
    -   [\[\]Раздел мастерсемеселектор](#masterthemeselector-section)
-   [Пример файла темы](#example-of-a-theme-file)
-   [Установка файлов темы](#installing-theme-files)
-   [Пакеты тем](#theme-packs)
-   [См. также](#related-topics)

## <a name="creating-a-theme-file"></a>Создание файла темы

Файл Theme позволяет изменять внешний вид определенных элементов рабочего стола. Создать или изменить файл Theme можно двумя способами.

-   Измените параметры персонализации или настройки экрана на панели управления и сохраните их в виде файла Theme. Инструкции см. в справке Windows.
-   Создайте файл Theme вручную, чтобы получить более высокий уровень контроля над сведениями о теме.

Чтобы сделать тему доступной для других пользователей, необходимо предоставить файл Theme, а также фоновый рисунок, экранная заставка и файлы значков. Это можно сделать с помощью [пакета темы](#theme-packs).

## <a name="description-of-a-theme-file"></a>Описание файла темы

Файлы темы содержат ряд обязательных и необязательных разделов. Ниже описаны разделы файлов Theme и приведены примеры указания изменений для различных элементов.

### <a name="theme-section"></a>\[\]Раздел темы

> [!Note]  
> Этот раздел является необязательным. Если этот раздел не включен в файл Theme, система использует параметры по умолчанию.

 

В \[ \] разделе тема указывается имя пользовательской темы, а также логотип фирменной символики и значки рабочего стола.

Первая часть \[ \] раздела тема содержит следующие два элемента:



| Элемент                                                                                                                    | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName = имя<br/> или<br/> DisplayName = @module ,-stringId<br/> Пример: DisplayName = @themeui.dll ,-2013 | DisplayName — это имя темы, которое будет отображаться на панели управления персонализации. Это может быть строка или ссылка на локализованное имя.<br/> Это поле является необязательным. Если он отсутствует, в качестве имени темы используется имя файла темы.<br/>                                                                                                                                                                                                                                         |
| Брандимаже = путь к изображению<br/> Пример: Брандимаже = c: \\ Fabrikam \\brand.png<br/>                                 | **Windows 7 и более поздние версии** Брандимаже указывает путь к графическому файлу с фирменной символикой, который включен в предварительную версию темы на панели управления персонализацией.<br/> Изображение значка должно быть PNG-файлом. Изображение масштабируется до 80x240 пикселей, поэтому рекомендуется предоставить изображение такого размера. В коллекции тем находятся прозрачные области значка торговой марки.<br/> Это поле является необязательным. Если он отсутствует, логотип не отображается в качестве значка темы.<br/> |



 

В остальной части \[ \] раздела тема указываются пользовательские значки для таких функций рабочего стола, как компьютер, мои документы, сеть и корзина. Если не указать настраиваемые значки рабочего стола, на рабочем столе будут отображаться системные значки по умолчанию.

Ниже приведены два примера того, как файл Theme задает значок **компьютера** .


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



Ниже приведены значения для значков рабочего стола по умолчанию в Windows 7.


```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55
```



### <a name="control-panelcolors-section"></a>\[Раздел "цвета" панели управления \\ \]

> [!Note]  
> Этот раздел является необязательным. Если этот раздел не включен в файл Theme, система использует параметры по умолчанию. Если в вашей теме используется визуальный стиль Aero, не следует переопределять значения по умолчанию в этом разделе.

 

Цвет элементов, таких как полосы прокрутки, текст и кнопки, является настраиваемым. В файле Theme указаны значения RGB, которые необходимо изменить для этих элементов. Значения переопределяют значения по умолчанию визуального стиля и используются, если тема основана на классической версии Windows, Windows 7 Basic или высокая контрастность темах.

Ниже приведен пример того, как устанавливаются цвета.


```
[Control Panel\Colors]
ActiveTitle=10 36 106
Background=166 202 240
Hilight=10 36 106
HilightText=255 255 255
TitleText=255 255 255
Window=255 255 255
WindowText=0 0 0
Scrollbar=212 208 200
InactiveTitle=128 128 128
Menu=212 208 200
WindowFrame=0 0 0
MenuText=0 0 0
ActiveBorder=212 208 200
InactiveBorder=212 208 200
AppWorkspace=128 128 128
ButtonFace=212 208 200
ButtonShadow=128 128 128
GrayText=128 128 128
ButtonText=0 0 0
InactiveTitleText=212 208 200
ButtonHilight=255 255 255
ButtonDkShadow=64 64 64
ButtonLight=212 208 200
InfoText=0 0 0
InfoWindow=255 255 225
GradientActiveTitle=166 202 240
GradientInactiveTitle=192 192 192
```



### <a name="control-panelcursors-section"></a>\[\\Раздел курсоров панели \] управления

> [!Note]  
> Этот раздел является необязательным. Если этот раздел не включен в файл Theme, система использует курсоры по умолчанию.

 

Тема также может изменять внешний вид курсоров. Для этого создайте cur файлы, чтобы заменить курсоры Windows по умолчанию. Следующий пример относится к файлу Theme, который определяет курсоры для темы с названием *Спорт*.


```
[Control Panel\Cursors]
Arrow=%SystemRoot%\sports_arrow.cur
Help=%SystemRoot%\sports_help.cur
AppStarting=%SystemRoot%\sports_wait.ani
Wait=%SystemRoot%\sports_busy.ani
NWPen=%SystemRoot%\sports_pen.cur
No=%SystemRoot%\sports_no.cur
SizeNS=%SystemRoot%\sports_size_ns.cur
SizeWE=%SystemRoot%\sports_size_we.cur
Crosshair=%SystemRoot%\sports_cross.cur
IBeam=%SystemRoot%\sports_beam.cur
SizeNWSE=%SystemRoot%\sports_size_nwse.cur
SizeNESW=%SystemRoot%\sports_size_nesw.cur
SizeAll=%SystemRoot%\sports_move.cur
UpArrow=%SystemRoot%\sports_up.cur
DefaultValue=Windows default
```



### <a name="control-paneldesktop-section"></a>\[Раздел " \\ Рабочий стол" панели управления \]

> [!Note]  
> Это обязательный раздел. Если этот раздел не включен в файл Theme, система пропустит вашу тему и не отобразит тему на панели управления.

 

Можно создать пользовательский фон рабочего стола и указать путь к файлу изображения. В следующем примере показано, как изменить внешний вид рабочего стола.


```
[Control Panel\Desktop]
Wallpaper=%WinDir%\web\wallpaper\Windows\img0.jpg
; The path to the wallpaper picture can point to a 
; .bmp, .gif, .jpg, .png, or .tif file.

TileWallpaper=0
; 0: The wallpaper picture should not be tiled 
; 1: The wallpaper picture should be tiled 

WallpaperStyle=2
; 0:  The image is centered if TileWallpaper=0 or tiled if TileWallpaper=1
; 2:  The image is stretched to fill the screen
; 6:  The image is resized to fit the screen while maintaining the aspect 
      ratio. (Windows 7 and later)
; 10: The image is resized and cropped to fill the screen while maintaining 
      the aspect ratio. (Windows 7 and later)
```



### <a name="slideshow-section"></a>\[Раздел "слайды" \]

**Windows 7 и более поздние версии.**

> [!Note]  
> Этот раздел является необязательным. Если этот раздел не включен в файл Theme, система использует фоновое изображение рабочего стола, указанное в \[ разделе Панель управления \\ Рабочий стол \] . При включении этого раздела необходимо указать здесь параметры показа слайдов.

 

В качестве фона темы можно использовать изображения, которые хранятся локально или на изображениях, обслуживаемых RSS-каналом. \[Раздел слайд-шоу \] файла содержит следующие атрибуты:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Интервал = число миллисекунд</td>
<td>Обязательный. Интервал — это число, определяющее частоту изменения фона. Измеряется в миллисекундах.</td>
</tr>
<tr class="even">
<td>Случайный = 0 или 1</td>
<td>Обязательный. Случайный выбор в случайном порядке определяет фоновый режим.<br/> 0 = отключено<br/> 1 = включено<br/></td>
</tr>
<tr class="odd">
<td>RSS-канал = URL-адрес канала RSS</td>
<td>Требуется, если не указан Имажесрутпас. RSS-канал указывает RSS-канал, используемый в качестве фонового показа слайдов. Чтобы канал работал, необходимо ссылаться на изображения с высоким разрешением, соответствующие &quot; &quot; стандартам, используемым <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">платформой RSS Windows</a>. Из-за этого ограничения файлы Theme, включающие RSS-канал, необходимо создавать вручную. <br/>
<blockquote>
[!Note]<br />
Нельзя указать одновременно RSS-канал и Имажесрутпас.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>Имажесрутпас = путь к папке изображений</td>
<td>Требуется, если не указан RSS-канал. Имажесрутпас задает путь к набору изображений, которые будут использоваться в качестве фонового показа слайдов. Изображения во вложенных папках не включаются в показ слайдов.<br/> Имажесрутпас поддерживает подстановки переменных среды в пути.<br/>
<blockquote>
[!Note]<br />
Нельзя указать одновременно RSS-канал и Имажесрутпас.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Элемент<em>N</em>путь = пути к конкретным изображениям</td>
<td>Для использования с Имажесрутпас. <br/> Элемент<em>N</em>path указывает пути к определенным изображениям, что позволяет ограничить показ слайдов определенными изображениями, а не всеми изображениями в папке. Если пути не указаны, все изображения в пути Имажесрутпас используются в слайдовой демонстрации, включая изображения, добавленные после создания и установки темы.<br/> Путь к элементу<em>N</em>поддерживает подстановки переменных среды в пути. <em>N</em> — 0, 1, 2 и т. д. <br/></td>
</tr>
</tbody>
</table>



 

В следующих примерах показано, как файл Theme указывает слайд-шоу для включения набора изображений, хранящихся локально.


```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%SystemRoot%\Web\Wallpaper
```




```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg
```



В следующем примере представлен шаблон для файла Theme, который создает слайд-шоу в фоновом режиме на рабочем столе с помощью изображений из RSS-канала. Чтобы настроить шаблон, выполните следующие действия.

1.  Скопируйте приведенный ниже пример и вставьте его в текстовый редактор.
2.  Замените {семенаме} именем, которое должно отображаться в коллекции "темы" панели управления персонализации.
3.  Замените {рссфидурл} полным путем к совместимому RSS-каналу.
4.  Сохраните изменения в файле с расширением Theme.


```
[Theme]
DisplayName={themename}

[Slideshow]
Interval=1800000
Shuffle=1
RssFeed={rssfeedurl}

[Control Panel\Desktop]
TileWallpaper=0
WallpaperStyle=10
Pattern=

[Control Panel\Cursors]
AppStarting=%SystemRoot%\cursors\aero_working.ani
Arrow=%SystemRoot%\cursors\aero_arrow.cur
Crosshair=
Hand=%SystemRoot%\cursors\aero_link.cur
Help=%SystemRoot%\cursors\aero_helpsel.cur
IBeam=
No=%SystemRoot%\cursors\aero_unavail.cur
NWPen=%SystemRoot%\cursors\aero_pen.cur
SizeAll=%SystemRoot%\cursors\aero_move.cur
SizeNESW=%SystemRoot%\cursors\aero_nesw.cur
SizeNS=%SystemRoot%\cursors\aero_ns.cur
SizeNWSE=%SystemRoot%\cursors\aero_nwse.cur
SizeWE=%SystemRoot%\cursors\aero_ew.cur
UpArrow=%SystemRoot%\cursors\aero_up.cur
Wait=%SystemRoot%\cursors\aero_busy.ani
DefaultValue=Windows Aero
Link=

[VisualStyles]
Path=%SystemRoot%\resources\themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X6B74B8FC
Transparency=1

[MasterThemeSelector]
MTSM=DABJDKT
```



### <a name="metrics-section"></a>\[Раздел метрик \]

> [!Note]  
> Этот раздел является необязательным. Если этот раздел не включен в файл Theme, система использует параметры визуального стиля по умолчанию.

 

Системные метрики можно указать в файле Theme. Системные метрики — это измерения различных отображаемых элементов, такие как ширина границы окна, Высота значка или ширина полосы прокрутки. Значения Нонклиентметрикс и Иконметрикс — это двоичные структуры, определяемые НОНКЛИЕНТМЕТРИКС и ИКОНМЕТРИКС в файле WinUser. h. Ниже приведен пример изменения системных метрик.


```
[Control Panel\Desktop\WindowMetrics]

[Metrics]
IconMetrics=76 0 0 0 139 0 0 0 139 0 0 0 1 0 0 0 245
255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0 0 0 0
0 0 0 0 84 97 104 111 109 97 0 119 0 0 7 0 0 0 0 0 216
31 7 0 28 52 1 1 216 31 7 0 176 36 1 1 
NonclientMetrics=84 1 0 0 1 0 0 0 16 0 0 0 16 0 0 0 18
0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
188 2 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 12 0 0 0
15 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 188 2
0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 80 37 11
0 0 0 0 0 140 221 6 0 227 115 247 119 2 40 11 0 7 0 0
0 18 0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0
0 0 0 144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0
0 0 0 0 0 60 222 6 0 50 71 252 119 120 1 7 0 76 73 252
119 8 6 7 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 119 0
0 7 0 120 1 7 0 120 1 7 0 40 37 11 0 120 1 7 0 120 1 7
0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0
0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 92 1 0 0 136 4
0 0 40 37 1 1 0 0 7 0 184 221 6 0 46 75 232 119 
```



### <a name="visual-styles-section"></a>\[Раздел стилей визуальных элементов \]

> [!Note]  
> Это обязательный раздел. Если этот раздел не включен в файл Theme, система пропустит вашу тему и не отобразит тему на панели управления.

 

Вы можете указать конкретные сведения о размере и цвете элементов рабочего стола в файлах мсстилес. Разделы "цвет" и "размер" в файлах Theme могут быть заменены файлами. мсстилес, которые позволяют более подробно изменять элементы рабочего стола. Эти файлы указываются в разделе Стили визуальных элементов файла Theme. Ниже приведен пример раздела визуальных стилей.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



Добавление элемента пути в мсстилес-файл является необязательным. При указании пути следует удалить секции метрик и цвет из файла Theme. При удалении этих разделов цвета, шрифты и размеры темы берутся из мсстилес-файла и соответствуют намерениям автора. мсстилес. Невозможность удаления разделов метрик и цветов может привести к проблемам с прорисовкой в Windows или приложениях.

**Windows Vista или Windows 7:** Когда путь указывает на Aero. мсстилес, можно указать требуемый цвет стекла, как показано в следующем примере.

**Windows 7:** Когда путь указывает на Aero. мсстилес, можно также указать нужное значение прозрачности, как показано в следующем примере.


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



Если значения Колоризатионколор и прозрачности точно соответствуют системному цвету, в панели управления персонализации отображается системное имя цвета. В противном случае цвет помечается как "настраиваемый".

Ниже приведен раздел VisualStyles для основной темы Windows 7.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



Ниже приведен раздел VisualStyles для классической темы Windows.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



Ниже приведен раздел VisualStyles для высокая контрастность черной темы.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[Разделы «звуки \] и \[ аппевентс \] » (звуки)

> [!Note]  
> Этот раздел является необязательным. Если этот раздел не включен в файл Theme, система использует параметры звука по умолчанию.

 

Пользователь может выбрать значок **звука** на панели управления, чтобы связать звуки с событиями, происходящими в приложениях. Например, WAV-файл может воспроизводиться при открытии приложения. В файле Theme можно указать WAV-файлы для замены значений по умолчанию. В приведенном ниже примере показано, как это сделать.


```
[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=%WinDir%\media\tada.wav

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=%WinDir%\media\The Microsoft Sound.wav

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav
```



**Windows 7 и более поздние версии:** Вместо перечисления каждого звука можно указать имя звуковой схемы.


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



Значение Счеменаме указывает имя звуковой схемы или локализованное имя звуковой схемы, как показано в примере выше.

### <a name="boot-section"></a>\[\]Раздел загрузки

> [!Note]  
> **Экранные заставки не рекомендуются в юбилейном обновлении Windows 10 и выходят за рамки.**

 

> [!Note]  
> Этот раздел является необязательным. Если этот раздел не включен в файл Theme, экранная заставка не используется.

 

В файле Theme можно указать экранную заставку Windows для использования. В следующем примере приведена иллюстрация этого.


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[\]Раздел мастерсемеселектор

> [!Note]  
> Это обязательный раздел. Если этот раздел не включен в файл Theme, система пропустит вашу тему и не отобразит тему на панели управления.

 

Раздел Selector главной темы файла Theme всегда должен быть включен в качестве тега, который указывает, что файл является допустимым. У вас нет выбора значений для этого параметра. Это показано ниже.


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>Пример файла темы

В следующем примере показан полный файл Theme.


```
[Theme]
DisplayName=My Current Theme
BrandImage=c:\Fabrikam\brand.png

; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55

[Control Panel\Cursors]
Arrow=
Help=
AppStarting=
Wait=
NWPen=
No=
SizeNS=
SizeWE=
Crosshair=
IBeam=
SizeNWSE=
SizeNESW=
SizeAll=
UpArrow=
DefaultValue=Windows default

[Control Panel\Desktop]
Wallpaper=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
TileWallpaper=0
WallpaperStyle=2
Pattern=
ScreenSaveActive=0

[AppEvents\Schemes\Apps\.Default\.Default]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\AppGPFault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Maximize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuCommand]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuPopup]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Minimize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Open]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreDown]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreUp]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RingIn]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Ringout]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemAsterisk]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemDefault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\Close]
DefaultValue=

[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg

[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr

[MasterThemeSelector]
MTSM=DABJDKT
ThemeColorBPP=4

[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x856E3BA1
Transparency=1
```



## <a name="installing-theme-files"></a>Установка файлов темы

При инициализации Windows операционная система перечисляет подкаталоги первого уровня% WinDir% \\ ресурсов \\ для обнаружения доступных тем. Системные файлы темы по умолчанию расположены в темах% WinDir% \\ ресурсов \\ . Файлы пользовательских тем хранятся в папках% WINDIR% \\ пользователей \\ <username> \\ AppData \\ локальные \\ \\ темы Microsoft Windows \\ .

Файл Theme имеет сопоставления файлов; Таким образом, приложения установщика тем могут вызвать [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) в файле Theme, чтобы открыть окно **персонализации** на панели управления для указанной темы.

## <a name="theme-packs"></a>Пакеты тем

**Windows 7 и более поздние версии.** Пакет темы — это CAB-файл, который содержит не только файл Theme, но и файлы, необходимые для реализации темы на другом компьютере, например звуковые файлы и изображения. Пользователи могут создавать пакеты тем с помощью панели управления персонализацией.

В число поддерживаемых типов файлов входят следующие:



| Тип файла    | Расширение                           |
|--------------|-------------------------------------|
| Тема        | .theme                              |
| Образ        | JPG, JPEG, BMP, DIB, TIF, PNG |
| Звук        | .wav                                |
| Курсор мыши | . cur,. ani                          |
| Значок рабочего стола | ICO                                |
| Логотип торговой марки   | .png                                |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Общие сведения о визуальных стилях](visual-styles-overview.md)
</dt> </dl>

