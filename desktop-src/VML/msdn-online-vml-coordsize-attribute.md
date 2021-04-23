---
title: Атрибут Курдсизе VML
description: Атрибут Курдсизе VML
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691524"
---
# <a name="vml-coordsize-attribute"></a><span data-ttu-id="39e15-103">Атрибут Курдсизе VML</span><span class="sxs-lookup"><span data-stu-id="39e15-103">VML CoordSize Attribute</span></span>

<span data-ttu-id="39e15-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="39e15-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="39e15-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="39e15-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="39e15-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="39e15-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="39e15-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="39e15-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="39e15-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="39e15-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="39e15-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="39e15-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="39e15-110">Задает горизонтальные и вертикальные единицы прямоугольника, ограничивающего фигуру.</span><span class="sxs-lookup"><span data-stu-id="39e15-110">Specifies the horizontal and vertical units of the rectangle that bounds a shape.</span></span> <span data-ttu-id="39e15-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="39e15-111">Read/write.</span></span> <span data-ttu-id="39e15-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="39e15-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="39e15-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="39e15-113">**Applies To**</span></span>

[<span data-ttu-id="39e15-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="39e15-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="39e15-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="39e15-115">**Tag Syntax**</span></span>

<span data-ttu-id="39e15-116"><v: *element* курдсизе = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="39e15-116"><v: *element* coordsize=" *expression* "></span></span>

<span data-ttu-id="39e15-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="39e15-117">**Script Syntax**</span></span>

<span data-ttu-id="39e15-118">*element* . курдсизе = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="39e15-118">*element* .coordsize="*expression*"</span></span>

<span data-ttu-id="39e15-119">*выражение* = *element*. курдсизе</span><span class="sxs-lookup"><span data-stu-id="39e15-119">*expression*=*element*.coordsize</span></span>

<span data-ttu-id="39e15-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="39e15-120">**Remarks**</span></span>

<span data-ttu-id="39e15-121">Если значение не указано, то размер координат совпадает с ограничивающим прямоугольником фигуры.</span><span class="sxs-lookup"><span data-stu-id="39e15-121">If not specified, the coordinate size is the same as the bounding box of the shape.</span></span>

<span data-ttu-id="39e15-122">Обратите внимание, что этот атрибут является вектором и единицы измерения зависят от длины и ширины ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="39e15-122">Note that this attribute is a vector and that the units are relative to the length and width of the bounding rectangle.</span></span>

<span data-ttu-id="39e15-123">Также обратите внимание, что сопоставление между **курдсизе** и ограничивающим прямоугольником можно сделать анизотропным.</span><span class="sxs-lookup"><span data-stu-id="39e15-123">Also note that mapping between **coordsize** and the bounding box can be made anisotropic.</span></span> <span data-ttu-id="39e15-124">Убедитесь, что ширина и высота **курдсизе** совпадают с **высотой** и **высотой** **стиля** , если вы не хотите искажать форму.</span><span class="sxs-lookup"><span data-stu-id="39e15-124">Make sure that the **coordsize width** and **coordsize height** is the same as the **style width** and **height** if you don't want to distort the shape.</span></span>

<span data-ttu-id="39e15-125">В сценариях, поскольку это Двумерные векторы, можно получить доступ к значениям x и y по отдельности, а также определить ожидаемый тип единиц.</span><span class="sxs-lookup"><span data-stu-id="39e15-125">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="39e15-126">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="39e15-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="39e15-127">**Пример**</span><span class="sxs-lookup"><span data-stu-id="39e15-127">**Example**</span></span>

<span data-ttu-id="39e15-128">Фигура имеет 100 точек высокого уровня и 100 точек в ширину, но каждая горизонтальная и вертикальная единицы в пространстве координат составляет 1/10 точек.</span><span class="sxs-lookup"><span data-stu-id="39e15-128">The shape is 100 points high and 100 points wide, but each horizontal and vertical unit in the coordinate space is 1/10 of a point.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="39e15-129">[Пример атрибута курдсизе](/previous-versions/bb229665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="39e15-129">[CoordSize Attribute Example](/previous-versions/bb229665(v=vs.85)).</span></span> <span data-ttu-id="39e15-130">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="39e15-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 