---
title: Использование предопределенных фигур
description: В этой статье описывается использование предопределенных фигур в VML, что является устаревшим компонентом Windows Internet Explorer 9.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Веб-семинар, стандартные фигуры
- Разработка веб-страниц, предопределенные фигуры
- Язык VML (VML), предопределенные фигуры
- VML (язык VML), предопределенные фигуры
- Векторная графика, предопределенные фигуры
- Фигуры VML, предварительно определенные
- предопределенные фигуры
- Язык VML (VML), элемент Rect
- VML (язык VML), элемент Rect
- Векторная графика, элемент Rect
- Rect, элемент
- Элементы VML, Rect
- Язык VML (VML), элемент раундрект
- VML (язык VML), элемент раундрект
- Векторная графика, элемент раундрект
- раундрект, элемент
- Элементы VML, раундрект
- Язык VML (VML), элемент Line
- VML (язык VML), элемент Line
- Векторная графика, элемент Line
- Line, элемент
- Элементы VML, линия
- Язык VML (VML), элемент ломаной линии
- VML (язык VML), элемент ломаной линии
- Векторная графика, элемент ломаной линии
- элемент ломаной линии
- Элементы VML, ломаная линия
- Язык VML (VML), элемент кривой
- VML (язык VML), элемент кривой
- Векторная графика, элемент кривой
- элемент кривой
- Элементы VML, кривая
- Язык VML (VML), элемент дуги
- VML (язык VML), элемент дуги
- Векторная графика, элемент дуги
- элемент дуги
- Элементы VML, дуга
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407687"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="60834-140">Использование предопределенных фигур</span><span class="sxs-lookup"><span data-stu-id="60834-140">Using Predefined Shapes</span></span>

<span data-ttu-id="60834-141">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="60834-141">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="60834-142">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="60834-142">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="60834-143">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="60834-143">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="60834-144">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="60834-144">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="60834-145">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="60834-145">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="60834-146">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="60834-146">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="60834-147">Как вы узнали, `<oval>` для создания простого овала можно использовать элемент VML.</span><span class="sxs-lookup"><span data-stu-id="60834-147">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="60834-148">VML предоставляет несколько других предопределенных элементов.</span><span class="sxs-lookup"><span data-stu-id="60834-148">VML provides several other predefined elements.</span></span> <span data-ttu-id="60834-149">В этом разделе показано, как рисовать графику с помощью этих элементов.</span><span class="sxs-lookup"><span data-stu-id="60834-149">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="60834-150">В этом разделе.</span><span class="sxs-lookup"><span data-stu-id="60834-150">In this topic:</span></span>

