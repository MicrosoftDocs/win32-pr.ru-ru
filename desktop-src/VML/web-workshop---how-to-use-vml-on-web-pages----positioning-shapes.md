---
title: Позиционирование фигур
description: В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Веб-семинар, позиционирование фигур
- Разработка веб-страниц, позиционирование фигур
- Язык VML (VML), позиционирование фигур
- VML (язык VML), позиционирование фигур
- Векторная графика, позиционирование фигур
- Фигуры VML, позиционирование
- позиционирование фигур
- Язык VML (VML), статический стиль расположения
- VML (язык VML), статический стиль расположения
- Векторная графика, стиль статического позиционирования
- статический стиль расположения
- Язык VML (VML), стиль относительного положения
- VML (язык VML), стиль относительного положения
- Векторная графика, стиль относительного положения
- стиль относительного положения
- Язык VML (VML), абсолютный стиль расположения
- VML (язык VML), абсолютный стиль расположения
- Векторная графика, стиль абсолютного расположения
- стиль абсолютного расположения
- Язык VML (VML), стиль позиции z-индекса
- VML (язык VML), стиль позиции z-индекса
- Векторная графика, стиль позиции z-индекса
- z — стиль позиции индекса
- Язык VML (VML), стиль расположения вращения
- VML (язык VML), стиль расположения вращения
- Векторная графика, стиль расположения вращения
- стиль расположения вращения
- Язык VML (VML), отразить стиль расположения
- VML (язык VML), отразить стиль расположения
- Векторная графика, отразить стиль расположения
- отразить стиль расположения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8e01d0c7962467b1894f0f4c2c6cd1f6b01509
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070161"
---
# <a name="positioning-shapes"></a><span data-ttu-id="21f36-135">Позиционирование фигур</span><span class="sxs-lookup"><span data-stu-id="21f36-135">Positioning Shapes</span></span>

<span data-ttu-id="21f36-136">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="21f36-136">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="21f36-137">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="21f36-137">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="21f36-138">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="21f36-138">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="21f36-139">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21f36-139">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="21f36-140">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="21f36-140">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="21f36-141">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="21f36-141">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="21f36-142">Вы узнали, как рисовать и цветировать фигуры на веб-странице с помощью VML.</span><span class="sxs-lookup"><span data-stu-id="21f36-142">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="21f36-143">В этом разделе для точного позиционирования графики на веб-странице используется VML.</span><span class="sxs-lookup"><span data-stu-id="21f36-143">In this topic, you'll use VML to precisely position graphics on a Web page.</span></span>

