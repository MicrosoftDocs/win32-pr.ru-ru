---
title: Атрибут Лигхтпоситион VML
description: Атрибут Лигхтпоситион VML
ms.assetid: 2ac3825d-319e-4761-905d-eb8127c4d4cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c7b1e034b8755da78e4a34cf72299380ca28af4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691518"
---
# <a name="vml-lightposition-attribute"></a><span data-ttu-id="844be-103">Атрибут Лигхтпоситион VML</span><span class="sxs-lookup"><span data-stu-id="844be-103">VML LightPosition Attribute</span></span>

<span data-ttu-id="844be-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="844be-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="844be-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="844be-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="844be-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="844be-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="844be-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="844be-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="844be-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="844be-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="844be-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="844be-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="844be-110">Задает расположение основного освещения в сцене.</span><span class="sxs-lookup"><span data-stu-id="844be-110">Specifies the position of the primary light in a scene.</span></span> <span data-ttu-id="844be-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="844be-111">Read/write.</span></span> <span data-ttu-id="844be-112">**VgVector3D**.</span><span class="sxs-lookup"><span data-stu-id="844be-112">**VgVector3D**..</span></span>

<span data-ttu-id="844be-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="844be-113">**Applies To**</span></span>

[<span data-ttu-id="844be-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="844be-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="844be-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="844be-115">**Tag Syntax**</span></span>

<span data-ttu-id="844be-116"><o: *element* лигхтпоситион = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="844be-116"><o: *element* lightposition=" *expression* "></span></span>

<span data-ttu-id="844be-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="844be-117">**Script Syntax**</span></span>

<span data-ttu-id="844be-118">*element* . лигхтпоситион = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="844be-118">*element* .lightposition="*expression*"</span></span>

<span data-ttu-id="844be-119">*выражение* = *element*. лигхтпоситион</span><span class="sxs-lookup"><span data-stu-id="844be-119">*expression*=*element*.lightposition</span></span>

<span data-ttu-id="844be-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="844be-120">**Remarks**</span></span>

<span data-ttu-id="844be-121">Используйте это значение для перемещения источника освещения для объема.</span><span class="sxs-lookup"><span data-stu-id="844be-121">Use this value to move the light source for an extrusion.</span></span> <span data-ttu-id="844be-122">Разные позиции будут светлее или темнее на каждой грани.</span><span class="sxs-lookup"><span data-stu-id="844be-122">Different positions will lighten or darken each face of the extrusion.</span></span> <span data-ttu-id="844be-123">Значение по умолчанию — 50000, 0, 10000.</span><span class="sxs-lookup"><span data-stu-id="844be-123">The default value is 50000,0,10000.</span></span>

<span data-ttu-id="844be-124">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="844be-124">*Microsoft Office Extensions Attribute*</span></span>

 

 