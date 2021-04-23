---
title: Использование локального пространства координат
description: Использование локального пространства координат
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Веб-семинар, локальное пространство координат
- Разработка веб-страниц, локальное пространство координат
- Язык VML (VML), локальное пространство координат
- VML (язык VML), локальное пространство координат
- Векторная графика, локальное пространство координат
- Локальное пространство координат
- Фигуры VML, локальное пространство координат
- Язык VML (VML), Группирование фигур
- VML (язык VML), Группирование фигур
- Векторная графика, Группирование фигур
- Фигуры VML, группирование
- Группирование фигур
- Язык VML (VML), масштабирование фигур
- VML (язык VML), масштабирование фигур
- Векторная графика, масштабирование фигур
- Фигуры VML, масштабирование
- масштабирование фигур
- Язык VML (VML), изменение размеров фигур
- VML (язык VML), изменение размеров фигур
- Векторная графика, изменение размеров фигур
- Фигуры VML, изменение размера
- изменение размеров фигур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793452"
---
# <a name="using-local-coordinate-space"></a><span data-ttu-id="7f560-125">Использование локального пространства координат</span><span class="sxs-lookup"><span data-stu-id="7f560-125">Using Local Coordinate Space</span></span>

<span data-ttu-id="7f560-126">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7f560-126">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7f560-127">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="7f560-127">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7f560-128">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="7f560-128">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7f560-129">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7f560-129">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7f560-130">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7f560-130">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7f560-131">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7f560-131">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7f560-132">Как вы узнали, можно указать атрибуты стиля **Width** и **Height** , определяющие размер содержащего поля, в пределах которого будет производиться отрисовка содержимого фигуры или группы.</span><span class="sxs-lookup"><span data-stu-id="7f560-132">As you've learned, you can specify the **width** and **height** style attributes to define the size of a containing box within which the contents of a shape or group will be rendered.</span></span> <span data-ttu-id="7f560-133">В этом разделе будет объяснено, что такое локальное пространство координат и как оно используется в VML для масштабирования фигур.</span><span class="sxs-lookup"><span data-stu-id="7f560-133">In this topic, we will explain what Local Coordinate Space is, and how it is used in VML to scale shapes.</span></span>

<span data-ttu-id="7f560-134">Если вам было предложено нарисовать прямоугольный прямоугольник с двумя углами на листе сетки, первое, что вы захотите определить, — начать (исходную точку).</span><span class="sxs-lookup"><span data-stu-id="7f560-134">If you were asked to draw a one-inch by two-inch rectangle on a piece of grid paper, the first thing you would figure out is where to start (the originating point).</span></span> <span data-ttu-id="7f560-135">Затем вы узнаете, как сопоставлять один дюйм с ячейками сетки (координаты).</span><span class="sxs-lookup"><span data-stu-id="7f560-135">Then, you would figure out how to map one inch to the cells of the grid paper (the coordinate).</span></span>

<span data-ttu-id="7f560-136">Аналогично, когда содержимое фигуры или группы отображается внутри содержащего его поля на веб-странице, необходимо определить исходную точку и координату.</span><span class="sxs-lookup"><span data-stu-id="7f560-136">Similarly, when the contents of a shape or group are rendered inside its containing box on a Web page, the originating point and the coordinate must be defined.</span></span> <span data-ttu-id="7f560-137">VML предоставляет локальное пространство координат, позволяющее каждой фигуре или группе определять собственную исходную точку и координату.</span><span class="sxs-lookup"><span data-stu-id="7f560-137">VML provides Local Coordinate Space to allow each shape or group to define its own originating point and coordinate.</span></span> <span data-ttu-id="7f560-138">Если не указать пространство координат, будет использоваться значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7f560-138">If you don't specify a coordinate space, the default one will be used.</span></span> <span data-ttu-id="7f560-139">По умолчанию источник начинается в левом верхнем углу содержащего поля.</span><span class="sxs-lookup"><span data-stu-id="7f560-139">By default, the origination starts at the top-left corner of the containing box.</span></span>

