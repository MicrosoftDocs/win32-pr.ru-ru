---
title: Атрибут Control2 VML
description: Атрибут Control2 VML
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7af3871981e26ff7eff471651de555483fd540
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133919"
---
# <a name="vml-control2-attribute"></a><span data-ttu-id="ef519-103">Атрибут Control2 VML</span><span class="sxs-lookup"><span data-stu-id="ef519-103">VML Control2 Attribute</span></span>

<span data-ttu-id="ef519-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ef519-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ef519-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ef519-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ef519-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ef519-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ef519-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ef519-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ef519-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ef519-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ef519-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ef519-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ef519-110">Определяет вторую контрольную точку кривой Безье.</span><span class="sxs-lookup"><span data-stu-id="ef519-110">Defines the second control point of a bezier curve.</span></span> <span data-ttu-id="ef519-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ef519-111">Read/write.</span></span> <span data-ttu-id="ef519-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="ef519-112">**VgVector2D**.</span></span>

<span data-ttu-id="ef519-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ef519-113">**Applies To**</span></span>

[<span data-ttu-id="ef519-114">Соединитель</span><span class="sxs-lookup"><span data-stu-id="ef519-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="ef519-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ef519-115">**Tag Syntax**</span></span>

<span data-ttu-id="ef519-116"><v: *element* control2 = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="ef519-116"><v: *element* control2=" *expression* "></span></span>

<span data-ttu-id="ef519-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ef519-117">**Script Syntax**</span></span>

<span data-ttu-id="ef519-118">*element* . control2 = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="ef519-118">*element* .control2="*expression*"</span></span>

<span data-ttu-id="ef519-119">*выражение* = *element*. control2</span><span class="sxs-lookup"><span data-stu-id="ef519-119">*expression*=*element*.control2</span></span>

<span data-ttu-id="ef519-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ef519-120">**Remarks**</span></span>

<span data-ttu-id="ef519-121">Определяет вторую контрольную точку кривой Безье третьего порядка в пространстве координат родительского элемента. Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="ef519-121">Defines the second control point of a cubic bezier curve in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="ef519-122">Значение по умолчанию — 20,0.</span><span class="sxs-lookup"><span data-stu-id="ef519-122">Default is 20.0.</span></span>

<span data-ttu-id="ef519-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="ef519-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="ef519-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ef519-124">**Example**</span></span>

<span data-ttu-id="ef519-125">Кривая является улыбкой.</span><span class="sxs-lookup"><span data-stu-id="ef519-125">The curve is smiling.</span></span> <span data-ttu-id="ef519-126">Он начинается слева и заканчивается справа.</span><span class="sxs-lookup"><span data-stu-id="ef519-126">It starts at the left and ends at the right.</span></span> <span data-ttu-id="ef519-127">Две контрольные точки располагаются по пути, так что для получения их внешнего вида улыбки нужно извлечь кривую вниз.</span><span class="sxs-lookup"><span data-stu-id="ef519-127">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 