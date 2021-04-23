---
title: Атрибут StartAngle в формате VML
description: Атрибут StartAngle в формате VML
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e779d343061ef65decb1dd21f615e054d561da28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070249"
---
# <a name="vml-startangle-attribute"></a><span data-ttu-id="d4e4f-103">Атрибут StartAngle в формате VML</span><span class="sxs-lookup"><span data-stu-id="d4e4f-103">VML StartAngle Attribute</span></span>

<span data-ttu-id="d4e4f-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d4e4f-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d4e4f-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d4e4f-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d4e4f-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d4e4f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d4e4f-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d4e4f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d4e4f-110">Определяет начальную точку дуги. Чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-110">Defines the starting point of the arc. Read/write.</span></span> <span data-ttu-id="d4e4f-111">[Вганглеиндегрис](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e4f-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="d4e4f-112">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="d4e4f-112">**Applies To**</span></span>

[<span data-ttu-id="d4e4f-113">Arc</span><span class="sxs-lookup"><span data-stu-id="d4e4f-113">Arc</span></span>](msdn-online-vml-arc-element.md)

<span data-ttu-id="d4e4f-114">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="d4e4f-114">**Tag Syntax**</span></span>

<span data-ttu-id="d4e4f-115"><v: *element* ендангле = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="d4e4f-115"><v: *element* endangle=" *expression* "></span></span>

<span data-ttu-id="d4e4f-116">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="d4e4f-116">**Script Syntax**</span></span>

<span data-ttu-id="d4e4f-117">*element* . ендангле = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="d4e4f-117">*element* .endAngle="*expression*"</span></span>

<span data-ttu-id="d4e4f-118">*выражение* = *element*. ендангле</span><span class="sxs-lookup"><span data-stu-id="d4e4f-118">*expression*=*element*.endAngle</span></span>

<span data-ttu-id="d4e4f-119">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="d4e4f-119">**Remarks**</span></span>

<span data-ttu-id="d4e4f-120">Дуга определяется как штрих, нарисованный вдоль овала, ограниченного атрибутами **стиля** фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-120">The arc is defined as a stroke drawn along an oval bounded by the **Style** attributes of a shape.</span></span> <span data-ttu-id="d4e4f-121">Начало штриха определяется углом, измеренным с начала (12 часов) по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-121">The start of the stroke is defined by an angle measured from straight up (12 o'clock) clockwise.</span></span> <span data-ttu-id="d4e4f-122">Значение по умолчанию — 0 градусов.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-122">The default value is 0 degrees.</span></span>

<span data-ttu-id="d4e4f-123">Стандартный атрибут VML</span><span class="sxs-lookup"><span data-stu-id="d4e4f-123">VML Standard Attribute</span></span>

<span data-ttu-id="d4e4f-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="d4e4f-124">**Example**</span></span>

<span data-ttu-id="d4e4f-125">Дуга является улыбкой.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-125">The arc is smiling.</span></span> <span data-ttu-id="d4e4f-126">Начальная точка находится на точке 90 градусов вписанный внутри прямоугольника, ограничивающего фигуру.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-126">The start point is at the 90-degree point of an oval inscribed inside the shape bounding box.</span></span> <span data-ttu-id="d4e4f-127">Конечная точка находится в точке овала в 270 градусов.</span><span class="sxs-lookup"><span data-stu-id="d4e4f-127">The end point is at the 270-degree point of the oval.</span></span>


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 