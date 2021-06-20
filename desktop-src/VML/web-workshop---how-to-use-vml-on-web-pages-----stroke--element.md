---
title: Использование элемента Stroke
description: В этой статье описывается использование элемента Stroke элемента VML, который является устаревшим в Windows Internet Explorer 9.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Веб-семинар, элемент Stroke
- Разработка веб-страниц, элемент Stroke
- Язык VML (VML), элемент Stroke
- VML (язык VML), элемент Stroke
- Векторная графика, элемент Stroke
- элемент Stroke
- Элементы VML, Stroke
- Фигуры VML, элемент Stroke
- Язык VML (VML), атрибут свойства DashStyle
- VML (язык VML), атрибут свойства DashStyle
- Векторная графика, атрибут свойства DashStyle
- атрибут свойства DashStyle
- Язык VML (VML), атрибут свойства Opacity
- VML (язык VML), атрибут свойства Opacity
- Векторная графика, атрибут свойства Opacity
- атрибут свойства Opacity
- Язык VML (VML), атрибут свойства линестиле
- VML (язык VML), атрибут свойства линестиле
- Векторная графика, атрибут свойства линестиле
- атрибут свойства линестиле
- Язык VML (VML), атрибут свойства жоинстиле
- VML (язык VML), атрибут свойства жоинстиле
- Векторная графика, атрибут свойства жоинстиле
- атрибут свойства жоинстиле
- Язык VML (VML), атрибут свойства объекта FillType
- VML (язык VML), атрибут свойства объекта FillType
- Векторная графика, атрибут свойства объекта FillType
- атрибут свойства объекта FillType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407847"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="d9272-131">Использование элемента Stroke</span><span class="sxs-lookup"><span data-stu-id="d9272-131">Using the Stroke Element</span></span>

<span data-ttu-id="d9272-132">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d9272-132">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d9272-133">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="d9272-133">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d9272-134">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="d9272-134">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d9272-135">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d9272-135">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d9272-136">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d9272-136">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d9272-137">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d9272-137">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d9272-138">Использование `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="d9272-138">Using `<stroke>`</span></span>

<span data-ttu-id="d9272-139">Как вы узнали, вы можете использовать атрибуты свойств **строкеколор** и **строкевеигхт** предопределенной фигуры, такие как `<oval>` ,,,, `<line>` `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --для указания цвета и веса контура фигуры.</span><span class="sxs-lookup"><span data-stu-id="d9272-139">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="d9272-140">В этом разделе показано, как нарисовать фигуру с более сложной структурой.</span><span class="sxs-lookup"><span data-stu-id="d9272-140">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="d9272-141">`<stroke>`Вложенный элемент можно поместить внутри `<shape>` , или или `<shapetype>` любого предопределенного элемента Shape, чтобы описать, как рисовать контур фигуры.</span><span class="sxs-lookup"><span data-stu-id="d9272-141">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="d9272-142">Затем можно использовать атрибуты свойств, например [DashStyle](#dashstyle), [Opacity](#opacity), [линестиле](#linestyle), [жоинстиле](#joinstyle), [объекта FillType](#filltype) --из `<stroke>` вложенного элемента для настройки структуры.</span><span class="sxs-lookup"><span data-stu-id="d9272-142">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="d9272-143">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="d9272-143">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="d9272-144">DashStyle</span><span class="sxs-lookup"><span data-stu-id="d9272-144">dashstyle</span></span>

<span data-ttu-id="d9272-145">Можно использовать атрибут свойства **DashStyle** `<stroke>` вложенного элемента для рисования контура с различными стилями пунктира.</span><span class="sxs-lookup"><span data-stu-id="d9272-145">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="d9272-146">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="d9272-146">**Examples:**</span></span>

<span data-ttu-id="d9272-147">Если указать `<v:stroke dashstyle="solid" />` внутри `<line>` элемента, можно создать сплошную линию, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-147">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 байт)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="d9272-149">Если изменить атрибут свойства **DashStyle** на "точка", можно создать пунктирную линию, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-149">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 байт)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="d9272-151">Если изменить атрибут свойства **DashStyle** на "тире", можно создать пунктирную линию, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-151">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 байт)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="d9272-153">Если изменить атрибут свойства **DashStyle** на "дашдот", можно создать линию с пунктирным и пунктирным стилем, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-153">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 байт)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="d9272-155">Если изменить атрибут свойства **DashStyle** на "лонгдаш", можно создать строку с длинным пунктирным стилем, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-155">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 байт)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="d9272-157">Если изменить атрибут свойства **DashStyle** на "лонгдашдот", можно создать строку с длинным пунктирным и пунктирным стилем, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-157">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 байт)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="d9272-159">Если поместить `<v:stroke dashstyle="dashdot" />` внутри `<rect>` элемента, можно создать прямоугольник, имеющий пунктирный и пунктирный контур, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-159">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 байт)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="d9272-161">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="d9272-161">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="d9272-162">непрозрачность</span><span class="sxs-lookup"><span data-stu-id="d9272-162">opacity</span></span>

