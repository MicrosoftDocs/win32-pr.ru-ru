---
title: Атрибут индекса VML Z
description: Атрибут индекса VML Z
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987575"
---
# <a name="vml-z-index-attribute"></a><span data-ttu-id="59e1d-103">Атрибут индекса VML Z</span><span class="sxs-lookup"><span data-stu-id="59e1d-103">VML Z-Index Attribute</span></span>

<span data-ttu-id="59e1d-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="59e1d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="59e1d-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="59e1d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="59e1d-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="59e1d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="59e1d-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="59e1d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="59e1d-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="59e1d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="59e1d-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="59e1d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="59e1d-110">Определяет порядок вывода перекрывающихся фигур.</span><span class="sxs-lookup"><span data-stu-id="59e1d-110">Determines the display order of overlapping shapes.</span></span> <span data-ttu-id="59e1d-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="59e1d-111">Read/write.</span></span> <span data-ttu-id="59e1d-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="59e1d-112">**String**.</span></span>

<span data-ttu-id="59e1d-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="59e1d-113">**Applies To**</span></span>

[<span data-ttu-id="59e1d-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="59e1d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="59e1d-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="59e1d-115">**Tag Syntax**</span></span>

<span data-ttu-id="59e1d-116"><v: Style *элемента* = "z-index: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="59e1d-116"><v: *element* style="z-index: *expression* "></span></span>

<span data-ttu-id="59e1d-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="59e1d-117">**Script Syntax**</span></span>

<span data-ttu-id="59e1d-118">*element* . Style. ZIndex = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="59e1d-118">*element* .style.zindex="*expression*"</span></span>

<span data-ttu-id="59e1d-119">*выражение* = *element*. Style. ZIndex</span><span class="sxs-lookup"><span data-stu-id="59e1d-119">*expression*=*element*.style.zindex</span></span>

<span data-ttu-id="59e1d-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="59e1d-120">**Remarks**</span></span>

<span data-ttu-id="59e1d-121">Атрибут **z-index** аналогичен стандартному атрибуту HTML **Z-Index** для стилей.</span><span class="sxs-lookup"><span data-stu-id="59e1d-121">The **Z-Index** attribute is similar to the standard HTML **Z-Index** attribute for styles.</span></span>

<span data-ttu-id="59e1d-122">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="59e1d-122">Values include:</span></span>



| <span data-ttu-id="59e1d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="59e1d-123">Value</span></span> | <span data-ttu-id="59e1d-124">Описание</span><span class="sxs-lookup"><span data-stu-id="59e1d-124">Description</span></span>                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e1d-125">Auto (Автоматически)</span><span class="sxs-lookup"><span data-stu-id="59e1d-125">Auto</span></span>  | <span data-ttu-id="59e1d-126">Порядок, в котором фигуры отображаются на странице HTML, будет использоваться снизу вверх.</span><span class="sxs-lookup"><span data-stu-id="59e1d-126">The order that the shapes appear in the HTML page will be used, bottom to top.</span></span>                                                                                                                         |
| <span data-ttu-id="59e1d-127">порядок</span><span class="sxs-lookup"><span data-stu-id="59e1d-127">order</span></span> | <span data-ttu-id="59e1d-128">Число, представляющее приоритет стека.</span><span class="sxs-lookup"><span data-stu-id="59e1d-128">A number that represents the stacking precedence.</span></span> <span data-ttu-id="59e1d-129">Фигура с более высоким числом будет отображаться так, как если бы она вереоверлаппинг (в «лицевой») фигуре с меньшим числом.</span><span class="sxs-lookup"><span data-stu-id="59e1d-129">A shape with a a higher number will be displayed as if it wereoverlapping (in "front" of) a shape with a lower number.</span></span> <span data-ttu-id="59e1d-130">Можно использовать отрицательные числа.</span><span class="sxs-lookup"><span data-stu-id="59e1d-130">Negative numbers can be used.</span></span> |



 

<span data-ttu-id="59e1d-131">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="59e1d-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="59e1d-132">**Пример**</span><span class="sxs-lookup"><span data-stu-id="59e1d-132">**Example**</span></span>

<span data-ttu-id="59e1d-133">Красная фигура будет отображаться в "лицевой" синей фигуре, так как она имеет более высокий z-индекс.</span><span class="sxs-lookup"><span data-stu-id="59e1d-133">The red shape will be displayed in "front" of the blue shape, because it has a higher z-index.</span></span>


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



<span data-ttu-id="59e1d-134">[Пример атрибута Z-Index](/previous-versions/ms530275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59e1d-134">[Z-Index Attribute Example](/previous-versions/ms530275(v=vs.85)).</span></span> <span data-ttu-id="59e1d-135">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="59e1d-135">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 