<span data-ttu-id="21f36-144">VML использует тот же синтаксис, что и в разделах [модель Box](https://www.w3.org/TR/PR-CSS2/box.mdl) и [модель визуальной отрисовки](https://www.w3.org/TR/PR-CSS2/visuren.mdl) [CSS2](https://www.w3.org/TR/PR-CSS2/) для размещения фигур на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="21f36-144">VML uses the same syntax defined in the [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) and [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) sections of [CSS2](https://www.w3.org/TR/PR-CSS2/) to position shapes on a Web page.</span></span> <span data-ttu-id="21f36-145">Для определения места расположения базовой точки на веб-странице можно использовать [статический](#static), [относительный](#relative)или [абсолютный](#absolute) .</span><span class="sxs-lookup"><span data-stu-id="21f36-145">You can use [static](#static), [relative](#relative), or [absolute](#absolute) to determine where the base point is located on a Web page.</span></span> <span data-ttu-id="21f36-146">Затем можно использовать атрибуты **верхнего** и **левого** стилей, чтобы указать смещение от базовой точки, в которой будет размещается поле, содержащее фигуру.</span><span class="sxs-lookup"><span data-stu-id="21f36-146">You can then use the **top** and **left** style attributes to specify the offset from the base point at which the containing box for the shape will be positioned.</span></span>

<span data-ttu-id="21f36-147">[Z-index](#z-index) также можно использовать для указания z-порядка фигур на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="21f36-147">You can also use [z-index](#z-index) to specify the z-order of shapes on a Web page.</span></span>

<span data-ttu-id="21f36-148">Кроме того, VML обеспечивает [поворот](#rotation) и [отражение](#flip) для поворота или отражения фигур.</span><span class="sxs-lookup"><span data-stu-id="21f36-148">In addition, VML provides [rotation](#rotation) and [flip](#flip) to rotate or flip shapes.</span></span>

<span data-ttu-id="21f36-149">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="21f36-149">In this topic:</span></span>

-   [<span data-ttu-id="21f36-150">static</span><span class="sxs-lookup"><span data-stu-id="21f36-150">static</span></span>](#static)
-   [<span data-ttu-id="21f36-151">relative</span><span class="sxs-lookup"><span data-stu-id="21f36-151">relative</span></span>](#relative)
-   [<span data-ttu-id="21f36-152">absolute</span><span class="sxs-lookup"><span data-stu-id="21f36-152">absolute</span></span>](#absolute)
-   [<span data-ttu-id="21f36-153">z-индекс</span><span class="sxs-lookup"><span data-stu-id="21f36-153">z-index</span></span>](#z-index)
-   [<span data-ttu-id="21f36-154">поворота</span><span class="sxs-lookup"><span data-stu-id="21f36-154">rotation</span></span>](#rotation)
-   [<span data-ttu-id="21f36-155">flip</span><span class="sxs-lookup"><span data-stu-id="21f36-155">flip</span></span>](#flip)
-   [<span data-ttu-id="21f36-156">Сводка</span><span class="sxs-lookup"><span data-stu-id="21f36-156">Summary</span></span>](#summary)

## <a name="static"></a><span data-ttu-id="21f36-157">static</span><span class="sxs-lookup"><span data-stu-id="21f36-157">static</span></span>

<span data-ttu-id="21f36-158">Стиль позиции по умолчанию — Static, который указывает браузерам разместить фигуру в текущей точке (в базовой точке) в потоке текста и игнорировать параметры в атрибутах **верхнего** и **левого** стилей.</span><span class="sxs-lookup"><span data-stu-id="21f36-158">The default position style is static, which instructs browsers to position the shape at the current point (the base point) in the text flow and ignore the settings in the **top** and **left** style attributes.</span></span>

<span data-ttu-id="21f36-159">Например, в следующем представлении VML красный овал располагается сразу после текста «начало фигуры:», как показано на следующем рисунке:</span><span class="sxs-lookup"><span data-stu-id="21f36-159">For example, in the following VML representation, the red oval is positioned immediately after the text "Beginning of the shape:", as shown in the following picture:</span></span>

![\-ps.gif shape1 (2123 байт)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="21f36-161">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="21f36-161">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="relative"></a><span data-ttu-id="21f36-162">relative</span><span class="sxs-lookup"><span data-stu-id="21f36-162">relative</span></span>

<span data-ttu-id="21f36-163">Установка атрибута стиля позиции в значение "относительный" позволяет поместить содержащее поле со смещением от текущей точки (базовой точки) в потоке текста.</span><span class="sxs-lookup"><span data-stu-id="21f36-163">Setting the position style attribute to "relative" allows you to place the containing box with an offset from the current point (the base point) in the text flow.</span></span> <span data-ttu-id="21f36-164">Смещение определяется параметрами в атрибутах **верхнего** и **левого** стилей.</span><span class="sxs-lookup"><span data-stu-id="21f36-164">The offset is determined by the settings in the **top** and **left** style attributes.</span></span> <span data-ttu-id="21f36-165">Имейте в виду, что содержащееся поле, расположенное как относительная, занимает место в потоке текста.</span><span class="sxs-lookup"><span data-stu-id="21f36-165">Be aware that the containing box that is positioned as relative takes up space in the text flow.</span></span>

<span data-ttu-id="21f36-166">Например, в следующем представлении VML красный овал размещается на 20 точках от левого угла до 10 пунктов сверху относительно текущей точки в потоке текста, как показано на следующем рисунке:</span><span class="sxs-lookup"><span data-stu-id="21f36-166">For example, in the following VML representation, the red oval is positioned 20 points from the left and 10 points from the top relative to the current point in the text flow, as shown in the following picture:</span></span>

![shape3.gif (2048 байт)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="21f36-168">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="21f36-168">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="absolute"></a><span data-ttu-id="21f36-169">absolute</span><span class="sxs-lookup"><span data-stu-id="21f36-169">absolute</span></span>

<span data-ttu-id="21f36-170">Присвоение атрибуту стиля позиции значения "Absolute" позволяет поместить содержащее поле в точное расстояние от верхнего левого угла (базовой точки) его родительского элемента (Позиционированный элемент, содержащий фигуру).</span><span class="sxs-lookup"><span data-stu-id="21f36-170">Setting the position style attribute to "absolute" allows you to place the containing box an exact distance from the top left corner (the base point) of its parent element (the positioned element that contains the shape).</span></span> <span data-ttu-id="21f36-171">Имейте в виду, что содержащее поле, расположенное как абсолютное, не занимает место в потоке текста.</span><span class="sxs-lookup"><span data-stu-id="21f36-171">Be aware that the containing box that is positioned as absolute doesn't take up space in the text flow.</span></span>

<span data-ttu-id="21f36-172">Например, в следующем представлении VML красный овал содержится внутри `<body>` элемента (вся веб-страница), поэтому базовая точка находится в левом верхнем углу веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="21f36-172">For example, in the following VML representation, the red oval is contained within the `<body>` element (the entire Web page); therefore, the base point is at the top left corner of the Web page.</span></span> <span data-ttu-id="21f36-173">Содержащееся в овале поле располагается ровно на 20 точек от левого угла до 10 пунктов сверху относительно левого верхнего угол веб-страницы, как показано на следующем рисунке:</span><span class="sxs-lookup"><span data-stu-id="21f36-173">The containing box for the oval is positioned exactly 20 points from the left and 10 points from the top, relative to the top left corner of the Web page, as shown in the following picture:</span></span>

![shape2.gif (2006 байт)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="21f36-175">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="21f36-175">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="z-index"></a><span data-ttu-id="21f36-176">z-index</span><span class="sxs-lookup"><span data-stu-id="21f36-176">z-index</span></span>

<span data-ttu-id="21f36-177">Можно разместить фигуру, которая пересекается с другой фигурой.</span><span class="sxs-lookup"><span data-stu-id="21f36-177">It is possible to position a shape that overlaps another shape.</span></span> <span data-ttu-id="21f36-178">Как правило, рисунок, указанный в коде HTML, отображается сверху.</span><span class="sxs-lookup"><span data-stu-id="21f36-178">Normally, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="21f36-179">В VML можно управлять z-порядком, используя атрибут стиля **z-index** .</span><span class="sxs-lookup"><span data-stu-id="21f36-179">In VML, you can control the z-order by using the **z-index** style attribute.</span></span> <span data-ttu-id="21f36-180">Значением этого атрибута может быть ноль, положительное целое число или отрицательное целое число.</span><span class="sxs-lookup"><span data-stu-id="21f36-180">The value of this attribute can be zero, a positive integer, or a negative integer.</span></span> <span data-ttu-id="21f36-181">Рисунок с большим значением z-индекса отображается поверх рисунка с меньшим значением z-индекса.</span><span class="sxs-lookup"><span data-stu-id="21f36-181">The graphic that has a larger z-index value is displayed on top of the graphic that has a smaller z-index value.</span></span> <span data-ttu-id="21f36-182">Если обе графические изображения имеют одинаковое значение z-индекса, в верхней части экрана отображается рисунок, указанный в коде HTML последним.</span><span class="sxs-lookup"><span data-stu-id="21f36-182">When both graphics have the same z-index value, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="21f36-183">Например, в следующем представлении VML красный овал отображается поверх синего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="21f36-183">For example, in the following VML representation, the red oval is displayed on top of the blue rectangle.</span></span> <span data-ttu-id="21f36-184">Это связано с тем, что значение z-индекса Красного овала больше значения z-индекса синего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="21f36-184">This is because the z-index value of the red oval is greater than the z-index value of the blue rectangle.</span></span>

![shape4.gif (572 байт)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





<span data-ttu-id="21f36-186">Если изменить z-индекс, как показано в следующем представлении VML, красный овал будет перемещаться позади синего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="21f36-186">If you change the z-index, as shown in the following VML representation, the red oval would move behind the blue rectangle.</span></span>

![shape5.gif (469 байт)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





<span data-ttu-id="21f36-188">Если вы передаете отрицательное целое число, можно использовать z-индекс для размещения графики позади обычного потока текста, как показано в следующем представлении VML.</span><span class="sxs-lookup"><span data-stu-id="21f36-188">If you supply a negative integer, you can use z-index to position graphics behind the normal text flow, as shown in the following VML representation.</span></span>

![shape6.gif (2125 байт)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="21f36-190">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="21f36-190">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rotation"></a><span data-ttu-id="21f36-191">Поворот</span><span class="sxs-lookup"><span data-stu-id="21f36-191">rotation</span></span>

<span data-ttu-id="21f36-192">Можно использовать атрибут «стиль **вращения** », чтобы указать, сколько градусов должна включать фигура на ее оси.</span><span class="sxs-lookup"><span data-stu-id="21f36-192">You can use the **rotation** style attribute to specify how many degrees you want a shape to turn on its axis.</span></span> <span data-ttu-id="21f36-193">Положительное значение обозначает поворот по часовой стрелке. отрицательное значение обозначает поворот по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="21f36-193">A positive value indicates a clockwise rotation; a negative value indicates a counter-clockwise rotation.</span></span>

<span data-ttu-id="21f36-194">Например, если указать **Style**= '... поворот: 90. фигуру можно повернуть на 90 градусов по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="21f36-194">For example, if you specify **style**='... rotation:90', you can rotate the shape 90 degrees clockwise.</span></span>

<span data-ttu-id="21f36-195">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="21f36-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="flip"></a><span data-ttu-id="21f36-196">flip</span><span class="sxs-lookup"><span data-stu-id="21f36-196">flip</span></span>

<span data-ttu-id="21f36-197">Атрибут « **перелистывание** стиля» можно использовать для отражения фигуры на оси x или y в соответствии со следующей таблицей.</span><span class="sxs-lookup"><span data-stu-id="21f36-197">You can use the **flip** style attribute to flip a shape on its x or y axis according to the following table:</span></span>



| <span data-ttu-id="21f36-198">Значение</span><span class="sxs-lookup"><span data-stu-id="21f36-198">Value</span></span> | <span data-ttu-id="21f36-199">Описание</span><span class="sxs-lookup"><span data-stu-id="21f36-199">Description</span></span>                                                  |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="21f36-200">x</span><span class="sxs-lookup"><span data-stu-id="21f36-200">x</span></span>     | <span data-ttu-id="21f36-201">Отражение повернутой фигуры относительно оси y (инверсия координат x)</span><span class="sxs-lookup"><span data-stu-id="21f36-201">Flip the rotated shape about the y axis (invert x ordinates)</span></span> |
| <span data-ttu-id="21f36-202">да</span><span class="sxs-lookup"><span data-stu-id="21f36-202">y</span></span>     | <span data-ttu-id="21f36-203">Отражение повернутой фигуры относительно оси x (обратные координаты y)</span><span class="sxs-lookup"><span data-stu-id="21f36-203">Flip the rotated shape about the x axis (invert y ordinates)</span></span> |



 

<span data-ttu-id="21f36-204">В свойстве отражения можно указать и x, и y.</span><span class="sxs-lookup"><span data-stu-id="21f36-204">Both x and y may be specified in the flip property.</span></span>

<span data-ttu-id="21f36-205">Например, если ввести **Style**= '... отразить: x y. Вы отразите фигуру на обеих осях x и y.</span><span class="sxs-lookup"><span data-stu-id="21f36-205">For example, if you type **style**='... flip:x y', you will flip the shape on both its x and y axis.</span></span>

<span data-ttu-id="21f36-206">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="21f36-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="21f36-207">Сводка</span><span class="sxs-lookup"><span data-stu-id="21f36-207">Summary</span></span>

<span data-ttu-id="21f36-208">В зависимости от того, что вы узнали, можно точно разместить фигуру на веб-странице, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="21f36-208">Based on what you've learned, you can precisely position a shape on a Web page by following these steps:</span></span>

1.  <span data-ttu-id="21f36-209">Определите, где должна отображаться фигура на веб-странице, и размер фигуры.</span><span class="sxs-lookup"><span data-stu-id="21f36-209">Decide where you want the shape to appear on a Web page, and the size of the shape.</span></span>
2.  <span data-ttu-id="21f36-210">Для определения базовой точки укажите **Style**= "позиционирует: relative (или Relative)".</span><span class="sxs-lookup"><span data-stu-id="21f36-210">Specify **style**='position:relative (or relative)' to determine the base point.</span></span>
3.  <span data-ttu-id="21f36-211">Используйте **левую** и **верхнюю части** , чтобы указать смещение от базовой точки.</span><span class="sxs-lookup"><span data-stu-id="21f36-211">Use **left** and **top** to specify the offset from the base point.</span></span>
4.  <span data-ttu-id="21f36-212">Используйте **ширину** и **высоту** , чтобы указать размер содержащего поля для фигуры.</span><span class="sxs-lookup"><span data-stu-id="21f36-212">Use **width** and **height** to specify the size of the containing box for the shape.</span></span>
5.  <span data-ttu-id="21f36-213">Используйте **z-index** , чтобы указать z-порядок фигуры.</span><span class="sxs-lookup"><span data-stu-id="21f36-213">Use **z-index** to specify the z-order of the shape.</span></span>

 

 