---
title: Использование элемента Текстпас
description: Использование элемента Текстпас
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Веб-семинар, элемент текстпас
- Разработка веб-страниц, элемент текстпас
- Язык VML (VML), элемент текстпас
- VML (язык VML), элемент текстпас
- Векторная графика, элемент текстпас
- текстпас, элемент
- Элементы VML, текстпас
- Фигуры VML, элемент текстпас
- Язык VML (VML), Рисование текста
- VML (язык VML), Рисование текста
- Векторная графика, Рисование текста VML
- рисование текста
- Фигуры VML, Рисование текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c032d14307dc07ec56911f4c5cc45a4c69664
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134498"
---
# <a name="using-the-textpath-element"></a><span data-ttu-id="95a63-116">Использование элемента Текстпас</span><span class="sxs-lookup"><span data-stu-id="95a63-116">Using the Textpath Element</span></span>

<span data-ttu-id="95a63-117">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="95a63-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="95a63-118">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="95a63-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="95a63-119">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="95a63-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="95a63-120">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="95a63-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="95a63-121">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="95a63-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="95a63-122">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="95a63-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="95a63-123">В этом разделе будет показано, как использовать `<textpath>` элемент для рисования текста с различными стилями.</span><span class="sxs-lookup"><span data-stu-id="95a63-123">In this topic, we will illustrate how to use the `<textpath>` element to draw text with various styles.</span></span>

<span data-ttu-id="95a63-124">`<textpath>`Вложенный элемент можно поместить внутрь `<shape>` или `<shapetype>` для рисования текста.</span><span class="sxs-lookup"><span data-stu-id="95a63-124">You can place the `<textpath>` sub-element inside `<shape>` or `<shapetype>` to draw text.</span></span> <span data-ttu-id="95a63-125">Затем можно использовать атрибуты свойств `<textpath>` вложенного элемента для настройки текста.</span><span class="sxs-lookup"><span data-stu-id="95a63-125">You can then use the property attributes of the `<textpath>` sub-element to customize the text.</span></span> <span data-ttu-id="95a63-126">Можно также использовать `<formulas>` вложенный элемент для определения контура текста.</span><span class="sxs-lookup"><span data-stu-id="95a63-126">You can also use the `<formulas>` sub-element to define the outline of the text.</span></span>

<span data-ttu-id="95a63-127">Например, чтобы создать текст, показанный на следующем рисунке, можно ввести следующее представление VML.</span><span class="sxs-lookup"><span data-stu-id="95a63-127">For example, to create the text shown in the following picture, you can type the VML representation below.</span></span> <span data-ttu-id="95a63-128">Обратите внимание, что мы используем `<shapetype>` элемент для определения прототипа для контура текста.</span><span class="sxs-lookup"><span data-stu-id="95a63-128">Notice that we use the `<shapetype>` element to define a prototype for the outline of the text.</span></span> <span data-ttu-id="95a63-129">Затем мы создаем две фигуры из одного шапетипе.</span><span class="sxs-lookup"><span data-stu-id="95a63-129">We then instantiate two shapes from the same shapetype.</span></span> <span data-ttu-id="95a63-130">Можно просто изменить атрибут свойства **строки** для вывода другого текста.</span><span class="sxs-lookup"><span data-stu-id="95a63-130">You can simply change the **string** property attribute to display different text.</span></span>

![\-1.gif shape1 (4898 байт)](images/shape1-1t.gif)

![\-2.gif shape1 (2789 байт)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





<span data-ttu-id="95a63-133">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span><span class="sxs-lookup"><span data-stu-id="95a63-133">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span></span>

 

 