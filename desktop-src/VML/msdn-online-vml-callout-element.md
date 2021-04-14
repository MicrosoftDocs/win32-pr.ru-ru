---
title: Элемент выноски VML
description: Элемент выноски VML
ms.assetid: 0e93fb2f-494c-44eb-b7ef-0e3786c64ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530d06bcd0e06247ee5a3f69974049761c705a0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487897"
---
# <a name="vml-callout-element"></a><span data-ttu-id="b5040-103">Элемент выноски VML</span><span class="sxs-lookup"><span data-stu-id="b5040-103">VML Callout Element</span></span>

<span data-ttu-id="b5040-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b5040-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b5040-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b5040-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b5040-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b5040-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b5040-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b5040-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b5040-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b5040-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b5040-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b5040-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b5040-110">Определяет выноску для фигуры.</span><span class="sxs-lookup"><span data-stu-id="b5040-110">Defines a callout for a shape.</span></span>

<span data-ttu-id="b5040-111">Следующие атрибуты изменяют внешний вызов.</span><span class="sxs-lookup"><span data-stu-id="b5040-111">The following attributes modify a callout.</span></span>



| <span data-ttu-id="b5040-112">attribute</span><span class="sxs-lookup"><span data-stu-id="b5040-112">Attribute</span></span>                                                        | <span data-ttu-id="b5040-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b5040-113">Description</span></span>                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5040-114">акцентбар</span><span class="sxs-lookup"><span data-stu-id="b5040-114">AccentBar</span></span>](msdn-online-vml-accentbar-attribute.md)             | <span data-ttu-id="b5040-115">Определяет, будет ли вызываемая черта использоваться с выноской.</span><span class="sxs-lookup"><span data-stu-id="b5040-115">Determines whether an accent bar will be used with the callout.</span></span>                         |
| [<span data-ttu-id="b5040-116">Под</span><span class="sxs-lookup"><span data-stu-id="b5040-116">Angle</span></span>](angle-attribute--callout--vml.md)                       | <span data-ttu-id="b5040-117">Определяет угол, который задается выноской относительно ограничивающего прямоугольника фигуры.</span><span class="sxs-lookup"><span data-stu-id="b5040-117">Defines the angle that the callout makes with respect to the bounding box of the shape.</span></span> |
| [<span data-ttu-id="b5040-118">расстояние;</span><span class="sxs-lookup"><span data-stu-id="b5040-118">Distance</span></span>](msdn-online-vml-distance-attribute.md)               | <span data-ttu-id="b5040-119">Определяет расстояние перетаскивания в выноске.</span><span class="sxs-lookup"><span data-stu-id="b5040-119">Defines the drop distance of a callout.</span></span>                                                 |
| [<span data-ttu-id="b5040-120">Тени</span><span class="sxs-lookup"><span data-stu-id="b5040-120">Drop</span></span>](msdn-online-vml-drop-attribute.md)                       | <span data-ttu-id="b5040-121">Определяет место, куда будет помещено удаление выноски.</span><span class="sxs-lookup"><span data-stu-id="b5040-121">Determines where the drop of a callout will be placed.</span></span>                                  |
| [<span data-ttu-id="b5040-122">дропауто</span><span class="sxs-lookup"><span data-stu-id="b5040-122">DropAuto</span></span>](msdn-online-vml-dropauto-attribute.md)               | <span data-ttu-id="b5040-123">Определяет, будет ли выноска автоматически удаляться.</span><span class="sxs-lookup"><span data-stu-id="b5040-123">Determines whether the callout will have an automatic drop.</span></span>                             |
| [<span data-ttu-id="b5040-124">WLAN</span><span class="sxs-lookup"><span data-stu-id="b5040-124">Ext</span></span>](ext-attribute--callout--vml.md)                           | <span data-ttu-id="b5040-125">Определяет, как обрабатываются выноски.</span><span class="sxs-lookup"><span data-stu-id="b5040-125">Defines how a callout is processed.</span></span>                                                     |
| [<span data-ttu-id="b5040-126">Контур</span><span class="sxs-lookup"><span data-stu-id="b5040-126">Gap</span></span>](msdn-online-vml-gap-attribute.md)                         | <span data-ttu-id="b5040-127">Определяет расстояние в выноски от ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="b5040-127">Defines the distance fo the callout from its bounding rectangle.</span></span>                        |
| [<span data-ttu-id="b5040-128">Длина</span><span class="sxs-lookup"><span data-stu-id="b5040-128">Length</span></span>](msdn-online-vml-length-attribute.md)                   | <span data-ttu-id="b5040-129">Определяет длину выноски.</span><span class="sxs-lookup"><span data-stu-id="b5040-129">Defines the length of the callout.</span></span>                                                      |
| [<span data-ttu-id="b5040-130">ленгсспеЦифиед</span><span class="sxs-lookup"><span data-stu-id="b5040-130">LengthSpecified</span></span>](msdn-online-vml-lengthspecified-attribute.md) | <span data-ttu-id="b5040-131">Определяет, будет ли использоваться атрибут **длины** для вызова.</span><span class="sxs-lookup"><span data-stu-id="b5040-131">Determines whether the **Length** attribute will be used for the callout.</span></span>               |
| [<span data-ttu-id="b5040-132">минускс</span><span class="sxs-lookup"><span data-stu-id="b5040-132">MinusX</span></span>](msdn-online-vml-minusx-attribute.md)                   | <span data-ttu-id="b5040-133">Определяет, переворачивается ли выноска вдоль оси x.</span><span class="sxs-lookup"><span data-stu-id="b5040-133">Determines whether the callout will flip along the x-axis.</span></span>                              |
| [<span data-ttu-id="b5040-134">Минус</span><span class="sxs-lookup"><span data-stu-id="b5040-134">MinusY</span></span>](msdn-online-vml-minusy-attribute.md)                   | <span data-ttu-id="b5040-135">Определяет, переворачивается ли выноска вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="b5040-135">Determines whether the callout will flip along the y-axis.</span></span>                              |
| <span data-ttu-id="b5040-136">[On](on-attribute--callout--vml.md) (Вкл.)</span><span class="sxs-lookup"><span data-stu-id="b5040-136">[On](on-attribute--callout--vml.md)</span></span>                             | <span data-ttu-id="b5040-137">Определяет, является ли фигура выноской.</span><span class="sxs-lookup"><span data-stu-id="b5040-137">Determines whether a shape is a callout.</span></span>                                                |
| [<span data-ttu-id="b5040-138">текстбордер</span><span class="sxs-lookup"><span data-stu-id="b5040-138">TextBorder</span></span>](msdn-online-vml-textborder-attribute.md)           | <span data-ttu-id="b5040-139">Определяет, будет ли выноска иметь текстовую границу.</span><span class="sxs-lookup"><span data-stu-id="b5040-139">Determines whether a callout will have a text border.</span></span>                                   |
| [<span data-ttu-id="b5040-140">Тип</span><span class="sxs-lookup"><span data-stu-id="b5040-140">Type</span></span>](type-attribute--callout--vml.md)                         | <span data-ttu-id="b5040-141">Определяет тип выноски.</span><span class="sxs-lookup"><span data-stu-id="b5040-141">Defines the type of callout.</span></span>                                                            |



 

<span data-ttu-id="b5040-142">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b5040-142">**Remarks**</span></span>

<span data-ttu-id="b5040-143">Этот элемент должен быть определен внутри элемента [Shape](shape-element--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="b5040-143">This element must be defined within a [Shape](shape-element--vml.md) element.</span></span>

<span data-ttu-id="b5040-144">Элемент **выноски** является расширением Microsoft Office для VML.</span><span class="sxs-lookup"><span data-stu-id="b5040-144">The **Callout** element is a Microsoft Office Extension to VML.</span></span>

 

 