---
title: Основные типы VML
description: В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Перенесите веб-страницы и приложения, использующие VML, в SVG или другие широко поддерживаемые стандарты.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Язык VML (VML), основные типы
- VML (язык VML), основные типы
- Векторная графика, базовые типы VML
- Язык VML (VML), типы
- VML (язык VML), типы
- Векторная графика, типы VML
- базовые типы VML
- логический тип
- Тип дробной части
- Тип оси ординат
- Тип длины
- Тип меры
- тип угла
- Тип цвета
- тип шрифта
- Тип точечного рисунка
- векторные типы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05b058c919496b608b875f96e6c03bbeb0d50e8
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104560614"
---
# <a name="basic-vml-types"></a><span data-ttu-id="7b2c2-121">Основные типы VML</span><span class="sxs-lookup"><span data-stu-id="7b2c2-121">Basic VML Types</span></span>

<span data-ttu-id="7b2c2-122">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7b2c2-123">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7b2c2-124">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7b2c2-125">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7b2c2-126">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7b2c2-127">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7b2c2-128">**Contents**</span><span class="sxs-lookup"><span data-stu-id="7b2c2-128">**Contents**</span></span>

-   [<span data-ttu-id="7b2c2-129">Введение</span><span class="sxs-lookup"><span data-stu-id="7b2c2-129">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="7b2c2-130">boolean</span><span class="sxs-lookup"><span data-stu-id="7b2c2-130">boolean</span></span>](#boolean)
-   [<span data-ttu-id="7b2c2-131">дробь</span><span class="sxs-lookup"><span data-stu-id="7b2c2-131">fraction</span></span>](#fraction)
-   [<span data-ttu-id="7b2c2-132">ординат</span><span class="sxs-lookup"><span data-stu-id="7b2c2-132">ordinate</span></span>](#ordinate)
-   [<span data-ttu-id="7b2c2-133">length</span><span class="sxs-lookup"><span data-stu-id="7b2c2-133">length</span></span>](#length)
    -   [<span data-ttu-id="7b2c2-134">Альтернативные представления</span><span class="sxs-lookup"><span data-stu-id="7b2c2-134">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="7b2c2-135">мер</span><span class="sxs-lookup"><span data-stu-id="7b2c2-135">measure</span></span>](#measure)
    -   [<span data-ttu-id="7b2c2-136">Альтернативные представления</span><span class="sxs-lookup"><span data-stu-id="7b2c2-136">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="7b2c2-137">angle</span><span class="sxs-lookup"><span data-stu-id="7b2c2-137">angle</span></span>](#angle)
    -   [<span data-ttu-id="7b2c2-138">Альтернативные представления</span><span class="sxs-lookup"><span data-stu-id="7b2c2-138">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="7b2c2-139">color</span><span class="sxs-lookup"><span data-stu-id="7b2c2-139">color</span></span>](#color)
    -   [<span data-ttu-id="7b2c2-140">Единицы цвета</span><span class="sxs-lookup"><span data-stu-id="7b2c2-140">Color units</span></span>](#color-units)
    -   [<span data-ttu-id="7b2c2-141">Цвета HTML</span><span class="sxs-lookup"><span data-stu-id="7b2c2-141">HTML colors</span></span>](#html-colors)
    -   [<span data-ttu-id="7b2c2-142">Цвета схемы</span><span class="sxs-lookup"><span data-stu-id="7b2c2-142">Scheme colors</span></span>](#scheme-colors)
    -   [<span data-ttu-id="7b2c2-143">Системные цвета</span><span class="sxs-lookup"><span data-stu-id="7b2c2-143">System colors</span></span>](#system-colors)
    -   [<span data-ttu-id="7b2c2-144">Чистые цвета</span><span class="sxs-lookup"><span data-stu-id="7b2c2-144">Pure colors</span></span>](#pure-colors)
    -   [<span data-ttu-id="7b2c2-145">Корректировки цвета</span><span class="sxs-lookup"><span data-stu-id="7b2c2-145">Color adjustments</span></span>](#color-adjustments)
-   [<span data-ttu-id="7b2c2-146">шрифтов</span><span class="sxs-lookup"><span data-stu-id="7b2c2-146">font</span></span>](#font)
-   [<span data-ttu-id="7b2c2-147">bitmap</span><span class="sxs-lookup"><span data-stu-id="7b2c2-147">bitmap</span></span>](#bitmap)
    -   [<span data-ttu-id="7b2c2-148">Форматы файлов изображений</span><span class="sxs-lookup"><span data-stu-id="7b2c2-148">Picture file formats</span></span>](#picture-file-formats)
-   [<span data-ttu-id="7b2c2-149">уязвимо</span><span class="sxs-lookup"><span data-stu-id="7b2c2-149">vector</span></span>](#vector)

## <a name="introduction"></a><span data-ttu-id="7b2c2-150">Введение</span><span class="sxs-lookup"><span data-stu-id="7b2c2-150">Introduction</span></span>

<span data-ttu-id="7b2c2-151">В этом предложении используется небольшое количество базовых типов, перечисленных в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-151">This proposal uses a small number of basic types, listed in the table below.</span></span>



| <span data-ttu-id="7b2c2-152">Тип</span><span class="sxs-lookup"><span data-stu-id="7b2c2-152">Type</span></span>                  | <span data-ttu-id="7b2c2-153">Элемент</span><span class="sxs-lookup"><span data-stu-id="7b2c2-153">Element</span></span>           | <span data-ttu-id="7b2c2-154">Фундаментальное представление</span><span class="sxs-lookup"><span data-stu-id="7b2c2-154">Fundamental Representation</span></span> | <span data-ttu-id="7b2c2-155">Описание</span><span class="sxs-lookup"><span data-stu-id="7b2c2-155">Description</span></span>                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b2c2-156">boolean</span><span class="sxs-lookup"><span data-stu-id="7b2c2-156">boolean</span></span>](#boolean)   |                   | <span data-ttu-id="7b2c2-157">1 бит</span><span class="sxs-lookup"><span data-stu-id="7b2c2-157">1 bit</span></span>                      | <span data-ttu-id="7b2c2-158">Логическое значение: true или false.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-158">A boolean value: true or false.</span></span>                                                                      |
| [<span data-ttu-id="7b2c2-159">дробь</span><span class="sxs-lookup"><span data-stu-id="7b2c2-159">fraction</span></span>](#fraction) |                   | <span data-ttu-id="7b2c2-160">номер 2 6</span><span class="sxs-lookup"><span data-stu-id="7b2c2-160">number 2 6</span></span>                 | <span data-ttu-id="7b2c2-161">Числовое значение, масштабируемое по 2 6 (65536) и хранящееся в виде целого числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-161">A numeric value, scaled by 2 6 (65536) and stored as a signed integer.</span></span>                               |
| [<span data-ttu-id="7b2c2-162">ординат</span><span class="sxs-lookup"><span data-stu-id="7b2c2-162">ordinate</span></span>](#ordinate) |                   | <span data-ttu-id="7b2c2-163">30-разрядное целое число, знак плюс</span><span class="sxs-lookup"><span data-stu-id="7b2c2-163">30-bit integer plus sign</span></span>   | <span data-ttu-id="7b2c2-164">Часть координат (например, в пути) — значения, определенные параметром курд.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-164">Part of a coordinate (e.g., in a path ), the values defined by coord.</span></span>                                |
| [<span data-ttu-id="7b2c2-165">length</span><span class="sxs-lookup"><span data-stu-id="7b2c2-165">length</span></span>](#length)     |                   | [<span data-ttu-id="7b2c2-166">ВХОДЯЩЕЙ</span><span class="sxs-lookup"><span data-stu-id="7b2c2-166">EMU</span></span>](#length)             | <span data-ttu-id="7b2c2-167">Физическая длина, например ширина линии или размер шрифта.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-167">A physical length, such as the width of a line or the size of a font.</span></span>                                |
| [<span data-ttu-id="7b2c2-168">мер</span><span class="sxs-lookup"><span data-stu-id="7b2c2-168">measure</span></span>](#measure)   |                   | <span data-ttu-id="7b2c2-169">ЕС или номер 2 6</span><span class="sxs-lookup"><span data-stu-id="7b2c2-169">EMU or number 2 6</span></span>          | <span data-ttu-id="7b2c2-170">Физическая длина, включая число пикселей устройства или часть другого количества.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-170">Either a physical length, including a number of device pixels, or a fraction of some other quantity.</span></span> |
| [<span data-ttu-id="7b2c2-171">angle</span><span class="sxs-lookup"><span data-stu-id="7b2c2-171">angle</span></span>](#angle)       |                   | <span data-ttu-id="7b2c2-172">градусы 2 6</span><span class="sxs-lookup"><span data-stu-id="7b2c2-172">degrees 2 6</span></span>                | <span data-ttu-id="7b2c2-173">Угол; положительный — по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-173">An angle; positive is clockwise.</span></span>                                                                     |
| [<span data-ttu-id="7b2c2-174">color</span><span class="sxs-lookup"><span data-stu-id="7b2c2-174">color</span></span>](#color)       | [<span data-ttu-id="7b2c2-175">c</span><span class="sxs-lookup"><span data-stu-id="7b2c2-175">c</span></span>](#color)       | <span data-ttu-id="7b2c2-176">complex</span><span class="sxs-lookup"><span data-stu-id="7b2c2-176">complex</span></span>                    | <span data-ttu-id="7b2c2-177">Элемент, допускающий наследование цвета.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-177">An element that allows a color to be derived.</span></span>                                                        |
| [<span data-ttu-id="7b2c2-178">шрифтов</span><span class="sxs-lookup"><span data-stu-id="7b2c2-178">font</span></span>](#font)         | [<span data-ttu-id="7b2c2-179">шрифтов</span><span class="sxs-lookup"><span data-stu-id="7b2c2-179">font</span></span>](#font)     | <span data-ttu-id="7b2c2-180">complex</span><span class="sxs-lookup"><span data-stu-id="7b2c2-180">complex</span></span>                    | <span data-ttu-id="7b2c2-181">Описание шрифта.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-181">A description of a font.</span></span>                                                                             |
| [<span data-ttu-id="7b2c2-182">bitmap</span><span class="sxs-lookup"><span data-stu-id="7b2c2-182">bitmap</span></span>](#bitmap)     | [<span data-ttu-id="7b2c2-183">bitmap</span><span class="sxs-lookup"><span data-stu-id="7b2c2-183">bitmap</span></span>](#bitmap) | <span data-ttu-id="7b2c2-184">href</span><span class="sxs-lookup"><span data-stu-id="7b2c2-184">href</span></span>                       | <span data-ttu-id="7b2c2-185">Ссылка на внешний файл изображения.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-185">A reference to an external picture file.</span></span>                                                             |
| [<span data-ttu-id="7b2c2-186">уязвимо</span><span class="sxs-lookup"><span data-stu-id="7b2c2-186">vector</span></span>](#vector)     | [<span data-ttu-id="7b2c2-187">3,3</span><span class="sxs-lookup"><span data-stu-id="7b2c2-187">v</span></span>](#vector)      | <span data-ttu-id="7b2c2-188">complex</span><span class="sxs-lookup"><span data-stu-id="7b2c2-188">complex</span></span>                    | <span data-ttu-id="7b2c2-189">Описание векторного пути</span><span class="sxs-lookup"><span data-stu-id="7b2c2-189">A description of a vector path</span></span>                                                                       |



 

<span data-ttu-id="7b2c2-190">«Фундаментальное представление» — это представление с наибольшим значением точности, которое требуется для реализации предложения для поддержки. данные будут потеряны, если реализация не сможет представить данные для требуемой точности.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-190">The "fundamental representation" is the highest precision representation that the proposal requires a conforming implementation to maintain; data will be lost if the implementation is not able to represent the data to the precision required.</span></span> <span data-ttu-id="7b2c2-191">Типы цвета, шрифта и вектора соответствуют элементам, которые сами по себе имеют структуру, но не являются базовыми типами. Тем не менее, в рамках этого предложения удобно обрабатывать их.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-191">The color, font, and vector types correspond to elements which themselves have structure -- in a sense, they are not basic types; however, it is convenient to treat them as such within this proposal.</span></span>

<span data-ttu-id="7b2c2-192">Каждый несложный базовый тип имеет связанный элемент с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-192">Each non-complex basic type has an associated element of the same name.</span></span> <span data-ttu-id="7b2c2-193">Эти имена элементов зарезервированы и не могут использоваться для других целей в расширениях, даже если они используются в элементе Extension \ View = «Skip».</span><span class="sxs-lookup"><span data-stu-id="7b2c2-193">These element names are reserved and may not be used for any other purpose within extensions, even if the use is within an onview="skip" extension element.</span></span> <span data-ttu-id="7b2c2-194">По этой причине реализация, которая встречает неизвестный XML-код, может обеспечить эффективное внутреннее хранение неизвестного XML, если значения заключены в элементы "Type".</span><span class="sxs-lookup"><span data-stu-id="7b2c2-194">Because of this, it is possible for an implementation that encounters unknown XML to provide efficient internal storage of the unknown XML as long as the values are enclosed in the "type" elements.</span></span>


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



<span data-ttu-id="7b2c2-195">В первом примере строка "1,578" должна храниться как последовательность символов (реализация не знает, является ли она строкой или числом); во втором примере элемент дробь указывает, что содержимое является числом, поэтому его можно преобразовать в представление дробной части высокой точности.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-195">In the first example above, the string "1.578" must be stored as a sequence of characters (the implementation does not know whether it is a string or a number); in the second example, the fraction element indicates that the content is a number, thus it may be converted to the high precision fraction representation.</span></span>

<span data-ttu-id="7b2c2-196">Сложные типы (включая точечные рисунки) имеют связанные имена элементов, которые используются для разделения значения.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-196">Complex types (including bitmap) have associated element names that are used to delimit the value.</span></span> <span data-ttu-id="7b2c2-197">Это упрощает синтаксический анализ, гарантируя, что более сложные задачи анализа связаны с уникальными тегами элементов.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-197">This simplifies parsing by ensuring that the more complex parsing tasks are associated with unique element tags.</span></span>

<span data-ttu-id="7b2c2-198">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-198">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="boolean"></a><span data-ttu-id="7b2c2-199">Логическое</span><span class="sxs-lookup"><span data-stu-id="7b2c2-199">boolean</span></span>


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="7b2c2-200">Логическое значение представлено в виде ключевого слова, указывающего состояние флага.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-200">A boolean value is represented as a keyword indicating the state of the flag.</span></span> <span data-ttu-id="7b2c2-201">Определены следующие ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-201">The following keywords are defined.</span></span>



| <span data-ttu-id="7b2c2-202">Значение true</span><span class="sxs-lookup"><span data-stu-id="7b2c2-202">Value for true</span></span> | <span data-ttu-id="7b2c2-203">Значение для false</span><span class="sxs-lookup"><span data-stu-id="7b2c2-203">Value for false</span></span> |
|----------------|-----------------|
| <span data-ttu-id="7b2c2-204">true</span><span class="sxs-lookup"><span data-stu-id="7b2c2-204">true</span></span>           | <span data-ttu-id="7b2c2-205">false</span><span class="sxs-lookup"><span data-stu-id="7b2c2-205">false</span></span>           |
| <span data-ttu-id="7b2c2-206">да</span><span class="sxs-lookup"><span data-stu-id="7b2c2-206">yes</span></span>            | <span data-ttu-id="7b2c2-207">Нет</span><span class="sxs-lookup"><span data-stu-id="7b2c2-207">no</span></span>              |
| <span data-ttu-id="7b2c2-208">on</span><span class="sxs-lookup"><span data-stu-id="7b2c2-208">on</span></span>             | <span data-ttu-id="7b2c2-209">off</span><span class="sxs-lookup"><span data-stu-id="7b2c2-209">off</span></span>             |
| <span data-ttu-id="7b2c2-210">t</span><span class="sxs-lookup"><span data-stu-id="7b2c2-210">t</span></span>              | <span data-ttu-id="7b2c2-211">f</span><span class="sxs-lookup"><span data-stu-id="7b2c2-211">f</span></span>               |
| <span data-ttu-id="7b2c2-212">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-212">1</span></span>              | <span data-ttu-id="7b2c2-213">0</span><span class="sxs-lookup"><span data-stu-id="7b2c2-213">0</span></span>               |



 

<span data-ttu-id="7b2c2-214">Реализация может записывать любое значение и должно распознавать все значения.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-214">An implementation may write any value and must recognize all values.</span></span> <span data-ttu-id="7b2c2-215">Реализация позволяет изменять значения из одного представления на другое.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-215">An implementation is free to change values from one representation to another.</span></span>

<span data-ttu-id="7b2c2-216">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-216">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="fraction"></a><span data-ttu-id="7b2c2-217">дробь</span><span class="sxs-lookup"><span data-stu-id="7b2c2-217">fraction</span></span>


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="7b2c2-218">Все числовые значения (т. е. значения количества безразмерности) в этом предложении могут храниться в виде целых чисел путем их масштабирования на 2 6 (65536).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-218">All numeric values (i.e., values of dimensionless quantities) within this proposal can be stored as integers by scaling them by 2  6 (65536).</span></span> <span data-ttu-id="7b2c2-219">Число может быть задано в этой форме с суффиксом f или десятичным числом без суффикса.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-219">A number may be given either in this form, with the suffix f or as a decimal number with no suffix.</span></span> <span data-ttu-id="7b2c2-220">Таким же значением являются следующие гипотетические элементы, представляющие одно и то же значение.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-220">Thus, the following hypothetical elements represent the same value.</span></span>


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



<span data-ttu-id="7b2c2-221">Количество с суффиксом f должно быть целым числом. дробные числа не допускаются.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-221">A quantity with the f suffix must be a whole number; fractional numbers are not permitted.</span></span> <span data-ttu-id="7b2c2-222">Результирующее целое число должно быть представлено как номер, дополненный 32-разрядным числом знаков дополнения. Таким же эффективным диапазоном представления будет 32768 (фактически, меньше 32768 и больше или равно-32768).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-222">The resultant integer must be representable as a 32-bit 2's complement signed number; thus, the effective range of the representation is  32768 (in fact, less than 32768 and greater than or equal to -32768.)</span></span>

<span data-ttu-id="7b2c2-223">Для сохранения значений, выраженных в виде значений f, требуется согласованная реализация.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-223">A conforming implementation is required to preserve values that are expressed as f values.</span></span> <span data-ttu-id="7b2c2-224">Значения, представленные в виде десятичных чисел, можно преобразовать в значение f и сохранить таким образом.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-224">Values represented as decimal numbers may be converted to an f value and stored that way.</span></span> <span data-ttu-id="7b2c2-225">Приложению разрешено записывать внутренние значения в любую соответствующую единицу; Однако значение, считанное из существующего документа, должно либо поддерживаться с полной исходной точностью, либо преобразовываться в значение f.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-225">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an f value.</span></span>

<span data-ttu-id="7b2c2-226">Если реализация не может сделать это, пользователь должен предупредить пользователя о том, что данные могут быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-226">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="7b2c2-227">(При первом обнаружении данных, созданных извне, допустимо выдать такое предупреждение.)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-227">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="7b2c2-228">При преобразовании десятичного значения в формат f реализация может использовать любой арифметический режим округления. Однако целое число должно быть полностью преобразовано в формат f.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-228">When a decimal value is converted into f format, the implementation may use any arithmetic rounding mode; however, a whole number must be converted to the f format exactly.</span></span> <span data-ttu-id="7b2c2-229">Рекомендуется, чтобы реализации преобразовываются путем округления до минус бесконечности и что преобразование всегда будет точным.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-229">It is recommended that implementations convert by rounding to minus infinity and that the convertion always be exact.</span></span>

<span data-ttu-id="7b2c2-230">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-230">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="ordinate"></a><span data-ttu-id="7b2c2-231">ординат</span><span class="sxs-lookup"><span data-stu-id="7b2c2-231">ordinate</span></span>


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="7b2c2-232">Модули системы координат, установленные курд, имеют определенный номинальный тип, который называется ординатой.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-232">The units of the coordinate system established by coord are of some nominal type, which is referred to as ordinate.</span></span> <span data-ttu-id="7b2c2-233">Это мера длины, но она используется только в отношении прямоугольника, установленного курд.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-233">This is a measure of length, but it is only used in relation to the rectangle that coord establishes.</span></span> <span data-ttu-id="7b2c2-234">Любое значение типа ординат будет масштабироваться по значениям *w* и *h* курд и полученному соотношением, используемому для установления реального измерения на выходном устройстве.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-234">Any value of type ordinate will be scaled by the *w* and *h* values of the coord and the resulting ratio used to establish a real measurement on the output device.</span></span>

<span data-ttu-id="7b2c2-235">Согласованная реализация должна иметь возможность обрабатывать значения координат до 30 бит плюс знак (т. е. 31-разрядное целое число со знаком, а не 32-разрядное целое число со знаком).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-235">A conforming implementation must be able to handle ordinate values of up to 30 bits plus sign (i.e., a 31-bit signed integer, not a 32-bit signed integer).</span></span> <span data-ttu-id="7b2c2-236">Однако рекомендуется, чтобы реализации предпринимали координаты для пути и похожих элементов, имеющих около 16 бит точности.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-236">It is recommended, however, that implementations attempt to produce coordinates for path and similar elements that have about 16 bits of precision.</span></span> <span data-ttu-id="7b2c2-237">Это снизит вероятность невозможности потери или переполнения в несогласованной реализации.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-237">This will minimize the chance of either underflow or overflow in a non-conforming implementation.</span></span>

<span data-ttu-id="7b2c2-238">значения ординат всегда являются целыми.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-238">ordinate values are always integral.</span></span> <span data-ttu-id="7b2c2-239">Десятичная точка может не отображаться в значении типа ординат.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-239">A decimal point may not appear in a value of type ordinate.</span></span> <span data-ttu-id="7b2c2-240">Спецификаторы единиц измерения не могут быть добавлены к значениям типа ординат.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-240">No unit specifiers may be appended to values of type ordinate.</span></span>

<span data-ttu-id="7b2c2-241">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-241">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="length"></a><span data-ttu-id="7b2c2-242">length</span><span class="sxs-lookup"><span data-stu-id="7b2c2-242">length</span></span>


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="7b2c2-243">Длина является реальным измерением или, иногда, измерением в пикселях устройства.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-243">A length is a real-world measurement or, sometimes, a measurement in device pixels.</span></span> <span data-ttu-id="7b2c2-244">Рекомендуется избегать использования пикселов устройства (ПКС) в реализациях.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-244">It is recommended that implementations avoid the use of device pixels (px).</span></span>

<span data-ttu-id="7b2c2-245">Все стандартные квалификаторы единиц [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) разрешены для длины.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-245">All the standard [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) unit qualifiers are permitted on a length.</span></span> <span data-ttu-id="7b2c2-246">Кроме того, можно использовать квалификаторы Европейского союза.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-246">In addition, the qualifier emu may be used.</span></span> <span data-ttu-id="7b2c2-247">Этот квалификатор относится к единице — ЕС (единица измерения "Английский (англ.)") — это общий знаменатель количественных показателей измерений, широко используемых в компьютерной графике.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-247">This qualifier refers to a unit -- the EMU (English Metric Unit) -- which is a common denominator of the measurement quantities in widespread use in computer graphics.</span></span> <span data-ttu-id="7b2c2-248">ЕС составляет <sup>дюймы</sup> и 914400, т. е. для каждого дюйма имеется 914400 ЕС.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-248">The EMU is <sup>inch</sup> / 914400, i.e., there are 914400 EMU per inch.</span></span> <span data-ttu-id="7b2c2-249">В следующей таблице приведено количество Емус в небольшом количестве часто встречающихся единиц.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-249">The following table lists the number of EMUs in a small number of commonly encountered units.</span></span>



| <span data-ttu-id="7b2c2-250">Число Емус</span><span class="sxs-lookup"><span data-stu-id="7b2c2-250">Number of EMUs</span></span> | <span data-ttu-id="7b2c2-251">Число на дюйм</span><span class="sxs-lookup"><span data-stu-id="7b2c2-251">Number per Inch</span></span> | <span data-ttu-id="7b2c2-252">Число на миллиметр</span><span class="sxs-lookup"><span data-stu-id="7b2c2-252">Number per Millimeter</span></span> | <span data-ttu-id="7b2c2-253">Описание</span><span class="sxs-lookup"><span data-stu-id="7b2c2-253">Description</span></span>             |
|----------------|-----------------|-----------------------|-------------------------|
| <span data-ttu-id="7b2c2-254">360</span><span class="sxs-lookup"><span data-stu-id="7b2c2-254">360</span></span>            |                 | <span data-ttu-id="7b2c2-255">0,01</span><span class="sxs-lookup"><span data-stu-id="7b2c2-255">0.01</span></span>                  | <span data-ttu-id="7b2c2-256">HIMETRIC Win32</span><span class="sxs-lookup"><span data-stu-id="7b2c2-256">Win32 HIMETRIC</span></span>          |
| <span data-ttu-id="7b2c2-257">12700</span><span class="sxs-lookup"><span data-stu-id="7b2c2-257">12700</span></span>          | <span data-ttu-id="7b2c2-258">72</span><span class="sxs-lookup"><span data-stu-id="7b2c2-258">72</span></span>              |                       | <span data-ttu-id="7b2c2-259">точки</span><span class="sxs-lookup"><span data-stu-id="7b2c2-259">"point"</span></span>                 |
| <span data-ttu-id="7b2c2-260">635</span><span class="sxs-lookup"><span data-stu-id="7b2c2-260">635</span></span>            | <span data-ttu-id="7b2c2-261">1440</span><span class="sxs-lookup"><span data-stu-id="7b2c2-261">1440</span></span>            |                       | <span data-ttu-id="7b2c2-262">Win32 ТВИПОВ</span><span class="sxs-lookup"><span data-stu-id="7b2c2-262">Win32 TWIP</span></span>              |
| <span data-ttu-id="7b2c2-263">762</span><span class="sxs-lookup"><span data-stu-id="7b2c2-263">762</span></span>            | <span data-ttu-id="7b2c2-264">1200</span><span class="sxs-lookup"><span data-stu-id="7b2c2-264">1200</span></span>            |                       | <span data-ttu-id="7b2c2-265">Принтер с высоким разрешением</span><span class="sxs-lookup"><span data-stu-id="7b2c2-265">High-resolution printer</span></span> |



 

<span data-ttu-id="7b2c2-266">Дробное число Емус не разрешено.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-266">Fractional numbers of EMUs are not permitted.</span></span> <span data-ttu-id="7b2c2-267">Любое измерение должно быть представлено как 32-разрядное целое число со знаком Емус--это ограничивает величину измерения до 2348 дюймов — около 59 метров или 65 метра.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-267">Any measurement must be representable as a 32-bit signed integral number of EMUs -- this limits the magnitude of a measurement to 2348 inches -- about 59 meters or 65 yards.</span></span> <span data-ttu-id="7b2c2-268">Поскольку измерения всегда ссылаются на размер отрисовки на устройстве вывода с номинальным экраном или на странице, они всегда будут находиться в пределах этого диапазона.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-268">Because the measurements always refer to the size of a rendering on a nominally screen- or page-sized output device, they will always be within this range.</span></span>

<span data-ttu-id="7b2c2-269">Однако обратите внимание, что представление не подходит для реальных измерений и где они записываются (например, для записи реального размера пути), необходимо использовать другое представление.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-269">Notice, however, that the representation is inappropriate for real-world measurements and that where these are recorded (for example, to record the real-world size of a path) some other representation must be used.</span></span>

<span data-ttu-id="7b2c2-270">Для сохранения значений, которые являются точным числом Емус, требуется согласованная реализация.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-270">A conforming implementation is required to preserve values that are exact numbers of EMUs.</span></span> <span data-ttu-id="7b2c2-271">Значения, представленные любым другим способом, могут быть преобразованы в значение ЕС и сохранены таким образом.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-271">Values represented in any other way may be converted to an EMU value and stored that way.</span></span> <span data-ttu-id="7b2c2-272">Приложению разрешено записывать внутренние значения в любую соответствующую единицу; Однако значение, считанное из существующего документа, должно либо поддерживаться с полной исходной точностью, либо должно быть преобразовано в значение ЕС.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-272">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an EMU value.</span></span>

<span data-ttu-id="7b2c2-273">Если реализация не может сделать это, пользователь должен предупредить пользователя о том, что данные могут быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-273">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="7b2c2-274">(При первом обнаружении данных, созданных извне, допустимо выдать такое предупреждение.)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-274">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="7b2c2-275">На практике физическая длина используется для относительно небольшого количества измерений в этом предложении.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-275">In practice, physical lengths are used for relatively few measurements in this proposal.</span></span> <span data-ttu-id="7b2c2-276">Данные, которые обычно наиболее важны, — это данные пути, которые кодируются в определенной системе координат для каждой фигуры по курд.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-276">The data which is normally most important is the path data and this is encoded in the coordinate system defined, on a per-shape basis, by coord.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="7b2c2-277">Альтернативные представления</span><span class="sxs-lookup"><span data-stu-id="7b2c2-277">Alternative representations</span></span>

<span data-ttu-id="7b2c2-278">Стандартные представления длины HTML определяются [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span><span class="sxs-lookup"><span data-stu-id="7b2c2-278">The standard length representations of HTML are defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span></span> <span data-ttu-id="7b2c2-279">Относительные единицы, за исключением пикселя, не имеют смысла в контексте, в котором длины используются в этом предложении и не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-279">Relative units, with the exception of the pixel, are not meaningful in the context within which lengths are used in this proposal and must not be used.</span></span> <span data-ttu-id="7b2c2-280">Если документ записывает предполагаемый (целевой) размер пикселя, он определяет перевод пикселов в ЕС; в противном случае следует использовать значение по умолчанию 90 dpi, определенное параметром [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span><span class="sxs-lookup"><span data-stu-id="7b2c2-280">If the document records the intended (target) pixel size, this defines the translation of pixels into EMU; otherwise, the default of 90 dpi defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) should be used.</span></span>

<span data-ttu-id="7b2c2-281">За исключением ЕС, любое значение может быть задано в виде десятичной дроби.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-281">With the exception of emu, any value may be given as a decimal fraction.</span></span> <span data-ttu-id="7b2c2-282">При преобразовании десятичного значения в ДЕНЕЖные знаки реализация может использовать любой арифметический режим округления.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-282">When a decimal value is converted to EMU, the implementation may use any arithmetic rounding mode.</span></span> <span data-ttu-id="7b2c2-283">(Единственным способом для создания приложения, гарантирующего определенный результат, является его указание в ЕС.)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-283">(The only way for an authoring application to guarantee a particular result is to specify it in emu.)</span></span>

<span data-ttu-id="7b2c2-284">Если в значении длины не указано ни одного описателя единиц измерения, реализация должна считаться ЕС.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-284">If no unit specifier is given in a length value, the implementation must assume emu.</span></span>

<span data-ttu-id="7b2c2-285">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-285">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="measure"></a><span data-ttu-id="7b2c2-286">measure</span><span class="sxs-lookup"><span data-stu-id="7b2c2-286">measure</span></span>


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="7b2c2-287">Мера — это количество, которое может быть либо [длиной](#length) , либо [дробной](#fraction).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-287">A measure is a quantity that may be either a [length](#length) or a [fraction](#fraction).</span></span> <span data-ttu-id="7b2c2-288">Это точно напоминает измерения длины HTML и CSS, которые во многих случаях могут быть либо физическими, либо процентами какого-либо другого количества.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-288">This closely resembles the HTML and CSS length measurements, which can, in many cases, either be physical measurements or percentages of some other quantity.</span></span> <span data-ttu-id="7b2c2-289">Если спецификатор единицы не указан, предполагается, что значение должно быть десятичной дробью (таким образом, это поведение наследуется от дробной части, а не от длины).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-289">If no unit specifier is given, the value must be assumed to be a decimal fraction (thus, this behavior is inherited from fraction, not from length.)</span></span>

<span data-ttu-id="7b2c2-290">В отличие от длины, значение пикселя имеет определенный контекст, поэтому преобразование в ЕС обычно не подходит.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-290">Unlike length, a pixel value has a context-defined meaning, so conversion to emu is normally inappropriate.</span></span> <span data-ttu-id="7b2c2-291">Существует три возможных фундаментальных представления, которые должна поддерживать реализация (т. е. одно представление не может быть преобразовано в другое без потери информации).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-291">There are three possible fundamental representations that the implementation must maintain (i.e., one representation cannot be converted into another without loss of information).</span></span>

1.  <span data-ttu-id="7b2c2-292">Дробное значение должно храниться в [дробном](#fraction) формате (значение f).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-292">A fractional value should be maintained in the [fraction](#fraction) format (an " f " value).</span></span>
2.  <span data-ttu-id="7b2c2-293">Физическая длина должна храниться в ЕС.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-293">A physical length should be maintained in EMU.</span></span>
3.  <span data-ttu-id="7b2c2-294">Значение пикселя должно поддерживаться целым числом пикселей.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-294">A pixel value should be maintained as a whole number of pixels.</span></span>

<span data-ttu-id="7b2c2-295">Дробное число пикселей не разрешено.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-295">Fractional numbers of pixels are not permitted.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="7b2c2-296">Альтернативные представления</span><span class="sxs-lookup"><span data-stu-id="7b2c2-296">Alternative representations</span></span>

<span data-ttu-id="7b2c2-297">Разрешены все альтернативные представления [дробной](#fraction) части и [длины](#length) .</span><span class="sxs-lookup"><span data-stu-id="7b2c2-297">All the alternate representations of both [fraction](#fraction) and [length](#length) are permitted.</span></span>

<span data-ttu-id="7b2c2-298">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-298">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="angle"></a><span data-ttu-id="7b2c2-299">angle</span><span class="sxs-lookup"><span data-stu-id="7b2c2-299">angle</span></span>


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="7b2c2-300">Фундаментальное представление угла — это число градусов, кратное 2 6 (65536) и хранящееся в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-300">The fundamental representation of an angle is a number of degrees multipled by 2 6 (65536) and stored as an integer.</span></span> <span data-ttu-id="7b2c2-301">Поскольку пространство координат инвертировано (отрицательная ось y не работает), угол по часовой стрелке положительный.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-301">Because the coordinate space is inverted (positive y axis is down), a clockwise angle is positive.</span></span> <span data-ttu-id="7b2c2-302">Для сохранения полной точности такого значения требуется согласованная реализация.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-302">A conforming implementation is required to preserve the full precision of such a value.</span></span>

<span data-ttu-id="7b2c2-303">Реализации разрешено использовать любой диапазон для углов и разрешается нормалисе угол (например, от-180 до + 180 или от 0 до 360).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-303">An implementation is permitted to use any range for angles and is permitted to normalise an angle (for example to -180  to +180  or 0 to 360 ).</span></span> <span data-ttu-id="7b2c2-304">Реализации не должны быть постоянными. Однако целочисленное представление угла не должно превышать диапазон 32-разрядного целого числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-304">Implementations are not required to be consistent; however, the integral representation of an angle must not exceed the range of a 32-bit signed integer.</span></span>

<span data-ttu-id="7b2c2-305">Суффикс демона используется для того, чтобы обозначить это представление угла (дробная степень).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-305">The suffix fd is used to identify this representation of an angle (fractional degree).</span></span> <span data-ttu-id="7b2c2-306">Обратите внимание, что это отличие от суффикса f для дробной части, хотя для его поддержки можно использовать идентичные арифметические операции.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-306">Notice that this is distinguished from the f suffix for a dimensionless fraction although identical arithmetic can be used to support it.</span></span> <span data-ttu-id="7b2c2-307">По умолчанию для углового значения используется простой градус, т. е. немасштабированное значение.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-307">The default for an angular value is simple degrees, i.e., an unscaled value.</span></span> <span data-ttu-id="7b2c2-308">Это также может подаваться с суффиксом "" (символ градуса); Однако использование этого параметра зависит от наличия подходящей кодировки документа, поэтому суффикс град также определяется как градусы.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-308">This may also be signalled with the suffix " " (the degree symbol); however, use of this depends on having a suitable document encoding -- consequently, the suffix deg is also defined to mean degrees.</span></span> <span data-ttu-id="7b2c2-309">Полный набор возможных допустимых вариантов приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-309">The full set of possible suffices are as follows.</span></span>



| <span data-ttu-id="7b2c2-310">Суффикс</span><span class="sxs-lookup"><span data-stu-id="7b2c2-310">Suffix</span></span>       | <span data-ttu-id="7b2c2-311">Коэффициент преобразования</span><span class="sxs-lookup"><span data-stu-id="7b2c2-311">Conversion Factor</span></span> | <span data-ttu-id="7b2c2-312">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b2c2-312">Comments</span></span>                               |
|--------------|-------------------|----------------------------------------|
| <span data-ttu-id="7b2c2-313">демо</span><span class="sxs-lookup"><span data-stu-id="7b2c2-313">fd</span></span>           | <span data-ttu-id="7b2c2-314">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-314">1</span></span>                 | <span data-ttu-id="7b2c2-315">Внутреннее представление высокой точности</span><span class="sxs-lookup"><span data-stu-id="7b2c2-315">High-precision internal representation</span></span> |
| <span data-ttu-id="7b2c2-316">нет, град,</span><span class="sxs-lookup"><span data-stu-id="7b2c2-316">none, deg,</span></span>   | <span data-ttu-id="7b2c2-317">65536</span><span class="sxs-lookup"><span data-stu-id="7b2c2-317">65536</span></span>             | <span data-ttu-id="7b2c2-318">Degrees</span><span class="sxs-lookup"><span data-stu-id="7b2c2-318">Degrees</span></span>                                |
| <span data-ttu-id="7b2c2-319">rad</span><span class="sxs-lookup"><span data-stu-id="7b2c2-319">rad</span></span>          | <span data-ttu-id="7b2c2-320">65536pi/180</span><span class="sxs-lookup"><span data-stu-id="7b2c2-320">65536pi/180</span></span>       | <span data-ttu-id="7b2c2-321">Radians</span><span class="sxs-lookup"><span data-stu-id="7b2c2-321">Radians</span></span>                                |



 

### <a name="alternative-representations"></a><span data-ttu-id="7b2c2-322">Альтернативные представления</span><span class="sxs-lookup"><span data-stu-id="7b2c2-322">Alternative representations</span></span>

<span data-ttu-id="7b2c2-323">Преобразование «масштабирование» имеет неоднородные четные кратные 45.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-323">The scaling transformation has discontinuities at odd multiples of 45 .</span></span> <span data-ttu-id="7b2c2-324">Таким образом, чрезвычайно важно, чтобы преобразование любого неточного количества было четко определено.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-324">It is, therefore, extremely important for the conversion of any inexact quantity to be well defined.</span></span> <span data-ttu-id="7b2c2-325">По этой причине арифметическое преобразование определяется для округления в сторону минус бесконечности.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-325">For this reason, the arithmetic of conversion is defined to round towards minus infinity.</span></span>

<span data-ttu-id="7b2c2-326">Так как это может быть трудно или невозможно гарантировать в некоторых реализациях, использование следующих компонентов определяется как функция уровня 3:</span><span class="sxs-lookup"><span data-stu-id="7b2c2-326">Because this may be difficult or impossible to guarantee in some implementations, the use of the following is defined to be a level 3 feature:</span></span>

1.  <span data-ttu-id="7b2c2-327">Любое значение дробной степени.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-327">Any fractional degree value.</span></span>
2.  <span data-ttu-id="7b2c2-328">Любое значение радианы</span><span class="sxs-lookup"><span data-stu-id="7b2c2-328">Any radian value</span></span>

<span data-ttu-id="7b2c2-329">Таким словами, значения с полными значениями демона и неполные целочисленные значения или целочисленные значения с полным или должны обрабатываться точно в соответствии с реализацией уровня 0. другие значения не требуются.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-329">Thus, values qualified fd and unqualified integral values, or integral values qualified deg or   must be handled exactly by a conforming level 0 implementation; other values need not.</span></span> <span data-ttu-id="7b2c2-330">Настоятельно рекомендуется, чтобы любая реализация обрабатывала преобразование из значения дробной степени в значение масштабируемой степени в точности.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-330">It is strongly recommended that any implementation handle the conversion from a fractional degree value to a scaled (fd) degree value exactly.</span></span> <span data-ttu-id="7b2c2-331">Это можно сделать без поддержки плавающих точек.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-331">This can be done without floating point support.</span></span>

<span data-ttu-id="7b2c2-332">Более точные требования для преобразования отличают процесс, отличающийся от f.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-332">The more exacting requirements for conversion distinguish fd from f.</span></span>

<span data-ttu-id="7b2c2-333">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-333">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="color"></a><span data-ttu-id="7b2c2-334">color</span><span class="sxs-lookup"><span data-stu-id="7b2c2-334">color</span></span>


```HTML
c
<!element c  %color;>
```



<span data-ttu-id="7b2c2-335">Цвета являются важнейшей частью современных компьютерных графиков.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-335">Colors are an essential part of modern computer graphics.</span></span> <span data-ttu-id="7b2c2-336">В предложении используются установленные методы для указания фиксированных цветов.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-336">The proposal uses the established methods of specifying fixed colors.</span></span> <span data-ttu-id="7b2c2-337">Однако цвета в диаграммах редко являются простыми статическими цветами. они часто являются производными от других элементов на схеме.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-337">However, colors in diagrams are rarely simple static colors; they are often derived from other elements in the diagram.</span></span> <span data-ttu-id="7b2c2-338">Большая часть этой информации очень специфична для приложений, поэтому в этом предложении предусмотрено два очень базовых механизма для указания такого поведения:</span><span class="sxs-lookup"><span data-stu-id="7b2c2-338">Much of this information is very application-specific, so this proposal provides two very basic mechanisms to specify such behavior:</span></span>

1.  <span data-ttu-id="7b2c2-339">Цвет может быть производным от другого цвета в той же фигуре.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-339">A color may be derived from another color in the same shape.</span></span>
2.  <span data-ttu-id="7b2c2-340">Небольшое количество арифметических операций определяется для формирования или изменения цвета.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-340">A small number of arithmetic operations are defined for deriving, or modifying, a color.</span></span>

<span data-ttu-id="7b2c2-341">Механизм формирования прототипа дополняет это, позволяя определять прототипы, из которых можно наследовать цвета.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-341">The prototype shape mechanism supplements this by allow prototypes to be defined from which colors can be inherited.</span></span>


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



<span data-ttu-id="7b2c2-342">Значение цвета представляет собой надмножество [определения цвета CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="7b2c2-342">A color value is a superset of the [CSS1 color definition](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span> <span data-ttu-id="7b2c2-343">Расширения позволяют определить значение цвета RGB на основе других цветов в фигуре или из общей цветовой схемы, определенной с помощью CSS1.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-343">The extensions allow the RGB color value to be determined from other colors within the shape or from an overall color scheme defined using CSS1.</span></span>

<span data-ttu-id="7b2c2-344">Если значение элемента определено как цвет, *содержимое* элемента определяет значение цвета с помощью одного маркера цвета, который может быть изменен с помощью арифметической операции с СООТВЕТСТВУЮЩИМ цветом RGB.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-344">If the value of an element is defined to be a color, the *content* of an element defines the color value by means of a single color token optionally modified by an arithmetic operation on the corresponding RGB color.</span></span>

<span data-ttu-id="7b2c2-345">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-345">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-units"></a><span data-ttu-id="7b2c2-346">Единицы цвета</span><span class="sxs-lookup"><span data-stu-id="7b2c2-346">Color units</span></span>

<span data-ttu-id="7b2c2-347">Полный набор маркеров цвета взят из различных источников: HTML, CSS1 и это предложение.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-347">The full set of color tokens come from a variety of sources: HTML, CSS1, and this proposal.</span></span> <span data-ttu-id="7b2c2-348">Они определяются следующим образом с помощью нотации из [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) или нотации кспоинтер, определенной для связывания XML.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-348">They are defined as follows using notation from [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) or the XPointer notation defined for XML linking.</span></span>

<span data-ttu-id="7b2c2-349">В определениях Кспоинтер источник расположения — это элемент, содержащий значение цвета, а выражение относится ко всему набору элементов фигуры, как будто все элементы базового прототипа были объединены с фигурой.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-349">In the XPointer definitions, the location source is the element containing the color value, and the expression refers to the whole element set of the shape as though any base prototype elements had been merged with the shape.</span></span> <span data-ttu-id="7b2c2-350">Если соответствующий элемент не существует, на его месте используется значение по умолчанию для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-350">When the corresponding element does not exist, the default value for that element is used in its place.</span></span>



| <span data-ttu-id="7b2c2-351">Цвет</span><span class="sxs-lookup"><span data-stu-id="7b2c2-351">Color</span></span>            | <span data-ttu-id="7b2c2-352">Определение</span><span class="sxs-lookup"><span data-stu-id="7b2c2-352">Definition</span></span>                                                                                                  | <span data-ttu-id="7b2c2-353">Level</span><span class="sxs-lookup"><span data-stu-id="7b2c2-353">Level</span></span> | <span data-ttu-id="7b2c2-354">Описание</span><span class="sxs-lookup"><span data-stu-id="7b2c2-354">Description</span></span>                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b2c2-355">name</span><span class="sxs-lookup"><span data-stu-id="7b2c2-355">name</span></span>             | <span data-ttu-id="7b2c2-356">См. ниже</span><span class="sxs-lookup"><span data-stu-id="7b2c2-356">See below</span></span>                                                                                                   | <span data-ttu-id="7b2c2-357">0</span><span class="sxs-lookup"><span data-stu-id="7b2c2-357">0</span></span>     | <span data-ttu-id="7b2c2-358">Имя цвета HTML, как указано в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-358">HTML color name, as listed in the table below.</span></span>                                                                                                                            |
| <span data-ttu-id="7b2c2-359">\#рр'гг'бб "</span><span class="sxs-lookup"><span data-stu-id="7b2c2-359">\#rr'gg'bb'</span></span>      | <span data-ttu-id="7b2c2-360">\#рр'гг'бб "</span><span class="sxs-lookup"><span data-stu-id="7b2c2-360">\#rr'gg'bb'</span></span>                                                                                                 | <span data-ttu-id="7b2c2-361">0</span><span class="sxs-lookup"><span data-stu-id="7b2c2-361">0</span></span>     | <span data-ttu-id="7b2c2-362">Стандартное цветовое представление CSS1/sRGB, использующее значения в диапазоне 0.. 255, представленные с использованием двух шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-362">Standard CSS1/sRGB color representation using values in the range 0..255 represented using 2 hexadecimal digits each.</span></span>                                                     |
| <span data-ttu-id="7b2c2-363">\#цвета</span><span class="sxs-lookup"><span data-stu-id="7b2c2-363">\#rgb</span></span>            | <span data-ttu-id="7b2c2-364">\#RRGGBB</span><span class="sxs-lookup"><span data-stu-id="7b2c2-364">\#rrggbb</span></span>                                                                                                    | <span data-ttu-id="7b2c2-365">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-365">1</span></span>     | <span data-ttu-id="7b2c2-366">Сокращенная форма CSS1 с тремя шестнадцатеричными цифрами.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-366">Shortened CSS1 form with only three hexadecimal digits.</span></span>                                                                                                                   |
| <span data-ttu-id="7b2c2-367">RGB (r, g, b)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-367">rgb(r,g,b)</span></span>       | <span data-ttu-id="7b2c2-368">\#Cерверный модуле &</span><span class="sxs-lookup"><span data-stu-id="7b2c2-368">\#(r)(g)(b)</span></span>                                                                                                 | <span data-ttu-id="7b2c2-369">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-369">1</span></span>     | <span data-ttu-id="7b2c2-370">CSS1 RGB Form; элементы значения RGB преобразуются, как определено в [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="7b2c2-370">CSS1 rgb form; the elements of the rgb value are converted as defined in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span>                                      |
| <span data-ttu-id="7b2c2-371">fill</span><span class="sxs-lookup"><span data-stu-id="7b2c2-371">fill</span></span>             | <span data-ttu-id="7b2c2-372">предок (1, фигура)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-372">ancestor(1,shape)</span></span><br/> <span data-ttu-id="7b2c2-373">дочерний элемент (1, Fill)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-373">child(1, fill)</span></span><br/> <span data-ttu-id="7b2c2-374">дочерний элемент (1, цвет)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-374">child(1, color)</span></span><br/>                           | <span data-ttu-id="7b2c2-375">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-375">1</span></span>     | <span data-ttu-id="7b2c2-376">Цвет заливки переднего плана фигуры.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-376">The foreground fill color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="7b2c2-377">филлбакк</span><span class="sxs-lookup"><span data-stu-id="7b2c2-377">fillBack</span></span>         | <span data-ttu-id="7b2c2-378">предок (1, фигура)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-378">ancestor(1,shape)</span></span><br/> <span data-ttu-id="7b2c2-379">дочерний элемент (1, Fill)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-379">child(1, fill)</span></span><br/> <span data-ttu-id="7b2c2-380">дочерний элемент (1, назад)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-380">child(1, back)</span></span><br/> <span data-ttu-id="7b2c2-381">дочерний элемент (1, цвет)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-381">child(1, color)</span></span><br/> | <span data-ttu-id="7b2c2-382">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-382">1</span></span>     | <span data-ttu-id="7b2c2-383">Цвет фона заливки фигуры.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-383">The background color of the shape fill.</span></span>                                                                                                                                   |
| <span data-ttu-id="7b2c2-384">line</span><span class="sxs-lookup"><span data-stu-id="7b2c2-384">line</span></span>             | <span data-ttu-id="7b2c2-385">предок (1, фигура)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-385">ancestor(1,shape)</span></span><br/> <span data-ttu-id="7b2c2-386">дочерний элемент (1, строка)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-386">child(1, line)</span></span><br/> <span data-ttu-id="7b2c2-387">дочерний элемент (1, цвет)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-387">child(1, color)</span></span><br/>                           | <span data-ttu-id="7b2c2-388">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-388">1</span></span>     | <span data-ttu-id="7b2c2-389">Цвет линии переднего плана фигуры.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-389">The foreground line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="7b2c2-390">линебакк</span><span class="sxs-lookup"><span data-stu-id="7b2c2-390">lineBack</span></span>         | <span data-ttu-id="7b2c2-391">предок (1, фигура)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-391">ancestor(1,shape)</span></span><br/> <span data-ttu-id="7b2c2-392">дочерний элемент (1, строка)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-392">child(1, line)</span></span><br/> <span data-ttu-id="7b2c2-393">дочерний элемент (1, назад)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-393">child(1,back)</span></span> <br/> <span data-ttu-id="7b2c2-394">дочерний элемент (1, цвет)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-394">child(1, color)</span></span><br/> | <span data-ttu-id="7b2c2-395">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-395">1</span></span>     | <span data-ttu-id="7b2c2-396">Цвет линии фона фигуры.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-396">The background line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="7b2c2-397">линеорфилл</span><span class="sxs-lookup"><span data-stu-id="7b2c2-397">lineOrFill</span></span>       | <span data-ttu-id="7b2c2-398">линия, заливка</span><span class="sxs-lookup"><span data-stu-id="7b2c2-398">line, fill</span></span>                                                                                                  | <span data-ttu-id="7b2c2-399">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-399">1</span></span>     | <span data-ttu-id="7b2c2-400">Значение строки, если не используется по умолчанию; в противном случае — значение Fill.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-400">The line value if not defaulted, otherwise the fill value.</span></span> <span data-ttu-id="7b2c2-401">Это эффективно возвращает цвет, который находится на границе фигуры.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-401">This effectively returns the color that is at the edge of the shape.</span></span>                                           |
| <span data-ttu-id="7b2c2-402">филлсенлине</span><span class="sxs-lookup"><span data-stu-id="7b2c2-402">fillThenLine</span></span>     | <span data-ttu-id="7b2c2-403">Заливка, линия</span><span class="sxs-lookup"><span data-stu-id="7b2c2-403">fill, line</span></span>                                                                                                  | <span data-ttu-id="7b2c2-404">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-404">1</span></span>     | <span data-ttu-id="7b2c2-405">Значение заполнения, если оно не используется по умолчанию, в противном случае — значение строки.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-405">The fill value if not defaulted, otherwise the line value.</span></span> <span data-ttu-id="7b2c2-406">Это эффективно Возвращает основной цвет фигуры (если фигура не заполнена, результатом будет цвет линии).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-406">This effectively returns the main shape color (if the shape is unfilled, the result will be the line color).</span></span>   |
| <span data-ttu-id="7b2c2-407">shadow</span><span class="sxs-lookup"><span data-stu-id="7b2c2-407">shadow</span></span>           | <span data-ttu-id="7b2c2-408">предок (1, фигура)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-408">ancestor(1,shape)</span></span><br/> <span data-ttu-id="7b2c2-409">дочерний (1, тень)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-409">child(1, shadow)</span></span><br/> <span data-ttu-id="7b2c2-410">дочерний элемент (1, цвет)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-410">child(1, color)</span></span><br/>                         | <span data-ttu-id="7b2c2-411">2</span><span class="sxs-lookup"><span data-stu-id="7b2c2-411">2</span></span>     | <span data-ttu-id="7b2c2-412">Цвет тени (это функция уровня 2).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-412">The color of the shadow (this is a level 2 feature).</span></span>                                                                                                                      |
| <span data-ttu-id="7b2c2-413">схема</span><span class="sxs-lookup"><span data-stu-id="7b2c2-413">scheme</span></span>           | <span data-ttu-id="7b2c2-414">См. ниже</span><span class="sxs-lookup"><span data-stu-id="7b2c2-414">See below</span></span>                                                                                                   | <span data-ttu-id="7b2c2-415">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-415">1</span></span>     | <span data-ttu-id="7b2c2-416">Цвет схемы из схемы, определенной для документа; см. ниже.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-416">A scheme color from the scheme defined for the document; see below.</span></span>                                                                                                       |
| <span data-ttu-id="7b2c2-417">Схема (*индекс*)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-417">scheme(*index*)</span></span>  | <span data-ttu-id="7b2c2-418">См. ниже</span><span class="sxs-lookup"><span data-stu-id="7b2c2-418">See below</span></span>                                                                                                   | <span data-ttu-id="7b2c2-419">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-419">1</span></span>     | <span data-ttu-id="7b2c2-420">*Индекс* цвета схемы, начиная с 0; см. ниже.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-420">Scheme color *index*, starting from 0; see below.</span></span>                                                                                                                         |
| <span data-ttu-id="7b2c2-421">this</span><span class="sxs-lookup"><span data-stu-id="7b2c2-421">this</span></span>             | <span data-ttu-id="7b2c2-422">Предполагаем</span><span class="sxs-lookup"><span data-stu-id="7b2c2-422">Implied</span></span>                                                                                                     | <span data-ttu-id="7b2c2-423">2</span><span class="sxs-lookup"><span data-stu-id="7b2c2-423">2</span></span>     | <span data-ttu-id="7b2c2-424">Операция (заполнение контура или прорисовка) определяется каким-то другим способом (например, как точечный рисунок), а цвет указывает на изменение цветов, что приводит к указанию.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-424">The operation (filling a path, or drawing it) is defined in some other way (for example, as a bitmap), and the color specifies a "modification" to the colors so implied.</span></span> |
| <span data-ttu-id="7b2c2-425">Палитра (*индекс*)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-425">palette(*index*)</span></span> | <span data-ttu-id="7b2c2-426">Предполагаем</span><span class="sxs-lookup"><span data-stu-id="7b2c2-426">Implied</span></span>                                                                                                     | <span data-ttu-id="7b2c2-427">3</span><span class="sxs-lookup"><span data-stu-id="7b2c2-427">3</span></span>     | <span data-ttu-id="7b2c2-428">Ведет себя так же, как это происходит, за исключением того, что определена ровно одна запись в таблице цветов точечных рисунков.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-428">Behaves in the same way as this, except that exactly one entry in a bitmap color table is identified.</span></span> <span data-ttu-id="7b2c2-429">Допускается только там, где указано явно.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-429">Permitted only where explicitly stated.</span></span>                             |
| <span data-ttu-id="7b2c2-430">нет</span><span class="sxs-lookup"><span data-stu-id="7b2c2-430">none</span></span>             | \-                                                                                                          | <span data-ttu-id="7b2c2-431">2</span><span class="sxs-lookup"><span data-stu-id="7b2c2-431">2</span></span>     | <span data-ttu-id="7b2c2-432">Указывает отсутствие цвета; может использоваться для отмены операции рисования, использующей цвет.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-432">Indicates the absence of a color; may be used to cancel a drawing operation that uses the color.</span></span>                                                                          |
| <span data-ttu-id="7b2c2-433">система</span><span class="sxs-lookup"><span data-stu-id="7b2c2-433">system</span></span>           | <span data-ttu-id="7b2c2-434">См. ниже</span><span class="sxs-lookup"><span data-stu-id="7b2c2-434">See below</span></span>                                                                                                   | <span data-ttu-id="7b2c2-435">3</span><span class="sxs-lookup"><span data-stu-id="7b2c2-435">3</span></span>     | <span data-ttu-id="7b2c2-436">Цвет, определяемый системным пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-436">A color defined by the system user interface.</span></span>                                                                                                                             |



 

<span data-ttu-id="7b2c2-437">Этот цвет позволяет значению цвета указать изменение цвета, который является производным другим способом. в частности, для всех цветов в точечном рисунке может быть задана одна операция.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-437">The this color allows a color value to specify a modification to a color which is derived in some other way; in particular, a single operation may be specified for all the colors in a bitmap.</span></span> <span data-ttu-id="7b2c2-438">Цвет палитры (*index*) определяет определенную запись в точечном рисунке, сопоставленном с палитрой.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-438">The palette(*index*) color identifies a particular entry in a palette-mapped bitmap.</span></span> <span data-ttu-id="7b2c2-439">Использование этого параметра определяется только для записи записи таблицы цветов, которая должна рассматриваться как прозрачная в таком точечном рисунке.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-439">Use of this is only defined for recording a color table entry that should be regarded as transparent in such a bitmap.</span></span>

<span data-ttu-id="7b2c2-440">Определение значения цвета не должно ссылаться ни на себя, ни на себя напрямую, ни косвенно.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-440">The definition of a color value must not refer to itself, either directly or indirectly.</span></span> <span data-ttu-id="7b2c2-441">При обнаружении такого определения рекомендуется, но не требуется, чтобы реализация считала неопределенное значение черным.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-441">If such a definition is encountered, it is recommended, but not required, that the implementation treat the undefined value as black.</span></span>

<span data-ttu-id="7b2c2-442">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-442">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="html-colors"></a><span data-ttu-id="7b2c2-443">Цвета HTML</span><span class="sxs-lookup"><span data-stu-id="7b2c2-443">HTML colors</span></span>

<span data-ttu-id="7b2c2-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) определяет следующие шестнадцати имен цветов:</span><span class="sxs-lookup"><span data-stu-id="7b2c2-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) defines the following sixteen color names:</span></span>



<span data-ttu-id="7b2c2-445">Имена цветов и значения sRGB</span><span class="sxs-lookup"><span data-stu-id="7b2c2-445">Color names and sRGB values</span></span>

![Пример черного цвета.](images/black.gif)

<span data-ttu-id="7b2c2-447">Black = " \# 000000"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-447">Black = "\#000000"</span></span>

![Пример зеленого цвета.](images/green.gif)

<span data-ttu-id="7b2c2-449">Green = " \# 008000"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-449">Green = "\#008000"</span></span>

![Пример серебристого цвета.](images/silver.gif)

<span data-ttu-id="7b2c2-451">Серебро = " \# c0c0c0"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-451">Silver = "\#C0C0C0"</span></span>

![Пример травяного цвета.](images/lime.gif)

<span data-ttu-id="7b2c2-453">Травяной = " \# 00FF00"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-453">Lime = "\#00FF00"</span></span>

![Пример серого цвета.](images/gray.gif)

<span data-ttu-id="7b2c2-455">Серый = " \# 808080"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-455">Gray = "\#808080"</span></span>

![Пример цвета оливковый.](images/olive.gif)

<span data-ttu-id="7b2c2-457">Оливковый = " \# 808000"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-457">Olive = "\#808000"</span></span>

![Пример белого цвета.](images/white.gif)

<span data-ttu-id="7b2c2-459">Белый = " \# ffffff"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-459">White = "\#FFFFFF"</span></span>

![Пример цвета ивллов.](images/yellow.gif)

<span data-ttu-id="7b2c2-461">Желтый = " \# FFFF00"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-461">Yellow = "\#FFFF00"</span></span>

![Пример цвета каштановый.](images/maroon.gif)

<span data-ttu-id="7b2c2-463">Каштановый = " \# 800000"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-463">Maroon = "\#800000"</span></span>

![Пример цвета ВМФ.](images/navy.gif)

<span data-ttu-id="7b2c2-465">ВМФ = " \# 000080"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-465">Navy = "\#000080"</span></span>

![Пример красного цвета.](images/red.gif)

<span data-ttu-id="7b2c2-467">Red = " \# FF0000"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-467">Red = "\#FF0000"</span></span>

![Пример синего цвета.](images/blue.gif)

<span data-ttu-id="7b2c2-469">Blue = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-469">Blue = "\#0000FF"</span></span>

![Пример пурпурного цвета.](images/purple.gif)

<span data-ttu-id="7b2c2-471">Фиолетовый = " \# 800080"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-471">Purple = "\#800080"</span></span>

![Пример синего цвета.](images/teal.gif)

<span data-ttu-id="7b2c2-473">Бирюзовый = " \# 008080"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-473">Teal = "\#008080"</span></span>

![Пример цвета фучсиа.](images/fuchsia.gif)

<span data-ttu-id="7b2c2-475">Фучсиа = " \# FF00FF"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-475">Fuchsia = "\#FF00FF"</span></span>

![Пример цвет морской волны.](images/aqua.gif)

<span data-ttu-id="7b2c2-477">Голубой = " \# 00FFFF"</span><span class="sxs-lookup"><span data-stu-id="7b2c2-477">Aqua = "\#00FFFF"</span></span>



 

<span data-ttu-id="7b2c2-478">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-478">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="scheme-colors"></a><span data-ttu-id="7b2c2-479">Цвета схемы</span><span class="sxs-lookup"><span data-stu-id="7b2c2-479">Scheme colors</span></span>

<span data-ttu-id="7b2c2-480">Цвета схемы, на которые ссылается схема, определяются на уровне документа с помощью тега meta с атрибутом Name атрибута «цветовая схема темы».</span><span class="sxs-lookup"><span data-stu-id="7b2c2-480">The scheme colors referenced by scheme are defined at the document level using the meta tag with a name attribute of "Theme Color Scheme".</span></span>


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



<span data-ttu-id="7b2c2-481">Этот тег позволяет определить до восьми цветов схемы.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-481">This tag allows up to eight scheme colors to be defined.</span></span> <span data-ttu-id="7b2c2-482">Неопределенные цвета должны по умолчанию быть черными.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-482">Undefined colors should default to black.</span></span> <span data-ttu-id="7b2c2-483">Цвета схемы позволяют изменить цветовую схему, используемую для полного документа, путем изменения содержимого цветовой схемы темы.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-483">The scheme colors allow the color scheme used for a complete document to be changed just by altering the Theme Color Scheme contents.</span></span> <span data-ttu-id="7b2c2-484">Чтобы обеспечить единообразное использование цветов схемы в графических объектах, импортированных из различных приложений, необходимо определить следующие интерпретации.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-484">To ensure that graphics imported from different authoring applications make consistent use of the scheme colors, the following interpretations are defined.</span></span> <span data-ttu-id="7b2c2-485">"Использование" — это краткое описание назначения, а в столбце "Описание" содержатся дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-485">The "usage" is a short description of the purpose, and the "description" column provides additional details.</span></span>



| <span data-ttu-id="7b2c2-486">Индекс</span><span class="sxs-lookup"><span data-stu-id="7b2c2-486">Index</span></span> | <span data-ttu-id="7b2c2-487">Имя</span><span class="sxs-lookup"><span data-stu-id="7b2c2-487">Name</span></span>              | <span data-ttu-id="7b2c2-488">Использование</span><span class="sxs-lookup"><span data-stu-id="7b2c2-488">Usage</span></span>                         | <span data-ttu-id="7b2c2-489">Описание</span><span class="sxs-lookup"><span data-stu-id="7b2c2-489">Description</span></span>                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b2c2-490">0</span><span class="sxs-lookup"><span data-stu-id="7b2c2-490">0</span></span>     | <span data-ttu-id="7b2c2-491">схема. фон</span><span class="sxs-lookup"><span data-stu-id="7b2c2-491">scheme.background</span></span> | <span data-ttu-id="7b2c2-492">Историческая справка</span><span class="sxs-lookup"><span data-stu-id="7b2c2-492">Background</span></span>                    | <span data-ttu-id="7b2c2-493">Цвет фона изображения (и часто для всей страницы).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-493">The color used for the background of a graphic (and, frequently, for the whole page).</span></span>                                    |
| <span data-ttu-id="7b2c2-494">1</span><span class="sxs-lookup"><span data-stu-id="7b2c2-494">1</span></span>     | <span data-ttu-id="7b2c2-495">схема. текст</span><span class="sxs-lookup"><span data-stu-id="7b2c2-495">scheme.text</span></span>       | <span data-ttu-id="7b2c2-496">Текст и строки</span><span class="sxs-lookup"><span data-stu-id="7b2c2-496">Text and lines</span></span>                | <span data-ttu-id="7b2c2-497">Цвет текста, присоединенного к фигуре, и Стандартный цвет линии.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-497">The color for text attached to a shape and the standard line color.</span></span>                                                      |
| <span data-ttu-id="7b2c2-498">2</span><span class="sxs-lookup"><span data-stu-id="7b2c2-498">2</span></span>     | <span data-ttu-id="7b2c2-499">схема. тень</span><span class="sxs-lookup"><span data-stu-id="7b2c2-499">scheme.shadow</span></span>     | <span data-ttu-id="7b2c2-500">Shadows</span><span class="sxs-lookup"><span data-stu-id="7b2c2-500">Shadows</span></span>                       | <span data-ttu-id="7b2c2-501">Стандартный цвет тени — цвет, обычно используемый для теней фигур.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-501">Standard shadow color -- the color typically used for shape shadows.</span></span>                                                     |
| <span data-ttu-id="7b2c2-502">3</span><span class="sxs-lookup"><span data-stu-id="7b2c2-502">3</span></span>     | <span data-ttu-id="7b2c2-503">схема. название</span><span class="sxs-lookup"><span data-stu-id="7b2c2-503">scheme.title</span></span>      | <span data-ttu-id="7b2c2-504">Текст заголовка</span><span class="sxs-lookup"><span data-stu-id="7b2c2-504">Title text</span></span>                    | <span data-ttu-id="7b2c2-505">Цвет, используемый для заголовка или текста заголовка.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-505">The color to use for heading or title text.</span></span>                                                                              |
| <span data-ttu-id="7b2c2-506">4</span><span class="sxs-lookup"><span data-stu-id="7b2c2-506">4</span></span>     | <span data-ttu-id="7b2c2-507">схема. Заливка</span><span class="sxs-lookup"><span data-stu-id="7b2c2-507">scheme.fill</span></span>       | <span data-ttu-id="7b2c2-508">Заполняла</span><span class="sxs-lookup"><span data-stu-id="7b2c2-508">Fills</span></span>                         | <span data-ttu-id="7b2c2-509">Цвет стандартной заливки — цвет, обычно используемый для заливки фигур.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-509">Standard fill color -- the color typically used to fill shapes.</span></span>                                                          |
| <span data-ttu-id="7b2c2-510">5</span><span class="sxs-lookup"><span data-stu-id="7b2c2-510">5</span></span>     | <span data-ttu-id="7b2c2-511">схема. акцент</span><span class="sxs-lookup"><span data-stu-id="7b2c2-511">scheme.accent</span></span>     | <span data-ttu-id="7b2c2-512">Буквы</span><span class="sxs-lookup"><span data-stu-id="7b2c2-512">Accent</span></span>                        | <span data-ttu-id="7b2c2-513">Стандартный "выделенный" цвет, используемый для выделения важного элемента изображения.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-513">Normal "highlight" color used to emphasis an important element of a graphic.</span></span>                                             |
| <span data-ttu-id="7b2c2-514">6</span><span class="sxs-lookup"><span data-stu-id="7b2c2-514">6</span></span>     | <span data-ttu-id="7b2c2-515">схема. гиперссылка</span><span class="sxs-lookup"><span data-stu-id="7b2c2-515">scheme.hyperlink</span></span>  | <span data-ttu-id="7b2c2-516">Диакритические знаки и гиперссылки</span><span class="sxs-lookup"><span data-stu-id="7b2c2-516">Accent and hyperlink</span></span>          | <span data-ttu-id="7b2c2-517">Цвет выделения гиперссылок.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-517">Highlight color used for hyperlinks.</span></span> <span data-ttu-id="7b2c2-518">Может использоваться в других целях, когда цвет обозначает ссылку на другую информацию.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-518">May be used for other purposes where the color denotes a link to other information.</span></span> |
| <span data-ttu-id="7b2c2-519">7</span><span class="sxs-lookup"><span data-stu-id="7b2c2-519">7</span></span>     | <span data-ttu-id="7b2c2-520">схема. Затем</span><span class="sxs-lookup"><span data-stu-id="7b2c2-520">scheme.followed</span></span>   | <span data-ttu-id="7b2c2-521">Акцент и просмотренная ссылка</span><span class="sxs-lookup"><span data-stu-id="7b2c2-521">Accent and followed hyperlink</span></span> | <span data-ttu-id="7b2c2-522">Цвет выделения для отслеживаемых гиперссылок; также подходит для обратных ссылок.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-522">Highlight color for followed hyperlinks; also appropriate for "backwards" links.</span></span>                                         |



 

<span data-ttu-id="7b2c2-523">Цвет схемы может называться либо по имени, либо по индексу, поэтому схема. Заливка и схема (4) имеют одинаковый цвет.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-523">A scheme color may be referred to either by name or by index, thus scheme.fill and scheme(4) are the same color.</span></span>

<span data-ttu-id="7b2c2-524">Цвета схемы не участвуют в схеме по умолчанию, если цвет не указан.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-524">Scheme colors do not participate in the defaulting scheme if a color is not specified.</span></span> <span data-ttu-id="7b2c2-525">Неопределенный цвет заливки всегда должен интерпретироваться как белый, независимо от цвета схемы 4.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-525">An unspecified fill color must always be interpreted as white, regardless of the color of scheme color 4.</span></span> <span data-ttu-id="7b2c2-526">Цвета "диакритические знаки" должны быть контрастны с цветами фона (0) и заливкой (4), а цвета текста и текста заголовка должны иметь одно и то же свойство.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-526">The "accent" colors should contrast with both the background (0) and the fill (4) colors, and text and title text colors should have the same property.</span></span> <span data-ttu-id="7b2c2-527">Один из стандартных методов заключается в том, чтобы сделать цвета акцентов и стандартного текста нецветными (обычно черно-белым).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-527">One standard technique is to make the accents colored and the standard text uncolored (typically black or white).</span></span>

<span data-ttu-id="7b2c2-528">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-528">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="system-colors"></a><span data-ttu-id="7b2c2-529">Системные цвета</span><span class="sxs-lookup"><span data-stu-id="7b2c2-529">System colors</span></span>

<span data-ttu-id="7b2c2-530">Приложения иногда записывают цвета на основе параметров операционной системы в графике.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-530">Applications sometimes record colors based on operating system settings within graphics.</span></span> <span data-ttu-id="7b2c2-531">Обычно они являются временными и не требуют написания. определения сесистемколор существуют исключительно для поддержки этого.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-531">Normally these are transient and need not be written out; thesystemcolor definitions exist solely to support this.</span></span> <span data-ttu-id="7b2c2-532">Системный цвет вводится путем определения соответствующего тега в новом пространстве имен и вставки соответствующей информации в содержимое элемента.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-532">A system color is introduced by defining an appropriate tag in a new namespace and inserting the appropriate information in the element content.</span></span>

<span data-ttu-id="7b2c2-533">Это предложение определяет такой тег для кодирования цветов пользовательского интерфейса Windows, определенных в файле заголовка Winuser. h.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-533">This proposal defines such a tag to encode the Windows user interface colors defined in the winuser.h header file.</span></span>


```HTML
win.color
<!element win.color #pcdata>
```



<span data-ttu-id="7b2c2-534">Содержимое элемента представляет собой одно целое число, которое содержит значение соответствующего цвета, \_ определенного в файле WinUser. h.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-534">The content of the element is a single integer which contains the value of the relevant COLOR\_ define from winuser.h.</span></span> <span data-ttu-id="7b2c2-535">Аналогичную методику можно использовать для любой спецификации цвета, определенной для системы или приложения.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-535">A similar technique can be adopted for any system- or application-specific color specification.</span></span> <span data-ttu-id="7b2c2-536">Настоятельно рекомендуется использовать эту функцию только для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-536">It is strongly recommended that this feature be used only for backward compatibility.</span></span>

<span data-ttu-id="7b2c2-537">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-537">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="pure-colors"></a><span data-ttu-id="7b2c2-538">Чистые цвета</span><span class="sxs-lookup"><span data-stu-id="7b2c2-538">Pure colors</span></span>


```HTML
pure
<!elementpure empty>
```



<span data-ttu-id="7b2c2-539">Если элемент <pure/> отображается в значении цвета, это указание, что цвет не должен быть приблизительным шаблоном сглаживания.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-539">If the element <pure/> appears in a color value, it is a hint that the color should not be approximated by a dither pattern.</span></span> <span data-ttu-id="7b2c2-540">Это функция уровня 1, и реализация соответствия не требует ее учитывать.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-540">This is a level 1 feature, and a conforming implementation need not honor it.</span></span> <span data-ttu-id="7b2c2-541">Это важно для графики, отображаемой на устройствах среднего разрешения, например в видеороликах, где небольшие функции (например, линии) могут привести к неправильному присвоению псевдонимов с помощью сглаженных цветов.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-541">The designation is important for graphics displayed on medium-resolution devices, such as video displays, where small features (such as lines) may cause bad aliasing with dithered colors.</span></span> <span data-ttu-id="7b2c2-542">На таких устройствах, как принтеры, которые обычно переключают все цвета, за исключением нескольких полностью насыщенных цветов, режим сглаживания обычно достаточно велик, чтобы избежать этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-542">On devices such as printers, which normally dither all colors except for the few fully saturated colors, the dithering is normally sufficiently fine to avoid this problem.</span></span>

<span data-ttu-id="7b2c2-543">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-543">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-adjustments"></a><span data-ttu-id="7b2c2-544">Корректировки цвета</span><span class="sxs-lookup"><span data-stu-id="7b2c2-544">Color adjustments</span></span>

<span data-ttu-id="7b2c2-545">Базовый цвет может быть скорректирован арифметическими операциями в значении RGB.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-545">The base color may be adjusted by arithmetic operations on the RGB value.</span></span> <span data-ttu-id="7b2c2-546">Эти операции определяются с помощью дополнительных элементов в значении цвета.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-546">These operations are defined using additional elements within the color value.</span></span> <span data-ttu-id="7b2c2-547">Такие корректировки полезны только при применении к цветам, производным от других элементов.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-547">Such adjustments are useful only when applied to colors derived from other elements.</span></span> <span data-ttu-id="7b2c2-548">Можно указать такую коррекцию для значения фиксированного цвета. Однако реализация может уменьшить это значение до соответствующего значения RGB и сохранить его вместо исходного.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-548">It is valid to specify such an adjustment on a fixed color value; however, an implementation is permitted to reduce this to the corresponding RGB value and store that instead of the original.</span></span>

<span data-ttu-id="7b2c2-549">Все функции коррекции цвета, описанные в этом разделе, являются компонентами уровня 1.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-549">All the color adjustment features described in this section are level 1 features.</span></span>


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



<span data-ttu-id="7b2c2-550">Параметр первых шести операций представляет собой одно целое число в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-550">The parameter of the first six operations is a single integral numeric value in the range 0 to 255.</span></span> <span data-ttu-id="7b2c2-551">Корректировка выполняется для значения 3x8bit RGB следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7b2c2-551">The adjustment is performed on the 3x8bit RGB value as follows:</span></span>

1.  <span data-ttu-id="7b2c2-552">Если <gray/> указан параметр, значение RGB заменяется на yyy, где y — значение светимости (y), вычисленное по значению sRGB в следующем примере ITU-r BT. 709.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-552">If <gray/> is specified, the RGB value is replaced by yyy, where y is the luminance (y') value calculated from the sRGB value in following the ITU-r BT.709.</span></span> <span data-ttu-id="7b2c2-553">Это вычисление:</span><span class="sxs-lookup"><span data-stu-id="7b2c2-553">This calculation is:</span></span>
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  <span data-ttu-id="7b2c2-554">Если задано изменение Color. op, каждый компонент по отдельности корректируется в соответствии с таблицей ниже.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-554">If a color.op modification is given, each component is separately adjusted according to the table below.</span></span> <span data-ttu-id="7b2c2-555">c является значением компонента, а p — значением Color.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-555">c is the component value, and p is the color.parameter value.</span></span>

    | <span data-ttu-id="7b2c2-556">Операция</span><span class="sxs-lookup"><span data-stu-id="7b2c2-556">Operation</span></span>       | <span data-ttu-id="7b2c2-557">Формула</span><span class="sxs-lookup"><span data-stu-id="7b2c2-557">Formula</span></span>                            |
    |-----------------|------------------------------------|
    | <span data-ttu-id="7b2c2-558">делает</span><span class="sxs-lookup"><span data-stu-id="7b2c2-558">darken</span></span>          | <span data-ttu-id="7b2c2-559">c: = cxp/255</span><span class="sxs-lookup"><span data-stu-id="7b2c2-559">c := cxp/255</span></span>                       |
    | <span data-ttu-id="7b2c2-560">Crash</span><span class="sxs-lookup"><span data-stu-id="7b2c2-560">lighten</span></span>         | <span data-ttu-id="7b2c2-561">c: = 255-(255-c) XP/255</span><span class="sxs-lookup"><span data-stu-id="7b2c2-561">c := 255 - (255-c)xp/255</span></span>           |
    | <span data-ttu-id="7b2c2-562">add</span><span class="sxs-lookup"><span data-stu-id="7b2c2-562">add</span></span>             | <span data-ttu-id="7b2c2-563">c: = c + p</span><span class="sxs-lookup"><span data-stu-id="7b2c2-563">c := c + p</span></span>                         |
    | <span data-ttu-id="7b2c2-564">вычитание</span><span class="sxs-lookup"><span data-stu-id="7b2c2-564">subtract</span></span>        | <span data-ttu-id="7b2c2-565">c: = c-p</span><span class="sxs-lookup"><span data-stu-id="7b2c2-565">c := c - p</span></span>                         |
    | <span data-ttu-id="7b2c2-566">реверсесубтракт</span><span class="sxs-lookup"><span data-stu-id="7b2c2-566">reversesubtract</span></span> | <span data-ttu-id="7b2c2-567">c: = p-c</span><span class="sxs-lookup"><span data-stu-id="7b2c2-567">c := p - c</span></span>                         |
    | <span data-ttu-id="7b2c2-568">блакквхите</span><span class="sxs-lookup"><span data-stu-id="7b2c2-568">blackwhite</span></span>      | <span data-ttu-id="7b2c2-569">Если c < p Сенк: = 0elsec: = 255</span><span class="sxs-lookup"><span data-stu-id="7b2c2-569">if c < p thenc := 0elsec := 255</span></span> |

    

     

    <span data-ttu-id="7b2c2-570">В каждом случае, если значение вычисляемого компонента, c, превышает 255, то используется 255, а если оно меньше 0, то используется 0.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-570">In each case, if the calculated component value, c, exceeds 255, then 255 is used, and if it is less than 0, then 0 is used.</span></span>

3.  <span data-ttu-id="7b2c2-571">Если задано <INVERT128/> , значение 128 вычитается или добавляется в каждый компонент в соответствии с тем, имеет ли компонент меньше 128.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-571">If <INVERT128/> is given, the value 128 is subtracted or added to each component according to whether the component is less than 128 or not.</span></span>
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  <span data-ttu-id="7b2c2-572">Если задано <invert/> значение, каждый компонент заменяется на 255 за вычетом значения компонента.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-572">If <invert/> is given, each component is replaced by 255 minus the value of the component.</span></span>
    ```HTML
    c := 255-c
    ```

    

<span data-ttu-id="7b2c2-573">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-573">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="font"></a><span data-ttu-id="7b2c2-574">font</span><span class="sxs-lookup"><span data-stu-id="7b2c2-574">font</span></span>


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



<span data-ttu-id="7b2c2-575">Шрифт определяется с помощью атрибута стиля, как определено в [разделе CSS1 5,2 (свойства шрифта)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span><span class="sxs-lookup"><span data-stu-id="7b2c2-575">A font is identified using a style attribute as defined in [CSS1 section 5.2 (font properties)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span></span> <span data-ttu-id="7b2c2-576">Тело элемента Font —, в настоящее время, не определено, но может использоваться в будущем для кодирования стандартных сведений о шрифтах.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-576">The body of the font element is, at present, undefined but may be used in the future to encode standard font information.</span></span> <span data-ttu-id="7b2c2-577">Начальные реализации этого предложения должны сохраняться, но не интерпретировать их.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-577">Initial implementations of this proposal should preserve but not interpret the information.</span></span>

<span data-ttu-id="7b2c2-578">Это представить, что поддержка будет добавлена в будущем для получения сведений о шрифте (загружаемых шрифтов или общих шрифтов).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-578">It is conceivable that support will be added in the future for out-of-line font information (downloadable fonts, or shared font resources).</span></span> <span data-ttu-id="7b2c2-579">Это делается элементом XML-компоновки в содержимом элемента Font, что обеспечивает обратную компатбилити с начальными реализациями.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-579">This will be done by an XML-link element within the content of the font element, ensuring backward compatbility with initial implementations.</span></span>

<span data-ttu-id="7b2c2-580">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-580">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="bitmap"></a><span data-ttu-id="7b2c2-581">bitmap</span><span class="sxs-lookup"><span data-stu-id="7b2c2-581">bitmap</span></span>


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



<span data-ttu-id="7b2c2-582">Элемент Bitmap позволяет включать ссылку на нестандартный ресурс изображения (обычно точечный рисунок) в графический объект.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-582">The bitmap element allows a reference to an out-of-line picture resource (normally a bitmap) to be included in a graphic.</span></span>

<span data-ttu-id="7b2c2-583">Битовая карта — это функция уровня 1.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-583">bitmap is a level 1 feature.</span></span>

<span data-ttu-id="7b2c2-584">Атрибут Behavior может использоваться для указания того, как точечный рисунок должен обрабатываться приложением редактирования.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-584">The behavior attribute may be used to indicate how the bitmap should be handled by an editing application.</span></span> <span data-ttu-id="7b2c2-585">Значением может быть один или оба следующих токена.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-585">The value may be one or both of the following tokens.</span></span>



| <span data-ttu-id="7b2c2-586">Токен</span><span class="sxs-lookup"><span data-stu-id="7b2c2-586">Token</span></span>    | <span data-ttu-id="7b2c2-587">Описание</span><span class="sxs-lookup"><span data-stu-id="7b2c2-587">Description</span></span>                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b2c2-588">отдельные</span><span class="sxs-lookup"><span data-stu-id="7b2c2-588">separate</span></span> | <span data-ttu-id="7b2c2-589">Помечает точечный рисунок как отдельную сущность, которую не следует рассматривать как целую часть документа.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-589">Marks the bitmap as a separate entity, which should not be regarded as an integral part of the document.</span></span> <span data-ttu-id="7b2c2-590">Точечный рисунок не должен храниться в документе.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-590">The bitmap should not be kept with the document.</span></span> <span data-ttu-id="7b2c2-591">Если документ копируется, точечный рисунок не копируется. Если документ перемещен, точечный рисунок не должен перемещаться вместе с ним.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-591">If the document is copied, the bitmap should not be copied; if the document is moved, the bitmap should not be moved with it.</span></span> |
| <span data-ttu-id="7b2c2-592">оригинальный</span><span class="sxs-lookup"><span data-stu-id="7b2c2-592">original</span></span> | <span data-ttu-id="7b2c2-593">Атрибут Title определяет исходное расположение точечного рисунка как URL-адрес. в противном случае значение Title не указывается.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-593">The title attribute identifies the original location of the bitmap as a URL; otherwise, the meaning of title is not specified.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="7b2c2-594">Эти значения являются указаниями как для ожидаемого поведения.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-594">These values are both hints as to the expected behavior.</span></span> <span data-ttu-id="7b2c2-595">Отдельный параметр относится к поведению данных, на которые ссылается href.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-595">The separate option refers to the behavior of the data referred to by href.</span></span> <span data-ttu-id="7b2c2-596">Если заданы как отдельные, так и исходные значения, приложение должно игнорировать URI href и повторно создать точечный рисунок из исходных данных.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-596">If both separate and original are given, the application is expected to disregard the href URI and regenerate the bitmap from the original data.</span></span> <span data-ttu-id="7b2c2-597">Если задан только исходный код, приложение должно использовать URI href для поиска точечного рисунка, но может дать пользователю возможность его повторного создания.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-597">If only original is given, the application is expected to use the href URI to find the bitmap but may give the user the option of regenerating it.</span></span>

<span data-ttu-id="7b2c2-598">Допустим, что URI href и атрибут Title имеют одинаковое (лексическое) значение — это подходит, если точечный рисунок, на который указывает ссылка, не хранится вместе с документом.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-598">It is valid to make the href URI and the title attribute the same (lexical) value -- this is appropriate if the referenced bitmap is not "stored with" the document.</span></span> <span data-ttu-id="7b2c2-599">Он предназначен (хотя и не требуется) для использования атрибута href в собственной копии точечного рисунка, который может быть удален, если ссылающиеся фигуры удалены, и этот заголовок будет использоваться для указания общей копии.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-599">It is intended (though not required) that href be used for the document's own copy of the bitmap -- which may be deleted if the referencing shapes are deleted -- and that title be used to indicate a shared copy.</span></span> <span data-ttu-id="7b2c2-600">Таким же, если оба значения содержат одно и то же значение, копирование для конкретного документа не существует.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-600">Thus, if both contain the same value there is no document-specific copy.</span></span>

<span data-ttu-id="7b2c2-601">Приложения могут игнорировать указание, если оно не помещается в реальной модели хранения XML-данных.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-601">Applications may disregard the hint if it does not fit in with the actual storage model of the XML data.</span></span>

<span data-ttu-id="7b2c2-602">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-602">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="picture-file-formats"></a><span data-ttu-id="7b2c2-603">Форматы файлов изображений</span><span class="sxs-lookup"><span data-stu-id="7b2c2-603">Picture file formats</span></span>

<span data-ttu-id="7b2c2-604">В контексте этого предложения внешние данные неизменно либо точечный рисунок, либо файл, который используется для создания точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-604">Within the context of this proposal, external data is invariably either a bitmap or a file which is used to produce a bitmap.</span></span> <span data-ttu-id="7b2c2-605">На уровне прорисовки 0 не требуется поддерживать внешний формат битовых рисунков — пути могут заполняться только сплошными цветами.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-605">At render level 0, no external bitmap format need be supported -- paths may only be filled with solid colors.</span></span> <span data-ttu-id="7b2c2-606">Чтобы отобразить полный набор заливок уровня прорисовки 1, необходимо поддерживать точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-606">To render the full set of render level 1 fills, bitmaps need to be supported.</span></span> <span data-ttu-id="7b2c2-607">Отрисовка уровня 1 включает (только) следующие форматы:</span><span class="sxs-lookup"><span data-stu-id="7b2c2-607">Render level 1 includes (only) the following formats:</span></span>

1.  <span data-ttu-id="7b2c2-608">JFIF, т. е. формат ISO/IEC 10918, внедренный в файл с заголовком JFIF (который можно рассматривать как определенный маркер APP0 после сои Maker) и включая (только) диапазон форматов JPEG, поддерживаемых кодом ИЖГ V6.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-608">JFIF, i.e. ISO/IEC 10918 format data embedded within a file with the JFIF header (which may be regarded as a particular APP0 marker after the SOI maker) and including (only) the range of JPEG formats supported by the IJG v6 code.</span></span>
2.  <span data-ttu-id="7b2c2-609">PNG, как определено в спецификации PNG версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-609">PNG, as defined by the PNG version 1.0 specification.</span></span>

<span data-ttu-id="7b2c2-610">Уровень прорисовки 2 также включает поддержку следующих действий:</span><span class="sxs-lookup"><span data-stu-id="7b2c2-610">Render level 2 also includes support for the following:</span></span>

-   <span data-ttu-id="7b2c2-611">GIF, как определено спецификацией GIF, публикуемой Компусерв в 1987 (обычно называется "GIF87a").</span><span class="sxs-lookup"><span data-stu-id="7b2c2-611">GIF, as defined by the GIF specification published by CompuServ in 1987 (normally referred to as "GIF87a").</span></span> <span data-ttu-id="7b2c2-612">GIF89a также должен поддерживаться на этом уровне в соответствии с ограничением того, что данные не должны содержать блоки расширений, для которых требуется интерпретация, чтобы отобразить точечный рисунок, отличный от требования к графическому элементу управления екстенсионсвисаута для пользовательского ввода или времени задержки.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-612">GIF89a must also be supported at this level, subject to the restriction that the data must not contain any extension blocks that need interpretation to display the bitmap other than graphics control extensionswithouta requirement for user input or a delay time.</span></span> <span data-ttu-id="7b2c2-613">Это позволяет включать комментарии, но не расширение обычного текста.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-613">This allows comments to be included, but not the plain text extension.</span></span> <span data-ttu-id="7b2c2-614">Приложение может вставлять расширения приложения (0x21, 0xFF), но, используя терминологию этого предложения, они должны содержать только редактирование, а не отрисовку данных.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-614">An application may insert application (0x21, 0xFF) extensions but, using the terminology of this proposal, these must contain only editing, not rendering, data.</span></span>

<span data-ttu-id="7b2c2-615">Любой другой формат данных, используемый на рисунке, приводит к тому, что изображение будет иметь вид как минимум на уровне 3 и, возможно, отрисовку на уровне 3 (если данные необходимы для отрисовки графика).</span><span class="sxs-lookup"><span data-stu-id="7b2c2-615">Any other data format used in the graphic forces that graphic to be at least editing level 3 and possibly rendering level 3 (if the data is necessary to render the graphic).</span></span> <span data-ttu-id="7b2c2-616">Приложению рекомендуется публиковать Поддерживаемые форматы.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-616">An application is encouraged to publish the formats which it supports.</span></span> <span data-ttu-id="7b2c2-617">Например, Microsoft Office поддерживает следующие дополнительные форматы в собственном режиме и, таким образом, могут записывать данные редактирования в этой форме:</span><span class="sxs-lookup"><span data-stu-id="7b2c2-617">For example, Microsoft Office supports the following additional formats natively and may therefore write editing data in this form:</span></span>

1.  <span data-ttu-id="7b2c2-618">WMF — метафайл Windows (формат Win 3,1)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-618">WMF -- Windows metafile (Win 3.1 format)</span></span>
2.  <span data-ttu-id="7b2c2-619">EMF — метафайл Windows "Расширенный" (формат Win32)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-619">EMF -- Windows "enhanced" metafile (Win32 format)</span></span>
3.  <span data-ttu-id="7b2c2-620">PICT — Mac OS Куиккдрав PICT File (все версии, но без записей QuickTime или других расширений)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-620">PICT -- Mac OS QuickDraw PICT file (all versions but with no QuickTime records or other extensions)</span></span>
4.  <span data-ttu-id="7b2c2-621">BMP — формат файла точечного рисунка Windows, форматы "OS/2" (БИТМАПКОРЕ), БИТМАПИНФО, BITMAPV4 и BITMAPV5</span><span class="sxs-lookup"><span data-stu-id="7b2c2-621">BMP -- Windows bitmap file format, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4, and BITMAPV5 formats</span></span>

<span data-ttu-id="7b2c2-622">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="7b2c2-622">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vector"></a><span data-ttu-id="7b2c2-623">вектор</span><span class="sxs-lookup"><span data-stu-id="7b2c2-623">vector</span></span>


```HTML
v
<!element v "( #pcdata | p )*">
```



<span data-ttu-id="7b2c2-624">Векторный графический путь кодируется как PCDATA.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-624">A vector graphic path is encoded as pcdata.</span></span> <span data-ttu-id="7b2c2-625">Содержимое элемента v является смешанным, содержащее описание векторного пути, которое может быть параметризовано с помощью элементов p.</span><span class="sxs-lookup"><span data-stu-id="7b2c2-625">The content of the v element is mixed, containing a vector path description optionally parameterized with p elements.</span></span>

[<span data-ttu-id="7b2c2-626">Назад к обзору VML</span><span class="sxs-lookup"><span data-stu-id="7b2c2-626">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

