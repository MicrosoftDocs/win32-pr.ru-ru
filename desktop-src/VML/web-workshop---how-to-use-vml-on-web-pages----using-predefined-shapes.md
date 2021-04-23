---
title: Использование предопределенных фигур
description: В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.
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
ms.openlocfilehash: 4c1cafacf00f6f3f9129c29c56837f3f485aa3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533269"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="f7a0b-141">Использование предопределенных фигур</span><span class="sxs-lookup"><span data-stu-id="f7a0b-141">Using Predefined Shapes</span></span>

<span data-ttu-id="f7a0b-142">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-142">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f7a0b-143">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-143">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f7a0b-144">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-144">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f7a0b-145">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-145">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f7a0b-146">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f7a0b-146">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f7a0b-147">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f7a0b-147">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f7a0b-148">Как вы узнали, `<oval>` для создания простого овала можно использовать элемент VML.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-148">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="f7a0b-149">VML предоставляет несколько других предопределенных элементов.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-149">VML provides several other predefined elements.</span></span> <span data-ttu-id="f7a0b-150">В этом разделе показано, как рисовать графику с помощью этих элементов.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-150">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="f7a0b-151">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="f7a0b-151">In this topic:</span></span>

-   [<span data-ttu-id="f7a0b-152">перетаскиваемые</span><span class="sxs-lookup"><span data-stu-id="f7a0b-152">rect</span></span>](#roundrect)
-   [<span data-ttu-id="f7a0b-153">раундрект</span><span class="sxs-lookup"><span data-stu-id="f7a0b-153">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="f7a0b-154">line</span><span class="sxs-lookup"><span data-stu-id="f7a0b-154">line</span></span>](#polyline)
-   [<span data-ttu-id="f7a0b-155">линию</span><span class="sxs-lookup"><span data-stu-id="f7a0b-155">polyline</span></span>](#polyline)
-   [<span data-ttu-id="f7a0b-156">кривая</span><span class="sxs-lookup"><span data-stu-id="f7a0b-156">curve</span></span>](#curve)
-   [<span data-ttu-id="f7a0b-157">дуги</span><span class="sxs-lookup"><span data-stu-id="f7a0b-157">arc</span></span>](#arc)
-   [<span data-ttu-id="f7a0b-158">Сводка</span><span class="sxs-lookup"><span data-stu-id="f7a0b-158">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="f7a0b-159">rect</span><span class="sxs-lookup"><span data-stu-id="f7a0b-159">rect</span></span>

<span data-ttu-id="f7a0b-160">`<rect>`Для рисования прямоугольника можно использовать элемент.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-160">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="f7a0b-161">Затем можно настроить прямоугольник, указав другие атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-161">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="f7a0b-162">Например, можно нарисовать прямоугольник, который заполняется синим цветом, указав **FillColor**= "Blue", и присвоить ему красную структуру 3,5-пт, указав **строкеколор**= "Red" **строкевеигхт**= "3,5 PT", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="f7a0b-162">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 байт)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="f7a0b-164">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="f7a0b-164">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="f7a0b-165">(Примечание. в спецификации VML отсутствует закладка для `<rect>` элемента.)</span><span class="sxs-lookup"><span data-stu-id="f7a0b-165">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="f7a0b-166">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="f7a0b-166">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="f7a0b-167">раундрект</span><span class="sxs-lookup"><span data-stu-id="f7a0b-167">roundrect</span></span>

<span data-ttu-id="f7a0b-168">Элемент можно использовать `<roundrect>` для рисования прямоугольника со скругленными углами.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-168">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="f7a0b-169">Затем можно настроить скругленный прямоугольник, указав различные атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-169">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="f7a0b-170">Например, можно нарисовать прямоугольник с закругленными углами размером 30% от половины меньшего размера прямоугольника, указав **арксизе**= "0,3", заполнить его желтым цветом, указав **FillColor**= "Yellow", и присвоив ему красную структуру с 2 точками, указав **строкеколор**= "Red" **строкевеигхт**= "2PT", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="f7a0b-170">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 байт)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="f7a0b-172">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="f7a0b-172">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="f7a0b-173">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="f7a0b-173">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="f7a0b-174">line</span><span class="sxs-lookup"><span data-stu-id="f7a0b-174">line</span></span>

<span data-ttu-id="f7a0b-175">`<line>`Для создания прямой линии можно использовать элемент.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-175">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="f7a0b-176">Затем можно настроить строку, указав другие атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-176">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="f7a0b-177">Например, можно нарисовать горизонтальную линию, указав **from**= "до пунктов, до пунктов" **to**= "100pt, до пунктов" и сделав ее 2-точечными и красными, указав **строкеколор**= "Red" **строкевеигхт**= "2PT", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="f7a0b-177">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 байт)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="f7a0b-179">Можно нарисовать вертикальную или диагональную линию, просто указав разные значения атрибутов свойств **from** и **to** , как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="f7a0b-179">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 байт)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="f7a0b-181">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span><span class="sxs-lookup"><span data-stu-id="f7a0b-181">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="f7a0b-182">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="f7a0b-182">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="f7a0b-183">линию</span><span class="sxs-lookup"><span data-stu-id="f7a0b-183">polyline</span></span>

<span data-ttu-id="f7a0b-184">Элемент можно использовать `<polyline>` для определения фигур, создаваемых из Соединенных линейных сегментов.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-184">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="f7a0b-185">Затем можно настроить фигуру, указав другие атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-185">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="f7a0b-186">Например, чтобы нарисовать фигуру, показанную на следующем рисунке, можно ввести следующее представление VML:</span><span class="sxs-lookup"><span data-stu-id="f7a0b-186">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 байт)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="f7a0b-188">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span><span class="sxs-lookup"><span data-stu-id="f7a0b-188">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="f7a0b-189">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="f7a0b-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="f7a0b-190">кривая</span><span class="sxs-lookup"><span data-stu-id="f7a0b-190">curve</span></span>

<span data-ttu-id="f7a0b-191">Элемент можно использовать `<curve>` для рисования кривой Безье третьего порядка.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-191">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="f7a0b-192">Затем можно настроить кривую, указав другие атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-192">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="f7a0b-193">Например, чтобы нарисовать кривую, как показано на следующем рисунке, можно ввести следующее представление VML:</span><span class="sxs-lookup"><span data-stu-id="f7a0b-193">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 байт)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="f7a0b-195">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span><span class="sxs-lookup"><span data-stu-id="f7a0b-195">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="f7a0b-196">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="f7a0b-196">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="f7a0b-197">дуга</span><span class="sxs-lookup"><span data-stu-id="f7a0b-197">arc</span></span>

