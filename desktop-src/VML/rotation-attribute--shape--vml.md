---
title: Атрибут вращения (Shape) (VML)
description: Атрибут вращения (Shape) (VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070570"
---
# <a name="rotation-attribute-shapevml"></a><span data-ttu-id="6ce0b-103">Атрибут вращения (Shape) (VML)</span><span class="sxs-lookup"><span data-stu-id="6ce0b-103">Rotation Attribute (Shape)(VML)</span></span>

<span data-ttu-id="6ce0b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6ce0b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6ce0b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6ce0b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6ce0b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6ce0b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6ce0b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6ce0b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6ce0b-110">Определяет угол поворота фигуры.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-110">Defines the angle that a shape is rotated.</span></span> <span data-ttu-id="6ce0b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-111">Read/write.</span></span> <span data-ttu-id="6ce0b-112">[Вганглеиндегрис](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="6ce0b-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span>

<span data-ttu-id="6ce0b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="6ce0b-113">**Applies To**</span></span>

[<span data-ttu-id="6ce0b-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="6ce0b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="6ce0b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="6ce0b-115">**Tag Syntax**</span></span>

<span data-ttu-id="6ce0b-116"><v: Style *элемента* = "вращение: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="6ce0b-116"><v: *element* style="rotation: *expression* "></span></span>

<span data-ttu-id="6ce0b-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="6ce0b-117">**Script Syntax**</span></span>

<span data-ttu-id="6ce0b-118">*element* . вращение = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="6ce0b-118">*element* .rotation="*expression*"</span></span>

<span data-ttu-id="6ce0b-119">*выражение* = *element*. вращение</span><span class="sxs-lookup"><span data-stu-id="6ce0b-119">*expression*=*element*.rotation</span></span>

<span data-ttu-id="6ce0b-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="6ce0b-120">**Remarks**</span></span>

<span data-ttu-id="6ce0b-121">Значение в градусах может быть положительным или отрицательным, а значения, превышающие 360, добавляются в модуль в виде круга 360 градусов.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-121">The value in degrees can be positive or negative, and values greater than 360 are modularized to a 360-degree circle.</span></span> <span data-ttu-id="6ce0b-122">Положительные углы — по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-122">Positive angles are clockwise.</span></span> <span data-ttu-id="6ce0b-123">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-123">The default value is 0.</span></span>

<span data-ttu-id="6ce0b-124">Обратите внимание, что фигура перемещается после поворота для отражения новых координат ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-124">Note that the shape is repositioned after the rotation to reflect the new bounding box coordinates.</span></span>

<span data-ttu-id="6ce0b-125">Также обратите внимание, что для сценариев атрибут **Style** не используется, и этот **поворот** рассматривается как прямой атрибут фигуры.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-125">Also note that for scripting, the **style** attribute is not used and that **Rotation** is treated as a direct attribute of the shape.</span></span>

<span data-ttu-id="6ce0b-126">Атрибут **вращения** аналогичен стандартному атрибуту **поворота** HTML для стилей.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-126">The **Rotation** attribute is similar to the standard HTML **Rotation** attribute for styles.</span></span>

<span data-ttu-id="6ce0b-127">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="6ce0b-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="6ce0b-128">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="6ce0b-128">**See Also**</span></span>

<span data-ttu-id="6ce0b-129">**Пример**</span><span class="sxs-lookup"><span data-stu-id="6ce0b-129">**Example**</span></span>

<span data-ttu-id="6ce0b-130">Прямоугольник будет наклонен на 45 градусов.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-130">The rectangle will be tilted 45 degrees.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



<span data-ttu-id="6ce0b-131">[Пример атрибута вращения](/previous-versions/bb264091(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6ce0b-131">[Rotation Attribute Example](/previous-versions/bb264091(v=vs.85)).</span></span> <span data-ttu-id="6ce0b-132">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="6ce0b-132">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 