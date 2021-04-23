---
title: Атрибут Ауторотатионцентер VML
description: Атрибут Ауторотатионцентер VML
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1624ab3f2c37e043a6d478ca8e422a714a83d157
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792390"
---
# <a name="vml-autorotationcenter-attribute"></a><span data-ttu-id="4ecb5-103">Атрибут Ауторотатионцентер VML</span><span class="sxs-lookup"><span data-stu-id="4ecb5-103">VML AutoRotationCenter Attribute</span></span>

<span data-ttu-id="4ecb5-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4ecb5-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4ecb5-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4ecb5-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4ecb5-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4ecb5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4ecb5-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4ecb5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4ecb5-110">Определяет, будет ли центр вращения являться геометрическим центром объема.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-110">Determines whether the center of rotation will be the geometric center of the extrusion.</span></span> <span data-ttu-id="4ecb5-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-111">Read/write.</span></span> <span data-ttu-id="4ecb5-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-112">**VgTriState**.</span></span>

<span data-ttu-id="4ecb5-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="4ecb5-113">**Applies To**</span></span>

[<span data-ttu-id="4ecb5-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="4ecb5-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="4ecb5-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="4ecb5-115">**Tag Syntax**</span></span>

<span data-ttu-id="4ecb5-116"><o: *element* ауторотатионцентер = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="4ecb5-116"><o: *element* autorotationcenter=" *expression* "></span></span>

<span data-ttu-id="4ecb5-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="4ecb5-117">**Script Syntax**</span></span>

<span data-ttu-id="4ecb5-118">*element* . ауторотатионцентер = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="4ecb5-118">*element* .autorotationcenter="*expression*"</span></span>

<span data-ttu-id="4ecb5-119">*выражение* = *element*. ауторотатионцентер</span><span class="sxs-lookup"><span data-stu-id="4ecb5-119">*expression*=*element*.autorotationcenter</span></span>

<span data-ttu-id="4ecb5-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="4ecb5-120">**Remarks**</span></span>

<span data-ttu-id="4ecb5-121">Геометрический центр вытянутой фигуры равен 0, 0, 0.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-121">The geometric center of an extruded shape is 0,0,0.</span></span> <span data-ttu-id="4ecb5-122">Если значение этого атрибута равно **false**, центр вращения определяется атрибутом [ротатионцентер](msdn-online-vml-rotationcenter-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="4ecb5-122">If the value of this attribute is **False**, the center of rotation is determined by the [RotationCenter](msdn-online-vml-rotationcenter-attribute.md) attribute.</span></span> <span data-ttu-id="4ecb5-123">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="4ecb5-123">The default is **False**.</span></span>

<span data-ttu-id="4ecb5-124">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="4ecb5-124">*Microsoft Office Extensions Attribute*</span></span>

 

 