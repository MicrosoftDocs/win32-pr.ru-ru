---
title: Атрибут Left в формате VML
description: Атрибут Left в формате VML
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488176"
---
# <a name="vml-left-attribute"></a><span data-ttu-id="ebc11-103">Атрибут Left в формате VML</span><span class="sxs-lookup"><span data-stu-id="ebc11-103">VML Left Attribute</span></span>

<span data-ttu-id="ebc11-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ebc11-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ebc11-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ebc11-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ebc11-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ebc11-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ebc11-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ebc11-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ebc11-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ebc11-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ebc11-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ebc11-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ebc11-110">Определяет расположение фигуры относительно элемента, находящихся слева от него в потоке документа.</span><span class="sxs-lookup"><span data-stu-id="ebc11-110">Determines the position of the shape relative to the element left of it in the document flow.</span></span> <span data-ttu-id="ebc11-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ebc11-111">Read/write.</span></span> <span data-ttu-id="ebc11-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="ebc11-112">**String**.</span></span>

<span data-ttu-id="ebc11-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ebc11-113">**Applies To**</span></span>

[<span data-ttu-id="ebc11-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="ebc11-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ebc11-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ebc11-115">**Tag Syntax**</span></span>

<span data-ttu-id="ebc11-116"><v: Style *элемента* = "Left: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ebc11-116"><v: *element* style="left: *expression* "></span></span>

<span data-ttu-id="ebc11-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ebc11-117">**Script Syntax**</span></span>

<span data-ttu-id="ebc11-118">*element* . Style. Left = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="ebc11-118">*element* .style.left="*expression*"</span></span>

<span data-ttu-id="ebc11-119">*выражение* = *element*. Style. Left</span><span class="sxs-lookup"><span data-stu-id="ebc11-119">*expression*=*element*.style.left</span></span>

<span data-ttu-id="ebc11-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ebc11-120">**Remarks**</span></span>

<span data-ttu-id="ebc11-121">**Левый** атрибут аналогичен стандартному атрибуту HTML **Left** для Styles.</span><span class="sxs-lookup"><span data-stu-id="ebc11-121">The **Left** attribute is similar to the standard HTML **Left** attribute for styles.</span></span>

<span data-ttu-id="ebc11-122">Единицы могут быть сопоставлены с родительским элементом или могут быть в абсолютных единицах.</span><span class="sxs-lookup"><span data-stu-id="ebc11-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="ebc11-123">Этот атрибут не будет записан для фигур, закрепленных встроенным.</span><span class="sxs-lookup"><span data-stu-id="ebc11-123">This attribute will not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="ebc11-124">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="ebc11-124">Values include:</span></span>



| <span data-ttu-id="ebc11-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ebc11-125">Value</span></span>      | <span data-ttu-id="ebc11-126">Описание</span><span class="sxs-lookup"><span data-stu-id="ebc11-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc11-127">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="ebc11-127">Auto</span></span>       | <span data-ttu-id="ebc11-128">Расположение элемента по умолчанию в потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="ebc11-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="ebc11-129">units</span><span class="sxs-lookup"><span data-stu-id="ebc11-129">units</span></span>      | <span data-ttu-id="ebc11-130">Число с абсолютными единицами измерения (cm, mm, in, PT, PC или px) или обозначение относительного числа единиц (EM или ex).</span><span class="sxs-lookup"><span data-stu-id="ebc11-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="ebc11-131">Если единицы не заданы, предполагается использование точек (ПКС).</span><span class="sxs-lookup"><span data-stu-id="ebc11-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="ebc11-132">процент</span><span class="sxs-lookup"><span data-stu-id="ebc11-132">percentage</span></span> | <span data-ttu-id="ebc11-133">Значение, выраженное в процентах от ширины родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="ebc11-133">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="ebc11-134">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="ebc11-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="ebc11-135">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="ebc11-135">**See Also**</span></span>

[<span data-ttu-id="ebc11-136">единиц(ы)</span><span class="sxs-lookup"><span data-stu-id="ebc11-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="ebc11-137">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ebc11-137">**Example**</span></span>

<span data-ttu-id="ebc11-138">Левое значение фигуры равно 1 в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="ebc11-138">The left value of the shape is set to 1 in the example below.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="ebc11-139">[Пример атрибута Left](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span><span class="sxs-lookup"><span data-stu-id="ebc11-139">[Left Attribute Example](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span></span> <span data-ttu-id="ebc11-140">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="ebc11-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 