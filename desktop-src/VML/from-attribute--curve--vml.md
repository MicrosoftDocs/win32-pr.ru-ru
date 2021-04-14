---
title: Из атрибута (кривая) (VML)
description: Из атрибута (кривая) (VML)
ms.assetid: 70e940c1-3fa8-4a30-9ca8-584483cea485
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d5f78dee46192efed48172a7d1f4d9cc77582f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413570"
---
# <a name="from-attribute-curvevml"></a><span data-ttu-id="f39cb-103">Из атрибута (кривая) (VML)</span><span class="sxs-lookup"><span data-stu-id="f39cb-103">From Attribute (Curve)(VML)</span></span>

<span data-ttu-id="f39cb-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f39cb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f39cb-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="f39cb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f39cb-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="f39cb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f39cb-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f39cb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f39cb-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f39cb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f39cb-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f39cb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f39cb-110">Определяет начальную точку кривой.</span><span class="sxs-lookup"><span data-stu-id="f39cb-110">Defines the starting point of a curve.</span></span> <span data-ttu-id="f39cb-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f39cb-111">Read/write.</span></span> <span data-ttu-id="f39cb-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="f39cb-112">**VgVector2D**.</span></span>

<span data-ttu-id="f39cb-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="f39cb-113">**Applies To**</span></span>

[<span data-ttu-id="f39cb-114">Соединитель</span><span class="sxs-lookup"><span data-stu-id="f39cb-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="f39cb-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="f39cb-115">**Tag Syntax**</span></span>

<span data-ttu-id="f39cb-116"><v: *элемент* из = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="f39cb-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="f39cb-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="f39cb-117">**Script Syntax**</span></span>

<span data-ttu-id="f39cb-118">*element* . from = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="f39cb-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="f39cb-119">*выражение* = *элемент*. from</span><span class="sxs-lookup"><span data-stu-id="f39cb-119">*expression*=*element*.from</span></span>

<span data-ttu-id="f39cb-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="f39cb-120">**Remarks**</span></span>

<span data-ttu-id="f39cb-121">Определяет начальную точку кривой Безье третьего порядка в пространстве координат родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="f39cb-121">Defines the starting point of a cubic bezier curve in the coordinate space of the parent element.</span></span> <span data-ttu-id="f39cb-122">Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="f39cb-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="f39cb-123">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="f39cb-123">Default is 0,0.</span></span>

<span data-ttu-id="f39cb-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="f39cb-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="f39cb-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="f39cb-125">**Example**</span></span>

<span data-ttu-id="f39cb-126">Кривая является улыбкой.</span><span class="sxs-lookup"><span data-stu-id="f39cb-126">The curve is smiling.</span></span> <span data-ttu-id="f39cb-127">Он начинается слева и заканчивается справа.</span><span class="sxs-lookup"><span data-stu-id="f39cb-127">It starts at the left and ends at the right.</span></span> <span data-ttu-id="f39cb-128">Две контрольные точки располагаются по пути, так что для получения их внешнего вида улыбки нужно извлечь кривую вниз.</span><span class="sxs-lookup"><span data-stu-id="f39cb-128">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```



 

 