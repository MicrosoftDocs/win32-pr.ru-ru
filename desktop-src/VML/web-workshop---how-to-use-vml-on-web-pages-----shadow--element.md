---
title: Использование элемента Shadow
description: Использование элемента Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Веб-семинар, элемент Shadow
- Проектирование веб-страниц, элемент Shadow
- Язык VML (VML), элемент Shadow
- VML (язык VML), элемент Shadow
- Векторная графика, элемент Shadow
- элемент Shadow
- Элементы VML, тень
- Фигуры VML, элемент Shadow
- Язык VML (VML), Рисование с помощью эффектов тени
- VML (язык VML), Рисование с помощью эффектов тени
- Векторная графика, Рисование с помощью эффектов тени
- Фигуры VML, Рисование с помощью эффектов тени
- Рисование с помощью эффектов тени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe32651fbeab6b84b49a40bae05a08ba3d9c33a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413563"
---
# <a name="using-the-shadow-element"></a><span data-ttu-id="7de7b-116">Использование элемента Shadow</span><span class="sxs-lookup"><span data-stu-id="7de7b-116">Using the Shadow Element</span></span>

<span data-ttu-id="7de7b-117">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7de7b-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7de7b-118">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="7de7b-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7de7b-119">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="7de7b-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7de7b-120">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7de7b-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7de7b-121">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7de7b-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7de7b-122">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7de7b-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7de7b-123">В этом разделе будет показано, как использовать `<shadow>` вложенный элемент для рисования фигуры с различными эффектами тени.</span><span class="sxs-lookup"><span data-stu-id="7de7b-123">In this topic, we will illustrate how to use the `<shadow>` sub-element to draw a shape that has various shadow effects.</span></span>

<span data-ttu-id="7de7b-124">`<shadow>`Вложенный элемент можно поместить внутри `<shape>` , `<shapetype>` или любого предопределенного элемента Shape, чтобы нарисовать фигуру с тенью.</span><span class="sxs-lookup"><span data-stu-id="7de7b-124">You can place the `<shadow>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to draw a shape with a shadow.</span></span> <span data-ttu-id="7de7b-125">Затем можно использовать атрибуты свойств `<shadow>` вложенного элемента для настройки тени.</span><span class="sxs-lookup"><span data-stu-id="7de7b-125">You can then use the property attributes of the `<shadow>` sub-element to customize the shadow.</span></span>

<span data-ttu-id="7de7b-126">Например, чтобы создать фигуру с тенью, как показано на следующем рисунке, в `<BODY>` области веб-страницы можно ввести следующие строки:</span><span class="sxs-lookup"><span data-stu-id="7de7b-126">For example, to create a shape with a shadow, as shown in the following picture, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![shape1.gif (887 байт)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   <span data-ttu-id="7de7b-128">`on="t"` и `type="perspective"` указывают на включение тени с помощью типа перспективы.</span><span class="sxs-lookup"><span data-stu-id="7de7b-128">`on="t"` and `type="perspective"` indicate to turn on the shadow using the perspective type.</span></span>
-   <span data-ttu-id="7de7b-129">**Источник** и **смещение** указывают, где следует нарисовать тень.</span><span class="sxs-lookup"><span data-stu-id="7de7b-129">The **origin** and **offset** indicate where to draw the shadow.</span></span>
-   <span data-ttu-id="7de7b-130">`matrix="..."` Указывает матрицу преобразования перспективы.</span><span class="sxs-lookup"><span data-stu-id="7de7b-130">`matrix="..."` specifies the perspective transform matrix.</span></span>

<span data-ttu-id="7de7b-131">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span><span class="sxs-lookup"><span data-stu-id="7de7b-131">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span></span>

 

 