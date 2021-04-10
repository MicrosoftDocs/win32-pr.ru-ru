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
# <a name="theme-file-format"></a><span data-ttu-id="b21be-105">Формат файла темы</span><span class="sxs-lookup"><span data-stu-id="b21be-105">Theme File Format</span></span>

<span data-ttu-id="b21be-106">В этом документе рассматривается формат файлов темы (Themes).</span><span class="sxs-lookup"><span data-stu-id="b21be-106">This document discusses the format of Theme (.theme) files.</span></span> <span data-ttu-id="b21be-107">Файл Theme — это текстовый файл. ini, разделенный на разделы, в которых указываются визуальные элементы, отображаемые на рабочем столе Windows.</span><span class="sxs-lookup"><span data-stu-id="b21be-107">A .theme file is a .ini text file that is divided into sections, which specify visual elements that appear on a Windows desktop.</span></span> <span data-ttu-id="b21be-108">Имена разделов упаковываются в квадратные скобки ( \[ \] ) в ini-файле.</span><span class="sxs-lookup"><span data-stu-id="b21be-108">Section names are wrapped in brackets (\[\]) in the .ini file.</span></span>

<span data-ttu-id="b21be-109">Новый формат файла,. семепакк, появился в Windows 7, чтобы помочь пользователям совместно использовать темы.</span><span class="sxs-lookup"><span data-stu-id="b21be-109">A new file format, .themepack, was introduced with Windows 7 to help users share themes.</span></span> <span data-ttu-id="b21be-110">Темы можно выбрать на панели управления персонализацией только в Windows 7 Домашняя расширенная или более поздней версии или только на Windows Server 2008 R2 при установке компонента Desktop.</span><span class="sxs-lookup"><span data-stu-id="b21be-110">Themes can be selected in the Personalization Control Panel only in Windows 7 Home Premium or higher, or only on Windows Server 2008 R2 when the Desktop component is installed.</span></span>

<span data-ttu-id="b21be-111">В этой статье рассматриваются следующие темы.</span><span class="sxs-lookup"><span data-stu-id="b21be-111">The following topics are discussed in this article.</span></span>

