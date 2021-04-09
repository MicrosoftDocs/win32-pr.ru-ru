---
title: Атрибут точек VML
description: Атрибут точек VML
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070099"
---
# <a name="vml-points-attribute"></a><span data-ttu-id="20be2-103">Атрибут точек VML</span><span class="sxs-lookup"><span data-stu-id="20be2-103">VML Points Attribute</span></span>

<span data-ttu-id="20be2-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="20be2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="20be2-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="20be2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="20be2-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="20be2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="20be2-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="20be2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="20be2-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="20be2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="20be2-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="20be2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="20be2-110">Определяет набор точек, образующих ломаную линию.</span><span class="sxs-lookup"><span data-stu-id="20be2-110">Defines a set of points that make up a polyline.</span></span> <span data-ttu-id="20be2-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="20be2-111">Read/write.</span></span> <span data-ttu-id="20be2-112">[Ивгпоинтс](msdn-online-vml-ivgpoints-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="20be2-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span></span>

<span data-ttu-id="20be2-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="20be2-113">**Applies To**</span></span>

[<span data-ttu-id="20be2-114">Ломаная линия</span><span class="sxs-lookup"><span data-stu-id="20be2-114">Polyline</span></span>](msdn-online-vml-polyline-element.md)

<span data-ttu-id="20be2-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="20be2-115">**Tag Syntax**</span></span>

<span data-ttu-id="20be2-116"><v: *element* Points = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="20be2-116"><v: *element* points=" *expression* "></span></span>

<span data-ttu-id="20be2-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="20be2-117">**Script Syntax**</span></span>

<span data-ttu-id="20be2-118">*element* . Points = "*выражение \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="20be2-118">*element* .points="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="20be2-119">*выражение* = *element*. Points</span><span class="sxs-lookup"><span data-stu-id="20be2-119">*expression*=*element*.points</span></span>

<span data-ttu-id="20be2-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="20be2-120">**Remarks**</span></span>

<span data-ttu-id="20be2-121">Определяет набор прямых линейных сегментов, состоящих из нескольких точек.</span><span class="sxs-lookup"><span data-stu-id="20be2-121">Defines a set of straight line segments that are composed of a series of points.</span></span> <span data-ttu-id="20be2-122">Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="20be2-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="20be2-123">Значение по умолчанию — 0, 0 10, 10.</span><span class="sxs-lookup"><span data-stu-id="20be2-123">The default value is "0,0 10,10".</span></span> <span data-ttu-id="20be2-124">Обратите внимание, что запятые не требуются, но они упрощают удобочитаемость.</span><span class="sxs-lookup"><span data-stu-id="20be2-124">Note that commas are not required, but they make for easier readability.</span></span>

<span data-ttu-id="20be2-125">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="20be2-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="20be2-126">**Пример**</span><span class="sxs-lookup"><span data-stu-id="20be2-126">**Example**</span></span>

<span data-ttu-id="20be2-127">Ломаная линия начинается в точке 10, 10 и заканчивается в 100 100, со значениями точек.</span><span class="sxs-lookup"><span data-stu-id="20be2-127">The polyline starts at the point 10,10 and ends at 100,100, with the valuesin points.</span></span>


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 