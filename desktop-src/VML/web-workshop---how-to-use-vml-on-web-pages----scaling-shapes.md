---
title: Масштабирование фигур
description: Масштабирование фигур
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Веб-семинар, масштабирование фигур
- Разработка веб-страниц, масштабирование фигур
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
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792103"
---
# <a name="scaling-shapes"></a><span data-ttu-id="8be99-115">Масштабирование фигур</span><span class="sxs-lookup"><span data-stu-id="8be99-115">Scaling Shapes</span></span>

<span data-ttu-id="8be99-116">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8be99-116">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8be99-117">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="8be99-117">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8be99-118">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="8be99-118">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8be99-119">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8be99-119">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8be99-120">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8be99-120">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8be99-121">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8be99-121">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8be99-122">Вы узнали, как рисовать и цветировать фигуры на веб-странице с помощью VML.</span><span class="sxs-lookup"><span data-stu-id="8be99-122">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="8be99-123">В этом разделе показано, как масштабировать фигуры до нужного размера.</span><span class="sxs-lookup"><span data-stu-id="8be99-123">In this topic, we will illustrate how to scale shapes to any size you want.</span></span>

<span data-ttu-id="8be99-124">VML использует тот же синтаксис, что и в разделе [сведения о модели визуальной визуализации](https://www.w3.org/TR/PR-CSS2/visudet.mdl) [спецификации CSS2](https://www.w3.org/TR/PR-CSS2/) , чтобы указать размер содержащего поля, чтобы содержимое фигуры было визуализировано (отображено) в пределах содержащего поля.</span><span class="sxs-lookup"><span data-stu-id="8be99-124">VML uses the same syntax defined in the [Visual Rendering Model Details](https://www.w3.org/TR/PR-CSS2/visudet.mdl) section of the [CSS2 specification](https://www.w3.org/TR/PR-CSS2/) to specify the size of the containing box so that the contents of a shape will be rendered (drawn) within the containing box.</span></span> <span data-ttu-id="8be99-125">Для определения размера содержащего поля можно использовать атрибуты стиля **Width** и **Height** .</span><span class="sxs-lookup"><span data-stu-id="8be99-125">You can use the **width** and **height** style attributes to define the size of the containing box.</span></span>

<span data-ttu-id="8be99-126">Например, если вы рисуете овал и указали **Style**= "Width: 75pt; Height: 100pt", овал будет рисоваться внутри содержащего поля с размером 75 точек (ширина) на 100 пунктов (высота), как показано на следующем рисунке:</span><span class="sxs-lookup"><span data-stu-id="8be99-126">For example, if you draw an oval and specify **style**='width:75pt;height:100pt', the oval will be drawn within a containing box at a size of 75 points (width) by 100 points (height), as shown in the following picture:</span></span>

![oval1.gif (660 байт)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





<span data-ttu-id="8be99-128">Если изменить размер на **Style**= "Width: 120pt; Height: 140pt", овал становится больше, так как он масштабируется внутри нового содержащего поля с размером 120 пунктов (ширина) на 140 пунктов (высота), как показано на следующем рисунке:</span><span class="sxs-lookup"><span data-stu-id="8be99-128">If you change the size to **style**='width:120pt;height:140pt', the oval becomes larger because it is scaled within the new containing box at a size of 120 points (width) by 140 points (height), as shown in the following picture:</span></span>

![oval2.gif (966 байт)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





<span data-ttu-id="8be99-130">При изменении размера на **Style**= "Width: 60PT; Height: 40pt" овал становится меньше, так как он масштабируется в пределах нового содержащего поля с размером 60 пунктов (ширина) на 40 пунктов (высота), как показано на следующем рисунке:</span><span class="sxs-lookup"><span data-stu-id="8be99-130">If you change the size to **style**='width:60pt;height:40pt', the oval becomes smaller because it is scaled within the new containing box at a size of 60 points (width) by 40 points (height), as shown in the following picture:</span></span>

![oval3.gif (394 байт)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 