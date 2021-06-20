---
title: Использование элемента Image
description: В этой статье описывается использование элемента Image в VML — функции, которая является устаревшей в Windows Internet Explorer 9.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Веб-семинар, элемент Image
- Разработка веб-страниц, элемент Image
- Язык VML (VML), элемент Image
- VML (язык VML), элемент Image
- Векторная графика, элемент Image
- элемент изображения
- Элементы VML, изображение
- Фигуры VML, элемент Image
- Язык VML (VML), атрибуты свойств обрезки
- VML (язык VML), атрибуты свойства кадрирования
- Векторная графика, атрибуты свойств обрезки
- Фигуры VML, атрибуты обрезки свойств
- обрезать атрибуты свойств
- Язык VML (VML), атрибут свойства усиления
- VML (язык VML), атрибут свойства усиления
- Векторная графика, атрибут свойства усиления
- Фигуры VML, атрибут свойства усиления
- получить атрибут свойства
- Язык VML (VML), контрастность
- VML (язык VML), контрастность
- Векторная графика, контрастность
- Фигуры VML, контрастность
- Язык VML (VML), атрибут свойства блакклевел
- VML (язык VML), атрибут свойства блакклевел
- Векторная графика, атрибут свойства блакклевел
- Фигуры VML, атрибут свойства блакклевел
- атрибут свойства блакклевел
- Язык VML (VML), яркость
- VML (язык VML), яркость
- Векторная графика, яркость
- Фигуры VML, яркость
- Язык VML (VML), атрибут свойства в градациях серого
- Атрибут свойства VML (язык VML), градации серого
- Векторная графика, атрибут свойства "оттенки серого"
- Фигуры VML, атрибут свойства в градациях серого
- атрибут свойства в градациях серого
- Язык VML (VML), атрибут свойства гаммы
- VML (язык VML), атрибут свойства гаммы
- Векторная графика, атрибут свойства гаммы
- Фигуры VML, атрибут гамма-свойства
- атрибут свойства гаммы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407807"
---
# <a name="using-the-image-element"></a><span data-ttu-id="999ad-144">Использование элемента Image</span><span class="sxs-lookup"><span data-stu-id="999ad-144">Using the Image Element</span></span>

<span data-ttu-id="999ad-145">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="999ad-145">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="999ad-146">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="999ad-146">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="999ad-147">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="999ad-147">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="999ad-148">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="999ad-148">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="999ad-149">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="999ad-149">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="999ad-150">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="999ad-150">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="999ad-151">Использование `<image>`</span><span class="sxs-lookup"><span data-stu-id="999ad-151">Using `<image>`</span></span>

