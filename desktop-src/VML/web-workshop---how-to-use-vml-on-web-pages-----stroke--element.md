---
title: Использование элемента Stroke
description: В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.
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
ms.openlocfilehash: 4b58e02945884ea63ad1be01e67cfc156951cd5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339100"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="006e0-132">Использование элемента Stroke</span><span class="sxs-lookup"><span data-stu-id="006e0-132">Using the Stroke Element</span></span>

<span data-ttu-id="006e0-133">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="006e0-133">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="006e0-134">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="006e0-134">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="006e0-135">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="006e0-135">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="006e0-136">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="006e0-136">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="006e0-137">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="006e0-137">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="006e0-138">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="006e0-138">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="006e0-139">Использование `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="006e0-139">Using `<stroke>`</span></span>

<span data-ttu-id="006e0-140">Как вы узнали, вы можете использовать атрибуты свойств **строкеколор** и **строкевеигхт** предопределенной фигуры, такие как `<oval>` ,,,, `<line>` `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --для указания цвета и веса контура фигуры.</span><span class="sxs-lookup"><span data-stu-id="006e0-140">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="006e0-141">В этом разделе показано, как нарисовать фигуру с более сложной структурой.</span><span class="sxs-lookup"><span data-stu-id="006e0-141">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="006e0-142">`<stroke>`Вложенный элемент можно поместить внутри `<shape>` , или или `<shapetype>` любого предопределенного элемента Shape, чтобы описать, как рисовать контур фигуры.</span><span class="sxs-lookup"><span data-stu-id="006e0-142">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="006e0-143">Затем можно использовать атрибуты свойств, например [DashStyle](#dashstyle), [Opacity](#opacity), [линестиле](#linestyle), [жоинстиле](#joinstyle), [объекта FillType](#filltype) --из `<stroke>` вложенного элемента для настройки структуры.</span><span class="sxs-lookup"><span data-stu-id="006e0-143">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="006e0-144">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="006e0-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="006e0-145">DashStyle</span><span class="sxs-lookup"><span data-stu-id="006e0-145">dashstyle</span></span>

<span data-ttu-id="006e0-146">Можно использовать атрибут свойства **DashStyle** `<stroke>` вложенного элемента для рисования контура с различными стилями пунктира.</span><span class="sxs-lookup"><span data-stu-id="006e0-146">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="006e0-147">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="006e0-147">**Examples:**</span></span>

<span data-ttu-id="006e0-148">Если указать `<v:stroke dashstyle="solid" />` внутри `<line>` элемента, можно создать сплошную линию, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-148">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 байт)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="006e0-150">Если изменить атрибут свойства **DashStyle** на "точка", можно создать пунктирную линию, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-150">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 байт)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="006e0-152">Если изменить атрибут свойства **DashStyle** на "тире", можно создать пунктирную линию, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-152">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 байт)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="006e0-154">Если изменить атрибут свойства **DashStyle** на "дашдот", можно создать линию с пунктирным и пунктирным стилем, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-154">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 байт)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="006e0-156">Если изменить атрибут свойства **DashStyle** на "лонгдаш", можно создать строку с длинным пунктирным стилем, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-156">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 байт)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="006e0-158">Если изменить атрибут свойства **DashStyle** на "лонгдашдот", можно создать строку с длинным пунктирным и пунктирным стилем, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-158">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 байт)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="006e0-160">Если поместить `<v:stroke dashstyle="dashdot" />` внутри `<rect>` элемента, можно создать прямоугольник, имеющий пунктирный и пунктирный контур, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-160">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 байт)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="006e0-162">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="006e0-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="006e0-163">непрозрачность</span><span class="sxs-lookup"><span data-stu-id="006e0-163">opacity</span></span>

<span data-ttu-id="006e0-164">Атрибут свойства **Opacity** `<stroke>` вложенного элемента можно использовать для рисования контура с различными стилями непрозрачности.</span><span class="sxs-lookup"><span data-stu-id="006e0-164">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="006e0-165">Значением атрибута **Opacity** свойства может быть любое число от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="006e0-165">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="006e0-166">По умолчанию это 1, что означает полную непрозрачность.</span><span class="sxs-lookup"><span data-stu-id="006e0-166">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="006e0-167">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="006e0-167">**Examples:**</span></span>

