---
title: Атрибут перелистывания VML
description: Атрибут перелистывания VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793759"
---
# <a name="vml-flip-attribute"></a><span data-ttu-id="3ba56-103">Атрибут перелистывания VML</span><span class="sxs-lookup"><span data-stu-id="3ba56-103">VML Flip Attribute</span></span>

<span data-ttu-id="3ba56-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3ba56-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3ba56-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="3ba56-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3ba56-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="3ba56-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3ba56-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3ba56-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3ba56-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3ba56-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3ba56-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3ba56-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3ba56-110">Переключает ориентацию фигуры.</span><span class="sxs-lookup"><span data-stu-id="3ba56-110">Switches the orientation of a shape.</span></span> <span data-ttu-id="3ba56-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="3ba56-111">Read/write.</span></span> <span data-ttu-id="3ba56-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="3ba56-112">**String**.</span></span>

<span data-ttu-id="3ba56-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="3ba56-113">**Applies To**</span></span>

[<span data-ttu-id="3ba56-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="3ba56-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3ba56-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="3ba56-115">**Tag Syntax**</span></span>

<span data-ttu-id="3ba56-116"><v: *элемент* Style = "отражение: *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="3ba56-116"><v: *element* style="flip: *expression* "></span></span>

<span data-ttu-id="3ba56-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="3ba56-117">**Script Syntax**</span></span>

<span data-ttu-id="3ba56-118">*element* . Style. reпереворот = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="3ba56-118">*element* .style.flip="*expression*"</span></span>

<span data-ttu-id="3ba56-119">*выражение* = *element*. Style. переворот</span><span class="sxs-lookup"><span data-stu-id="3ba56-119">*expression*=*element*.style.flip</span></span>

<span data-ttu-id="3ba56-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="3ba56-120">**Remarks**</span></span>

<span data-ttu-id="3ba56-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="3ba56-121">Values include:</span></span>



| <span data-ttu-id="3ba56-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3ba56-122">Value</span></span> | <span data-ttu-id="3ba56-123">Описание</span><span class="sxs-lookup"><span data-stu-id="3ba56-123">Description</span></span>                                           |
|-------|-------------------------------------------------------|
| <span data-ttu-id="3ba56-124">x</span><span class="sxs-lookup"><span data-stu-id="3ba56-124">x</span></span>     | <span data-ttu-id="3ba56-125">Поворачивает вдоль оси y, отменяя координаты *x*.</span><span class="sxs-lookup"><span data-stu-id="3ba56-125">Flip along the y-axis, reversing the *x*-coordinates.</span></span> |
| <span data-ttu-id="3ba56-126">да</span><span class="sxs-lookup"><span data-stu-id="3ba56-126">y</span></span>     | <span data-ttu-id="3ba56-127">Переверните по оси *x*, отменив координаты y.</span><span class="sxs-lookup"><span data-stu-id="3ba56-127">Flip along the *x*-axis, reversing the y-coordinates.</span></span> |
| <span data-ttu-id="3ba56-128">xy</span><span class="sxs-lookup"><span data-stu-id="3ba56-128">xy</span></span>    | <span data-ttu-id="3ba56-129">Переразите по осям y и *x*.</span><span class="sxs-lookup"><span data-stu-id="3ba56-129">Flip along both the y- and *x*-axis.</span></span>                  |
| <span data-ttu-id="3ba56-130">икс</span><span class="sxs-lookup"><span data-stu-id="3ba56-130">yx</span></span>    | <span data-ttu-id="3ba56-131">Переразите по оси *x* и *y*.</span><span class="sxs-lookup"><span data-stu-id="3ba56-131">Flip along both the *x*- and *y*-axis.</span></span>                |



 

<span data-ttu-id="3ba56-132">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="3ba56-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="3ba56-133">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="3ba56-133">**See Also**</span></span>

[<span data-ttu-id="3ba56-134">вгфлипориентатион</span><span class="sxs-lookup"><span data-stu-id="3ba56-134">VgFlipOrientation</span></span>](msdn-online-vector-markup-language-object-model-reference.md)

<span data-ttu-id="3ba56-135">**Пример**</span><span class="sxs-lookup"><span data-stu-id="3ba56-135">**Example**</span></span>

<span data-ttu-id="3ba56-136">Фигура перемещается вдоль оси *y* путем обращения к координатам *x* .</span><span class="sxs-lookup"><span data-stu-id="3ba56-136">The shape is flipped along the *y* -axis by reversing the *x* -coordinates.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



<span data-ttu-id="3ba56-137">[Пример атрибута для отражения](/previous-versions/bb229670(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ba56-137">[Flip Attribute Example](/previous-versions/bb229670(v=vs.85)).</span></span> <span data-ttu-id="3ba56-138">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="3ba56-138">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 