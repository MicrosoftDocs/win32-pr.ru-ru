---
title: Атрибут Виевпоинторигин VML
description: Атрибут Виевпоинторигин VML
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad256f0f5d38c6fbbfb5722e803985506efca217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487856"
---
# <a name="vml-viewpointorigin-attribute"></a><span data-ttu-id="b4325-103">Атрибут Виевпоинторигин VML</span><span class="sxs-lookup"><span data-stu-id="b4325-103">VML ViewpointOrigin Attribute</span></span>

<span data-ttu-id="b4325-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b4325-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b4325-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b4325-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b4325-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b4325-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b4325-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b4325-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b4325-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b4325-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b4325-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b4325-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b4325-110">Определяет источник точки зрения в ограничивающем прямоугольнике фигуры.</span><span class="sxs-lookup"><span data-stu-id="b4325-110">Defines the origin of the viewpoint within the bounding box of the shape.</span></span> <span data-ttu-id="b4325-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b4325-111">Read/write.</span></span> <span data-ttu-id="b4325-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="b4325-112">**VgVector2D**.</span></span>

<span data-ttu-id="b4325-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="b4325-113">**Applies To**</span></span>

[<span data-ttu-id="b4325-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="b4325-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="b4325-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="b4325-115">**Tag Syntax**</span></span>

<span data-ttu-id="b4325-116"><o: *element* виевпоинторигин = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="b4325-116"><o: *element* viewpointorigin=" *expression* "></span></span>

<span data-ttu-id="b4325-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="b4325-117">**Script Syntax**</span></span>

<span data-ttu-id="b4325-118">*element* . виевпоинторигин = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="b4325-118">*element* .viewpointorigin="*expression*"</span></span>

<span data-ttu-id="b4325-119">*выражение* = *element*. виевпоинторигин</span><span class="sxs-lookup"><span data-stu-id="b4325-119">*expression*=*element*.viewpointorigin</span></span>

<span data-ttu-id="b4325-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b4325-120">**Remarks**</span></span>

<span data-ttu-id="b4325-121">Определяет точку зрения в терминах значений x и y исходной фигуры.</span><span class="sxs-lookup"><span data-stu-id="b4325-121">Defines the viewpoint in terms of the x and y values of the original shape.</span></span> <span data-ttu-id="b4325-122">Значения x и y находятся в диапазоне от 0,5 до-0,5 (50% до-50% от начала координат фигуры).</span><span class="sxs-lookup"><span data-stu-id="b4325-122">The x and y values range from 0.5 to -0.5 (50% to -50% of the shape's coordinate origin).</span></span> <span data-ttu-id="b4325-123">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="b4325-123">The default is 0,0.</span></span>

<span data-ttu-id="b4325-124">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="b4325-124">*Microsoft Office Extensions Attribute*</span></span>

 

 