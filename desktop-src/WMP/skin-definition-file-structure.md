---
title: Структура файла определения обложки
description: Структура файла определения обложки
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Обложки проигрывателя Windows Media, файлы определения обложки
- обложки, файлы определения обложки
- файлы для обложек, определение обложки
- файлы определения обложки, структура
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068241"
---
# <a name="skin-definition-file-structure"></a><span data-ttu-id="9520d-107">Структура файла определения обложки</span><span class="sxs-lookup"><span data-stu-id="9520d-107">Skin Definition File Structure</span></span>

<span data-ttu-id="9520d-108">Файл определения обложки должен соответствовать определенной структуре.</span><span class="sxs-lookup"><span data-stu-id="9520d-108">The skin definition file must follow a specific structure.</span></span> <span data-ttu-id="9520d-109">Начните с элемента **Theme** , создайте один или несколько элементов **представления** , а затем определите каждый элемент **представления** с элементами пользовательского интерфейса, соответствующими типу представления, которое вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="9520d-109">You start with a **THEME** element, create one or more **VIEW** elements, and then define each **VIEW** element with the user interface elements appropriate for the type of view you want to use.</span></span>

## <a name="theme-elements"></a><span data-ttu-id="9520d-110">Элементы темы</span><span class="sxs-lookup"><span data-stu-id="9520d-110">THEME Elements</span></span>

<span data-ttu-id="9520d-111">На верхнем уровне необходимо запустить файл определения обложки с помощью элемента **Theme** и закрыть его.</span><span class="sxs-lookup"><span data-stu-id="9520d-111">At the top level, you must start the skin definition file with the **THEME** element and close with it.</span></span>


```C++
<THEME>
    ...
</THEME>

```



