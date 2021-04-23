---
title: Атрибут Курдоригин VML
description: Атрибут Курдоригин VML
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890696"
---
# <a name="vml-coordorigin-attribute"></a><span data-ttu-id="b9796-103">Атрибут Курдоригин VML</span><span class="sxs-lookup"><span data-stu-id="b9796-103">VML CoordOrigin Attribute</span></span>

<span data-ttu-id="b9796-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b9796-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b9796-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b9796-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b9796-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b9796-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b9796-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b9796-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b9796-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b9796-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b9796-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b9796-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b9796-110">Указывает происхождение единицы координат прямоугольника, ограничивающего фигуру.</span><span class="sxs-lookup"><span data-stu-id="b9796-110">Specifies the coordinate unit origin of the rectangle that bounds a shape.</span></span> <span data-ttu-id="b9796-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b9796-111">Read/write.</span></span> <span data-ttu-id="b9796-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="b9796-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="b9796-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="b9796-113">**Applies To**</span></span>

[<span data-ttu-id="b9796-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="b9796-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b9796-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="b9796-115">**Tag Syntax**</span></span>

<span data-ttu-id="b9796-116"><v: *element* курдоригин = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="b9796-116"><v: *element* coordorigin=" *expression* "></span></span>

<span data-ttu-id="b9796-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="b9796-117">**Script Syntax**</span></span>

<span data-ttu-id="b9796-118">*element* . курдоригин = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="b9796-118">*element* .coordorigin="*expression*"</span></span>

<span data-ttu-id="b9796-119">*выражение* = *element*. курдоригин</span><span class="sxs-lookup"><span data-stu-id="b9796-119">*expression*=*element*.coordorigin</span></span>

<span data-ttu-id="b9796-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b9796-120">**Remarks**</span></span>

<span data-ttu-id="b9796-121">Если значение не указано, координаты источника равны (0, 0) в левом верхнем углу ограничивающего прямоугольника фигуры.</span><span class="sxs-lookup"><span data-stu-id="b9796-121">If not specified, the origin coordinates are (0,0) at the top left corner of the shape bounding box.</span></span>

<span data-ttu-id="b9796-122">Значение x **курдсизе** добавляется к значению x объекта **курдоригин** , чтобы определить диапазон горизонтальных значений.</span><span class="sxs-lookup"><span data-stu-id="b9796-122">The x value of **CoordSize** is added to the x value of **CoordOrigin** to determine the range of the horizontal values.</span></span> <span data-ttu-id="b9796-123">Например, если значение x **курдоригин** равно-100, а значение x **курдсизе** — 200, то горизонтальные единицы будут находиться в диапазоне от-100 до + 100.</span><span class="sxs-lookup"><span data-stu-id="b9796-123">For example,if the x value of **CoordOrigin** is -100 and the x value of **CoordSize** is 200, the horizontal units will range from -100 to +100.</span></span> <span data-ttu-id="b9796-124">Если значение x **курдоригин** равно 100, а значение x **курдсизе** равно 200, то горизонтальные единицы будут находиться в диапазоне от 100 до 300, все в пределах ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="b9796-124">If the x value of **CoordOrigin** is 100 and the x value of **CoordSize** is 200, the horizontal units will range from 100 to 300, all within the bounding box.</span></span> <span data-ttu-id="b9796-125">То же самое справедливо и для значений y.</span><span class="sxs-lookup"><span data-stu-id="b9796-125">The same is true for the y values.</span></span>

<span data-ttu-id="b9796-126">Обратите внимание, что этот атрибут является вектором, а единицы измерения совпадают с типом Unit, [курдсизе](msdn-online-vml-coordsize-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="b9796-126">Note that this attribute is a vector and that the units are the same type of unit as [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span></span>

<span data-ttu-id="b9796-127">В сценариях, поскольку это Двумерные векторы, можно получить доступ к значениям x и y по отдельности, а также определить ожидаемый тип единиц.</span><span class="sxs-lookup"><span data-stu-id="b9796-127">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="b9796-128">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="b9796-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="b9796-129">**Пример**</span><span class="sxs-lookup"><span data-stu-id="b9796-129">**Example**</span></span>

<span data-ttu-id="b9796-130">Центром ограничивающего прямоугольника будет источник (0, 0) контура для фигуры.</span><span class="sxs-lookup"><span data-stu-id="b9796-130">The center of the bounding box will be the origin (0,0) of the path for the shape.</span></span> <span data-ttu-id="b9796-131">Так как **курдоригин** имеет значение "-500-500", а **курдсизе** — "1000 1000", горизонтальные и вертикальные единицы будут находиться в диапазоне от-500 до + 500.</span><span class="sxs-lookup"><span data-stu-id="b9796-131">Because **CoordOrigin** is "-500 -500" and **CoordSize** is "1000 1000", the horizontal and vertical units will range from -500 to +500.</span></span> <span data-ttu-id="b9796-132">Левый и верхний угол пути будут находиться в центре ограничивающего прямоугольника, определяемого левым и верхним точками, как определено **стилем**.</span><span class="sxs-lookup"><span data-stu-id="b9796-132">The left and top corner of the path will be at the center of the bounding box defined by the left and top points as defined by **Style**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="b9796-133">[Пример атрибута курдоригин](/previous-versions/bb229664(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b9796-133">[CoordOrigin Attribute Example](/previous-versions/bb229664(v=vs.85)).</span></span> <span data-ttu-id="b9796-134">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="b9796-134">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 