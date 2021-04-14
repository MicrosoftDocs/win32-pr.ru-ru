---
title: Использование элемента Шапетипе
description: Использование элемента Шапетипе
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Веб-семинар, элемент шапетипе
- Разработка веб-страниц, элемент шапетипе
- Язык VML (VML), элемент шапетипе
- VML (язык VML), элемент шапетипе
- Векторная графика, элемент шапетипе
- шапетипе, элемент
- Элементы VML, шапетипе
- Фигуры VML, элемент шапетипе
- Язык VML (VML), определение часто используемых фигур
- VML (язык VML), определение часто используемых фигур
- Векторная графика, определение часто используемых фигур
- определение часто используемых фигур
- Фигуры VML, определение часто используемых
- Язык VML (VML), создание копий фигур
- VML (язык VML), создание копий фигур
- Векторная графика, создание экземпляров фигур
- Создание экземпляров фигур
- Фигуры VML, создание экземпляров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488169"
---
# <a name="using-the-shapetype-element"></a><span data-ttu-id="a6d51-121">Использование элемента Шапетипе</span><span class="sxs-lookup"><span data-stu-id="a6d51-121">Using the Shapetype Element</span></span>

<span data-ttu-id="a6d51-122">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a6d51-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a6d51-123">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="a6d51-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a6d51-124">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="a6d51-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a6d51-125">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a6d51-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a6d51-126">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a6d51-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a6d51-127">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a6d51-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a6d51-128">В этом разделе мы продемонстрируем, как использовать `<shapetype>` элемент для определения собственных часто используемых форм, а также создания экземпляров и создание фигур из шапетипе.</span><span class="sxs-lookup"><span data-stu-id="a6d51-128">In this topic, we will illustrate how to use the `<shapetype>` element to define your own frequently-used shapes and then instantiate, or create, shapes from the shapetype.</span></span>

<span data-ttu-id="a6d51-129">Если вы хотите нарисовать множество фигур с одинаковыми или похожими свойствами, это было бы утомительным, если пришлось бы многократно вводить одни и те же атрибуты свойств для каждой фигуры.</span><span class="sxs-lookup"><span data-stu-id="a6d51-129">If you wanted to draw many shapes that have the same or similar properties, it would be tedious if you had to repeatedly type the same property attributes for each shape.</span></span> <span data-ttu-id="a6d51-130">VML предоставляет `<shapetype>` элемент, чтобы можно было определить прототип фигуры.</span><span class="sxs-lookup"><span data-stu-id="a6d51-130">VML provides the `<shapetype>` element so that you can define a prototype of a shape.</span></span> <span data-ttu-id="a6d51-131">Затем можно использовать `<shape>` элемент для создания экземпляра нескольких копий фигур из одного шапетипе.</span><span class="sxs-lookup"><span data-stu-id="a6d51-131">You can then use the `<shape>` element to instantiate many copies of shapes from the same shapetype.</span></span>

<span data-ttu-id="a6d51-132">Вы можете выполнить три шага, чтобы определить шапетипе, а затем создать экземпляр Shape из шапетипе:</span><span class="sxs-lookup"><span data-stu-id="a6d51-132">You can follow the three steps to define a shapetype, and then instantiate a shape from the shapetype:</span></span>

1.  <span data-ttu-id="a6d51-133">Введите `<shapetype>` элемент и присвойте ему имя, указав атрибут ID.</span><span class="sxs-lookup"><span data-stu-id="a6d51-133">Type a `<shapetype>` element and give it a name by specifying the id attribute.</span></span>
2.  <span data-ttu-id="a6d51-134">Опишите шапетипе с помощью атрибутов свойств или вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="a6d51-134">Describe the shapetype by using its property attributes or sub-elements.</span></span>
3.  <span data-ttu-id="a6d51-135">Создание экземпляра фигуры путем ввода `<shape>` элемента и ссылки на атрибут типа Shape на атрибут ID объекта шапетипе.</span><span class="sxs-lookup"><span data-stu-id="a6d51-135">Instantiate a shape by typing a `<shape>` element, and refer the type attribute of the shape to the id attribute of the shapetype.</span></span>

<span data-ttu-id="a6d51-136">Например, введите следующие строки, чтобы создать шапетипе с именем "Мишапе":</span><span class="sxs-lookup"><span data-stu-id="a6d51-136">For example, you type the following lines to create a shapetype called "MyShape":</span></span>


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



<span data-ttu-id="a6d51-137">Затем вы изменяете шапетипе, задавая некоторые атрибуты свойств, такие как `fillcolor="red" strokecolor="blue"` .</span><span class="sxs-lookup"><span data-stu-id="a6d51-137">Then, you alter the shapetype by setting some property attributes, such as `fillcolor="red" strokecolor="blue"`.</span></span> <span data-ttu-id="a6d51-138">Кроме того, можно использовать вложенные элементы внутри шапетипе, такие как `<path>` , `<fill>` `<stroke>` (мы поговорим об этих подэлементах в следующих разделах).</span><span class="sxs-lookup"><span data-stu-id="a6d51-138">Or, you can use sub-elements inside the shapetype, such as `<path>`, `<fill>`, `<stroke>` (we will talk about those sub-elements in later topics).</span></span>


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