<span data-ttu-id="9520d-112">Элемент **Theme** является корневым элементом для обложки.</span><span class="sxs-lookup"><span data-stu-id="9520d-112">The **THEME** element is the root element for your skin.</span></span> <span data-ttu-id="9520d-113">В файле определения обложки может быть только один элемент **Theme** , который должен находиться на верхнем уровне.</span><span class="sxs-lookup"><span data-stu-id="9520d-113">There can be only one **THEME** element in a skin definition file, and it must be at the top level.</span></span> <span data-ttu-id="9520d-114">Элементы **темы** имеют определенные и внешние атрибуты, хотя в большинстве случаев их не нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="9520d-114">**THEME** elements have specific and ambient attributes, though most of the time you will not need to use them.</span></span> <span data-ttu-id="9520d-115">Дополнительные сведения об этих атрибутах см. в [справочнике по программированию для обложки](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9520d-115">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="view-elements"></a><span data-ttu-id="9520d-116">Просмотр элементов</span><span class="sxs-lookup"><span data-stu-id="9520d-116">VIEW Elements</span></span>

<span data-ttu-id="9520d-117">Каждая **Тема** должна иметь по крайней мере один элемент **View** .</span><span class="sxs-lookup"><span data-stu-id="9520d-117">Each **THEME** must have at least one **VIEW** element.</span></span> <span data-ttu-id="9520d-118">Элемент **View** управляет определенным изображением, которое отображается на экране.</span><span class="sxs-lookup"><span data-stu-id="9520d-118">The **VIEW** element governs the particular image you see on the screen.</span></span> <span data-ttu-id="9520d-119">Может потребоваться несколько представлений, чтобы можно было переключаться назад и вперед.</span><span class="sxs-lookup"><span data-stu-id="9520d-119">You may want to have more than one view, so you can switch back and forth.</span></span> <span data-ttu-id="9520d-120">Например, может потребоваться большое представление для работы с списками воспроизведения, среднее представление для просмотра визуализаций и маленькое представление, которое помещается в углу экрана.</span><span class="sxs-lookup"><span data-stu-id="9520d-120">For example, you might want to have a large view for working with playlists, a medium view for watching visualizations, and a tiny view that fits in a corner of the screen.</span></span>

<span data-ttu-id="9520d-121">При создании нескольких представлений необходимо убедиться, что каждое представление имеет уникальное значение атрибута **ID** , которое будет использоваться для идентификации представления.</span><span class="sxs-lookup"><span data-stu-id="9520d-121">If you are creating multiple views, you will want to make sure that each view has a unique **ID** attribute value that will be used to identify the view.</span></span> <span data-ttu-id="9520d-122">Необходимо определить атрибут **backgroundImage** , иначе представление не будет иметь начального изображения.</span><span class="sxs-lookup"><span data-stu-id="9520d-122">You must define the **backgroundImage** attribute or your view will have no starting image.</span></span> <span data-ttu-id="9520d-123">Если вы не хотите отображать прямоугольное изображение, вы, вероятно, захотите использовать атрибут **клиппингколор** , чтобы определить области обложки, которые не будут отображаться, и, вероятно, захотите задать атрибут **заголовка** элемента **View** .</span><span class="sxs-lookup"><span data-stu-id="9520d-123">If you do not want to display a rectangular image, you will probably want to use the **clippingColor** attribute to define the areas of your skin that will not display, and you will probably want to set the **titleBar** attribute of the **VIEW** element.</span></span>

<span data-ttu-id="9520d-124">Каждый элемент **представления** может также иметь одно или несколько элементов вложенного **представления** .</span><span class="sxs-lookup"><span data-stu-id="9520d-124">Each **VIEW** element can also have one or more **SUBVIEW** elements.</span></span> <span data-ttu-id="9520d-125">Элемент вложенного **представления** аналогичен **представлению** и может использоваться для частей обложки, которые нужно перемещать вокруг, скрывать или отображать.</span><span class="sxs-lookup"><span data-stu-id="9520d-125">A **SUBVIEW** element is similar to a **VIEW** and can be used for parts of your skin that you want to move around, hide, or show.</span></span> <span data-ttu-id="9520d-126">Например, элемент вложенного **представления** может использоваться для создания скользящего лотка, который выводится из обложки для отображения графического эквалайзера.</span><span class="sxs-lookup"><span data-stu-id="9520d-126">For example, a **SUBVIEW** element might be used to create a sliding tray that pops out of your skin to display a graphic equalizer.</span></span> <span data-ttu-id="9520d-127">Элементы вложенного **представления** могут быть согласованы с **представлением** и иметь другие специальные связи с **представлением**.</span><span class="sxs-lookup"><span data-stu-id="9520d-127">**SUBVIEW** elements can be aligned with the **VIEW** and have other special relationships to the **VIEW**.</span></span>

## <a name="initializing-windows-media-player"></a><span data-ttu-id="9520d-128">Инициализация проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="9520d-128">Initializing Windows Media Player</span></span>

<span data-ttu-id="9520d-129">Вы можете задать определенные начальные свойства проигрывателя Windows Media с помощью параметров " **проигрыватель**", " **Параметры**" и " **элементы управления** ".</span><span class="sxs-lookup"><span data-stu-id="9520d-129">You can set certain initial properties of Windows Media Player by using the **PLAYER**, **SETTINGS**, and **CONTROLS** elements.</span></span> <span data-ttu-id="9520d-130">Например, можно задать для тома первоначальный уровень или задать значение по умолчанию для имени файла.</span><span class="sxs-lookup"><span data-stu-id="9520d-130">For example, you could set the volume to an initial level or give a default value for a file name.</span></span>

<span data-ttu-id="9520d-131">В следующем коде показано, как задать значение **URL-адреса** в обложке:</span><span class="sxs-lookup"><span data-stu-id="9520d-131">The following code shows how to set the **URL** value in a skin:</span></span>


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



<span data-ttu-id="9520d-132">Если вы хотите задать для атрибута " **Автозапуск** " **параметров** значение false, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="9520d-132">If you wanted to set the **autoStart** attribute of **SETTINGS** to False, you would use the following code:</span></span>


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



<span data-ttu-id="9520d-133">Обратите внимание, что элемент **Settings** вложен внутри элемента **Player** .</span><span class="sxs-lookup"><span data-stu-id="9520d-133">Note that the **SETTINGS** element is nested inside the **PLAYER** element.</span></span>

<span data-ttu-id="9520d-134">Используя эти элементы, во время разработки можно указать следующие атрибуты и события:</span><span class="sxs-lookup"><span data-stu-id="9520d-134">Using these elements, the following attributes and events can be specified at design time:</span></span>

<span data-ttu-id="9520d-135">**Атрибуты элемента PLAYER**</span><span class="sxs-lookup"><span data-stu-id="9520d-135">**PLAYER Element Attributes**</span></span>

-   <span data-ttu-id="9520d-136">**url**</span><span class="sxs-lookup"><span data-stu-id="9520d-136">**url**</span></span>
-   <span data-ttu-id="9520d-137">**ответов**</span><span class="sxs-lookup"><span data-stu-id="9520d-137">**Buffering**</span></span>
-   <span data-ttu-id="9520d-138">**куррентитемчанже**</span><span class="sxs-lookup"><span data-stu-id="9520d-138">**Currentitemchange**</span></span>
-   <span data-ttu-id="9520d-139">**куррентплайлистчанже**</span><span class="sxs-lookup"><span data-stu-id="9520d-139">**Currentplaylistchange**</span></span>
-   <span data-ttu-id="9520d-140">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="9520d-140">**Error**</span></span>
-   <span data-ttu-id="9520d-141">**маркерхит**</span><span class="sxs-lookup"><span data-stu-id="9520d-141">**Markerhit**</span></span>
-   <span data-ttu-id="9520d-142">**медиачанже**</span><span class="sxs-lookup"><span data-stu-id="9520d-142">**Mediachange**</span></span>
-   <span data-ttu-id="9520d-143">**медиаколлектиончанже**</span><span class="sxs-lookup"><span data-stu-id="9520d-143">**Mediacollectionchange**</span></span>
-   <span data-ttu-id="9520d-144">**модечанже**</span><span class="sxs-lookup"><span data-stu-id="9520d-144">**Modechange**</span></span>
-   <span data-ttu-id="9520d-145">**мпенстатечанже**</span><span class="sxs-lookup"><span data-stu-id="9520d-145">**Mpenstatechange**</span></span>
-   <span data-ttu-id="9520d-146">**млайлистчанже**</span><span class="sxs-lookup"><span data-stu-id="9520d-146">**Mlaylistchange**</span></span>
-   <span data-ttu-id="9520d-147">**млайстатечанже**</span><span class="sxs-lookup"><span data-stu-id="9520d-147">**Mlaystatechange**</span></span>
-   <span data-ttu-id="9520d-148">**моситиончанже**</span><span class="sxs-lookup"><span data-stu-id="9520d-148">**Mositionchange**</span></span>
-   <span data-ttu-id="9520d-149">**мкрипткомманд**</span><span class="sxs-lookup"><span data-stu-id="9520d-149">**Mcriptcommand**</span></span>
-   <span data-ttu-id="9520d-150">**мтатусчанже**</span><span class="sxs-lookup"><span data-stu-id="9520d-150">**Mtatuschange**</span></span>

<span data-ttu-id="9520d-151">**Атрибуты элемента SETTINGS**</span><span class="sxs-lookup"><span data-stu-id="9520d-151">**SETTINGS Element Attributes**</span></span>

-   <span data-ttu-id="9520d-152">**Автозапуска**</span><span class="sxs-lookup"><span data-stu-id="9520d-152">**autoStart**</span></span>
-   <span data-ttu-id="9520d-153">**между**</span><span class="sxs-lookup"><span data-stu-id="9520d-153">**balance**</span></span>
-   <span data-ttu-id="9520d-154">**baseURL**</span><span class="sxs-lookup"><span data-stu-id="9520d-154">**baseURL**</span></span>
-   <span data-ttu-id="9520d-155">**дефаултфраме**</span><span class="sxs-lookup"><span data-stu-id="9520d-155">**defaultFrame**</span></span>
-   <span data-ttu-id="9520d-156">**енаблиррордиалогс**</span><span class="sxs-lookup"><span data-stu-id="9520d-156">**enableErrorDialogs**</span></span>
-   <span data-ttu-id="9520d-157">**инвокеурлс**</span><span class="sxs-lookup"><span data-stu-id="9520d-157">**invokeURLs**</span></span>
-   <span data-ttu-id="9520d-158">**отключен**</span><span class="sxs-lookup"><span data-stu-id="9520d-158">**mute**</span></span>
-   <span data-ttu-id="9520d-159">**плайкаунт**</span><span class="sxs-lookup"><span data-stu-id="9520d-159">**playCount**</span></span>
-   <span data-ttu-id="9520d-160">**курсе**</span><span class="sxs-lookup"><span data-stu-id="9520d-160">**rate**</span></span>
-   <span data-ttu-id="9520d-161">**тома**</span><span class="sxs-lookup"><span data-stu-id="9520d-161">**volume**</span></span>

## <a name="controls-element-attributes"></a><span data-ttu-id="9520d-162">Элементы управления атрибутами элементов</span><span class="sxs-lookup"><span data-stu-id="9520d-162">CONTROLS Element Attributes</span></span>

-   <span data-ttu-id="9520d-163">**куррентмаркер**</span><span class="sxs-lookup"><span data-stu-id="9520d-163">**currentMarker**</span></span>
-   <span data-ttu-id="9520d-164">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="9520d-164">**currentPosition**</span></span>

## <a name="other-user-interface-elements"></a><span data-ttu-id="9520d-165">Другие элементы пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="9520d-165">Other User Interface Elements</span></span>

<span data-ttu-id="9520d-166">Определив элементы **темы** и **представления** , необходимо заполнить **представление** конкретными элементами пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9520d-166">Once you have defined your **THEME** and **VIEW** elements, you must populate your **VIEW** with specific user interface elements.</span></span> <span data-ttu-id="9520d-167">Не обязательно использовать все доступные элементы в обложке, а именно те, которые вам нужны.</span><span class="sxs-lookup"><span data-stu-id="9520d-167">You do not have to use all the available elements in a skin, just the ones you need.</span></span>

<span data-ttu-id="9520d-168">Если пользователь может видеть элемент, он называется элементом управления.</span><span class="sxs-lookup"><span data-stu-id="9520d-168">If an element can be seen by the user, it is called a control.</span></span> <span data-ttu-id="9520d-169">Для обложек доступны следующие элементы управления:</span><span class="sxs-lookup"><span data-stu-id="9520d-169">The following controls are available for skins:</span></span>

-   <span data-ttu-id="9520d-170">Кнопки</span><span class="sxs-lookup"><span data-stu-id="9520d-170">Buttons</span></span>
-   <span data-ttu-id="9520d-171">Ползунки, настраиваемые ползунки и индикаторы выполнения</span><span class="sxs-lookup"><span data-stu-id="9520d-171">Sliders, custom sliders, and progress bars</span></span>
-   <span data-ttu-id="9520d-172">Текстовые поля</span><span class="sxs-lookup"><span data-stu-id="9520d-172">Text boxes</span></span>
-   <span data-ttu-id="9520d-173">Окна видео</span><span class="sxs-lookup"><span data-stu-id="9520d-173">Video windows</span></span>
-   <span data-ttu-id="9520d-174">Окна визуализации</span><span class="sxs-lookup"><span data-stu-id="9520d-174">Visualization windows</span></span>
-   <span data-ttu-id="9520d-175">Окна списков воспроизведения</span><span class="sxs-lookup"><span data-stu-id="9520d-175">Playlist windows</span></span>
-   <span data-ttu-id="9520d-176">Окна подпредставления</span><span class="sxs-lookup"><span data-stu-id="9520d-176">Subview windows</span></span>

<span data-ttu-id="9520d-177">Кроме того, для дальнейшего определения действий проигрывателя Windows Media можно использовать несколько элементов, но для них требуются визуальные элементы, такие как кнопки или ползунки:</span><span class="sxs-lookup"><span data-stu-id="9520d-177">In addition, several elements can be used to further define Windows Media Player actions, but they require visual elements such as buttons or sliders:</span></span>

-   <span data-ttu-id="9520d-178">Параметры видео</span><span class="sxs-lookup"><span data-stu-id="9520d-178">Video settings</span></span>
-   <span data-ttu-id="9520d-179">Параметры эквалайзера</span><span class="sxs-lookup"><span data-stu-id="9520d-179">Equalizer Settings</span></span>
-   <span data-ttu-id="9520d-180">Параметры визуализации</span><span class="sxs-lookup"><span data-stu-id="9520d-180">Visualization settings</span></span>

## <a name="buttons"></a><span data-ttu-id="9520d-181">Кнопки</span><span class="sxs-lookup"><span data-stu-id="9520d-181">Buttons</span></span>

<span data-ttu-id="9520d-182">Кнопки являются наиболее популярными частью обложки.</span><span class="sxs-lookup"><span data-stu-id="9520d-182">Buttons are the most popular part of a skin.</span></span> <span data-ttu-id="9520d-183">Можно использовать кнопки для запуска таких действий, как воспроизведение, завершение, выход, уменьшение и переключение в другое представление.</span><span class="sxs-lookup"><span data-stu-id="9520d-183">You can use buttons to trigger actions such as play, stop, quit, minimize, and switch to different view.</span></span> <span data-ttu-id="9520d-184">Проигрыватель Windows Media предоставляет создателю обложки два типа элементов Button: элемент **Button** и элемент **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="9520d-184">Windows Media Player provides the skin creator with two types of button elements: the **BUTTON** element and the **BUTTONGROUP** element.</span></span> <span data-ttu-id="9520d-185">Кроме того, существует несколько предопределенных типов кнопок.</span><span class="sxs-lookup"><span data-stu-id="9520d-185">In addition, there are several predefined types of buttons.</span></span>

-   <span data-ttu-id="9520d-186">**Элемент BUTTON.**</span><span class="sxs-lookup"><span data-stu-id="9520d-186">**BUTTON element.**</span></span> <span data-ttu-id="9520d-187">Элемент **Button** используется для отдельных кнопок.</span><span class="sxs-lookup"><span data-stu-id="9520d-187">The **BUTTON** element is used for individual buttons.</span></span> <span data-ttu-id="9520d-188">При использовании элемента **Button** необходимо предоставить изображение для каждой кнопки и определить точное расположение, в котором должна отображаться кнопка относительно фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="9520d-188">If you use the **BUTTON** element, you must supply an image for each button and define the exact location where you want the button to appear relative to the background image.</span></span> <span data-ttu-id="9520d-189">Одним из преимуществ элемента **Button** является то, что можно динамически изменить изображение кнопки.</span><span class="sxs-lookup"><span data-stu-id="9520d-189">One of the advantages of the **BUTTON** element is that you can change the button image dynamically.</span></span>
-   <span data-ttu-id="9520d-190">**Элемент BUTTONGROUP.**</span><span class="sxs-lookup"><span data-stu-id="9520d-190">**BUTTONGROUP element.**</span></span> <span data-ttu-id="9520d-191">Элемент **BUTTONGROUP** используется для групп кнопок.</span><span class="sxs-lookup"><span data-stu-id="9520d-191">The **BUTTONGROUP** element is used for groups of buttons.</span></span> <span data-ttu-id="9520d-192">На самом деле каждый элемент **BUTTONGROUP** необходимо заключать в пару тегов **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="9520d-192">In fact, you must enclose each **BUTTONGROUP** element with a pair of **BUTTONGROUP** tags.</span></span> <span data-ttu-id="9520d-193">Использование групп кнопок проще, чем использование отдельных кнопок, так как нет необходимости указывать точное расположение для каждой кнопки.</span><span class="sxs-lookup"><span data-stu-id="9520d-193">Using button groups is easier than using individual buttons because you do not have to specify the exact location for each button.</span></span> <span data-ttu-id="9520d-194">Вместо этого вы предоставляете отдельную карту изображения, определяющую действия, которые будут выполняться при наведении указателя мыши на область фона или щелчке мышью.</span><span class="sxs-lookup"><span data-stu-id="9520d-194">Instead, you supply a separate image map that defines the actions that will take place when the mouse hovers over or clicks an area on your background.</span></span> <span data-ttu-id="9520d-195">Использование карт изображений несложно, так как вы можете взять рисунок, созданный для фона, и скопировать его на слой сопоставления в программе редактирования графики.</span><span class="sxs-lookup"><span data-stu-id="9520d-195">Using image maps is easy because you can take the art you created for your background and copy it to a mapping layer in your graphics editing program.</span></span> <span data-ttu-id="9520d-196">Использование программы редактирования графики выполняется быстрее и точнее, чем попытка определить точное место размещения отдельной кнопки на фоне.</span><span class="sxs-lookup"><span data-stu-id="9520d-196">Using your graphics editing program is faster and more precise than trying to define exactly where an individual button should be placed on your background.</span></span>
-   <span data-ttu-id="9520d-197">**Стандартные кнопки.**</span><span class="sxs-lookup"><span data-stu-id="9520d-197">**Predefined buttons.**</span></span> <span data-ttu-id="9520d-198">Существует несколько предопределенных кнопок.</span><span class="sxs-lookup"><span data-stu-id="9520d-198">There are several predefined buttons.</span></span> <span data-ttu-id="9520d-199">Например, можно использовать кнопку ПЛАЙЕЛЕМЕНТ для воспроизведения цифровых мультимедийных файлов и СТОПЕЛЕМЕНТ, чтобы прерывать воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="9520d-199">For example, you can use a PLAYELEMENT button to play digital media files, and a STOPELEMENT to stop playback.</span></span> <span data-ttu-id="9520d-200">См. раздел элемент [BUTTONGROUP](buttongroup-element.md) и [элемент Button](button-element.md) в справочнике по программированию для обложки.</span><span class="sxs-lookup"><span data-stu-id="9520d-200">See [BUTTONGROUP](buttongroup-element.md) Element and [BUTTON Element](button-element.md) in the Skin Programming Reference.</span></span> <span data-ttu-id="9520d-201">[IMAGEBUTTON](imagebutton.md) можно использовать для вывода изображений, которые могут меняться в ответ на определенные события.</span><span class="sxs-lookup"><span data-stu-id="9520d-201">The [IMAGEBUTTON](imagebutton.md) can be used to display images that can change in response to specific events.</span></span>

## <a name="sliders"></a><span data-ttu-id="9520d-202">Ползунки</span><span class="sxs-lookup"><span data-stu-id="9520d-202">Sliders</span></span>

<span data-ttu-id="9520d-203">Ползунки полезны для работы со сведениями, которые изменяются со временем.</span><span class="sxs-lookup"><span data-stu-id="9520d-203">Sliders are useful for working with information that changes over time.</span></span> <span data-ttu-id="9520d-204">Например, можно использовать ползунок, чтобы указать объем музыки, которая уже воспроизводилась для конкретного файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9520d-204">For example, you might use a slider to indicate the amount of music that has already played for a particular media file.</span></span> <span data-ttu-id="9520d-205">Ползунки могут быть горизонтальными или вертикальными, линейными или циклическими, или любой фигурой, которую можно представить.</span><span class="sxs-lookup"><span data-stu-id="9520d-205">Sliders can be horizontal or vertical, linear or circular, or any shape you can think of.</span></span> <span data-ttu-id="9520d-206">Ползунки бывают трех видов: ползунки, индикаторы выполнения и настраиваемые ползунки.</span><span class="sxs-lookup"><span data-stu-id="9520d-206">Sliders come in three varieties: sliders, progress bars, and custom sliders.</span></span>

-   <span data-ttu-id="9520d-207">**Ползунки.**</span><span class="sxs-lookup"><span data-stu-id="9520d-207">**Sliders.**</span></span> <span data-ttu-id="9520d-208">Можно использовать элемент **Slider** для элементов управления громкостью или разрешить пользователю переходить на другую часть мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="9520d-208">You can use the **SLIDER** element for volume controls or to allow the user to move to a different part of the media content.</span></span>
-   <span data-ttu-id="9520d-209">**Индикаторы выполнения.**</span><span class="sxs-lookup"><span data-stu-id="9520d-209">**Progress bars.**</span></span> <span data-ttu-id="9520d-210">Индикаторы выполнения похожи на ползунки.</span><span class="sxs-lookup"><span data-stu-id="9520d-210">Progress bars are similar to sliders.</span></span> <span data-ttu-id="9520d-211">Индикаторы выполнения предназначены для графического отображения процента определенного процесса, который был завершен, но не для процесса, с которым пользователь хочет взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="9520d-211">Progress bars are designed for graphically displaying the percentage of a particular process that has been completed, but not for a process that the user will want to interact with.</span></span> <span data-ttu-id="9520d-212">Например, может потребоваться использовать индикатор выполнения для указания хода выполнения буферизации.</span><span class="sxs-lookup"><span data-stu-id="9520d-212">For example, you might want to use a progress bar to indicate buffering progress.</span></span>
-   <span data-ttu-id="9520d-213">**Настраиваемые ползунки.**</span><span class="sxs-lookup"><span data-stu-id="9520d-213">**Custom sliders.**</span></span> <span data-ttu-id="9520d-214">Предусмотрена настраиваемая функция ползунка, позволяющая создавать такие элементы управления, как регуляторы, или делать необычные механизмы управления.</span><span class="sxs-lookup"><span data-stu-id="9520d-214">Custom slider functionality is provided so you can create controls such as knobs, or make unusual control mechanisms.</span></span> <span data-ttu-id="9520d-215">Например, если вы хотите создать элемент управления "том", который охватывает обложку, это можно сделать с помощью настраиваемого ползунка.</span><span class="sxs-lookup"><span data-stu-id="9520d-215">For example, if you want to create a volume control that wraps around your skin, you can do it with a custom slider.</span></span> <span data-ttu-id="9520d-216">Чтобы настроить настраиваемый ползунок, необходимо создать карту изображения, которая содержит изображения в градациях серого, чтобы определить расположение значений на ползунке.</span><span class="sxs-lookup"><span data-stu-id="9520d-216">To set up the custom slider, you must create an image map that contains grayscale images to define the locations of the values on the slider.</span></span> <span data-ttu-id="9520d-217">Это относительно легко сделать с помощью программы редактирования графики, поддерживающей слои.</span><span class="sxs-lookup"><span data-stu-id="9520d-217">This is relatively easy to do with a graphics editing program that supports layers.</span></span>

## <a name="text"></a><span data-ttu-id="9520d-218">Текст</span><span class="sxs-lookup"><span data-stu-id="9520d-218">Text</span></span>

<span data-ttu-id="9520d-219">Элемент **Text** можно использовать для показа текста в обложке, например заголовков песен.</span><span class="sxs-lookup"><span data-stu-id="9520d-219">You can use the **TEXT** element to display text on your skin, such as song titles.</span></span>

## <a name="video"></a><span data-ttu-id="9520d-220">Видео</span><span class="sxs-lookup"><span data-stu-id="9520d-220">Video</span></span>

<span data-ttu-id="9520d-221">Видео можно отображать в обложке.</span><span class="sxs-lookup"><span data-stu-id="9520d-221">You can display video in your skin.</span></span> <span data-ttu-id="9520d-222">Элемент **Video** позволяет задать размер и расположение окна видео.</span><span class="sxs-lookup"><span data-stu-id="9520d-222">The **VIDEO** element allows you to set the size and position of the video window.</span></span>

<span data-ttu-id="9520d-223">Вы также можете разрешить пользователю изменять параметры видео с помощью элемента **видеосеттингс** .</span><span class="sxs-lookup"><span data-stu-id="9520d-223">You can also allow the user to change the video settings with the **VIDEOSETTINGS** element.</span></span> <span data-ttu-id="9520d-224">Например, можно создать элементы управления для настройки яркости видео.</span><span class="sxs-lookup"><span data-stu-id="9520d-224">For example, you can create controls to adjust the brightness of the video.</span></span>

<span data-ttu-id="9520d-225">Если не указать элемент видео и содержимое содержит видео, проигрыватель Windows Media вернется в полноэкранный режим, и обложка не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="9520d-225">If you do not supply a video element and the content contains video, Windows Media Player will return to full mode and your skin will not be displayed.</span></span>

## <a name="equalizer-settings"></a><span data-ttu-id="9520d-226">Параметры эквалайзера</span><span class="sxs-lookup"><span data-stu-id="9520d-226">Equalizer Settings</span></span>

<span data-ttu-id="9520d-227">Вы можете задать фильтрацию для конкретных диапазонов звуковых частот с помощью элемента **екуализерсеттингс** .</span><span class="sxs-lookup"><span data-stu-id="9520d-227">You can set the filtering for specific audio frequency bands by using the **EQUALIZERSETTINGS** element.</span></span> <span data-ttu-id="9520d-228">Вы можете увеличить низкие частоты, настроить высокие настройки и установить звуки в соответствии с вашими ушкими или вашими проживания.</span><span class="sxs-lookup"><span data-stu-id="9520d-228">You can boost the bass, tweak the treble, and set up your sounds to match your ears or your living room.</span></span>

## <a name="visualizations"></a><span data-ttu-id="9520d-229">Визуализации</span><span class="sxs-lookup"><span data-stu-id="9520d-229">Visualizations</span></span>

<span data-ttu-id="9520d-230">Визуализации можно отображать в обложке.</span><span class="sxs-lookup"><span data-stu-id="9520d-230">You can display visualizations in your skin.</span></span> <span data-ttu-id="9520d-231">Визуализации — это визуальные эффекты, которые меняются со временем при воспроизведении звука с помощью проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9520d-231">Visualizations are visual effects that change over time as audio is playing through Windows Media Player.</span></span> <span data-ttu-id="9520d-232">Элемент **Effects** определяет, где будут воспроизводиться визуализации, какой размер окна будет отображаться и какие визуализации будут воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="9520d-232">The **EFFECTS** element determines where the visualizations will play, what size the window will be, and which visualizations will be played.</span></span>

## <a name="playlists"></a><span data-ttu-id="9520d-233">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="9520d-233">Playlists</span></span>

<span data-ttu-id="9520d-234">Можно использовать элемент **списка воспроизведения** , чтобы пользователь мог выбрать элемент из определенного списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9520d-234">You can use the **PLAYLIST** element to let the user select an item from a specific playlist.</span></span>

## <a name="subviews"></a><span data-ttu-id="9520d-235">Вложенные представления</span><span class="sxs-lookup"><span data-stu-id="9520d-235">Subviews</span></span>

<span data-ttu-id="9520d-236">Можно использовать элемент вложенного **представления** для отображения вторичных наборов элементов управления интерфейса, например списков воспроизведения или элементов управления видео.</span><span class="sxs-lookup"><span data-stu-id="9520d-236">You can use the **SUBVIEW** element to display secondary sets of interface controls, such as a playlist or video controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9520d-237">См. также</span><span class="sxs-lookup"><span data-stu-id="9520d-237">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9520d-238">**Файлы обложки**</span><span class="sxs-lookup"><span data-stu-id="9520d-238">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




