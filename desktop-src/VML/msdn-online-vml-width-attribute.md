---
title: Атрибут ширины VML
description: Атрибут ширины VML
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691557"
---
# <a name="vml-width-attribute"></a><span data-ttu-id="94b75-103">Атрибут ширины VML</span><span class="sxs-lookup"><span data-stu-id="94b75-103">VML Width Attribute</span></span>

<span data-ttu-id="94b75-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="94b75-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="94b75-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="94b75-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="94b75-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="94b75-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="94b75-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="94b75-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="94b75-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="94b75-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="94b75-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="94b75-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="94b75-110">Определяет ширину фигуры.</span><span class="sxs-lookup"><span data-stu-id="94b75-110">Defines the width of the shape.</span></span> <span data-ttu-id="94b75-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="94b75-111">Read/write.</span></span> <span data-ttu-id="94b75-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="94b75-112">**String**.</span></span>

<span data-ttu-id="94b75-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="94b75-113">**Applies To**</span></span>

[<span data-ttu-id="94b75-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="94b75-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="94b75-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="94b75-115">**Tag Syntax**</span></span>

<span data-ttu-id="94b75-116"><v: Style *элемента* = "Width: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="94b75-116"><v: *element* style="width: *expression* "></span></span>

<span data-ttu-id="94b75-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="94b75-117">**Script Syntax**</span></span>

<span data-ttu-id="94b75-118">*element* . Style. Width = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="94b75-118">*element* .style.width="*expression*"</span></span>

<span data-ttu-id="94b75-119">*выражение* = *элемент*. Style. Width</span><span class="sxs-lookup"><span data-stu-id="94b75-119">*expression*=*element*.style.width</span></span>

<span data-ttu-id="94b75-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="94b75-120">**Remarks**</span></span>

<span data-ttu-id="94b75-121">Атрибут **Width** аналогичен стандартному атрибуту **ширины** HTML для стилей.</span><span class="sxs-lookup"><span data-stu-id="94b75-121">The **Width** attribute is similar to the standard HTML **Width** attribute for styles.</span></span>

<span data-ttu-id="94b75-122">Единицы могут быть сопоставлены с родительским элементом или могут быть в абсолютных единицах.</span><span class="sxs-lookup"><span data-stu-id="94b75-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="94b75-123">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="94b75-123">Values include:</span></span>



| <span data-ttu-id="94b75-124">Значение</span><span class="sxs-lookup"><span data-stu-id="94b75-124">Value</span></span>      | <span data-ttu-id="94b75-125">Описание</span><span class="sxs-lookup"><span data-stu-id="94b75-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94b75-126">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="94b75-126">Auto</span></span>       | <span data-ttu-id="94b75-127">Расположение элемента по умолчанию в потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="94b75-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="94b75-128">units</span><span class="sxs-lookup"><span data-stu-id="94b75-128">units</span></span>      | <span data-ttu-id="94b75-129">Число с абсолютными единицами измерения (cm, mm, in, PT, PC или px) или обозначение относительного числа единиц (EM или ex).</span><span class="sxs-lookup"><span data-stu-id="94b75-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="94b75-130">Если единицы не заданы, предполагается использование точек (ПКС).</span><span class="sxs-lookup"><span data-stu-id="94b75-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="94b75-131">процент</span><span class="sxs-lookup"><span data-stu-id="94b75-131">percentage</span></span> | <span data-ttu-id="94b75-132">Значение, выраженное в процентах от ширины родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="94b75-132">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="94b75-133">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="94b75-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="94b75-134">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="94b75-134">**See Also**</span></span>

[<span data-ttu-id="94b75-135">единиц(ы)</span><span class="sxs-lookup"><span data-stu-id="94b75-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="94b75-136">**Пример**</span><span class="sxs-lookup"><span data-stu-id="94b75-136">**Example**</span></span>

<span data-ttu-id="94b75-137">Ширина фигуры равна 25.</span><span class="sxs-lookup"><span data-stu-id="94b75-137">The width of the shape is 25.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



<span data-ttu-id="94b75-138">[Пример атрибута Width](/previous-versions/bb264101(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94b75-138">[Width Attribute Example](/previous-versions/bb264101(v=vs.85)).</span></span> <span data-ttu-id="94b75-139">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="94b75-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 