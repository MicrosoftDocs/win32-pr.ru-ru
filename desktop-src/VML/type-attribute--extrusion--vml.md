---
title: Атрибут типа (объемная) (VML)
description: Атрибут типа (объемная) (VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890853"
---
# <a name="type-attribute-extrusionvml"></a><span data-ttu-id="e0c9a-103">Атрибут типа (объемная) (VML)</span><span class="sxs-lookup"><span data-stu-id="e0c9a-103">Type Attribute (Extrusion)(VML)</span></span>

<span data-ttu-id="e0c9a-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e0c9a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e0c9a-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="e0c9a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e0c9a-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="e0c9a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e0c9a-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e0c9a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e0c9a-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e0c9a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e0c9a-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e0c9a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e0c9a-110">Определяет способ вытягивания фигуры.</span><span class="sxs-lookup"><span data-stu-id="e0c9a-110">Defines the way that the shape is extruded.</span></span> <span data-ttu-id="e0c9a-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="e0c9a-111">Read/write.</span></span> <span data-ttu-id="e0c9a-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="e0c9a-112">**String**.</span></span>

<span data-ttu-id="e0c9a-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="e0c9a-113">**Applies To**</span></span>

[<span data-ttu-id="e0c9a-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="e0c9a-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="e0c9a-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="e0c9a-115">**Tag Syntax**</span></span>

<span data-ttu-id="e0c9a-116"><o: *element* Type = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="e0c9a-116"><o: *element* type=" *expression* "></span></span>

<span data-ttu-id="e0c9a-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="e0c9a-117">**Script Syntax**</span></span>

<span data-ttu-id="e0c9a-118">*element* . Type = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="e0c9a-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="e0c9a-119">*выражение* = *element*. Type</span><span class="sxs-lookup"><span data-stu-id="e0c9a-119">*expression*=*element*.type</span></span>

<span data-ttu-id="e0c9a-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="e0c9a-120">**Remarks**</span></span>

<span data-ttu-id="e0c9a-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="e0c9a-121">Values include:</span></span>



| <span data-ttu-id="e0c9a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e0c9a-122">Value</span></span>       | <span data-ttu-id="e0c9a-123">Описание</span><span class="sxs-lookup"><span data-stu-id="e0c9a-123">Description</span></span>                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c9a-124">parallel</span><span class="sxs-lookup"><span data-stu-id="e0c9a-124">parallel</span></span>    | <span data-ttu-id="e0c9a-125">Объем выводится таким образом, что центр проекции бесконечно выходит из него. Это значит, что линии объемной фигуры не сходятся (в отличие от проекций перспективы).</span><span class="sxs-lookup"><span data-stu-id="e0c9a-125">Extrusion is rendered so that the center of projection is infinitely far away; that is, the extrusion lines do not converge (unlike perspective projections).</span></span> <span data-ttu-id="e0c9a-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0c9a-126">Default.</span></span> |
| <span data-ttu-id="e0c9a-127">перспектива</span><span class="sxs-lookup"><span data-stu-id="e0c9a-127">perspective</span></span> | <span data-ttu-id="e0c9a-128">Объем выводится в центре проекции, который аналогичен точке исчезновения для неповернутых объектов.</span><span class="sxs-lookup"><span data-stu-id="e0c9a-128">Extrusion is rendered to a center of projection, which is the same as the vanishing point for unrotated objects.</span></span>                                                       |



 

<span data-ttu-id="e0c9a-129">**Атрибут расширений Microsoft Office**</span><span class="sxs-lookup"><span data-stu-id="e0c9a-129">**Microsoft Office Extensions Attribute**</span></span>

 

 