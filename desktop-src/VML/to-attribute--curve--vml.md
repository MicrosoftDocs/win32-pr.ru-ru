---
title: К атрибуту (кривая) (VML)
description: К атрибуту (кривая) (VML)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c0c9a858ff2cc8304ffacefb1cae477614e470
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891061"
---
# <a name="to-attribute-curvevml"></a><span data-ttu-id="ffcb2-103">К атрибуту (кривая) (VML)</span><span class="sxs-lookup"><span data-stu-id="ffcb2-103">To Attribute (Curve)(VML)</span></span>

<span data-ttu-id="ffcb2-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ffcb2-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ffcb2-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ffcb2-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ffcb2-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ffcb2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ffcb2-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ffcb2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ffcb2-110">Определяет конечную точку кривой.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-110">Defines the ending point of a curve.</span></span> <span data-ttu-id="ffcb2-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-111">Read/write.</span></span> <span data-ttu-id="ffcb2-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-112">**VgVector2D**.</span></span>

<span data-ttu-id="ffcb2-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ffcb2-113">**Applies To**</span></span>

[<span data-ttu-id="ffcb2-114">Соединитель</span><span class="sxs-lookup"><span data-stu-id="ffcb2-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="ffcb2-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ffcb2-115">**Tag Syntax**</span></span>

<span data-ttu-id="ffcb2-116"><v: *element* to = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="ffcb2-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="ffcb2-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ffcb2-117">**Script Syntax**</span></span>

<span data-ttu-id="ffcb2-118">*element* . to = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="ffcb2-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="ffcb2-119">*выражение* = *element*. to</span><span class="sxs-lookup"><span data-stu-id="ffcb2-119">*expression*=*element*.to</span></span>

<span data-ttu-id="ffcb2-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ffcb2-120">**Remarks**</span></span>

<span data-ttu-id="ffcb2-121">Определяет конечную точку кривой Безье третьего порядка в пространстве координат родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-121">Defines the ending point of a cubic bezier curve in the coordinate space of the parent element.</span></span> <span data-ttu-id="ffcb2-122">Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="ffcb2-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="ffcb2-123">Значение по умолчанию — 30, 20.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-123">Default is 30,20.</span></span>

<span data-ttu-id="ffcb2-124">**Стандартный атрибут VML**</span><span class="sxs-lookup"><span data-stu-id="ffcb2-124">**VML Standard Attribute**</span></span>

<span data-ttu-id="ffcb2-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ffcb2-125">**Example**</span></span>

<span data-ttu-id="ffcb2-126">Кривая является улыбкой.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-126">The curve is smiling.</span></span> <span data-ttu-id="ffcb2-127">Он начинается слева и заканчивается справа.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-127">It starts at the left and ends at the right.</span></span> <span data-ttu-id="ffcb2-128">Две контрольные точки располагаются по пути, так что для получения их внешнего вида улыбки нужно извлечь кривую вниз.</span><span class="sxs-lookup"><span data-stu-id="ffcb2-128">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 