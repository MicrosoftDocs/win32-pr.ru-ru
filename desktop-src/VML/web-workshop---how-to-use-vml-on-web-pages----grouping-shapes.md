---
title: Группирование фигур
description: В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Веб-семинар, Группирование фигур
- Проектирование веб-страниц, Группирование фигур
- Язык VML (VML), Группирование фигур
- VML (язык VML), Группирование фигур
- Векторная графика, Группирование фигур
- Фигуры VML, группирование
- Группирование фигур
- Язык VML (VML), элемент Group
- VML (язык VML), элемент Group
- Векторная графика, элемент Group
- элемент группы
- Элементы VML, Группа
- Язык VML (VML), локальное пространство координат
- VML (язык VML), локальное пространство координат
- Векторная графика, локальное пространство координат
- Локальное пространство координат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eed282094e2d24d2d27e338b93731eaaa1eec0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070522"
---
# <a name="grouping-shapes"></a><span data-ttu-id="32c79-120">Группирование фигур</span><span class="sxs-lookup"><span data-stu-id="32c79-120">Grouping Shapes</span></span>

<span data-ttu-id="32c79-121">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="32c79-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="32c79-122">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="32c79-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="32c79-123">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="32c79-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="32c79-124">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="32c79-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="32c79-125">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="32c79-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="32c79-126">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="32c79-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="32c79-127">Как вы узнали, вы можете легко рисовать отдельные фигуры с помощью VML.</span><span class="sxs-lookup"><span data-stu-id="32c79-127">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="32c79-128">В этом разделе будут объяснены преимущества группирования фигур и группирования фигур.</span><span class="sxs-lookup"><span data-stu-id="32c79-128">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="32c79-129">Если у вас много фигур, которые необходимо масштабировать, переместить или поворачивать вместе, можно было бы задать атрибуты отдельно для каждой фигуры.</span><span class="sxs-lookup"><span data-stu-id="32c79-129">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="32c79-130">Кроме того, вы порождаете поля для ошибок.</span><span class="sxs-lookup"><span data-stu-id="32c79-130">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="32c79-131">Было бы лучше, если бы вы могли сгруппировать фигуры, а затем задать атрибуты для всей группы.</span><span class="sxs-lookup"><span data-stu-id="32c79-131">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="32c79-132">В VML можно использовать `<group>` элемент для группировки многих фигур вместе, чтобы их можно было преобразовать как одну единицу.</span><span class="sxs-lookup"><span data-stu-id="32c79-132">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="32c79-133">Например, как показано в следующем представлении VML, можно легко сгруппировать две фигуры.</span><span class="sxs-lookup"><span data-stu-id="32c79-133">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="32c79-134">Если фигуры сгруппированы, они используют [Локальное пространство координат](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) группы.</span><span class="sxs-lookup"><span data-stu-id="32c79-134">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="32c79-135">Таким образом, фигуры внутри группы можно масштабировать и перемещать вместе.</span><span class="sxs-lookup"><span data-stu-id="32c79-135">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="32c79-136">В разделе Использование локального пространства координат вы увидите дополнительные примеры.</span><span class="sxs-lookup"><span data-stu-id="32c79-136">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="32c79-137">Внутри группы можно создать любое количество фигур или групп.</span><span class="sxs-lookup"><span data-stu-id="32c79-137">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="32c79-138">Если группа находится внутри другой группы, она называется "вложенная группа".</span><span class="sxs-lookup"><span data-stu-id="32c79-138">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="32c79-139">На уровни вложенности нет ограничений.</span><span class="sxs-lookup"><span data-stu-id="32c79-139">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="32c79-140">Например, в следующих строках показана 3-уровневая вложенная группа.</span><span class="sxs-lookup"><span data-stu-id="32c79-140">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="32c79-141">Shape3 и Shape4 находятся в Граупк.</span><span class="sxs-lookup"><span data-stu-id="32c79-141">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="32c79-142">Shape2 и Граупк находятся в Граупб.</span><span class="sxs-lookup"><span data-stu-id="32c79-142">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="32c79-143">Shape1 и Граупб находятся в группе a.</span><span class="sxs-lookup"><span data-stu-id="32c79-143">Shape1 and GroupB are in GroupA.</span></span>


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



<span data-ttu-id="32c79-144">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span><span class="sxs-lookup"><span data-stu-id="32c79-144">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="32c79-145">[![назад ](images/top.gif) к началу](#top)</span><span class="sxs-lookup"><span data-stu-id="32c79-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="32c79-146">Сводка</span><span class="sxs-lookup"><span data-stu-id="32c79-146">Summary</span></span>

<span data-ttu-id="32c79-147">Элемент можно использовать `<group>` для группировки многих фигур вместе, чтобы их можно было преобразовать как одну единицу.</span><span class="sxs-lookup"><span data-stu-id="32c79-147">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 