<span data-ttu-id="f7a0b-198">Элемент можно использовать `<arc>` для рисования дуги, которая определена как сегмент овала.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-198">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="f7a0b-199">Дуга определяется пересечением овала с векторами радиуса начала и конца, заданными углами.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-199">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="f7a0b-200">Углы вычисляются с помощью свойств круга (ширина равна высоте), а затем масштабируется анисотропикалли до нужной ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-200">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="f7a0b-201">Например, можно нарисовать дугу, начинающуюся с 0 градусов и заканчивающуюся в 90 градусов, указав **startAngle**= "0" **ендангле**= "90", как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="f7a0b-201">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 байт)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="f7a0b-203">Можно изменить дугу, указав различные значения **startAngle** и **ендангле** , как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="f7a0b-203">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

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





<span data-ttu-id="f7a0b-206">Дополнительные сведения об этом элементе см. в [спецификации VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span><span class="sxs-lookup"><span data-stu-id="f7a0b-206">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="f7a0b-207">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="f7a0b-207">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="f7a0b-208">Сводка</span><span class="sxs-lookup"><span data-stu-id="f7a0b-208">Summary</span></span>

<span data-ttu-id="f7a0b-209">Вы можете использовать предварительно определенные элементы VML, такие как `<oval>` , `<line>` , `<polyline>` ,, `<curve>` `<rect>` , `<roundrect>` и, `<arc>` чтобы легко рисовать графические данные на веб-странице, а затем настраивать эти изображения, просто изменяя их атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="f7a0b-209">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 