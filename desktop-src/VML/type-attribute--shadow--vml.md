---
title: Атрибут Type (shadow) (VML)
description: Атрибут Type (shadow) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413310"
---
# <a name="type-attribute-shadowvml"></a><span data-ttu-id="434b8-103">Атрибут Type (shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="434b8-103">Type Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="434b8-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="434b8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="434b8-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="434b8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="434b8-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="434b8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="434b8-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="434b8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="434b8-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="434b8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="434b8-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="434b8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="434b8-110">Задает тип тени.</span><span class="sxs-lookup"><span data-stu-id="434b8-110">Specifies the type of shadow.</span></span> <span data-ttu-id="434b8-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="434b8-111">Read/write.</span></span> <span data-ttu-id="434b8-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="434b8-112">**String**.</span></span>

<span data-ttu-id="434b8-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="434b8-113">**Applies To**</span></span>

[<span data-ttu-id="434b8-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="434b8-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="434b8-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="434b8-115">**Tag Syntax**</span></span>

<span data-ttu-id="434b8-116"><v: *element* Type = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="434b8-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="434b8-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="434b8-117">**Script Syntax**</span></span>

<span data-ttu-id="434b8-118">*element* . Type = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="434b8-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="434b8-119">*выражение* = *element*. Type</span><span class="sxs-lookup"><span data-stu-id="434b8-119">*expression*=*element*.type</span></span>

<span data-ttu-id="434b8-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="434b8-120">**Remarks**</span></span>

<span data-ttu-id="434b8-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="434b8-121">Values include:</span></span>



| <span data-ttu-id="434b8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="434b8-122">Value</span></span>           | <span data-ttu-id="434b8-123">Описание</span><span class="sxs-lookup"><span data-stu-id="434b8-123">Description</span></span>                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="434b8-124">single</span><span class="sxs-lookup"><span data-stu-id="434b8-124">single</span></span>          | <span data-ttu-id="434b8-125">Одна тень.</span><span class="sxs-lookup"><span data-stu-id="434b8-125">Single shadow.</span></span> <span data-ttu-id="434b8-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="434b8-126">Default.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="434b8-127">double</span><span class="sxs-lookup"><span data-stu-id="434b8-127">double</span></span>          | <span data-ttu-id="434b8-128">Двойная тень.</span><span class="sxs-lookup"><span data-stu-id="434b8-128">A double shadow.</span></span> <span data-ttu-id="434b8-129">[Color2](color2-attribute--shadow--vml.md) используется для цвета второй тени и [Offset2](msdn-online-vml-offset2-attribute.md) используется для смещения второй тени.</span><span class="sxs-lookup"><span data-stu-id="434b8-129">[Color2](color2-attribute--shadow--vml.md) is used for the color of the second shadow and [Offset2](msdn-online-vml-offset2-attribute.md) is used for the second shadow's offset.</span></span> |
| <span data-ttu-id="434b8-130">перспектива</span><span class="sxs-lookup"><span data-stu-id="434b8-130">perspective</span></span>     | <span data-ttu-id="434b8-131">Тень перспективы.</span><span class="sxs-lookup"><span data-stu-id="434b8-131">A perspective shadow.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="434b8-132">шаперелативе</span><span class="sxs-lookup"><span data-stu-id="434b8-132">shapeRelative</span></span>   | <span data-ttu-id="434b8-133">Тень создается относительно фигуры.</span><span class="sxs-lookup"><span data-stu-id="434b8-133">The shadow is created relative to the shape.</span></span>                                                                                                                                                         |
| <span data-ttu-id="434b8-134">дравингрелативе</span><span class="sxs-lookup"><span data-stu-id="434b8-134">drawingRelative</span></span> | <span data-ttu-id="434b8-135">Тень создается относительно рисунка.</span><span class="sxs-lookup"><span data-stu-id="434b8-135">The shadow is created relative to the drawing.</span></span>                                                                                                                                                       |
| <span data-ttu-id="434b8-136">поднят</span><span class="sxs-lookup"><span data-stu-id="434b8-136">emboss</span></span>          | <span data-ttu-id="434b8-137">Тень выглядит приподнятой.</span><span class="sxs-lookup"><span data-stu-id="434b8-137">The shadow has an embossed look.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="434b8-138">**Стандартный атрибут VML**</span><span class="sxs-lookup"><span data-stu-id="434b8-138">**VML Standard Attribute**</span></span>

<span data-ttu-id="434b8-139">**Пример**</span><span class="sxs-lookup"><span data-stu-id="434b8-139">**Example**</span></span>

<span data-ttu-id="434b8-140">Двойная тень создается со второй тенью зеленого цвета и смещением 5 точек вниз и вправо.</span><span class="sxs-lookup"><span data-stu-id="434b8-140">A double shadow is created with the second shadow green and offset 5 points down and to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 