<span data-ttu-id="7f560-140">Например, в представлении VML для красного овала, показанного ниже, не указаны атрибуты свойств **курдсизе** и **курдоригин** .</span><span class="sxs-lookup"><span data-stu-id="7f560-140">For example, the VML representation for the red oval shown below doesn't specify the **coordsize** and **coordorigin** property attributes.</span></span> <span data-ttu-id="7f560-141">Поэтому используется локальное пространство координат по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7f560-141">Therefore, a default local coordinate space is used.</span></span> <span data-ttu-id="7f560-142">Размер овала — 100 точек (ширина) на 75 пунктов (высота).</span><span class="sxs-lookup"><span data-stu-id="7f560-142">The size of the oval is 100 points (width) by 75 points (height).</span></span> <span data-ttu-id="7f560-143">Можно изменить размер овала, указав другую ширину или высоту, как описано в разделе [масштабирование фигур](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) .</span><span class="sxs-lookup"><span data-stu-id="7f560-143">You can resize the oval by specifying a different width or height, as you've learned in the [Scale Shapes](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) topic.</span></span>

![oval1.gif (627 байт)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





<span data-ttu-id="7f560-145">Когда фигура станет более сложной, или если вы хотите сгруппировать несколько фигур и масштабировать их вместе, следует использовать функцию локального координатного пространства, предоставляемую в VML.</span><span class="sxs-lookup"><span data-stu-id="7f560-145">When the shape becomes more complicated, or when you would like to group several shapes and scale them together, you should use the Local Coordinate Space feature provided in VML.</span></span>

<span data-ttu-id="7f560-146">Для каждой фигуры или группы можно использовать атрибуты свойств **курдсизе** и **курдоригин** , чтобы определить локальное пространство координат фигуры или группы.</span><span class="sxs-lookup"><span data-stu-id="7f560-146">For each shape or group, you can use the **coordsize** and **coordorigin** property attributes to define the shape's or group's local coordinate space.</span></span> <span data-ttu-id="7f560-147">Атрибут **курдсизе** задает количество единиц вдоль ширины и высоту содержащего поля.</span><span class="sxs-lookup"><span data-stu-id="7f560-147">The **coordsize** attribute specifies the number of units along the width and the height of the containing box.</span></span> <span data-ttu-id="7f560-148">Атрибут **курдоригин** определяет координату в левом верхнем углу содержащего поля.</span><span class="sxs-lookup"><span data-stu-id="7f560-148">The **coordorigin** attribute defines the coordinate at the top left corner of the containing box.</span></span> <span data-ttu-id="7f560-149">Все сведения, относящиеся к положению (такие как ширина, высота, левое, верхнее, путь и т. д.), выражаются с точки зрения единицы в локальном пространстве координат.</span><span class="sxs-lookup"><span data-stu-id="7f560-149">All position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span>

<span data-ttu-id="7f560-150">Например, как показано в следующем представлении VML, `width: 100pt; height: 100pt;` определяет размер содержащего поля фигуры в 100 точек на 100 точек.</span><span class="sxs-lookup"><span data-stu-id="7f560-150">For example, as shown in the following VML representation, `width: 100pt; height: 100pt;` defines the size of the containing box for the shape to be 100 points by 100 points.</span></span>

![cord1.gif (836 байт)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   <span data-ttu-id="7f560-152">`coordsize="21600,21600"` Определяет размер локального координатного пространства для фигуры в 21600 единиц на 21600 единиц.</span><span class="sxs-lookup"><span data-stu-id="7f560-152">`coordsize="21600,21600"` defines the size of the Local Coordinate Space for the shape to be 21600 units by 21600 units.</span></span> <span data-ttu-id="7f560-153">Таким образом, одна единица в локальном пространстве координат эквивалентна точке 1/216.</span><span class="sxs-lookup"><span data-stu-id="7f560-153">Therefore, one unit in the Local Coordinate Space is equivalent to 1/216 point.</span></span>
-   <span data-ttu-id="7f560-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` определяет контур фигуры в виде ромба.</span><span class="sxs-lookup"><span data-stu-id="7f560-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` defines the outline of the shape as a diamond shape.</span></span> <span data-ttu-id="7f560-155">Как мы узнали, все сведения, относящиеся к положению (например, ширина, высота, левое, верхнее место, путь и т. д.), выражаются с точки зрения единицы в локальном пространстве координат.</span><span class="sxs-lookup"><span data-stu-id="7f560-155">As we've learned, all position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span> <span data-ttu-id="7f560-156">Таким образом, 10800 в `<path>` означает единицу 10800, которая эквивалентна 50 точек.</span><span class="sxs-lookup"><span data-stu-id="7f560-156">Therefore, 10800 in the `<path>` means 10800 units, which is equivalent to 50 points.</span></span>

<span data-ttu-id="7f560-157">Если нужно изменить размер этой фигуры-ромба, просто укажите другую ширину или высоту. нет необходимости изменять какое бы то ни было значение в `<path>` .</span><span class="sxs-lookup"><span data-stu-id="7f560-157">When you want to resize this diamond shape, simply specify a different width or height -- that's it; you don't have to change any value in the `<path>`.</span></span> <span data-ttu-id="7f560-158">Для этой сложной фигуры, если вы не использовали локальную функцию координатного пространства, вам пришлось бы изменять каждое значение в `<path>` каждый раз, когда нужно изменить его размер.</span><span class="sxs-lookup"><span data-stu-id="7f560-158">For this complicated shape, if you didn't use the Local Coordinate Space feature, you would have to change every value in the `<path>` whenever you wanted to resize it.</span></span>

<span data-ttu-id="7f560-159">Например, можно масштабировать фигуру ромба, просто указав другую ширину или высоту, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="7f560-159">For example, you can scale the diamond shape by simply specifying a different width or height, as shown in the following VML representation:</span></span>

![cord2.gif (1692 байт)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





<span data-ttu-id="7f560-161">Можно также использовать локальное пространство координат в `<group>` элементе, чтобы содержимое всех фигур в группе было масштабировано в соответствии с одинаковой координатой.</span><span class="sxs-lookup"><span data-stu-id="7f560-161">You can also use Local Coordinate Space in the `<group>` element so that the contents of all shapes within the group are scaled together according to the same coordinate.</span></span> <span data-ttu-id="7f560-162">Затем, если нужно масштабировать или переместить группу фигур, просто измените ширину и высоту, а также параметры **курдсизе** и **курдоригин** группы.</span><span class="sxs-lookup"><span data-stu-id="7f560-162">Then, whenever you want to scale or move a group of shapes, simply change the width and height, or **coordsize** and **coordorigin** settings, of the group.</span></span>

<span data-ttu-id="7f560-163">Например, в следующем представлении VML `<v:group style='... width:200pt;height:200pt;'>` определяет размер содержащего поля для группы в 200 точек на 200 точек.</span><span class="sxs-lookup"><span data-stu-id="7f560-163">For example, in the following VML representation, `<v:group style='... width:200pt;height:200pt;'>` defines the size of the containing box for the group to be 200 points by 200 points.</span></span>

![cord3.gif (645 байт)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   <span data-ttu-id="7f560-165">`coordsize="1000,1000"` Определяет размер локального координатного пространства для группы в 1000 единиц на 1000 единиц.</span><span class="sxs-lookup"><span data-stu-id="7f560-165">`coordsize="1000,1000"` defines the size of the Local Coordinate Space for the group to be 1000 units by 1000 units.</span></span> <span data-ttu-id="7f560-166">Поэтому 1 единица в локальном пространстве координат эквивалентна точке 1/5.</span><span class="sxs-lookup"><span data-stu-id="7f560-166">Therefore, 1 unit in the Local Coordinate Space is equivalent to 1/5 point.</span></span>
-   <span data-ttu-id="7f560-167">`coordorigin="-500,-500"` определяет верхний левый угол содержащего поля, чтобы он был "-500,-500".</span><span class="sxs-lookup"><span data-stu-id="7f560-167">`coordorigin="-500,-500"` defines the top left corner of the containing box to be "-500, -500".</span></span> <span data-ttu-id="7f560-168">Таким образом, система координат внутри содержащего поля находится в диапазоне от-500 до 500 вдоль оси x, а-500 — в 500 вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="7f560-168">Therefore, the coordinate system inside the containing box ranges from -500 to 500 along the x-axis, and -500 to 500 along the y-axis.</span></span> <span data-ttu-id="7f560-169">Иными словами, центр содержащего поля имеет значение «0, 0».</span><span class="sxs-lookup"><span data-stu-id="7f560-169">In other words, the center of the containing box is "0, 0".</span></span>
-   <span data-ttu-id="7f560-170">`<v:oval style='... width:400;height:300;'>` Определяет размер содержащего поля для красного овала в 400 единиц (ширина) на 300 единиц (высота).</span><span class="sxs-lookup"><span data-stu-id="7f560-170">`<v:oval style='... width:400;height:300;'>` defines the size of the containing box for the red oval to be 400 units (width) by 300 units (height).</span></span> <span data-ttu-id="7f560-171">Поскольку одна единица в локальном пространстве координат эквивалентна 1/5 точке, размер содержащего его бокса для красного овала составляет 80 точек (ширина) на 60 пунктов (высота).</span><span class="sxs-lookup"><span data-stu-id="7f560-171">Because one unit in the Local Coordinate Space is equivalent to 1/5 point, the size of the containing box for the red oval is 80 points (width) by 60 points (height).</span></span>

<span data-ttu-id="7f560-172">Аналогичным образом, размер содержащего поля для зеленого раундрект — 50 точек (ширина) на 40 пунктов (высота).</span><span class="sxs-lookup"><span data-stu-id="7f560-172">Similarly, the size of the containing box for the green roundrect is 50 points (width) by 40 points (height).</span></span>

<span data-ttu-id="7f560-173">Если нужно изменить размер красного овала и зеленого раундрект, просто измените `<v:group style='... width:200pt;height:200pt;'>` .</span><span class="sxs-lookup"><span data-stu-id="7f560-173">When you want to to resize both the red oval and the green roundrect, simply change `<v:group style='... width:200pt;height:200pt;'>`.</span></span> <span data-ttu-id="7f560-174">Это не обязательно изменять размер двух фигур отдельно.</span><span class="sxs-lookup"><span data-stu-id="7f560-174">That's it -- you don't have to individually change the size of the two shapes.</span></span>

<span data-ttu-id="7f560-175">Например, если изменить `<v:group style='... width:200pt;height:200pt;'>` на `<v:group style='... width:300pt;height:300pt;'>` , фигуры станут больше, как показано на следующем рисунке:</span><span class="sxs-lookup"><span data-stu-id="7f560-175">For example, if you change `<v:group style='... width:200pt;height:200pt;'>` to `<v:group style='... width:300pt;height:300pt;'>`, the shapes become larger, as shown in the following picture:</span></span>

![cord4.gif (943 байт)](images/cord4.gif)



<span data-ttu-id="7f560-177">Также обратите внимание, что фигуры расположены по-разному.</span><span class="sxs-lookup"><span data-stu-id="7f560-177">You'd also notice that the shapes are located differently.</span></span> <span data-ttu-id="7f560-178">Это обусловлено тем, что фигуры рисуются с "0, 0", который находится в центре содержащего поля.</span><span class="sxs-lookup"><span data-stu-id="7f560-178">This is because the shapes are drawn from "0, 0" which is located at the center of the containing box.</span></span> <span data-ttu-id="7f560-179">Так как размер содержащего его поля больше, также перемещается центр содержащего поля.</span><span class="sxs-lookup"><span data-stu-id="7f560-179">Because you make the containing box bigger, the center of the containing box is also moved.</span></span>

<span data-ttu-id="7f560-180">Если изменить `coordorigin="-500,-500"` на `coordorigin="0,0"` , как показано на следующем рисунке, то красный овал и зеленый раундрект сдвигаются в новое место.</span><span class="sxs-lookup"><span data-stu-id="7f560-180">If you change `coordorigin="-500,-500"` to `coordorigin="0,0"`, as shown in the following picture, you'll notice that the red oval and the green roundrect are both shifted up to the new location.</span></span> <span data-ttu-id="7f560-181">Это происходит потому, что "0, 0" теперь находится в левом верхнем углу содержащего поля.</span><span class="sxs-lookup"><span data-stu-id="7f560-181">This is because "0, 0" now locates at the top left corner of the containing box.</span></span>

![cord5.gif (648 байт)](images/cord5.gif)



<span data-ttu-id="7f560-183">Также важно отметить, что содержащий поле не создает область отсечения.</span><span class="sxs-lookup"><span data-stu-id="7f560-183">It is also important to note that the containing box does not establish a clipping region.</span></span> <span data-ttu-id="7f560-184">Графические объекты могут отображаться за пределами границ содержащего поля.</span><span class="sxs-lookup"><span data-stu-id="7f560-184">Graphics may be drawn outside the boundaries of the containing box.</span></span> <span data-ttu-id="7f560-185">Содержащее поле просто служит для отображения локального пространства координат в пространстве страницы.</span><span class="sxs-lookup"><span data-stu-id="7f560-185">The containing box merely serves to map the local coordinate space to the page space.</span></span>

<span data-ttu-id="7f560-186">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span><span class="sxs-lookup"><span data-stu-id="7f560-186">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span></span>

 

 