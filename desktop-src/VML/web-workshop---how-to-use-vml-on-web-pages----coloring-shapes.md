---
title: Цветовые фигуры
description: В этой статье описываются цвета фигур в VML, а также функция, устаревшая до Windows Internet Explorer 9.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Веб-семинар, цвета фигур
- Разработка веб-страниц, выделение цветом фигур
- Язык VML (VML), цветные фигуры
- VML (язык VML), цветные фигуры
- Векторная графика, цветные фигуры
- Фигуры VML, выделение цветом
- цветовые фигуры
- Язык VML (VML), имена цветов ключевых слов
- VML (язык VML), имена цветов ключевых слов
- Векторная графика, имена цветов ключевых слов
- имена цветов ключевых слов
- Язык VML (VML), RGB триады
- VML (язык VML), RGB триады
- Векторная графика, RGB триады
- Триады RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c203debd01d4234ae58900a023944511f9fc73c1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407747"
---
# <a name="coloring-shapes"></a><span data-ttu-id="86e37-118">Цветовые фигуры</span><span class="sxs-lookup"><span data-stu-id="86e37-118">Coloring Shapes</span></span>

<span data-ttu-id="86e37-119">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="86e37-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="86e37-120">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="86e37-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="86e37-121">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="86e37-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="86e37-122">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="86e37-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="86e37-123">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="86e37-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="86e37-124">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="86e37-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="86e37-125">Как упоминалось в предыдущих разделах, можно использовать "Red" для представления цвета красным цветом, "синий" для представления цвета синим цветом и т. д.</span><span class="sxs-lookup"><span data-stu-id="86e37-125">As we mentioned in earlier sections, you can use "red" to represent a color in red, "blue" to represent a color in blue, and so on.</span></span> <span data-ttu-id="86e37-126">В этом разделе показано, как нарисовать фигуры в любом нужном цвете.</span><span class="sxs-lookup"><span data-stu-id="86e37-126">In this topic, we will illustrate how to draw shapes in any color you want.</span></span>

