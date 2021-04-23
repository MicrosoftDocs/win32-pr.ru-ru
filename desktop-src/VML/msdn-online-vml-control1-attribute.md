---
title: Атрибут Control1 VML
description: Атрибут Control1 VML
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88516592c371a19a7a3b001a708c507d3103927a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672287"
---
# <a name="vml-control1-attribute"></a><span data-ttu-id="e52b2-103">Атрибут Control1 VML</span><span class="sxs-lookup"><span data-stu-id="e52b2-103">VML Control1 Attribute</span></span>

<span data-ttu-id="e52b2-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e52b2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e52b2-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="e52b2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e52b2-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="e52b2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e52b2-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e52b2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e52b2-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e52b2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e52b2-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e52b2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e52b2-110">Определяет первую контрольную точку кривой Безье.</span><span class="sxs-lookup"><span data-stu-id="e52b2-110">Defines the first control point of a bezier curve.</span></span> <span data-ttu-id="e52b2-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="e52b2-111">Read/write.</span></span> <span data-ttu-id="e52b2-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="e52b2-112">**VgVector2D**.</span></span>

<span data-ttu-id="e52b2-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="e52b2-113">**Applies To**</span></span>

[<span data-ttu-id="e52b2-114">Соединитель</span><span class="sxs-lookup"><span data-stu-id="e52b2-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="e52b2-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="e52b2-115">**Tag Syntax**</span></span>

<span data-ttu-id="e52b2-116"><v: *element* Control1 = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="e52b2-116"><v: *element* control1=" *expression* "></span></span>

<span data-ttu-id="e52b2-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="e52b2-117">**Script Syntax**</span></span>

<span data-ttu-id="e52b2-118">*element* . Control1 = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="e52b2-118">*element* .control1="*expression*"</span></span>

<span data-ttu-id="e52b2-119">*выражение* = *element*. Control1</span><span class="sxs-lookup"><span data-stu-id="e52b2-119">*expression*=*element*.control1</span></span>

<span data-ttu-id="e52b2-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="e52b2-120">**Remarks**</span></span>

<span data-ttu-id="e52b2-121">Определяет первую контрольную точку кривой Безье третьего порядка в пространстве координат родительского элемента. Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="e52b2-121">Defines the first control point of a cubic bezier curve in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="e52b2-122">Значение по умолчанию — 10, 10.</span><span class="sxs-lookup"><span data-stu-id="e52b2-122">Default is 10,10.</span></span>

<span data-ttu-id="e52b2-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="e52b2-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="e52b2-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="e52b2-124">**Example**</span></span>

<span data-ttu-id="e52b2-125">Кривая является улыбкой.</span><span class="sxs-lookup"><span data-stu-id="e52b2-125">The curve is smiling.</span></span> <span data-ttu-id="e52b2-126">Он начинается слева и заканчивается справа.</span><span class="sxs-lookup"><span data-stu-id="e52b2-126">It starts at the left and ends at the right.</span></span> <span data-ttu-id="e52b2-127">Две контрольные точки располагаются по пути, так что для получения их внешнего вида улыбки нужно извлечь кривую вниз.</span><span class="sxs-lookup"><span data-stu-id="e52b2-127">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 