<span data-ttu-id="d9272-163">Атрибут свойства **Opacity** `<stroke>` вложенного элемента можно использовать для рисования контура с различными стилями непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="d9272-163">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="d9272-164">Значением атрибута **Opacity** свойства может быть любое число от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="d9272-164">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="d9272-165">По умолчанию это 1, что означает полную непрозрачность.</span><span class="sxs-lookup"><span data-stu-id="d9272-165">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="d9272-166">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="d9272-166">**Examples:**</span></span>

<span data-ttu-id="d9272-167">Следующее представление VML создает линию с полной прозрачностью:</span><span class="sxs-lookup"><span data-stu-id="d9272-167">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 байт)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="d9272-169">Если добавить `<v:stroke opacity="0.5" />` внутри `<line>` элемента, можно создать линию со степенью непрозрачности 50%, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-169">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 байт)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="d9272-171">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="d9272-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="d9272-172">линестиле</span><span class="sxs-lookup"><span data-stu-id="d9272-172">linestyle</span></span>

<span data-ttu-id="d9272-173">Можно использовать атрибут свойства **линестиле** `<stroke>` вложенного элемента для рисования контура с различными стилями линий.</span><span class="sxs-lookup"><span data-stu-id="d9272-173">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="d9272-174">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="d9272-174">**Examples:**</span></span>

<span data-ttu-id="d9272-175">Если указать `<v:stroke linestyle="single" />` внутри `<rect>` элемента, можно создать прямоугольник с одной структурой, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-175">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 байт)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="d9272-177">Если изменить атрибут свойства **линестиле** на "синсин", можно создать прямоугольник с контуром (1:1:1), как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-177">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 байт)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="d9272-179">Если изменить атрибут свойства **линестиле** на "синсикк", можно создать прямоугольник с контуром (1:1:2), как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-179">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 байт)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="d9272-181">Если изменить атрибут свойства **линестиле** на "сикксин", можно создать прямоугольник с контуром (2:1:1), как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-181">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 байт)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="d9272-183">Если изменить атрибут свойства **линестиле** на "сиккбетвинсин", можно создать прямоугольник с контуром (1:1:2:1:1), как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-183">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 байт)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="d9272-185">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="d9272-185">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="d9272-186">жоинстиле</span><span class="sxs-lookup"><span data-stu-id="d9272-186">joinstyle</span></span>

<span data-ttu-id="d9272-187">С помощью атрибута **жоинстиле** `<stroke>` вложенного элемента можно определить, как объединяются линии.</span><span class="sxs-lookup"><span data-stu-id="d9272-187">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="d9272-188">Например, чтобы создать фигуру с контуром круглого объединения, как показано на следующем рисунке, можно указать `<v:stroke joinstyle="round" />` внутри `<polyline>` элемента, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-188">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 байт)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="d9272-190">Если изменить атрибут свойства **жоинстиле** на «скос», можно создать фигуру с контуром рельефного объединения, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-190">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 байт)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="d9272-192">Если изменить атрибут свойства **жоинстиле** на «угловой», можно создать фигуру с контуром «угловой соединитель», как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-192">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 байт)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="d9272-194">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="d9272-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="d9272-195">объекта FillType</span><span class="sxs-lookup"><span data-stu-id="d9272-195">filltype</span></span>

<span data-ttu-id="d9272-196">Атрибут свойства **объекта FillType** `<stroke>` вложенного элемента можно использовать для рисования контура с различными эффектами заливки.</span><span class="sxs-lookup"><span data-stu-id="d9272-196">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="d9272-197">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="d9272-197">**Examples:**</span></span>

<span data-ttu-id="d9272-198">Если указать `<v:stroke filltype="solid" />` внутри `<roundrect>` элемента, можно создать скругленный прямоугольник с заполненной сплошной структурой, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-198">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 байт)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="d9272-200">Если изменить атрибут свойства **объекта FillType** на «pattern», укажите в атрибуте свойства **src** расположение файла изображения шаблона и задайте атрибуту свойства **color2** второй цвет шаблона, а затем можно создать скругленный прямоугольник с контуром шаблона, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-200">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 байт)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="d9272-202">Если изменить атрибут свойства **объекта FillType** на "плитку" и указать атрибуту свойства **src** расположение файла изображения, можно создать скругленный прямоугольник с мозаичным контуром, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-202">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 байт)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="d9272-204">Если изменить атрибут свойства **объекта FillType** на "Frame" и указать атрибуту свойства **src** расположение файла изображения, можно создать скругленный прямоугольник с контуром изображения, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="d9272-204">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 байт)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="d9272-206">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="d9272-206">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 