<span data-ttu-id="86e37-127">VML расширяет синтаксис HTML и цвета CSS.</span><span class="sxs-lookup"><span data-stu-id="86e37-127">VML extends HTML and CSS color syntax.</span></span> <span data-ttu-id="86e37-128">Если тип атрибута элемента VML имеет цвет (например, **FillColor** и **строкеколор** ), можно выразить цвет с помощью [имени ключевого слова](#keyword-color-name) или [tripletа RGB](#rgb-triplet).</span><span class="sxs-lookup"><span data-stu-id="86e37-128">When the attribute type of a VML element is color -- such as **fillcolor** and **strokecolor** -- you can express the color by using either a [keyword color name](#keyword-color-name) or an [RGB triplet](#rgb-triplet).</span></span>

<span data-ttu-id="86e37-129">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="86e37-129">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="keyword-color-name"></a><span data-ttu-id="86e37-130">Имя цвета ключевого слова</span><span class="sxs-lookup"><span data-stu-id="86e37-130">Keyword Color Name</span></span>

<span data-ttu-id="86e37-131">HTML 4,0 определяет список имен цветов ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="86e37-131">HTML 4.0 defines a list of keyword color names.</span></span> <span data-ttu-id="86e37-132">Они имеют голубой, черный, синий, фучсиа, серый, зеленый, травяной, каштановый, ВМФ, оливковый, сиреневый, красный, серебро, бирюзовый, белый и желтый.</span><span class="sxs-lookup"><span data-stu-id="86e37-132">They are aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow.</span></span> <span data-ttu-id="86e37-133">Значение RGB для этих 16 цветов определяется в [спецификации HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span><span class="sxs-lookup"><span data-stu-id="86e37-133">The RGB value for these 16 colors are defined in [HTML 4.0 specification](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span></span>

<span data-ttu-id="86e37-134">Например, можно нарисовать прямоугольник, заполненный желтым цветом, указав `fillcolor="yellow"` , и присвоить ему синий контур, указав `strokecolor="blue"` , как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="86e37-134">For example, you can draw a rectangle filled with yellow by specifying `fillcolor="yellow"`, and give it a blue outline by specifying `strokecolor="blue"`, as shown in the following VML representation:</span></span>

![color1.gif (305 байт)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





<span data-ttu-id="86e37-136">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="86e37-136">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rgb-triplet"></a><span data-ttu-id="86e37-137">Triplet RGB</span><span class="sxs-lookup"><span data-stu-id="86e37-137">RGB Triplet</span></span>

<span data-ttu-id="86e37-138">Если цвет не является [именем цвета ключевого слова](#keyword-color-name), можно выразить цвет в виде десятичного tripletа RGB или шестнадцатеричного Triplet RGB.</span><span class="sxs-lookup"><span data-stu-id="86e37-138">If the color is not a [keyword color name](#keyword-color-name), you can express the color as either an RGB decimal triplet or an RGB hexadecimal triplet.</span></span> <span data-ttu-id="86e37-139">С помощью RGB триады можно указать значения для красного, зеленого и синего компонентов цвета, присвоив каждому компоненту значение в диапазоне от 0 до 255 в десятичном формате или от 00 до FF в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="86e37-139">With RGB triplets, you can specify values for the red, green, and blue components of the color, setting each component to a value ranging from 0 through 255 in decimal, or 00 through FF in hexadecimal.</span></span>

<span data-ttu-id="86e37-140">Например, можно создать прямоугольник, который заполняется настроенным цветом со значением RGB 253, 249, 186 в десятичном формате, указав либо `fillcolor="rgb(253,249, 186)"` или `fillcolor="#FDF9BA"` , как показано в следующем представлении VML.</span><span class="sxs-lookup"><span data-stu-id="86e37-140">For example, you can create a rectangle that is filled with a customized color with an RGB value of 253, 249, 186 in decimal by specifying either `fillcolor="rgb(253,249, 186)"` or `fillcolor="#FDF9BA"`, as shown in the following VML representation.</span></span> <span data-ttu-id="86e37-141">В шестнадцатеричном формате значение 253 превращается в Демон, 249 — на F9, а 186 — в ба.</span><span class="sxs-lookup"><span data-stu-id="86e37-141">In hexadecimal, the value 253 becomes FD, 249 becomes F9, and 186 becomes BA.</span></span>

![color2.gif (305 байт)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





<span data-ttu-id="86e37-143">Если RGB в шестнадцатеричном формате имеет шаблон, например КСКСИИЗЗ, его можно сократить до XYZ.</span><span class="sxs-lookup"><span data-stu-id="86e37-143">If the RGB in hexadecimal has a pattern such as XXYYZZ, you can abbreviate it to XYZ.</span></span> <span data-ttu-id="86e37-144">Например, " \# 66FF99" можно записать как " \# 6F9".</span><span class="sxs-lookup"><span data-stu-id="86e37-144">For example, "\#66FF99" can be written out as "\#6F9".</span></span>

<span data-ttu-id="86e37-145">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="86e37-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="86e37-146">Итоги</span><span class="sxs-lookup"><span data-stu-id="86e37-146">Summary</span></span>

<span data-ttu-id="86e37-147">В VML можно представить цвет в одном из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="86e37-147">In VML, you can represent a color in one of the following formats:</span></span>

1.  <span data-ttu-id="86e37-148">FillColor = "синий"</span><span class="sxs-lookup"><span data-stu-id="86e37-148">fillcolor="blue"</span></span>
2.  <span data-ttu-id="86e37-149">FillColor = "RGB (0, 0255)"</span><span class="sxs-lookup"><span data-stu-id="86e37-149">fillcolor="rgb(0,0,255)"</span></span>
3.  <span data-ttu-id="86e37-150">FillColor = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="86e37-150">fillcolor="\#0000ff"</span></span>

 

 