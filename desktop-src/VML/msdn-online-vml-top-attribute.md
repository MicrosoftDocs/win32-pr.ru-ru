---
title: Атрибут Top VML
description: Атрибут Top VML
ms.assetid: faad0c76-3566-4a51-962b-971667df2025
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c76a39035bc3dd3f0ae348280561e614d7dab4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792331"
---
# <a name="vml-top-attribute"></a><span data-ttu-id="8abef-103">Атрибут Top VML</span><span class="sxs-lookup"><span data-stu-id="8abef-103">VML Top Attribute</span></span>

<span data-ttu-id="8abef-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8abef-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8abef-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="8abef-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8abef-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="8abef-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8abef-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8abef-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8abef-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8abef-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8abef-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8abef-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8abef-110">Определяет расположение фигуры относительно элемента, расположенного над ним в потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="8abef-110">Defines the position of the shape relative to the element above it in the flow of the page.</span></span> <span data-ttu-id="8abef-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="8abef-111">Read/write.</span></span> <span data-ttu-id="8abef-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="8abef-112">**String**.</span></span>

<span data-ttu-id="8abef-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="8abef-113">**Applies To**</span></span>

[<span data-ttu-id="8abef-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="8abef-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="8abef-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="8abef-115">**Tag Syntax**</span></span>

<span data-ttu-id="8abef-116"><v: Style *элемента* = "Top: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="8abef-116"><v: *element* style="top: *expression* "></span></span>

<span data-ttu-id="8abef-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="8abef-117">**Script Syntax**</span></span>

<span data-ttu-id="8abef-118">*element* . Style.Top = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="8abef-118">*element* .style.top="*expression*"</span></span>

<span data-ttu-id="8abef-119">*выражение* = *element*. Style.Top</span><span class="sxs-lookup"><span data-stu-id="8abef-119">*expression*=*element*.style.top</span></span>

<span data-ttu-id="8abef-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="8abef-120">**Remarks**</span></span>

<span data-ttu-id="8abef-121">Атрибут **Top** аналогичен стандартному атрибуту HTML **Top** для Styles.</span><span class="sxs-lookup"><span data-stu-id="8abef-121">The **Top** attribute is similar to the standard HTML **Top** attribute for styles.</span></span>

<span data-ttu-id="8abef-122">Единицы могут быть сопоставлены с родительским элементом или могут быть в абсолютных единицах.</span><span class="sxs-lookup"><span data-stu-id="8abef-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="8abef-123">Этот атрибут не может быть записан для фигур, закрепленных встроенным.</span><span class="sxs-lookup"><span data-stu-id="8abef-123">This attribute may not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="8abef-124">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="8abef-124">Values include:</span></span>



| <span data-ttu-id="8abef-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8abef-125">Value</span></span>      | <span data-ttu-id="8abef-126">Описание</span><span class="sxs-lookup"><span data-stu-id="8abef-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8abef-127">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="8abef-127">Auto</span></span>       | <span data-ttu-id="8abef-128">Расположение элемента по умолчанию в потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="8abef-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="8abef-129">units</span><span class="sxs-lookup"><span data-stu-id="8abef-129">units</span></span>      | <span data-ttu-id="8abef-130">Число с абсолютными единицами измерения (cm, mm, in, PT, PC или px) или обозначение относительного числа единиц (EM или ex).</span><span class="sxs-lookup"><span data-stu-id="8abef-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="8abef-131">Если единицы не заданы, предполагается использование точек (ПКС).</span><span class="sxs-lookup"><span data-stu-id="8abef-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="8abef-132">процент</span><span class="sxs-lookup"><span data-stu-id="8abef-132">percentage</span></span> | <span data-ttu-id="8abef-133">Значение, выраженное в процентах от высоты родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="8abef-133">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="8abef-134">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="8abef-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="8abef-135">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="8abef-135">**See Also**</span></span>

[<span data-ttu-id="8abef-136">единиц(ы)</span><span class="sxs-lookup"><span data-stu-id="8abef-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="8abef-137">**Пример**</span><span class="sxs-lookup"><span data-stu-id="8abef-137">**Example**</span></span>

<span data-ttu-id="8abef-138">Верхний край фигуры находится на 5 пикселях под объектом, расположенном перед ним в потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="8abef-138">The top edge of the shape is 5 pixels below the object that precedes it in the flow of the page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:5;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="8abef-139">[Пример атрибута Top](/previous-versions/bb264098(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8abef-139">[Top Attribute Example](/previous-versions/bb264098(v=vs.85)).</span></span> <span data-ttu-id="8abef-140">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="8abef-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 