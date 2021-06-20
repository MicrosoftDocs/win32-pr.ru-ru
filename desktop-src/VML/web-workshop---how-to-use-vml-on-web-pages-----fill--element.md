---
title: Использование элемента заливки
description: В этой статье описывается использование элемента Fill в VML, который является устаревшим в Windows Internet Explorer 9.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Веб-семинар, элемент Fill
- Разработка веб-страниц, элемент Fill
- Язык VML (VML), элемент Fill
- VML (язык VML), элемент Fill
- Векторная графика, элемент Fill
- Fill, элемент
- Элементы VML, Fill
- Фигуры VML, элемент Fill
- Язык VML (VML), градиентная заливка
- VML (язык VML), градиентная заливка
- Векторная графика, градиентная заливка
- Фигуры VML, градиентная заливка
- заполненные градиентом фигуры
- Язык VML (VML), узорная заливка
- VML (язык VML), узорная заливка
- Векторная графика, узорная заливка
- Фигуры VML, узорная заливка
- фигуры с заполненным шаблоном
- Язык VML (VML), заливка изображения
- VML (язык VML), Заливка рисунков
- Векторная графика, Заливка рисунков
- Фигуры VML, Заливка рисунков
- заполненные изображениями фигуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb243e4896443fd36a1b22c2ac3a0ab0bedfb2b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407797"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="3f879-126">Использование элемента заливки</span><span class="sxs-lookup"><span data-stu-id="3f879-126">Using the Fill Element</span></span>

<span data-ttu-id="3f879-127">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3f879-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3f879-128">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="3f879-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3f879-129">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="3f879-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3f879-130">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3f879-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3f879-131">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3f879-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3f879-132">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3f879-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3f879-133">Как вы узнали, вы можете использовать атрибут свойства **FillColor** предопределенного элемента Shape, например,,,, `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --для указания цвета, используемого для заполнения фигуры.</span><span class="sxs-lookup"><span data-stu-id="3f879-133">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="3f879-134">В этом разделе мы рассмотрим, как нарисовать фигуру, которая заполняется более сложными эффектами.</span><span class="sxs-lookup"><span data-stu-id="3f879-134">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="3f879-135">`<fill>`Вложенный элемент можно поместить внутри `<shape>` , или или `<shapetype>` любого предопределенного элемента Shape, чтобы описать, как заполнять фигуру.</span><span class="sxs-lookup"><span data-stu-id="3f879-135">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="3f879-136">Затем можно использовать атрибуты свойств `<fill>` вложенного элемента для настройки заливки, такие как [Градиентная заливка](#gradient-fill), [узорная](#pattern-fill)заливка, [Заливка рисунков](#picture-fill).</span><span class="sxs-lookup"><span data-stu-id="3f879-136">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="3f879-137">В этом разделе.</span><span class="sxs-lookup"><span data-stu-id="3f879-137">In this topic:</span></span>

-   [<span data-ttu-id="3f879-138">Градиентная заливка</span><span class="sxs-lookup"><span data-stu-id="3f879-138">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="3f879-139">Узорная заливка</span><span class="sxs-lookup"><span data-stu-id="3f879-139">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="3f879-140">Заливка рисунка</span><span class="sxs-lookup"><span data-stu-id="3f879-140">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="3f879-141">Градиентная заливка</span><span class="sxs-lookup"><span data-stu-id="3f879-141">Gradient Fill</span></span>

<span data-ttu-id="3f879-142">Для рисования фигуры с заливкой градиента можно задать атрибуту свойства **Type** `<fill>` вложенного элемента значение "градиент" или "градиентрадиал", а затем указать другие атрибуты `<fill>` вложенного элемента, такие как **метод**, **color2**, **фокус** и **угол**.</span><span class="sxs-lookup"><span data-stu-id="3f879-142">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="3f879-143">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="3f879-143">**Examples:**</span></span>

<span data-ttu-id="3f879-144">Чтобы создать фигуру, заполненную градиентом по горизонтали, можно задать для атрибута свойства **Type** значение "градиент", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="3f879-144">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 байт)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="3f879-146">Если изменить атрибут свойства **FillColor** фигуры, то фигура будет заполнена градиентом другим цветом.</span><span class="sxs-lookup"><span data-stu-id="3f879-146">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="3f879-147">Второй цвет можно добавить, указав атрибут свойства **color2** `<fill>` вложенного элемента.</span><span class="sxs-lookup"><span data-stu-id="3f879-147">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="3f879-148">Например, чтобы создать фигуру, заполняемую градиентом в два цвета, можно добавить второй цвет, указав атрибут свойства **color2** `<fill>` вложенного элемента, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="3f879-148">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 байт)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="3f879-150">Атрибуту свойства **method** можно присвоить значение «линейный», «Сигма», «Any» или «None».</span><span class="sxs-lookup"><span data-stu-id="3f879-150">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="3f879-151">Результат градиента немного отличается.</span><span class="sxs-lookup"><span data-stu-id="3f879-151">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="3f879-152">Кроме того, можно использовать атрибут свойства **Angle**,**Focus**,**фокуссизе** или **фокуспоситион** , чтобы изменить способ перехода градиента.</span><span class="sxs-lookup"><span data-stu-id="3f879-152">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="3f879-153">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="3f879-153">**Examples:**</span></span>

 

<span data-ttu-id="3f879-154">Чтобы создать фигуру, заполненную градиентом по вертикали, можно задать для атрибута Angle значение Angle = "-90", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="3f879-154">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 байт)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="3f879-156">Чтобы создать фигуру, заполненную градиентом от диагонального движения вверх, можно задать для атрибута **Angle** значение Angle = "-135", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="3f879-156">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 байт)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="3f879-158">Чтобы создать фигуру, заполненную градиентом от диагонали вниз, можно задать для атрибута **Angle** значение Angle = "-45", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="3f879-158">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 байт)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="3f879-160">Чтобы создать фигуру с градиентной заливкой из центра, можно указать `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="3f879-160">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 байт)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="3f879-162">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="3f879-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="3f879-163">Узорная заливка</span><span class="sxs-lookup"><span data-stu-id="3f879-163">Pattern Fill</span></span>