<span data-ttu-id="a6d51-139">Затем создается экземпляр фигуры из шапетипе "Мишапе" путем указания `type="#MyShape"` , как показано в следующем представлении VML.</span><span class="sxs-lookup"><span data-stu-id="a6d51-139">Then, you instantiate a shape from the shapetype "MyShape" by specifying `type="#MyShape"`, as shown in the following VML representation.</span></span> <span data-ttu-id="a6d51-140">Эта фигура наследует все свойства от шапетипе "Мишапе" и отображается в его содержащем поле размером 100 на 80.</span><span class="sxs-lookup"><span data-stu-id="a6d51-140">This shape inherits all properties from the shapetype "MyShape", and is displayed within its containing box at a size of 100 by 80.</span></span>


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



<span data-ttu-id="a6d51-141">Можно создать экземпляр другой фигуры из шапетипе "Мишапе", указав `type="#MyShape"` и перезапишу некоторые свойства, такие как `fillcolor="maroon"` , как показано в следующем представлении VML.</span><span class="sxs-lookup"><span data-stu-id="a6d51-141">You can instantiate another shape from the shapetype "MyShape" by specifying `type="#MyShape"` and overwrite some properties, such as `fillcolor="maroon"`, as shown in the following VML representation.</span></span> <span data-ttu-id="a6d51-142">Эта фигура наследует все свойства от шапетипе "Мишапе", за исключением свойства FillColor, и отображается в его содержащем поле размером 70 на 90.</span><span class="sxs-lookup"><span data-stu-id="a6d51-142">This shape inherits all properties from the shapetype "MyShape" except the fillcolor property, and is displayed within its containing box at a size of 70 by 90.</span></span>


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



<span data-ttu-id="a6d51-143">Ниже приведено полное представление VML для предыдущего примера.</span><span class="sxs-lookup"><span data-stu-id="a6d51-143">Here is the complete VML representation for the preceding example:</span></span>

![\-1.gif Type1 (477 байт)](images/type1-1.gif)![\-2.gif Type1 (471 байт)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





<span data-ttu-id="a6d51-146">Как вы узнали, при создании экземпляра Shape из шапетипе он наследует все атрибуты свойств из шапетипе.</span><span class="sxs-lookup"><span data-stu-id="a6d51-146">As you've learned, when a shape is instantiated from a shapetype, it inherits all of the property attributes from the shapetype.</span></span> <span data-ttu-id="a6d51-147">Некоторые или все наследуемые атрибуты можно перезаписать путем переопределения атрибутов внутри `<shape>` элемента.</span><span class="sxs-lookup"><span data-stu-id="a6d51-147">You can overwrite some or all of the inherited attributes by redefining attributes inside the `<shape>` element.</span></span> <span data-ttu-id="a6d51-148">Имейте в виду, что наследование имеет только один уровень.</span><span class="sxs-lookup"><span data-stu-id="a6d51-148">Be aware that the inheritance is only one level.</span></span> <span data-ttu-id="a6d51-149">Это связано с тем, что только `<shape>` элемент может ссылаться на `<shapetype>` элемент.</span><span class="sxs-lookup"><span data-stu-id="a6d51-149">This is because only a `<shape>` element can reference a `<shapetype>` element.</span></span> <span data-ttu-id="a6d51-150">`<shapetype>`Элемент не может ссылаться на другой `<shapetype>` элемент.</span><span class="sxs-lookup"><span data-stu-id="a6d51-150">A `<shapetype>` element cannot reference another `<shapetype>` element.</span></span>

<span data-ttu-id="a6d51-151">Кроме того, шапетипе не принадлежит ни к одной группе.</span><span class="sxs-lookup"><span data-stu-id="a6d51-151">Also, a shapetype doesn't belong to any group.</span></span> <span data-ttu-id="a6d51-152">Таким образом, `<shapetype>` элемент может располагаться сам по себе или внутри `<group>` элемента.</span><span class="sxs-lookup"><span data-stu-id="a6d51-152">Therefore, the `<shapetype>` element can appear by itself or inside a `<group>` element.</span></span> <span data-ttu-id="a6d51-153">В разных группах можно использовать несколько фигур, ссылающихся на один шапетипе.</span><span class="sxs-lookup"><span data-stu-id="a6d51-153">You can have many shapes inside different groups that reference the same shapetype.</span></span> <span data-ttu-id="a6d51-154">Если шапетипе находится внутри группы, то фигура, которая находится в другой группе, по-прежнему может ссылаться на этот шапетипе.</span><span class="sxs-lookup"><span data-stu-id="a6d51-154">If a shapetype appears inside a group, a shape living in another group can still reference this shapetype.</span></span>

<span data-ttu-id="a6d51-155">Например, в следующем представлении VML Прямоуг1 и rect2 находятся в группе a, а Rect3 — в Граупб.</span><span class="sxs-lookup"><span data-stu-id="a6d51-155">For example, in the following VML representation, Rect1 and Rect2 are in GroupA, and Rect3 is in GroupB.</span></span> <span data-ttu-id="a6d51-156">Все три прямоугольника создаются из Мишапе шапетипе.</span><span class="sxs-lookup"><span data-stu-id="a6d51-156">All three rectangles are instantiated from MyShape shapetype.</span></span>


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



<span data-ttu-id="a6d51-157">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span><span class="sxs-lookup"><span data-stu-id="a6d51-157">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span></span>

 

 