<span data-ttu-id="999ad-152">В этом разделе показано, как использовать `<image>` элемент для отображения изображений с различными специальными эффектами.</span><span class="sxs-lookup"><span data-stu-id="999ad-152">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="999ad-153">Если вы хотите отобразить изображение, которое было загружено из внешнего источника, обычно используется `<img>` элемент, указанный в HTML, а затем атрибуту свойства **src** задается расположение файла изображения.</span><span class="sxs-lookup"><span data-stu-id="999ad-153">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="999ad-154">Кроме того, можно использовать `<image>` элемент, указанный в VML.</span><span class="sxs-lookup"><span data-stu-id="999ad-154">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="999ad-155">При использовании `<image>` элемента можно создать только один файл изображения, а затем отобразить изображение по-другому, изменив атрибуты свойства `<image>` элемента.</span><span class="sxs-lookup"><span data-stu-id="999ad-155">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="999ad-156">Кроме того, `<image>` элемент предоставляет несколько специальных эффектов, которые нельзя выполнить, просто используя `<img>` элемент HTML, например [Кадрирование](#crop), [контрастность](#contrast), [яркость](#brightness), [гамма](#gamma)и [градации серого](#grayscale).</span><span class="sxs-lookup"><span data-stu-id="999ad-156">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="999ad-157">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="999ad-157">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="999ad-158">обрезка</span><span class="sxs-lookup"><span data-stu-id="999ad-158">crop</span></span>

<span data-ttu-id="999ad-159">С помощью атрибутов свойств **кропботтом**, **кроптоп**, **кроплефт** и **кропригхт** `<image>` элемента можно отображать различные изображения, обрезанные из одного файла изображения.</span><span class="sxs-lookup"><span data-stu-id="999ad-159">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="999ad-160">Значение этих атрибутов обрезки представляет процентную отрезку от края изображения.</span><span class="sxs-lookup"><span data-stu-id="999ad-160">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="999ad-161">Значение может быть любым числом от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="999ad-161">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="999ad-162">По умолчанию значение равно 0, что обозначает отсутствие кадрирования от границы.</span><span class="sxs-lookup"><span data-stu-id="999ad-162">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="999ad-163">Значение 0,1 обозначает Кадрирование на 10 процентов от края, значение 0,15 обозначает Кадрирование на 15 процентов от края и т. д.</span><span class="sxs-lookup"><span data-stu-id="999ad-163">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="999ad-164">Например, чтобы отобразить пять изображений, обрезанных из одного и того же файла изображения, можно использовать `<image>` элемент и указать другие значения кадрирования, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="999ad-164">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

![image1.jpg (5770 байт)](images/image1.jpg)![\-2.jpg Image1 (1969 байт)](images/image1-2.jpg)![\-3.jpg Image1 (1148 байт)](images/image1-3.jpg)![\-4.jpg Image1 (1686 байт)](images/image1-4.jpg)![\-5.jpg Image1 (1364 байт)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





<span data-ttu-id="999ad-170">Первое изображение, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` не имеет значения обрезки.</span><span class="sxs-lookup"><span data-stu-id="999ad-170">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="999ad-171">Таким образом, 100% исходного изображения отображается с размером 100 пунктов на 80 точек.</span><span class="sxs-lookup"><span data-stu-id="999ad-171">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="999ad-172">Второе изображение, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` ,, имеет некоторые значения кадрирования.</span><span class="sxs-lookup"><span data-stu-id="999ad-172">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="999ad-173">`cropbottom="0.2"` Указывает, что 20 процентов изображения будут обрезаны снизу; `cropright="0.15"` указывает, что 15 процентов изображения будут обрезаны от правого края.</span><span class="sxs-lookup"><span data-stu-id="999ad-173">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="999ad-174">Оставшаяся картинка отображается с размером 85 пунктов на 64 пунктов.</span><span class="sxs-lookup"><span data-stu-id="999ad-174">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="999ad-175">Аналогичным образом, третье, четвертое и пятое изображения имеют некоторые значения кадрирования.</span><span class="sxs-lookup"><span data-stu-id="999ad-175">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="999ad-176">Исходная картинка обрезается в соответствии со значениями кадрирования, а затем отображается в соответствии со значением Width и Height.</span><span class="sxs-lookup"><span data-stu-id="999ad-176">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="999ad-177">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="999ad-177">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="999ad-178">контрастность</span><span class="sxs-lookup"><span data-stu-id="999ad-178">contrast</span></span>

<span data-ttu-id="999ad-179">С помощью атрибута свойства " **прибыль** " элемента можно `<image>` отображать различные изображения с разными параметрами контрастности.</span><span class="sxs-lookup"><span data-stu-id="999ad-179">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="999ad-180">Значением атрибута свойства **прибыль** может быть любое число.</span><span class="sxs-lookup"><span data-stu-id="999ad-180">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="999ad-181">По умолчанию значение равно 1, что означает использование той же контрастности, что и исходное изображение.</span><span class="sxs-lookup"><span data-stu-id="999ad-181">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="999ad-182">Значение 0 означает отсутствие контраста.</span><span class="sxs-lookup"><span data-stu-id="999ad-182">The value 0 indicates no contrast.</span></span> <span data-ttu-id="999ad-183">Чем больше это число, тем выше контрастность.</span><span class="sxs-lookup"><span data-stu-id="999ad-183">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="999ad-184">Например, чтобы отобразить пять изображений с разными параметрами контраста, можно использовать `<image>` элемент и задать другое значение для атрибута свойства **усиления** , как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="999ad-184">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 байт)](images/image1.jpg)![\-2.jpg изображение 2 (270 байт)](images/image2-2.jpg)![\-3.jpg изображение 2 (1919 байт)](images/image2-3.jpg)![\-4.jpg изображение 2 (3143 байт)](images/image2-4.jpg)![\-5.jpg изображение 2 (1724 байт)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="999ad-190">Если атрибут свойства **усиления** имеет значение 0, все изображение становится серым, так как нет контрастности.</span><span class="sxs-lookup"><span data-stu-id="999ad-190">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="999ad-191">Контрастность более заметна, если атрибут свойства **усиления** имеет значение 3, чем значение 0,5.</span><span class="sxs-lookup"><span data-stu-id="999ad-191">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="999ad-192">Контраст отменяется, если атрибуту свойства " **прибыль** " присвоено отрицательное значение, например-0,4.</span><span class="sxs-lookup"><span data-stu-id="999ad-192">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="999ad-193">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="999ad-193">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="999ad-194">brightness</span><span class="sxs-lookup"><span data-stu-id="999ad-194">brightness</span></span>

<span data-ttu-id="999ad-195">Атрибут свойства **блакклевел** элемента можно использовать `<image>` для просмотра различных изображений с разными настройками яркости.</span><span class="sxs-lookup"><span data-stu-id="999ad-195">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="999ad-196">Значением атрибута свойства **блакклевел** может быть любое значение в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="999ad-196">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="999ad-197">По умолчанию значение равно 0, что означает, что уровень яркости исходного изображения сохраняется.</span><span class="sxs-lookup"><span data-stu-id="999ad-197">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="999ad-198">Значение 1 указывает на самый высокий уровень яркости.</span><span class="sxs-lookup"><span data-stu-id="999ad-198">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="999ad-199">Например, чтобы отобразить пять рисунков с разными параметрами яркости, можно использовать `<image>` элемент и задать другое значение для атрибута свойства **блакклевел** , как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="999ad-199">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 байт)](images/image1.jpg)![\-2.jpg image3 (2579 байт)](images/image3-2.jpg)![\-3.jpg image3 (2330 байт)](images/image3-3.jpg)![\-4.jpg image3 (2727 байт)](images/image3-4.jpg)![\-5.jpg image3 (2435 байт)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="999ad-205">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="999ad-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="999ad-206">оттенки серого</span><span class="sxs-lookup"><span data-stu-id="999ad-206">grayscale</span></span>

<span data-ttu-id="999ad-207">С помощью атрибута свойства " **градации серого** " `<image>` элемента можно отображать изображения с оттенками серого или без них.</span><span class="sxs-lookup"><span data-stu-id="999ad-207">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="999ad-208">Значением атрибута свойства **градации серого** может быть либо true, либо false.</span><span class="sxs-lookup"><span data-stu-id="999ad-208">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="999ad-209">По умолчанию устанавливается значение false, чтобы изображение отображалось в цвете.</span><span class="sxs-lookup"><span data-stu-id="999ad-209">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="999ad-210">Если задано значение true, изображение будет отображаться в оттенках серого.</span><span class="sxs-lookup"><span data-stu-id="999ad-210">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="999ad-211">Например, как показано на следующем рисунке, первое изображение использует значение по умолчанию (false) атрибута градации серого ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="999ad-211">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="999ad-212">Поэтому изображение отображается в цвете.</span><span class="sxs-lookup"><span data-stu-id="999ad-212">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="999ad-213">На втором изображении атрибуту оттенков серого присваивается значение true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span><span class="sxs-lookup"><span data-stu-id="999ad-213">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="999ad-214">Таким образом, изображение отображается в оттенках серого, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="999ad-214">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 байт)](images/image1.jpg)![\-2.jpg image4 (2138 байт)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="999ad-217">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="999ad-217">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="999ad-218">gamma</span><span class="sxs-lookup"><span data-stu-id="999ad-218">gamma</span></span>

<span data-ttu-id="999ad-219">Атрибут свойства **гаммы** элемента можно использовать `<image>` для вывода изображений с разными параметрами гаммы.</span><span class="sxs-lookup"><span data-stu-id="999ad-219">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="999ad-220">Значением атрибута гамма свойства может быть любое значение от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="999ad-220">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="999ad-221">По умолчанию устанавливается значение 1.</span><span class="sxs-lookup"><span data-stu-id="999ad-221">By default, the value is set to 1.</span></span>

<span data-ttu-id="999ad-222">Например, чтобы отобразить три рисунка с разными параметрами гаммы, можно использовать `<image>` элемент и задать другое значение атрибута **гамма** свойства, как показано в следующем представлении VML:</span><span class="sxs-lookup"><span data-stu-id="999ad-222">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![\-1.jpg image5 (2714 байт)](images/image5-1.jpg)![\-2.jpg image5 (2729 байт)](images/image5-2.jpg)![\-3.jpg image5 (2726 байт)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="999ad-226">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="999ad-226">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 