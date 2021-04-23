---
title: Атрибут высоты VML
description: Атрибут высоты VML
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41751e4863fdb128dbbedf2e3abf8e7f0a6736d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134074"
---
# <a name="vml-height-attribute"></a><span data-ttu-id="f9c8f-103">Атрибут высоты VML</span><span class="sxs-lookup"><span data-stu-id="f9c8f-103">VML Height Attribute</span></span>

<span data-ttu-id="f9c8f-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f9c8f-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f9c8f-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f9c8f-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f9c8f-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f9c8f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f9c8f-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f9c8f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f9c8f-110">Задает высоту фигуры.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-110">Specifies the height of the shape.</span></span> <span data-ttu-id="f9c8f-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-111">Read/write.</span></span> <span data-ttu-id="f9c8f-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-112">**String**.</span></span>

<span data-ttu-id="f9c8f-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="f9c8f-113">**Applies To**</span></span>

[<span data-ttu-id="f9c8f-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="f9c8f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="f9c8f-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="f9c8f-115">**Tag Syntax**</span></span>

<span data-ttu-id="f9c8f-116"><v: Style *элемента* = "Height: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="f9c8f-116"><v: *element* style="height: *expression* "></span></span>

<span data-ttu-id="f9c8f-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="f9c8f-117">**Script Syntax**</span></span>

<span data-ttu-id="f9c8f-118">*element* . Style. Height = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="f9c8f-118">*element* .style.height="*expression*"</span></span>

<span data-ttu-id="f9c8f-119">*выражение* = *элемент*. Style. Height</span><span class="sxs-lookup"><span data-stu-id="f9c8f-119">*expression*=*element*.style.height</span></span>

<span data-ttu-id="f9c8f-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="f9c8f-120">**Remarks**</span></span>

<span data-ttu-id="f9c8f-121">Атрибут **Height** аналогичен стандартному атрибуту « **Высота** HTML» для стилей.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-121">The **Height** attribute is similar to the standard HTML **Height** attribute for styles.</span></span>

<span data-ttu-id="f9c8f-122">Единицы могут быть сопоставлены с родительским элементом или могут быть в абсолютных единицах.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="f9c8f-123">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-123">Values include:</span></span>



| <span data-ttu-id="f9c8f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f9c8f-124">Value</span></span>      | <span data-ttu-id="f9c8f-125">Описание</span><span class="sxs-lookup"><span data-stu-id="f9c8f-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c8f-126">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="f9c8f-126">Auto</span></span>       | <span data-ttu-id="f9c8f-127">Расположение элемента по умолчанию в потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="f9c8f-128">units</span><span class="sxs-lookup"><span data-stu-id="f9c8f-128">units</span></span>      | <span data-ttu-id="f9c8f-129">Число с абсолютными единицами измерения (cm, mm, in, PT, PC или px) или обозначение относительного числа единиц (EM или ex).</span><span class="sxs-lookup"><span data-stu-id="f9c8f-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="f9c8f-130">Если единицы не заданы, предполагается использование точек (ПКС).</span><span class="sxs-lookup"><span data-stu-id="f9c8f-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="f9c8f-131">процент</span><span class="sxs-lookup"><span data-stu-id="f9c8f-131">percentage</span></span> | <span data-ttu-id="f9c8f-132">Значение, выраженное в процентах от высоты родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-132">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="f9c8f-133">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="f9c8f-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="f9c8f-134">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="f9c8f-134">**See Also**</span></span>

[<span data-ttu-id="f9c8f-135">единиц(ы)</span><span class="sxs-lookup"><span data-stu-id="f9c8f-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="f9c8f-136">**Пример**</span><span class="sxs-lookup"><span data-stu-id="f9c8f-136">**Example**</span></span>

<span data-ttu-id="f9c8f-137">Высота фигуры равна 30.</span><span class="sxs-lookup"><span data-stu-id="f9c8f-137">The height of the shape is set to 30.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



<span data-ttu-id="f9c8f-138">[Пример атрибута Height](/previous-versions/bb229671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f9c8f-138">[Height Attribute Example](/previous-versions/bb229671(v=vs.85)).</span></span> <span data-ttu-id="f9c8f-139">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="f9c8f-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 