-   [<span data-ttu-id="60834-151">перетаскиваемые</span><span class="sxs-lookup"><span data-stu-id="60834-151">rect</span></span>](#roundrect)
-   [<span data-ttu-id="60834-152">раундрект</span><span class="sxs-lookup"><span data-stu-id="60834-152">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="60834-153">line</span><span class="sxs-lookup"><span data-stu-id="60834-153">line</span></span>](#polyline)
-   [<span data-ttu-id="60834-154">линию</span><span class="sxs-lookup"><span data-stu-id="60834-154">polyline</span></span>](#polyline)
-   [<span data-ttu-id="60834-155">кривая</span><span class="sxs-lookup"><span data-stu-id="60834-155">curve</span></span>](#curve)
-   [<span data-ttu-id="60834-156">дуга</span><span class="sxs-lookup"><span data-stu-id="60834-156">arc</span></span>](#arc)
-   [<span data-ttu-id="60834-157">Сводка</span><span class="sxs-lookup"><span data-stu-id="60834-157">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="60834-158">rect</span><span class="sxs-lookup"><span data-stu-id="60834-158">rect</span></span>

<span data-ttu-id="60834-159">`<rect>`Для рисования прямоугольника можно использовать элемент.</span><span class="sxs-lookup"><span data-stu-id="60834-159">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="60834-160">Затем можно настроить прямоугольник, указав другие атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="60834-160">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="60834-161">Например, можно нарисовать прямоугольник, который заполняется синим цветом, указав **FillColor**= "Blue", и присвоить ему красную структуру 3,5-пт, указав **строкеколор**= "Red" **строкевеигхт**= "3,5 PT", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="60834-161">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 байт)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="60834-163">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="60834-163">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="60834-164">(Примечание. в спецификации VML отсутствует закладка для `<rect>` элемента.)</span><span class="sxs-lookup"><span data-stu-id="60834-164">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="60834-165">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="60834-165">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="60834-166">раундрект</span><span class="sxs-lookup"><span data-stu-id="60834-166">roundrect</span></span>

<span data-ttu-id="60834-167">Элемент можно использовать `<roundrect>` для рисования прямоугольника со скругленными углами.</span><span class="sxs-lookup"><span data-stu-id="60834-167">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="60834-168">Затем можно настроить скругленный прямоугольник, указав различные атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="60834-168">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="60834-169">Например, можно нарисовать прямоугольник с закругленными углами размером 30% от половины меньшего размера прямоугольника, указав **арксизе**= "0,3", заполнить его желтым цветом, указав **FillColor**= "Yellow", и присвоив ему красную структуру с 2 точками, указав **строкеколор**= "Red" **строкевеигхт**= "2PT", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="60834-169">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 байт)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="60834-171">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="60834-171">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="60834-172">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="60834-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="60834-173">line</span><span class="sxs-lookup"><span data-stu-id="60834-173">line</span></span>

<span data-ttu-id="60834-174">`<line>`Для создания прямой линии можно использовать элемент.</span><span class="sxs-lookup"><span data-stu-id="60834-174">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="60834-175">Затем можно настроить строку, указав другие атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="60834-175">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="60834-176">Например, можно нарисовать горизонтальную линию, указав **from**= "до пунктов, до пунктов" **to**= "100pt, до пунктов" и сделав ее 2-точечными и красными, указав **строкеколор**= "Red" **строкевеигхт**= "2PT", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="60834-176">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 байт)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="60834-178">Можно нарисовать вертикальную или диагональную линию, просто указав разные значения атрибутов свойств **from** и **to** , как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="60834-178">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 байт)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="60834-180">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span><span class="sxs-lookup"><span data-stu-id="60834-180">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="60834-181">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="60834-181">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="60834-182">линию</span><span class="sxs-lookup"><span data-stu-id="60834-182">polyline</span></span>

<span data-ttu-id="60834-183">Элемент можно использовать `<polyline>` для определения фигур, создаваемых из Соединенных линейных сегментов.</span><span class="sxs-lookup"><span data-stu-id="60834-183">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="60834-184">Затем можно настроить фигуру, указав другие атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="60834-184">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="60834-185">Например, чтобы нарисовать фигуру, показанную на следующем рисунке, можно ввести следующее представление VML:</span><span class="sxs-lookup"><span data-stu-id="60834-185">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 байт)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="60834-187">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span><span class="sxs-lookup"><span data-stu-id="60834-187">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="60834-188">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="60834-188">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="60834-189">кривая</span><span class="sxs-lookup"><span data-stu-id="60834-189">curve</span></span>

<span data-ttu-id="60834-190">Элемент можно использовать `<curve>` для рисования кривой Безье третьего порядка.</span><span class="sxs-lookup"><span data-stu-id="60834-190">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="60834-191">Затем можно настроить кривую, указав другие атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="60834-191">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="60834-192">Например, чтобы нарисовать кривую, как показано на следующем рисунке, можно ввести следующее представление VML:</span><span class="sxs-lookup"><span data-stu-id="60834-192">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 байт)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="60834-194">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span><span class="sxs-lookup"><span data-stu-id="60834-194">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="60834-195">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="60834-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="60834-196">дуга</span><span class="sxs-lookup"><span data-stu-id="60834-196">arc</span></span>

<span data-ttu-id="60834-197">Элемент можно использовать `<arc>` для рисования дуги, которая определена как сегмент овала.</span><span class="sxs-lookup"><span data-stu-id="60834-197">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="60834-198">Дуга определяется пересечением овала с векторами радиуса начала и конца, заданными углами.</span><span class="sxs-lookup"><span data-stu-id="60834-198">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="60834-199">Углы вычисляются с помощью свойств круга (ширина равна высоте), а затем масштабируется анисотропикалли до нужной ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="60834-199">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="60834-200">Например, можно нарисовать дугу, начинающуюся с 0 градусов и заканчивающуюся в 90 градусов, указав **startAngle**= "0" **ендангле**= "90", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="60834-200">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 байт)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="60834-202">Можно изменить дугу, указав различные значения **startAngle** и **ендангле** , как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="60834-202">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

![arc2.gif (608 байт)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 байт)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="60834-205">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span><span class="sxs-lookup"><span data-stu-id="60834-205">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="60834-206">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="60834-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="60834-207">Итоги</span><span class="sxs-lookup"><span data-stu-id="60834-207">Summary</span></span>

<span data-ttu-id="60834-208">Вы можете использовать предварительно определенные элементы VML, такие как `<oval>` , `<line>` , `<polyline>` ,, `<curve>` `<rect>` , `<roundrect>` и, `<arc>` чтобы легко рисовать графические данные на веб-странице, а затем настраивать эти изображения, просто изменяя их атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="60834-208">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 