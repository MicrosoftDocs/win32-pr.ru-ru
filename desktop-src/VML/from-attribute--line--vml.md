---
title: Из атрибута (line) (VML)
description: Из атрибута (line) (VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793656"
---
# <a name="from-attribute-linevml"></a><span data-ttu-id="79c4f-103">Из атрибута (line) (VML)</span><span class="sxs-lookup"><span data-stu-id="79c4f-103">From Attribute (Line)(VML)</span></span>

<span data-ttu-id="79c4f-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="79c4f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="79c4f-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="79c4f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="79c4f-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="79c4f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="79c4f-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="79c4f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="79c4f-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="79c4f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="79c4f-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="79c4f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="79c4f-110">Определяет начальную точку линии.</span><span class="sxs-lookup"><span data-stu-id="79c4f-110">Defines the starting point of a line.</span></span> <span data-ttu-id="79c4f-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="79c4f-111">Read/write.</span></span> <span data-ttu-id="79c4f-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="79c4f-112">**VgVector2D**.</span></span>

<span data-ttu-id="79c4f-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="79c4f-113">**Applies To**</span></span>

[<span data-ttu-id="79c4f-114">Line</span><span class="sxs-lookup"><span data-stu-id="79c4f-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="79c4f-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="79c4f-115">**Tag Syntax**</span></span>

<span data-ttu-id="79c4f-116"><v: *элемент* из = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="79c4f-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="79c4f-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="79c4f-117">**Script Syntax**</span></span>

<span data-ttu-id="79c4f-118">*element* . from = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="79c4f-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="79c4f-119">*выражение* = *элемент*. from</span><span class="sxs-lookup"><span data-stu-id="79c4f-119">*expression*=*element*.from</span></span>

<span data-ttu-id="79c4f-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="79c4f-120">**Remarks**</span></span>

<span data-ttu-id="79c4f-121">Определяет начальную точку линии в пространстве координат родительского элемента. Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="79c4f-121">Defines the starting point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="79c4f-122">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="79c4f-122">Default is 0,0.</span></span>

<span data-ttu-id="79c4f-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="79c4f-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="79c4f-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="79c4f-124">**Example**</span></span>

<span data-ttu-id="79c4f-125">Линия начинается с позиции 10, а затем на 10 пунктов справа от верхнего левого угла родительского пространства.</span><span class="sxs-lookup"><span data-stu-id="79c4f-125">The line starts at a location 10 points down and 10 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 