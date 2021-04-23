---
title: Атрибут расположения (H) (VML)
description: Атрибут расположения (H) (VML)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691640"
---
# <a name="position-attribute-hvml"></a><span data-ttu-id="e7939-103">Атрибут расположения (H) (VML)</span><span class="sxs-lookup"><span data-stu-id="e7939-103">Position Attribute (H)(VML)</span></span>

<span data-ttu-id="e7939-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e7939-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e7939-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="e7939-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e7939-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="e7939-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e7939-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e7939-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e7939-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e7939-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e7939-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e7939-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e7939-110">Задает значения секс и y для маркера.</span><span class="sxs-lookup"><span data-stu-id="e7939-110">Specifies thex and y values of the handle.</span></span> <span data-ttu-id="e7939-111">Чтение и запись **VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="e7939-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="e7939-112">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="e7939-112">**Applies To**</span></span>

<span data-ttu-id="e7939-113">[H](msdn-online-vml-h-element.md) (вложенный элемент [дескрипторов](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="e7939-113">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="e7939-114">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="e7939-114">**Tag Syntax**</span></span>

<span data-ttu-id="e7939-115"><v: расположение *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="e7939-115"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="e7939-116">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="e7939-116">**Remarks**</span></span>

<span data-ttu-id="e7939-117">значения x и y могут быть одного из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="e7939-117">x and y values can be one of the following types:</span></span>

-   <span data-ttu-id="e7939-118">constant</span><span class="sxs-lookup"><span data-stu-id="e7939-118">constant</span></span>
-   <span data-ttu-id="e7939-119">Формула (например, @2 )</span><span class="sxs-lookup"><span data-stu-id="e7939-119">formula (for example, @2)</span></span>
-   <span data-ttu-id="e7939-120">Настройте (например, \# 3)</span><span class="sxs-lookup"><span data-stu-id="e7939-120">adjust (for example, \#3)</span></span>
-   <span data-ttu-id="e7939-121">центр</span><span class="sxs-lookup"><span data-stu-id="e7939-121">center</span></span>
-   <span data-ttu-id="e7939-122">топлефт</span><span class="sxs-lookup"><span data-stu-id="e7939-122">topleft</span></span>
-   <span data-ttu-id="e7939-123">боттомригхт</span><span class="sxs-lookup"><span data-stu-id="e7939-123">bottomright</span></span>

<span data-ttu-id="e7939-124">Если указаны какие-либо из перечисленных выше типов, кроме « *корректировать* », то в этом измерении зафиксирована единица обработки.</span><span class="sxs-lookup"><span data-stu-id="e7939-124">If any of the above types except *adjust* are specified, the handle position is fixed in that dimension.</span></span> <span data-ttu-id="e7939-125">Если задан маркер корректировки, маркер может быть перемещен в это измерение, а значение корректировки определяется положением маркера.</span><span class="sxs-lookup"><span data-stu-id="e7939-125">If an adjust handle is specified, the handle is free to move in that dimension and the adjust value is determined by the position of the handle.</span></span>

<span data-ttu-id="e7939-126">Если указан [Полярный](msdn-online-vml-polar-attribute.md) атрибут, атрибут « **позиционирование** » представляет радиус и значения угла маркера, а не x и y.</span><span class="sxs-lookup"><span data-stu-id="e7939-126">If a [Polar](msdn-online-vml-polar-attribute.md) attribute is specified, the **Position** attribute represents the radius and angle values of the handle instead of x and y.</span></span>

<span data-ttu-id="e7939-127">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="e7939-127">The default value is 0,0.</span></span>

<span data-ttu-id="e7939-128">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="e7939-128">*VML Standard Attribute*</span></span>

 

 