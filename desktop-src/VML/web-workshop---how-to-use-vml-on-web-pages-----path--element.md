---
title: Использование элемента Path
description: Использование элемента Path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Веб-семинар, элемент Path
- Разработка веб-страниц, элемент Path
- Язык VML (VML), элемент Path
- VML (язык VML), элемент Path
- Векторная графика, элемент Path
- элемент Path
- Элементы VML, путь
- Фигуры VML, элемент Path
- Язык VML (VML), Настройка контуров фигур
- VML (язык VML), Настройка контуров фигур
- Векторная графика, Настройка контуров фигур
- Фигуры VML, Настройка контуров
- Настройка контуров фигур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793464"
---
# <a name="using-the-path-element"></a><span data-ttu-id="9162c-116">Использование элемента Path</span><span class="sxs-lookup"><span data-stu-id="9162c-116">Using the Path Element</span></span>

<span data-ttu-id="9162c-117">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9162c-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9162c-118">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="9162c-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9162c-119">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="9162c-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9162c-120">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9162c-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9162c-121">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9162c-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9162c-122">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9162c-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9162c-123">Вы узнали, что для рисования фигуры можно использовать предварительно определенные элементы формы VML, такие как `<oval>` ,, `<line>` ,, `<polyline>` `<curve>` `<rect>` , `<roundrect>` и `<arc>` --.</span><span class="sxs-lookup"><span data-stu-id="9162c-123">You've learned that you can use the VML predefined shape elements -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` -- to draw a shape.</span></span> <span data-ttu-id="9162c-124">В этом разделе будет показано, как использовать `<path>` вложенный элемент для настройки контура фигуры.</span><span class="sxs-lookup"><span data-stu-id="9162c-124">In this topic, we will illustrate how to use the `<path>` sub-element to customize the outline of a shape.</span></span>

<span data-ttu-id="9162c-125">`<path>`Вложенный элемент можно поместить внутри `<shape>` `<shapetype>` элемента или.</span><span class="sxs-lookup"><span data-stu-id="9162c-125">You can place the `<path>` sub-element inside the `<shape>` or `<shapetype>` element.</span></span> <span data-ttu-id="9162c-126">Затем можно использовать атрибуты свойств `<path>` вложенного элемента для настройки контура фигуры.</span><span class="sxs-lookup"><span data-stu-id="9162c-126">You can then use the property attributes of the `<path>` sub-element to customize the outline of the shape.</span></span>

<span data-ttu-id="9162c-127">Например, чтобы нарисовать настраиваемую фигуру, показанную на следующем рисунке, можно использовать `<path>` вложенный элемент для определения контура фигуры, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="9162c-127">For example, to draw the customized shape illustrated in the following picture, you can use the `<path>` sub-element to define the outline of the shape, as shown in the following VML representation:</span></span>

![shape1.gif (1301 байт)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   <span data-ttu-id="9162c-129">Значения `m 8,65` указывают, что рисование начинается в точке (8, 65).</span><span class="sxs-lookup"><span data-stu-id="9162c-129">The values `m 8,65` indicate that the drawing starts at the point (8,65).</span></span>
-   <span data-ttu-id="9162c-130">Значения `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` указывают, что прямая линия начинается с текущей точки (8, 65) и заканчивается в заданной точке (72, 65), которая станет новой текущей точкой.</span><span class="sxs-lookup"><span data-stu-id="9162c-130">The values `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicate that a straight line begins at the current point (8, 65) and ends at the given point (72, 65), which becomes the new current point.</span></span> <span data-ttu-id="9162c-131">Новая строка начинается с текущей точки (72, 65) и заканчивается в заданной точке, которая становится новой текущей точкой и т. д. до последней точки (60, 100).</span><span class="sxs-lookup"><span data-stu-id="9162c-131">A new line begins at the current point (72, 65) and ends at the given point, which becomes the new current point, and so on, to the final point (60, 100).</span></span>
-   <span data-ttu-id="9162c-132">`x` Указывает, что путь будет закрыт прямой линией, которая начинается с текущей точки (60, 100) и заканчивается в исходной точке (8, 65).</span><span class="sxs-lookup"><span data-stu-id="9162c-132">`x` indicates that the path will close by a straight line that starts at the current point (60, 100) and ends at the original point (8, 65).</span></span>
-   <span data-ttu-id="9162c-133">`e` Указывает на завершение рисования.</span><span class="sxs-lookup"><span data-stu-id="9162c-133">`e` indicates stop drawing.</span></span>

<span data-ttu-id="9162c-134">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span><span class="sxs-lookup"><span data-stu-id="9162c-134">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span></span>

 

 