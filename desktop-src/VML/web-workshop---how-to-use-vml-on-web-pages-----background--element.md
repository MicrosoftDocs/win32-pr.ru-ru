---
title: Использование элемента Background
description: Использование элемента Background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Веб-семинар, элемент Background
- Разработка веб-страниц, элемент Background
- Язык VML (VML), элемент Background
- VML (язык VML), элемент Background
- Векторная графика, элемент Background
- элемент Background
- Элементы VML, фон
- Фигуры VML, элемент Background
- Язык VML (VML), Настройка фона
- VML (язык VML), Настройка фона
- Векторная графика, Настройка фона
- Фигуры VML, Настройка фона
- Настройка фона
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890744"
---
# <a name="using-the-background-element"></a><span data-ttu-id="e37de-116">Использование элемента Background</span><span class="sxs-lookup"><span data-stu-id="e37de-116">Using the Background Element</span></span>

<span data-ttu-id="e37de-117">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e37de-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e37de-118">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="e37de-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e37de-119">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="e37de-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e37de-120">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e37de-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e37de-121">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e37de-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e37de-122">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e37de-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e37de-123">В этом разделе мы рассмотрим, как можно настроить фон веб-страницы с помощью `<background>` элемента, указанного в VML.</span><span class="sxs-lookup"><span data-stu-id="e37de-123">In this topic, we will illustrate how you can customize the background of a Web page by using the `<background>` element provided in VML.</span></span>

<span data-ttu-id="e37de-124">Как вы узнали из раздела [ `<fill>` use](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) , можно поместить `<fill>` вложенный элемент внутри `<shape>` , `<shapetype>` или любого предопределенного элемента Shape, чтобы описать, как заполнить фигуру.</span><span class="sxs-lookup"><span data-stu-id="e37de-124">As you've learned from the [Use `<fill>`](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) topic, you can place the `<fill>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span>

<span data-ttu-id="e37de-125">Аналогичным образом можно поместить `<fill>` вложенный элемент внутри `<background>` элемента, чтобы описать, как заполнять фон веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="e37de-125">Similarly, you can place the `<fill>` sub-element inside the `<background>` element to describe how to fill the background of a Web page.</span></span> <span data-ttu-id="e37de-126">Затем можно использовать атрибуты свойств `<fill>` вложенного элемента для настройки заливки, такие как [Градиентная заливка](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [узорная заливка](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)или [Заливка рисунков](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span><span class="sxs-lookup"><span data-stu-id="e37de-126">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [pattern fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), or [picture fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span></span>

<span data-ttu-id="e37de-127">Например, для рисования фона, заполненного градиентом, можно ввести следующие строки в `<BODY>` области веб-страницы:</span><span class="sxs-lookup"><span data-stu-id="e37de-127">For example, to draw a gradient-filled background, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





<span data-ttu-id="e37de-128">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span><span class="sxs-lookup"><span data-stu-id="e37de-128">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span></span>

 

 