<span data-ttu-id="006e0-168">Следующее представление VML создает линию с полной прозрачностью:</span><span class="sxs-lookup"><span data-stu-id="006e0-168">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 байт)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="006e0-170">Если добавить `<v:stroke opacity="0.5" />` внутри `<line>` элемента, можно создать линию со степенью непрозрачности 50%, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-170">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 байт)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="006e0-172">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="006e0-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="006e0-173">линестиле</span><span class="sxs-lookup"><span data-stu-id="006e0-173">linestyle</span></span>

<span data-ttu-id="006e0-174">Можно использовать атрибут свойства **линестиле** `<stroke>` вложенного элемента для рисования контура с различными стилями линий.</span><span class="sxs-lookup"><span data-stu-id="006e0-174">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="006e0-175">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="006e0-175">**Examples:**</span></span>

<span data-ttu-id="006e0-176">Если указать `<v:stroke linestyle="single" />` внутри `<rect>` элемента, можно создать прямоугольник с одной структурой, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-176">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 байт)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="006e0-178">Если изменить атрибут свойства **линестиле** на "синсин", можно создать прямоугольник с контуром (1:1:1), как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-178">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 байт)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="006e0-180">Если изменить атрибут свойства **линестиле** на "синсикк", можно создать прямоугольник с контуром (1:1:2), как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-180">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 байт)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="006e0-182">Если изменить атрибут свойства **линестиле** на "сикксин", можно создать прямоугольник с контуром (2:1:1), как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-182">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 байт)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="006e0-184">Если изменить атрибут свойства **линестиле** на "сиккбетвинсин", можно создать прямоугольник с контуром (1:1:2:1:1), как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-184">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 байт)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="006e0-186">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="006e0-186">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="006e0-187">жоинстиле</span><span class="sxs-lookup"><span data-stu-id="006e0-187">joinstyle</span></span>

<span data-ttu-id="006e0-188">С помощью атрибута **жоинстиле** `<stroke>` вложенного элемента можно определить, как объединяются линии.</span><span class="sxs-lookup"><span data-stu-id="006e0-188">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="006e0-189">Например, чтобы создать фигуру с контуром круглого объединения, как показано на следующем рисунке, можно указать `<v:stroke joinstyle="round" />` внутри `<polyline>` элемента, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-189">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 байт)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="006e0-191">Если изменить атрибут свойства **жоинстиле** на «скос», можно создать фигуру с контуром рельефного объединения, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-191">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 байт)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="006e0-193">Если изменить атрибут свойства **жоинстиле** на «угловой», можно создать фигуру с контуром «угловой соединитель», как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-193">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 байт)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="006e0-195">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="006e0-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="006e0-196">объекта FillType</span><span class="sxs-lookup"><span data-stu-id="006e0-196">filltype</span></span>

<span data-ttu-id="006e0-197">Атрибут свойства **объекта FillType** `<stroke>` вложенного элемента можно использовать для рисования контура с различными эффектами заливки.</span><span class="sxs-lookup"><span data-stu-id="006e0-197">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="006e0-198">**Примеры:**</span><span class="sxs-lookup"><span data-stu-id="006e0-198">**Examples:**</span></span>

<span data-ttu-id="006e0-199">Если указать `<v:stroke filltype="solid" />` внутри `<roundrect>` элемента, можно создать скругленный прямоугольник с заполненной сплошной структурой, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-199">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 байт)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="006e0-201">Если изменить атрибут свойства **объекта FillType** на «pattern», укажите в атрибуте свойства **src** расположение файла изображения шаблона и задайте атрибуту свойства **color2** второй цвет шаблона, а затем можно создать скругленный прямоугольник с контуром шаблона, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-201">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 байт)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="006e0-203">Если изменить атрибут свойства **объекта FillType** на "плитку" и указать атрибуту свойства **src** расположение файла изображения, можно создать скругленный прямоугольник с мозаичным контуром, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-203">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 байт)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="006e0-205">Если изменить атрибут свойства **объекта FillType** на "Frame" и указать атрибуту свойства **src** расположение файла изображения, можно создать скругленный прямоугольник с контуром изображения, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="006e0-205">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 байт)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="006e0-207">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="006e0-207">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 