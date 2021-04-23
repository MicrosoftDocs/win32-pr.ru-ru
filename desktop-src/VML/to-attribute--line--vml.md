---
title: К атрибуту (line) (VML)
description: К атрибуту (line) (VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793747"
---
# <a name="to-attribute-linevml"></a><span data-ttu-id="00074-103">К атрибуту (line) (VML)</span><span class="sxs-lookup"><span data-stu-id="00074-103">To Attribute (Line)(VML)</span></span>

<span data-ttu-id="00074-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="00074-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="00074-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="00074-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="00074-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="00074-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="00074-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="00074-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="00074-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="00074-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="00074-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="00074-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="00074-110">Определяет конечную точку линии.</span><span class="sxs-lookup"><span data-stu-id="00074-110">Defines the ending point of a line.</span></span> <span data-ttu-id="00074-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="00074-111">Read/write.</span></span> <span data-ttu-id="00074-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="00074-112">**VgVector2D**.</span></span>

<span data-ttu-id="00074-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="00074-113">**Applies To**</span></span>

[<span data-ttu-id="00074-114">Line</span><span class="sxs-lookup"><span data-stu-id="00074-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="00074-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="00074-115">**Tag Syntax**</span></span>

<span data-ttu-id="00074-116"><v: *element* to = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="00074-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="00074-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="00074-117">**Script Syntax**</span></span>

<span data-ttu-id="00074-118">*element* . to = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="00074-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="00074-119">*выражение* = *element*. to</span><span class="sxs-lookup"><span data-stu-id="00074-119">*expression*=*element*.to</span></span>

<span data-ttu-id="00074-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="00074-120">**Remarks**</span></span>

<span data-ttu-id="00074-121">Определяет конечную точку линии в пространстве координат родительского элемента. Если родительский элемент не является элементом VML, то [единицей](msdn-online-vml-units.md) по умолчанию является пиксель (но в нем также может быть указана система cm, mm, PT, PC).</span><span class="sxs-lookup"><span data-stu-id="00074-121">Defines the ending point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="00074-122">Значение по умолчанию — 10, 10.</span><span class="sxs-lookup"><span data-stu-id="00074-122">Default is 10,10.</span></span>

<span data-ttu-id="00074-123">**Стандартный атрибут VML**</span><span class="sxs-lookup"><span data-stu-id="00074-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="00074-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="00074-124">**Example**</span></span>

<span data-ttu-id="00074-125">Линия заканчивается в расположении 100 указывает на угол вниз, а 100 указывает на право верхнего левого угла родительского пространства.</span><span class="sxs-lookup"><span data-stu-id="00074-125">The line ends at a location 100 points down and 100 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 