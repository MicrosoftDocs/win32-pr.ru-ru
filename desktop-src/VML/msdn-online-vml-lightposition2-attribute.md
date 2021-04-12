---
title: Атрибут LightPosition2 VML
description: Атрибут LightPosition2 VML
ms.assetid: 75ae4154-240f-4981-a527-d9e0a721e8b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5306be47bec8b72b6bafc49e404b3369ace19e50
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337708"
---
# <a name="vml-lightposition2-attribute"></a><span data-ttu-id="66c94-103">Атрибут LightPosition2 VML</span><span class="sxs-lookup"><span data-stu-id="66c94-103">VML LightPosition2 Attribute</span></span>

<span data-ttu-id="66c94-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="66c94-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="66c94-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="66c94-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="66c94-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="66c94-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="66c94-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="66c94-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="66c94-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="66c94-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="66c94-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="66c94-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="66c94-110">Задает расположение дополнительного освещения в сцене.</span><span class="sxs-lookup"><span data-stu-id="66c94-110">Specifies the position of the secondary light in a scene.</span></span> <span data-ttu-id="66c94-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="66c94-111">Read/write.</span></span> <span data-ttu-id="66c94-112">**VgVector3D**.</span><span class="sxs-lookup"><span data-stu-id="66c94-112">**VgVector3D**.</span></span>

<span data-ttu-id="66c94-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="66c94-113">**Applies To**</span></span>

[<span data-ttu-id="66c94-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="66c94-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="66c94-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="66c94-115">**Tag Syntax**</span></span>

<span data-ttu-id="66c94-116"><o: *element* lightposition2 = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="66c94-116"><o: *element* lightposition2=" *expression* "></span></span>

<span data-ttu-id="66c94-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="66c94-117">**Script Syntax**</span></span>

<span data-ttu-id="66c94-118">*element* . lightposition2 = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="66c94-118">*element* .lightposition2="*expression*"</span></span>

<span data-ttu-id="66c94-119">*выражение* = *element*. lightposition2</span><span class="sxs-lookup"><span data-stu-id="66c94-119">*expression*=*element*.lightposition2</span></span>

<span data-ttu-id="66c94-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="66c94-120">**Remarks**</span></span>

<span data-ttu-id="66c94-121">Используйте это значение для перемещения второго источника освещения для объемной фигуры.</span><span class="sxs-lookup"><span data-stu-id="66c94-121">Use this value to move the second light source for an extrusion.</span></span> <span data-ttu-id="66c94-122">Разные позиции будут светлее или темнее на каждой грани.</span><span class="sxs-lookup"><span data-stu-id="66c94-122">Different positions will lighten or darken each face of the extrusion.</span></span> <span data-ttu-id="66c94-123">Значение по умолчанию — 50000, 0, 10000.</span><span class="sxs-lookup"><span data-stu-id="66c94-123">The default value is -50000, 0, 10000.</span></span>

<span data-ttu-id="66c94-124">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="66c94-124">*Microsoft Office Extensions Attribute*</span></span>

 

 