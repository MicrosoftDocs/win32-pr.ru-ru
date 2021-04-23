---
title: Атрибут Линестиле VML
description: Атрибут Линестиле VML
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e69371e61a3d81f97de0243af19381f36c0555
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791719"
---
# <a name="vml-linestyle-attribute"></a><span data-ttu-id="8e07e-103">Атрибут Линестиле VML</span><span class="sxs-lookup"><span data-stu-id="8e07e-103">VML LineStyle Attribute</span></span>

<span data-ttu-id="8e07e-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8e07e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8e07e-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="8e07e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8e07e-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="8e07e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8e07e-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8e07e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8e07e-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8e07e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8e07e-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8e07e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8e07e-110">Определяет стиль линии для штриха.</span><span class="sxs-lookup"><span data-stu-id="8e07e-110">Defines the line style of the stroke.</span></span> <span data-ttu-id="8e07e-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="8e07e-111">Read/write.</span></span> <span data-ttu-id="8e07e-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="8e07e-112">**String**.</span></span>

<span data-ttu-id="8e07e-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="8e07e-113">**Applies To**</span></span>

[<span data-ttu-id="8e07e-114">Водок</span><span class="sxs-lookup"><span data-stu-id="8e07e-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="8e07e-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="8e07e-115">**Tag Syntax**</span></span>

<span data-ttu-id="8e07e-116"><v: *element* линестиле = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="8e07e-116"><v: *element* linestyle=" *expression* "></span></span>

<span data-ttu-id="8e07e-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="8e07e-117">**Script Syntax**</span></span>

<span data-ttu-id="8e07e-118">*element* . линестиле = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="8e07e-118">*element* .linestyle="*expression*"</span></span>

<span data-ttu-id="8e07e-119">*выражение* = *element*. линестиле</span><span class="sxs-lookup"><span data-stu-id="8e07e-119">*expression*=*element*.linestyle</span></span>

<span data-ttu-id="8e07e-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="8e07e-120">**Remarks**</span></span>

<span data-ttu-id="8e07e-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="8e07e-121">Values include:</span></span>

-   <span data-ttu-id="8e07e-122">Single (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e07e-122">Single (default)</span></span>
-   <span data-ttu-id="8e07e-123">синсин</span><span class="sxs-lookup"><span data-stu-id="8e07e-123">ThinThin</span></span>
-   <span data-ttu-id="8e07e-124">синсикк</span><span class="sxs-lookup"><span data-stu-id="8e07e-124">ThinThick</span></span>
-   <span data-ttu-id="8e07e-125">сикксин</span><span class="sxs-lookup"><span data-stu-id="8e07e-125">ThickThin</span></span>
-   <span data-ttu-id="8e07e-126">сиккбетвинсин</span><span class="sxs-lookup"><span data-stu-id="8e07e-126">ThickBetweenThin</span></span>

<span data-ttu-id="8e07e-127">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="8e07e-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="8e07e-128">**Пример**</span><span class="sxs-lookup"><span data-stu-id="8e07e-128">**Example**</span></span>

<span data-ttu-id="8e07e-129">Двойная линия рисуется с помощью двух тонких штрихов.</span><span class="sxs-lookup"><span data-stu-id="8e07e-129">A double line is drawn with two thin strokes.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 