<span data-ttu-id="3f879-164">Чтобы нарисовать фигуру, заполненную узором, можно установить атрибут свойства **Type** `<fill>` вложенного элемента в значение "Pattern", а затем указать другие атрибуты `<fill>` вложенного элемента, такие как **src** и **color2**.</span><span class="sxs-lookup"><span data-stu-id="3f879-164">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="3f879-165">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="3f879-165">**Examples:**</span></span>

<span data-ttu-id="3f879-166">Чтобы создать фигуру, которая заполняется изображением шаблона, можно указать для атрибута свойства **Type** значение pattern и указать атрибуту свойства **src** расположение файла изображения шаблона, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="3f879-166">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 байт)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="3f879-168">Если указать для атрибута свойства **src** другой файл шаблона, можно создать фигуру, которая заполняется другим шаблоном.</span><span class="sxs-lookup"><span data-stu-id="3f879-168">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="3f879-169">Кроме того, можно изменить цвет, указав другое значение для атрибута свойства **FillColor** или **color2** , как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="3f879-169">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 байт)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="3f879-171">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="3f879-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="3f879-172">Заливка рисунка</span><span class="sxs-lookup"><span data-stu-id="3f879-172">Picture Fill</span></span>

<span data-ttu-id="3f879-173">Для рисования фигуры, заполненной рисунком, можно задать атрибуту свойства **Type** `<fill>` вложенного элемента значение Frame, а затем указать другие атрибуты `<fill>` вложенного элемента, такие как **src** и **color2**.</span><span class="sxs-lookup"><span data-stu-id="3f879-173">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="3f879-174">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="3f879-174">**Examples:**</span></span>

<span data-ttu-id="3f879-175">Чтобы создать фигуру, заполняемую с помощью файла изображения, можно указать для атрибута свойства **Type** значение Frame, а затем указать атрибуту свойства **src** расположение файла изображения, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="3f879-175">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 байт)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="3f879-177">Можно легко создать фигуру, которая заполняется другой картинкой, указав для атрибута свойства **src** другой файл.</span><span class="sxs-lookup"><span data-stu-id="3f879-177">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="3f879-178">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span><span class="sxs-lookup"><span data-stu-id="3f879-178">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 