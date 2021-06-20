---
title: Рисование базовых фигур
description: В этой статье описывается рисование базовых фигур в VML, что является устаревшим компонентом Windows Internet Explorer 9.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Веб-семинар, Рисование фигур
- Разработка веб-страниц, Рисование фигур
- Язык VML (VML), Рисование фигур
- VML (язык VML), Рисование фигур
- Векторная графика, Рисование фигур
- рисование фигур
- Фигуры VML, рисование
- Язык VML (VML), XML
- VML (язык VML), XML
- Векторная графика, XML
- Язык VML (VML), CSS2
- VML (язык VML), CSS2
- Векторная графика, CSS2
- Язык VML (VML), элементы
- VML (язык VML), элементы
- Векторная графика, элементы
- Элементы VML, Рисование фигур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00701e8ac77bd5bda7156c04ca25427d131646bf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407737"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="5c9ce-120">Рисование базовых фигур</span><span class="sxs-lookup"><span data-stu-id="5c9ce-120">Drawing Basic Shapes</span></span>

<span data-ttu-id="5c9ce-121">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5c9ce-122">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5c9ce-123">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5c9ce-124">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5c9ce-125">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5c9ce-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5c9ce-126">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5c9ce-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5c9ce-127">В этом разделе мы продемонстрируем, как легко нарисовать фигуру с помощью VML.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-127">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="5c9ce-128">Чтобы создать красный овал на веб-странице, как показано на следующем рисунке, можно нарисовать овал с помощью графического средства редактирования, сохранить рисунок в виде точечного рисунка, а затем вставить точечный рисунок на веб-страницу:</span><span class="sxs-lookup"><span data-stu-id="5c9ce-128">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 байт)](images/oval1.gif)

<span data-ttu-id="5c9ce-130">Кроме того, для рисования графики можно использовать VML.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-130">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="5c9ce-131">В предыдущем примере можно ввести следующие строки в `<BODY>` области веб-страницы, чтобы нарисовать красный овал:</span><span class="sxs-lookup"><span data-stu-id="5c9ce-131">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="5c9ce-132">`<v:...>` и `</v:...>` являются открывающим и закрывающим тегами в [синтаксисе XML](#xml-structure).`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="5c9ce-132">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="5c9ce-133">предоставляет [сведения CSS](#css-information).</span><span class="sxs-lookup"><span data-stu-id="5c9ce-133">provides [CSS information](#css-information).</span></span> <span data-ttu-id="5c9ce-134">**овал** и **FillColor**= "Red" являются [элементами VML](#vml-elements).</span><span class="sxs-lookup"><span data-stu-id="5c9ce-134">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="5c9ce-135">Вы можете изменить графику, просто изменив их атрибуты свойств в VML.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-135">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="5c9ce-136">В предыдущем примере, если изменить `fillcolor="red"` на `fillcolor="blue"` , как показано в следующем представлении VML, красный овал изменится на синий:</span><span class="sxs-lookup"><span data-stu-id="5c9ce-136">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="5c9ce-137">Браузеры, поддерживающие VML, могут визуализировать и отображать графику, представленную в формате VML, без необходимости загружать отдельные файлы изображений.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-137">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="5c9ce-138">Большинство изображений, представленных в формате VML, отображаются быстрее в браузерах и требует меньше места на диске и времени загрузки.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-138">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="5c9ce-139">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="5c9ce-139">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="5c9ce-140">Структура XML</span><span class="sxs-lookup"><span data-stu-id="5c9ce-140">XML Structure</span></span>

<span data-ttu-id="5c9ce-141">Формат VML форматируется в соответствии с правилами язык XML (XML).</span><span class="sxs-lookup"><span data-stu-id="5c9ce-141">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="5c9ce-142">Любой стандартный синтаксический анализатор XML может проанализировать VML и передать полученные данные в процессор, относящийся к VML.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-142">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="5c9ce-143">Чтобы обозреватели могли передавать данные в процессор, характерный для VML, необходимо ввести некоторую информацию, например [пространства имен](web-workshop---how-to-use-vml-on-web-pages----appendix.md) и [внедренные пользовательские объекты](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span><span class="sxs-lookup"><span data-stu-id="5c9ce-143">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="5c9ce-144">Затем можно использовать VML для ввода графики в регион точно так же, `<BODY>` как в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-144">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="5c9ce-145">`"v:"`Префикс для каждого XML-тега определяет тег как VML.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-145">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="5c9ce-146">`"v:"`Префикс в `<BODY>` регионе должен соответствовать `<html xmlns:v="...">` .</span><span class="sxs-lookup"><span data-stu-id="5c9ce-146">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="5c9ce-147">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="5c9ce-147">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="5c9ce-148">Сведения CSS</span><span class="sxs-lookup"><span data-stu-id="5c9ce-148">CSS Information</span></span>

<span data-ttu-id="5c9ce-149">VML использует [каскадные таблицы стилей, уровень 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) для определения размера графика и размещения графики на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-149">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="5c9ce-150">В предыдущем примере мы указали размер овала как 100 точек (ширина) на 75 точек (высота) ( `style='width:100pt;height:75pt'` ).</span><span class="sxs-lookup"><span data-stu-id="5c9ce-150">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="5c9ce-151">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="5c9ce-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="5c9ce-152">Элементы VML</span><span class="sxs-lookup"><span data-stu-id="5c9ce-152">VML Elements</span></span>

<span data-ttu-id="5c9ce-153">В предыдущем примере мы использовали предварительно определенный элемент VML `<oval>` для рисования овала.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-153">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="5c9ce-154">Затем мы использовали атрибут свойства **FillColor** `<oval>` элемента для заполнения овала красным.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-154">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="5c9ce-155">В соответствии с разделом " [Начало-Теги", "конечные теги" и "теги Empty-Element](https://www.w3.org/TR/REC-xml#sec-starttags) " [спецификации XML 1,0](https://www.w3.org/TR/REC-xml), Теги пустых элементов могут использоваться для любого элемента, не имеющего содержимого.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-155">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="5c9ce-156">Например, как показано в следующем представлении VML, в элементе нет содержимого (вложенного элемента) `<oval>` .</span><span class="sxs-lookup"><span data-stu-id="5c9ce-156">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="5c9ce-157">(Обратите внимание, что **Style** и **FillColor** являются атрибутами `<oval>` элемента; они не являются вложенными элементами.)</span><span class="sxs-lookup"><span data-stu-id="5c9ce-157">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="5c9ce-158">Таким образом, можно использовать тег пустого элемента, как показано в следующем представлении VML, для представления того же результата, что и в приведенной выше строке.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-158">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="5c9ce-159">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="5c9ce-159">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="5c9ce-160">Итоги</span><span class="sxs-lookup"><span data-stu-id="5c9ce-160">Summary</span></span>

<span data-ttu-id="5c9ce-161">С помощью VML можно рисовать графики на веб-странице, а затем настраивать эти изображения, просто изменяя их атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-161">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="5c9ce-162">Кроме того, большинство графических изображений, представленных в формате VML, отображаются быстрее в браузерах, а время загрузки и место на диске занимают меньше места.</span><span class="sxs-lookup"><span data-stu-id="5c9ce-162">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 