-   [<span data-ttu-id="b21be-112">Создание файла темы</span><span class="sxs-lookup"><span data-stu-id="b21be-112">Creating a Theme File</span></span>](#creating-a-theme-file)
-   [<span data-ttu-id="b21be-113">Описание файла темы</span><span class="sxs-lookup"><span data-stu-id="b21be-113">Description of a Theme File</span></span>](#description-of-a-theme-file)
    -   <span data-ttu-id="b21be-114">[\[\]Раздел темы](#theme-section)</span><span class="sxs-lookup"><span data-stu-id="b21be-114">[\[Theme\] Section](#theme-section)</span></span>
    -   <span data-ttu-id="b21be-115">[\[Раздел "цвета" панели управления \\ \]](#control-panelcolors-section)</span><span class="sxs-lookup"><span data-stu-id="b21be-115">[\[Control Panel\\Colors\] Section](#control-panelcolors-section)</span></span>
    -   <span data-ttu-id="b21be-116">[\[\\Раздел курсоров панели \] управления](#control-panelcursors-section)</span><span class="sxs-lookup"><span data-stu-id="b21be-116">[\[Control Panel\\Cursors\] Section](#control-panelcursors-section)</span></span>
    -   <span data-ttu-id="b21be-117">[\[Раздел " \\ Рабочий стол" панели управления \]](#control-paneldesktop-section)</span><span class="sxs-lookup"><span data-stu-id="b21be-117">[\[Control Panel\\Desktop\] Section](#control-paneldesktop-section)</span></span>
    -   <span data-ttu-id="b21be-118">[\[Раздел "слайды" \]](#slideshow-section)</span><span class="sxs-lookup"><span data-stu-id="b21be-118">[\[Slideshow\] Section](#slideshow-section)</span></span>
    -   <span data-ttu-id="b21be-119">[\[Раздел метрик \]](#metrics-section)</span><span class="sxs-lookup"><span data-stu-id="b21be-119">[\[Metrics\] Section](#metrics-section)</span></span>
    -   <span data-ttu-id="b21be-120">[\[Раздел стилей визуальных элементов \]](#visual-styles-section)</span><span class="sxs-lookup"><span data-stu-id="b21be-120">[\[Visual Styles\] Section](#visual-styles-section)</span></span>
    -   <span data-ttu-id="b21be-121">[\[Разделы «звуки \] и \[ аппевентс \] » (звуки)](#sounds-and-appevents-sections-sounds)</span><span class="sxs-lookup"><span data-stu-id="b21be-121">[\[Sounds\] and \[AppEvents\] Sections (Sounds)](#sounds-and-appevents-sections-sounds)</span></span>
    -   <span data-ttu-id="b21be-122">[\[\]Раздел загрузки](#boot-section)</span><span class="sxs-lookup"><span data-stu-id="b21be-122">[\[Boot\] Section](#boot-section)</span></span>
    -   <span data-ttu-id="b21be-123">[\[\]Раздел мастерсемеселектор](#masterthemeselector-section)</span><span class="sxs-lookup"><span data-stu-id="b21be-123">[\[MasterThemeSelector\] Section](#masterthemeselector-section)</span></span>
-   [<span data-ttu-id="b21be-124">Пример файла темы</span><span class="sxs-lookup"><span data-stu-id="b21be-124">Example of a Theme File</span></span>](#example-of-a-theme-file)
-   [<span data-ttu-id="b21be-125">Установка файлов темы</span><span class="sxs-lookup"><span data-stu-id="b21be-125">Installing Theme Files</span></span>](#installing-theme-files)
-   [<span data-ttu-id="b21be-126">Пакеты тем</span><span class="sxs-lookup"><span data-stu-id="b21be-126">Theme Packs</span></span>](#theme-packs)
-   [<span data-ttu-id="b21be-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b21be-127">Related topics</span></span>](#related-topics)

## <a name="creating-a-theme-file"></a><span data-ttu-id="b21be-128">Создание файла темы</span><span class="sxs-lookup"><span data-stu-id="b21be-128">Creating a Theme File</span></span>

<span data-ttu-id="b21be-129">Файл Theme позволяет изменять внешний вид определенных элементов рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b21be-129">A .theme file enables you to change the appearance of certain desktop elements.</span></span> <span data-ttu-id="b21be-130">Создать или изменить файл Theme можно двумя способами.</span><span class="sxs-lookup"><span data-stu-id="b21be-130">You can create or modify a .theme file in two ways:</span></span>

-   <span data-ttu-id="b21be-131">Измените параметры персонализации или настройки экрана на панели управления и сохраните их в виде файла Theme.</span><span class="sxs-lookup"><span data-stu-id="b21be-131">Modify personalization or display settings in Control Panel and save the settings as a .theme file.</span></span> <span data-ttu-id="b21be-132">Инструкции см. в справке Windows.</span><span class="sxs-lookup"><span data-stu-id="b21be-132">See your Windows Help for instructions.</span></span>
-   <span data-ttu-id="b21be-133">Создайте файл Theme вручную, чтобы получить более высокий уровень контроля над сведениями о теме.</span><span class="sxs-lookup"><span data-stu-id="b21be-133">Create a .theme file manually for a greater level of control over the details of your theme.</span></span>

<span data-ttu-id="b21be-134">Чтобы сделать тему доступной для других пользователей, необходимо предоставить файл Theme, а также фоновый рисунок, экранная заставка и файлы значков.</span><span class="sxs-lookup"><span data-stu-id="b21be-134">To make your theme available to other users, you must supply your .theme file, as well as the background picture, screen saver, and icons files.</span></span> <span data-ttu-id="b21be-135">Это можно сделать с помощью [пакета темы](#theme-packs).</span><span class="sxs-lookup"><span data-stu-id="b21be-135">You can do this with a [theme pack](#theme-packs).</span></span>

## <a name="description-of-a-theme-file"></a><span data-ttu-id="b21be-136">Описание файла темы</span><span class="sxs-lookup"><span data-stu-id="b21be-136">Description of a Theme File</span></span>

<span data-ttu-id="b21be-137">Файлы темы содержат ряд обязательных и необязательных разделов.</span><span class="sxs-lookup"><span data-stu-id="b21be-137">Theme files have a number of required and optional sections.</span></span> <span data-ttu-id="b21be-138">Ниже описаны разделы файлов Theme и приведены примеры указания изменений для различных элементов.</span><span class="sxs-lookup"><span data-stu-id="b21be-138">The following describe the sections of .theme files and provide examples of how to specify changes for the different elements.</span></span>

### <a name="theme-section"></a><span data-ttu-id="b21be-139">\[\]Раздел темы</span><span class="sxs-lookup"><span data-stu-id="b21be-139">\[Theme\] Section</span></span>

> [!Note]  
> <span data-ttu-id="b21be-140">Этот раздел является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b21be-140">This section is optional.</span></span> <span data-ttu-id="b21be-141">Если этот раздел не включен в файл Theme, система использует параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b21be-141">If you do not include this section in your .theme file, the system uses default settings.</span></span>

 

<span data-ttu-id="b21be-142">В \[ \] разделе тема указывается имя пользовательской темы, а также логотип фирменной символики и значки рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b21be-142">The \[Theme\] section identifies the name of your custom theme and specifies your theme's brand logo and desktop icons.</span></span>

<span data-ttu-id="b21be-143">Первая часть \[ \] раздела тема содержит следующие два элемента:</span><span class="sxs-lookup"><span data-stu-id="b21be-143">The first part of the \[Theme\] section contains the following two elements:</span></span>



| <span data-ttu-id="b21be-144">Элемент</span><span class="sxs-lookup"><span data-stu-id="b21be-144">Element</span></span>                                                                                                                    | <span data-ttu-id="b21be-145">Описание</span><span class="sxs-lookup"><span data-stu-id="b21be-145">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b21be-146">DisplayName = имя</span><span class="sxs-lookup"><span data-stu-id="b21be-146">DisplayName=name</span></span><br/> <span data-ttu-id="b21be-147">или</span><span class="sxs-lookup"><span data-stu-id="b21be-147">or</span></span><br/> <span data-ttu-id="b21be-148">DisplayName = @module ,-stringId</span><span class="sxs-lookup"><span data-stu-id="b21be-148">DisplayName=@module,-stringId</span></span><br/> <span data-ttu-id="b21be-149">Пример: DisplayName = @themeui.dll ,-2013</span><span class="sxs-lookup"><span data-stu-id="b21be-149">example: DisplayName=@themeui.dll,-2013</span></span> | <span data-ttu-id="b21be-150">DisplayName — это имя темы, которое будет отображаться на панели управления персонализации.</span><span class="sxs-lookup"><span data-stu-id="b21be-150">DisplayName is the theme name that will show up in the Personalization Control Panel.</span></span> <span data-ttu-id="b21be-151">Это может быть строка или ссылка на локализованное имя.</span><span class="sxs-lookup"><span data-stu-id="b21be-151">It can be a string or a reference to a localized name.</span></span><br/> <span data-ttu-id="b21be-152">Это поле является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b21be-152">This field is optional.</span></span> <span data-ttu-id="b21be-153">Если он отсутствует, в качестве имени темы используется имя файла темы.</span><span class="sxs-lookup"><span data-stu-id="b21be-153">If it is missing, the theme filename is used as the theme name.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="b21be-154">Брандимаже = путь к изображению</span><span class="sxs-lookup"><span data-stu-id="b21be-154">BrandImage=path to image</span></span><br/> <span data-ttu-id="b21be-155">Пример: Брандимаже = c: \\ Fabrikam \\brand.png</span><span class="sxs-lookup"><span data-stu-id="b21be-155">example: BrandImage=c:\\Fabrikam\\brand.png</span></span><br/>                                 | <span data-ttu-id="b21be-156">**Windows 7 и более поздние версии** Брандимаже указывает путь к графическому файлу с фирменной символикой, который включен в предварительную версию темы на панели управления персонализацией.</span><span class="sxs-lookup"><span data-stu-id="b21be-156">**Windows 7 and later** BrandImage specifies the path to a branded graphic file that is incorporated in the theme preview in the Personalization Control Panel.</span></span><br/> <span data-ttu-id="b21be-157">Изображение значка должно быть PNG-файлом.</span><span class="sxs-lookup"><span data-stu-id="b21be-157">The icon graphic must be a PNG file.</span></span> <span data-ttu-id="b21be-158">Изображение масштабируется до 80x240 пикселей, поэтому рекомендуется предоставить изображение такого размера.</span><span class="sxs-lookup"><span data-stu-id="b21be-158">The graphic is scaled to 80x240 pixels, so it is recommended that you provide an image of that size.</span></span> <span data-ttu-id="b21be-159">В коллекции тем находятся прозрачные области значка торговой марки.</span><span class="sxs-lookup"><span data-stu-id="b21be-159">The Theme gallery respects the transparent regions of your brand icon.</span></span><br/> <span data-ttu-id="b21be-160">Это поле является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b21be-160">This field is optional.</span></span> <span data-ttu-id="b21be-161">Если он отсутствует, логотип не отображается в качестве значка темы.</span><span class="sxs-lookup"><span data-stu-id="b21be-161">If it is missing, no logo is displayed as the theme icon.</span></span><br/> |



 

<span data-ttu-id="b21be-162">В остальной части \[ \] раздела тема указываются пользовательские значки для таких функций рабочего стола, как компьютер, мои документы, сеть и корзина.</span><span class="sxs-lookup"><span data-stu-id="b21be-162">The rest of the \[Theme\] section specifies custom icons for desktop features like Computer, My Documents, Network, and Recycle Bin.</span></span> <span data-ttu-id="b21be-163">Если не указать настраиваемые значки рабочего стола, на рабочем столе будут отображаться системные значки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b21be-163">If you do not specify custom desktop icons, the desktop displays the system default desktop icons.</span></span>

<span data-ttu-id="b21be-164">Ниже приведены два примера того, как файл Theme задает значок **компьютера** .</span><span class="sxs-lookup"><span data-stu-id="b21be-164">The following are two examples of how a .theme file sets the **Computer** icon.</span></span>


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



<span data-ttu-id="b21be-165">Ниже приведены значения для значков рабочего стола по умолчанию в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b21be-165">The following are values for the default desktop icons in Windows 7.</span></span>


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



### <a name="control-panelcolors-section"></a><span data-ttu-id="b21be-166">\[Раздел "цвета" панели управления \\ \]</span><span class="sxs-lookup"><span data-stu-id="b21be-166">\[Control Panel\\Colors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="b21be-167">Этот раздел является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b21be-167">This section is optional.</span></span> <span data-ttu-id="b21be-168">Если этот раздел не включен в файл Theme, система использует параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b21be-168">If you do not include this section in your .theme file, the system uses default settings.</span></span> <span data-ttu-id="b21be-169">Если в вашей теме используется визуальный стиль Aero, не следует переопределять значения по умолчанию в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="b21be-169">If your theme uses the Aero visual style, you should avoid overriding the default values in this section.</span></span>

 

<span data-ttu-id="b21be-170">Цвет элементов, таких как полосы прокрутки, текст и кнопки, является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="b21be-170">The color of elements, such as scroll bars, text, and buttons, are customizable.</span></span> <span data-ttu-id="b21be-171">В файле Theme указаны значения RGB, которые необходимо изменить для этих элементов.</span><span class="sxs-lookup"><span data-stu-id="b21be-171">The .theme file specifies the RGB values to change for these elements.</span></span> <span data-ttu-id="b21be-172">Значения переопределяют значения по умолчанию визуального стиля и используются, если тема основана на классической версии Windows, Windows 7 Basic или высокая контрастность темах.</span><span class="sxs-lookup"><span data-stu-id="b21be-172">The values override the default values of the visual style and are used when your theme is based on Windows Classic, Windows 7 Basic, or High Contrast themes.</span></span>

<span data-ttu-id="b21be-173">Ниже приведен пример того, как устанавливаются цвета.</span><span class="sxs-lookup"><span data-stu-id="b21be-173">Following is an example of how colors are set.</span></span>


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



### <a name="control-panelcursors-section"></a><span data-ttu-id="b21be-174">\[\\Раздел курсоров панели \] управления</span><span class="sxs-lookup"><span data-stu-id="b21be-174">\[Control Panel\\Cursors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="b21be-175">Этот раздел является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b21be-175">This section is optional.</span></span> <span data-ttu-id="b21be-176">Если этот раздел не включен в файл Theme, система использует курсоры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b21be-176">If you do not include this section in your .theme file, the system uses default cursors.</span></span>

 

<span data-ttu-id="b21be-177">Тема также может изменять внешний вид курсоров.</span><span class="sxs-lookup"><span data-stu-id="b21be-177">A theme can also change the appearance of cursors.</span></span> <span data-ttu-id="b21be-178">Для этого создайте cur файлы, чтобы заменить курсоры Windows по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b21be-178">To do so, you create .cur files to replace the default Windows cursors.</span></span> <span data-ttu-id="b21be-179">Следующий пример относится к файлу Theme, который определяет курсоры для темы с названием *Спорт*.</span><span class="sxs-lookup"><span data-stu-id="b21be-179">The following example is from a .theme file that defines the cursors for a theme called *Sports*.</span></span>


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



### <a name="control-paneldesktop-section"></a><span data-ttu-id="b21be-180">\[Раздел " \\ Рабочий стол" панели управления \]</span><span class="sxs-lookup"><span data-stu-id="b21be-180">\[Control Panel\\Desktop\] Section</span></span>

> [!Note]  
> <span data-ttu-id="b21be-181">Это обязательный раздел.</span><span class="sxs-lookup"><span data-stu-id="b21be-181">This section is required.</span></span> <span data-ttu-id="b21be-182">Если этот раздел не включен в файл Theme, система пропустит вашу тему и не отобразит тему на панели управления.</span><span class="sxs-lookup"><span data-stu-id="b21be-182">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="b21be-183">Можно создать пользовательский фон рабочего стола и указать путь к файлу изображения.</span><span class="sxs-lookup"><span data-stu-id="b21be-183">You can create a custom desktop background and specify a path to the image file.</span></span> <span data-ttu-id="b21be-184">В следующем примере показано, как изменить внешний вид рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b21be-184">The following example shows how to modify the desktop appearance.</span></span>


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



### <a name="slideshow-section"></a><span data-ttu-id="b21be-185">\[Раздел "слайды" \]</span><span class="sxs-lookup"><span data-stu-id="b21be-185">\[Slideshow\] Section</span></span>

<span data-ttu-id="b21be-186">**Windows 7 и более поздние версии.**</span><span class="sxs-lookup"><span data-stu-id="b21be-186">**Windows 7 and later.**</span></span>

> [!Note]  
> <span data-ttu-id="b21be-187">Этот раздел является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b21be-187">This section is optional.</span></span> <span data-ttu-id="b21be-188">Если этот раздел не включен в файл Theme, система использует фоновое изображение рабочего стола, указанное в \[ разделе Панель управления \\ Рабочий стол \] .</span><span class="sxs-lookup"><span data-stu-id="b21be-188">If you do not include this section in your .theme file, the system uses the desktop background image specified in the \[Control Panel\\Desktop\] section.</span></span> <span data-ttu-id="b21be-189">При включении этого раздела необходимо указать здесь параметры показа слайдов.</span><span class="sxs-lookup"><span data-stu-id="b21be-189">If you include this section, you must specify slide show settings here.</span></span>

 

<span data-ttu-id="b21be-190">В качестве фона темы можно использовать изображения, которые хранятся локально или на изображениях, обслуживаемых RSS-каналом.</span><span class="sxs-lookup"><span data-stu-id="b21be-190">Your theme's background can be a slide show either of images stored locally or of images served by an RSS feed.</span></span> <span data-ttu-id="b21be-191">\[Раздел слайд-шоу \] файла содержит следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="b21be-191">The \[Slideshow\] section of the file contains the following attributes:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b21be-192">attribute</span><span class="sxs-lookup"><span data-stu-id="b21be-192">Attribute</span></span></th>
<th><span data-ttu-id="b21be-193">Описание</span><span class="sxs-lookup"><span data-stu-id="b21be-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b21be-194">Интервал = число миллисекунд</span><span class="sxs-lookup"><span data-stu-id="b21be-194">Interval=number of milliseconds</span></span></td>
<td><span data-ttu-id="b21be-195">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b21be-195">Required.</span></span> <span data-ttu-id="b21be-196">Интервал — это число, определяющее частоту изменения фона.</span><span class="sxs-lookup"><span data-stu-id="b21be-196">Interval is a number that determines how often the background changes.</span></span> <span data-ttu-id="b21be-197">Измеряется в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="b21be-197">It is measured in milliseconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b21be-198">Случайный = 0 или 1</span><span class="sxs-lookup"><span data-stu-id="b21be-198">Shuffle=0 or 1</span></span></td>
<td><span data-ttu-id="b21be-199">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="b21be-199">Required.</span></span> <span data-ttu-id="b21be-200">Случайный выбор в случайном порядке определяет фоновый режим.</span><span class="sxs-lookup"><span data-stu-id="b21be-200">Shuffle identifies whether the background shuffles.</span></span><br/> <span data-ttu-id="b21be-201">0 = отключено</span><span class="sxs-lookup"><span data-stu-id="b21be-201">0 = Disabled</span></span><br/> <span data-ttu-id="b21be-202">1 = включено</span><span class="sxs-lookup"><span data-stu-id="b21be-202">1 = Enabled</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b21be-203">RSS-канал = URL-адрес канала RSS</span><span class="sxs-lookup"><span data-stu-id="b21be-203">RSSFeed=URL to RSS feed</span></span></td>
<td><span data-ttu-id="b21be-204">Требуется, если не указан Имажесрутпас.</span><span class="sxs-lookup"><span data-stu-id="b21be-204">Required if ImagesRootPath is not specified.</span></span> <span data-ttu-id="b21be-205">RSS-канал указывает RSS-канал, используемый в качестве фонового показа слайдов.</span><span class="sxs-lookup"><span data-stu-id="b21be-205">RSSFeed specifies an RSS feed to use as the background slide show.</span></span> <span data-ttu-id="b21be-206">Чтобы канал работал, необходимо ссылаться на изображения с высоким разрешением, соответствующие &quot; &quot; стандартам, используемым <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">платформой RSS Windows</a>.</span><span class="sxs-lookup"><span data-stu-id="b21be-206">For the feed to work, you need to reference high-resolution images adhering to the &quot;enclosures&quot; standard used by the <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS Platform</a>.</span></span> <span data-ttu-id="b21be-207">Из-за этого ограничения файлы Theme, включающие RSS-канал, необходимо создавать вручную.</span><span class="sxs-lookup"><span data-stu-id="b21be-207">Because of this limitation, .theme files that include an RSS feed must be created manually.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b21be-208">Нельзя указать одновременно RSS-канал и Имажесрутпас.</span><span class="sxs-lookup"><span data-stu-id="b21be-208">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b21be-209">Имажесрутпас = путь к папке изображений</span><span class="sxs-lookup"><span data-stu-id="b21be-209">ImagesRootPath=path to image folder</span></span></td>
<td><span data-ttu-id="b21be-210">Требуется, если не указан RSS-канал.</span><span class="sxs-lookup"><span data-stu-id="b21be-210">Required if RSSFeed is not specified.</span></span> <span data-ttu-id="b21be-211">Имажесрутпас задает путь к набору изображений, которые будут использоваться в качестве фонового показа слайдов.</span><span class="sxs-lookup"><span data-stu-id="b21be-211">ImagesRootPath specifies a path to a set of images you want to use as the background slide show.</span></span> <span data-ttu-id="b21be-212">Изображения во вложенных папках не включаются в показ слайдов.</span><span class="sxs-lookup"><span data-stu-id="b21be-212">Images in subfolders are not included in the slide show.</span></span><br/> <span data-ttu-id="b21be-213">Имажесрутпас поддерживает подстановки переменных среды в пути.</span><span class="sxs-lookup"><span data-stu-id="b21be-213">ImagesRootPath supports Environment Variable substitutions in the path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b21be-214">Нельзя указать одновременно RSS-канал и Имажесрутпас.</span><span class="sxs-lookup"><span data-stu-id="b21be-214">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b21be-215">Элемент<em>N</em>путь = пути к конкретным изображениям</span><span class="sxs-lookup"><span data-stu-id="b21be-215">Item<em>N</em>Path=path(s) to specific image(s)</span></span></td>
<td><span data-ttu-id="b21be-216">Для использования с Имажесрутпас.</span><span class="sxs-lookup"><span data-stu-id="b21be-216">For use with ImagesRootPath.</span></span> <br/> <span data-ttu-id="b21be-217">Элемент<em>N</em>path указывает пути к определенным изображениям, что позволяет ограничить показ слайдов определенными изображениями, а не всеми изображениями в папке.</span><span class="sxs-lookup"><span data-stu-id="b21be-217">Item<em>N</em>Path specifies paths to specific images, so that you can limit the slide show to particular images instead of all images in a folder.</span></span> <span data-ttu-id="b21be-218">Если пути не указаны, все изображения в пути Имажесрутпас используются в слайдовой демонстрации, включая изображения, добавленные после создания и установки темы.</span><span class="sxs-lookup"><span data-stu-id="b21be-218">If no paths are specified, all images in the ImagesRootPath path are used in the slide show, including images added after creating and installing the theme.</span></span><br/> <span data-ttu-id="b21be-219">Путь к элементу<em>N</em>поддерживает подстановки переменных среды в пути.</span><span class="sxs-lookup"><span data-stu-id="b21be-219">Item<em>N</em>Path supports Environment Variable substitutions in the path.</span></span> <span data-ttu-id="b21be-220"><em>N</em> — 0, 1, 2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="b21be-220"><em>N</em> is 0, 1, 2, and so on.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b21be-221">В следующих примерах показано, как файл Theme указывает слайд-шоу для включения набора изображений, хранящихся локально.</span><span class="sxs-lookup"><span data-stu-id="b21be-221">The following examples show how a .theme file specifies the slide show to include a set of images stored locally.</span></span>


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



<span data-ttu-id="b21be-222">В следующем примере представлен шаблон для файла Theme, который создает слайд-шоу в фоновом режиме на рабочем столе с помощью изображений из RSS-канала.</span><span class="sxs-lookup"><span data-stu-id="b21be-222">The following example is a template for a .theme file that creates a desktop background slide show using images from an RSS feed.</span></span> <span data-ttu-id="b21be-223">Чтобы настроить шаблон, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b21be-223">Follow these steps to customize the template:</span></span>

1.  <span data-ttu-id="b21be-224">Скопируйте приведенный ниже пример и вставьте его в текстовый редактор.</span><span class="sxs-lookup"><span data-stu-id="b21be-224">Copy the following example and paste it into a text editor.</span></span>
2.  <span data-ttu-id="b21be-225">Замените {семенаме} именем, которое должно отображаться в коллекции "темы" панели управления персонализации.</span><span class="sxs-lookup"><span data-stu-id="b21be-225">Replace {themename} with the name you want to appear in the Personalization Control Panel themes gallery.</span></span>
3.  <span data-ttu-id="b21be-226">Замените {рссфидурл} полным путем к совместимому RSS-каналу.</span><span class="sxs-lookup"><span data-stu-id="b21be-226">Replace {rssfeedurl} with the full path to a compatible RSS feed.</span></span>
4.  <span data-ttu-id="b21be-227">Сохраните изменения в файле с расширением Theme.</span><span class="sxs-lookup"><span data-stu-id="b21be-227">Save the changes as a file with the ".theme" extension.</span></span>


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



### <a name="metrics-section"></a><span data-ttu-id="b21be-228">\[Раздел метрик \]</span><span class="sxs-lookup"><span data-stu-id="b21be-228">\[Metrics\] Section</span></span>

> [!Note]  
> <span data-ttu-id="b21be-229">Этот раздел является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b21be-229">This section is optional.</span></span> <span data-ttu-id="b21be-230">Если этот раздел не включен в файл Theme, система использует параметры визуального стиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b21be-230">If you do not include this section in your .theme file, the system uses default visual style settings.</span></span>

 

<span data-ttu-id="b21be-231">Системные метрики можно указать в файле Theme.</span><span class="sxs-lookup"><span data-stu-id="b21be-231">You can specify system metrics in a .theme file.</span></span> <span data-ttu-id="b21be-232">Системные метрики — это измерения различных отображаемых элементов, такие как ширина границы окна, Высота значка или ширина полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="b21be-232">System metrics are the dimensions of various display elements, such as the window border width, icon height, or scroll bar width.</span></span> <span data-ttu-id="b21be-233">Значения Нонклиентметрикс и Иконметрикс — это двоичные структуры, определяемые НОНКЛИЕНТМЕТРИКС и ИКОНМЕТРИКС в файле WinUser. h.</span><span class="sxs-lookup"><span data-stu-id="b21be-233">The NonclientMetrics and IconMetrics values are binary structures defined by NONCLIENTMETRICS and ICONMETRICS in winuser.h.</span></span> <span data-ttu-id="b21be-234">Ниже приведен пример изменения системных метрик.</span><span class="sxs-lookup"><span data-stu-id="b21be-234">Following is an example of how to change system metrics.</span></span>


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



### <a name="visual-styles-section"></a><span data-ttu-id="b21be-235">\[Раздел стилей визуальных элементов \]</span><span class="sxs-lookup"><span data-stu-id="b21be-235">\[Visual Styles\] Section</span></span>

> [!Note]  
> <span data-ttu-id="b21be-236">Это обязательный раздел.</span><span class="sxs-lookup"><span data-stu-id="b21be-236">This section is required.</span></span> <span data-ttu-id="b21be-237">Если этот раздел не включен в файл Theme, система пропустит вашу тему и не отобразит тему на панели управления.</span><span class="sxs-lookup"><span data-stu-id="b21be-237">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="b21be-238">Вы можете указать конкретные сведения о размере и цвете элементов рабочего стола в файлах мсстилес.</span><span class="sxs-lookup"><span data-stu-id="b21be-238">You can supply specific information concerning the size and color of desktop elements in .msstyles files.</span></span> <span data-ttu-id="b21be-239">Разделы "цвет" и "размер" в файлах Theme могут быть заменены файлами. мсстилес, которые позволяют более подробно изменять элементы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b21be-239">The color and size sections of .theme files can be replaced by .msstyles files which enable you to modify desktop elements in more detail.</span></span> <span data-ttu-id="b21be-240">Эти файлы указываются в разделе Стили визуальных элементов файла Theme.</span><span class="sxs-lookup"><span data-stu-id="b21be-240">These files are specified in the visual styles section of a .theme file.</span></span> <span data-ttu-id="b21be-241">Ниже приведен пример раздела визуальных стилей.</span><span class="sxs-lookup"><span data-stu-id="b21be-241">Following is an example of a visual styles section.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



<span data-ttu-id="b21be-242">Добавление элемента пути в мсстилес-файл является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b21be-242">Adding a Path element to a .msstyles file is optional.</span></span> <span data-ttu-id="b21be-243">При указании пути следует удалить секции метрик и цвет из файла Theme.</span><span class="sxs-lookup"><span data-stu-id="b21be-243">If you supply a path, you should remove the metrics and color sections from the .theme file.</span></span> <span data-ttu-id="b21be-244">При удалении этих разделов цвета, шрифты и размеры темы берутся из мсстилес-файла и соответствуют намерениям автора. мсстилес.</span><span class="sxs-lookup"><span data-stu-id="b21be-244">When these sections are removed, the colors, fonts, and sizes for a theme come from the .msstyles file and match the .msstyles author's intent.</span></span> <span data-ttu-id="b21be-245">Невозможность удаления разделов метрик и цветов может привести к проблемам с прорисовкой в Windows или приложениях.</span><span class="sxs-lookup"><span data-stu-id="b21be-245">Failing to remove the metric and color sections can cause Windows or applications to have drawing problems.</span></span>

<span data-ttu-id="b21be-246">**Windows Vista или Windows 7:** Когда путь указывает на Aero. мсстилес, можно указать требуемый цвет стекла, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b21be-246">**Windows Vista / Windows 7:** When the path points to Aero.msstyles, you can specify the desired Glass Color, as shown in the following example.</span></span>

<span data-ttu-id="b21be-247">**Windows 7:** Когда путь указывает на Aero. мсстилес, можно также указать нужное значение прозрачности, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b21be-247">**Windows 7:** When the path points to Aero.msstyles, you can also specify the desired Transparency value, as shown in the following example.</span></span>


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



<span data-ttu-id="b21be-248">Если значения Колоризатионколор и прозрачности точно соответствуют системному цвету, в панели управления персонализации отображается системное имя цвета.</span><span class="sxs-lookup"><span data-stu-id="b21be-248">If the ColorizationColor and Transparency values exactly match a system color, the Personalization Control Panel displays the system name for the color.</span></span> <span data-ttu-id="b21be-249">В противном случае цвет помечается как "настраиваемый".</span><span class="sxs-lookup"><span data-stu-id="b21be-249">Otherwise, the color is labeled "Custom."</span></span>

<span data-ttu-id="b21be-250">Ниже приведен раздел VisualStyles для основной темы Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b21be-250">The following shows a VisualStyles section for the Windows 7 Basic theme.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



<span data-ttu-id="b21be-251">Ниже приведен раздел VisualStyles для классической темы Windows.</span><span class="sxs-lookup"><span data-stu-id="b21be-251">The following shows a VisualStyles section for the Windows Classic theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



<span data-ttu-id="b21be-252">Ниже приведен раздел VisualStyles для высокая контрастность черной темы.</span><span class="sxs-lookup"><span data-stu-id="b21be-252">The following shows a VisualStyles section for a High Contrast Black theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a><span data-ttu-id="b21be-253">\[Разделы «звуки \] и \[ аппевентс \] » (звуки)</span><span class="sxs-lookup"><span data-stu-id="b21be-253">\[Sounds\] and \[AppEvents\] Sections (Sounds)</span></span>

> [!Note]  
> <span data-ttu-id="b21be-254">Этот раздел является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b21be-254">This section is optional.</span></span> <span data-ttu-id="b21be-255">Если этот раздел не включен в файл Theme, система использует параметры звука по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b21be-255">If you do not include this section in your .theme file, the system uses default sound settings.</span></span>

 

<span data-ttu-id="b21be-256">Пользователь может выбрать значок **звука** на панели управления, чтобы связать звуки с событиями, происходящими в приложениях.</span><span class="sxs-lookup"><span data-stu-id="b21be-256">The user can select the **Sound** icon in Control Panel to associate sounds with events that occur in applications.</span></span> <span data-ttu-id="b21be-257">Например, WAV-файл может воспроизводиться при открытии приложения.</span><span class="sxs-lookup"><span data-stu-id="b21be-257">For example, a .wav file can play when an application is opened.</span></span> <span data-ttu-id="b21be-258">В файле Theme можно указать WAV-файлы для замены значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b21be-258">A .theme file can specify .wav files to replace the default ones.</span></span> <span data-ttu-id="b21be-259">В приведенном ниже примере показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="b21be-259">The following example shows how to do this.</span></span>


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



<span data-ttu-id="b21be-260">**Windows 7 и более поздние версии:** Вместо перечисления каждого звука можно указать имя звуковой схемы.</span><span class="sxs-lookup"><span data-stu-id="b21be-260">**Windows 7 and later:** A sound scheme name can be specified instead of listing each sound separately.</span></span>


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



<span data-ttu-id="b21be-261">Значение Счеменаме указывает имя звуковой схемы или локализованное имя звуковой схемы, как показано в примере выше.</span><span class="sxs-lookup"><span data-stu-id="b21be-261">The SchemeName value specifies the sound scheme name or the localized sound scheme name, as shown in the example above.</span></span>

### <a name="boot-section"></a><span data-ttu-id="b21be-262">\[\]Раздел загрузки</span><span class="sxs-lookup"><span data-stu-id="b21be-262">\[Boot\] Section</span></span>

> [!Note]  
> <span data-ttu-id="b21be-263">**Экранные заставки не рекомендуются в юбилейном обновлении Windows 10 и выходят за рамки.**</span><span class="sxs-lookup"><span data-stu-id="b21be-263">**Screen Savers are deprecated in the Windows 10 Anniversary Update and beyond.**</span></span>

 

> [!Note]  
> <span data-ttu-id="b21be-264">Этот раздел является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b21be-264">This section is optional.</span></span> <span data-ttu-id="b21be-265">Если этот раздел не включен в файл Theme, экранная заставка не используется.</span><span class="sxs-lookup"><span data-stu-id="b21be-265">If you do not include this section in your .theme file, no screen saver is used.</span></span>

 

<span data-ttu-id="b21be-266">В файле Theme можно указать экранную заставку Windows для использования.</span><span class="sxs-lookup"><span data-stu-id="b21be-266">In the .theme file, you can specify the screen saver for Windows to use.</span></span> <span data-ttu-id="b21be-267">В следующем примере приведена иллюстрация этого.</span><span class="sxs-lookup"><span data-stu-id="b21be-267">The following example shows this.</span></span>


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a><span data-ttu-id="b21be-268">\[\]Раздел мастерсемеселектор</span><span class="sxs-lookup"><span data-stu-id="b21be-268">\[MasterThemeSelector\] Section</span></span>

> [!Note]  
> <span data-ttu-id="b21be-269">Это обязательный раздел.</span><span class="sxs-lookup"><span data-stu-id="b21be-269">This section is required.</span></span> <span data-ttu-id="b21be-270">Если этот раздел не включен в файл Theme, система пропустит вашу тему и не отобразит тему на панели управления.</span><span class="sxs-lookup"><span data-stu-id="b21be-270">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="b21be-271">Раздел Selector главной темы файла Theme всегда должен быть включен в качестве тега, который указывает, что файл является допустимым.</span><span class="sxs-lookup"><span data-stu-id="b21be-271">The master theme selector section of the .theme file should always be included as a tag that indicates the file is valid.</span></span> <span data-ttu-id="b21be-272">У вас нет выбора значений для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="b21be-272">You do not have a choice of values for this parameter.</span></span> <span data-ttu-id="b21be-273">Это показано ниже.</span><span class="sxs-lookup"><span data-stu-id="b21be-273">The following shows this.</span></span>


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a><span data-ttu-id="b21be-274">Пример файла темы</span><span class="sxs-lookup"><span data-stu-id="b21be-274">Example of a Theme File</span></span>

<span data-ttu-id="b21be-275">В следующем примере показан полный файл Theme.</span><span class="sxs-lookup"><span data-stu-id="b21be-275">The following example shows a complete .theme file.</span></span>


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



## <a name="installing-theme-files"></a><span data-ttu-id="b21be-276">Установка файлов темы</span><span class="sxs-lookup"><span data-stu-id="b21be-276">Installing Theme Files</span></span>

<span data-ttu-id="b21be-277">При инициализации Windows операционная система перечисляет подкаталоги первого уровня% WinDir% \\ ресурсов \\ для обнаружения доступных тем.</span><span class="sxs-lookup"><span data-stu-id="b21be-277">When Windows is initialized, the operating system enumerates the first-level subdirectories of %WinDir%\\Resources\\ to identify available themes.</span></span> <span data-ttu-id="b21be-278">Системные файлы темы по умолчанию расположены в темах% WinDir% \\ ресурсов \\ .</span><span class="sxs-lookup"><span data-stu-id="b21be-278">The system default theme files are located in %WinDir%\\Resources\\Themes.</span></span> <span data-ttu-id="b21be-279">Файлы пользовательских тем хранятся в папках% WINDIR% \\ пользователей \\ <username> \\ AppData \\ локальные \\ \\ темы Microsoft Windows \\ .</span><span class="sxs-lookup"><span data-stu-id="b21be-279">The user theme files are stored in %WinDir%\\Users\\<username>\\AppData\\Local\\Microsoft\\Windows\\Themes.</span></span>

<span data-ttu-id="b21be-280">Файл Theme имеет сопоставления файлов; Таким образом, приложения установщика тем могут вызвать [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) в файле Theme, чтобы открыть окно **персонализации** на панели управления для указанной темы.</span><span class="sxs-lookup"><span data-stu-id="b21be-280">A .theme file has file associations; therefore, theme installer applications can call [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) on a .theme file to open the **Personalization** window in Control Panel to the specified theme.</span></span>

## <a name="theme-packs"></a><span data-ttu-id="b21be-281">Пакеты тем</span><span class="sxs-lookup"><span data-stu-id="b21be-281">Theme Packs</span></span>

<span data-ttu-id="b21be-282">**Windows 7 и более поздние версии.**</span><span class="sxs-lookup"><span data-stu-id="b21be-282">**Windows 7 and later.**</span></span> <span data-ttu-id="b21be-283">Пакет темы — это CAB-файл, который содержит не только файл Theme, но и файлы, необходимые для реализации темы на другом компьютере, например звуковые файлы и изображения.</span><span class="sxs-lookup"><span data-stu-id="b21be-283">A theme pack is a .cab file that contains not only the .theme file but also the files needed to implement the theme on another computer, such as sound files and images.</span></span> <span data-ttu-id="b21be-284">Пользователи могут создавать пакеты тем с помощью панели управления персонализацией.</span><span class="sxs-lookup"><span data-stu-id="b21be-284">Users can create theme packs through the Personalization Control Panel.</span></span>

<span data-ttu-id="b21be-285">В число поддерживаемых типов файлов входят следующие:</span><span class="sxs-lookup"><span data-stu-id="b21be-285">Supported file types include the following:</span></span>



| <span data-ttu-id="b21be-286">Тип файла</span><span class="sxs-lookup"><span data-stu-id="b21be-286">File type</span></span>    | <span data-ttu-id="b21be-287">Расширение</span><span class="sxs-lookup"><span data-stu-id="b21be-287">Extension</span></span>                           |
|--------------|-------------------------------------|
| <span data-ttu-id="b21be-288">Тема</span><span class="sxs-lookup"><span data-stu-id="b21be-288">Theme</span></span>        | <span data-ttu-id="b21be-289">.theme</span><span class="sxs-lookup"><span data-stu-id="b21be-289">.theme</span></span>                              |
| <span data-ttu-id="b21be-290">Образ</span><span class="sxs-lookup"><span data-stu-id="b21be-290">Image</span></span>        | <span data-ttu-id="b21be-291">JPG, JPEG, BMP, DIB, TIF, PNG</span><span class="sxs-lookup"><span data-stu-id="b21be-291">.jpg, .jpeg, .bmp, .dib, .tif, .png</span></span> |
| <span data-ttu-id="b21be-292">Звук</span><span class="sxs-lookup"><span data-stu-id="b21be-292">Sound</span></span>        | <span data-ttu-id="b21be-293">.wav</span><span class="sxs-lookup"><span data-stu-id="b21be-293">.wav</span></span>                                |
| <span data-ttu-id="b21be-294">Курсор мыши</span><span class="sxs-lookup"><span data-stu-id="b21be-294">Mouse cursor</span></span> | <span data-ttu-id="b21be-295">. cur,. ani</span><span class="sxs-lookup"><span data-stu-id="b21be-295">.cur, .ani</span></span>                          |
| <span data-ttu-id="b21be-296">Значок рабочего стола</span><span class="sxs-lookup"><span data-stu-id="b21be-296">Desktop icon</span></span> | <span data-ttu-id="b21be-297">ICO</span><span class="sxs-lookup"><span data-stu-id="b21be-297">.ico</span></span>                                |
| <span data-ttu-id="b21be-298">Логотип торговой марки</span><span class="sxs-lookup"><span data-stu-id="b21be-298">Brand logo</span></span>   | <span data-ttu-id="b21be-299">.png</span><span class="sxs-lookup"><span data-stu-id="b21be-299">.png</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="b21be-300">См. также</span><span class="sxs-lookup"><span data-stu-id="b21be-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b21be-301">Общие сведения о визуальных стилях</span><span class="sxs-lookup"><span data-stu-id="b21be-301">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

