---
title: Атрибут Ендангле VML
description: Атрибут Ендангле VML
ms.assetid: fc8276dc-8f61-42f4-b405-e92ca31e4637
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b22f157a1ccfc2337baa0bb5de747332bb78d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339108"
---
# <a name="vml-endangle-attribute"></a><span data-ttu-id="bac4b-103">Атрибут Ендангле VML</span><span class="sxs-lookup"><span data-stu-id="bac4b-103">VML EndAngle Attribute</span></span>

<span data-ttu-id="bac4b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bac4b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bac4b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="bac4b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bac4b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="bac4b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bac4b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bac4b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bac4b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bac4b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bac4b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bac4b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bac4b-110">Определяет конечную точку дуги. Чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="bac4b-110">Defines the endpoint of the arc. Read/write.</span></span> <span data-ttu-id="bac4b-111">[Вганглеиндегрис](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="bac4b-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="bac4b-112">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="bac4b-112">**Applies To**</span></span>

[<span data-ttu-id="bac4b-113">Arc</span><span class="sxs-lookup"><span data-stu-id="bac4b-113">Arc</span></span>](msdn-online-vml-arc-element.md)

<span data-ttu-id="bac4b-114">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="bac4b-114">**Tag Syntax**</span></span>

<span data-ttu-id="bac4b-115"><v: *element* ендангле = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="bac4b-115"><v: *element* endangle=" *expression* "></span></span>

<span data-ttu-id="bac4b-116">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="bac4b-116">**Script Syntax**</span></span>

<span data-ttu-id="bac4b-117">*element* . ендангле = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="bac4b-117">*element* .endAngle="*expression*"</span></span>

<span data-ttu-id="bac4b-118">*выражение* = *element*. ендангле</span><span class="sxs-lookup"><span data-stu-id="bac4b-118">*expression*=*element*.endAngle</span></span>

<span data-ttu-id="bac4b-119">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="bac4b-119">**Remarks**</span></span>

<span data-ttu-id="bac4b-120">Дуга определяется как штрих, нарисованный вдоль овала, ограниченного атрибутами **стиля** фигуры.</span><span class="sxs-lookup"><span data-stu-id="bac4b-120">The arc is defined as a stroke drawn along an oval bounded by the **Style** attributes of a shape.</span></span> <span data-ttu-id="bac4b-121">Конец штриха определяется углом, измеряемым от вертикального угла (12 часов) по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="bac4b-121">The end of the stroke is defined by an angle measured from straight up (12 o'clock) clockwise.</span></span> <span data-ttu-id="bac4b-122">Значение по умолчанию — 90 градусов.</span><span class="sxs-lookup"><span data-stu-id="bac4b-122">The default value is 90 degrees.</span></span>

<span data-ttu-id="bac4b-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="bac4b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="bac4b-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="bac4b-124">**Example**</span></span>

<span data-ttu-id="bac4b-125">Дуга является улыбкой.</span><span class="sxs-lookup"><span data-stu-id="bac4b-125">The arc is smiling.</span></span> <span data-ttu-id="bac4b-126">Начальная точка находится на точке 90 градусов вписанный внутри прямоугольника, ограничивающего фигуру.</span><span class="sxs-lookup"><span data-stu-id="bac4b-126">The start point is at the 90-degree point of an oval inscribed inside the shape bounding box.</span></span> <span data-ttu-id="bac4b-127">Конечная точка находится в точке овала в 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="bac4b-127">The end point is at the 270-degree point of the oval.</span></span>


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 