---
title: Атрибут глубины в формате VML
description: Атрибут глубины в формате VML
ms.assetid: afac0e39-1006-4d73-a4d9-7ed2484019a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07faa74fc22b506550904a5a8125d0c26f36637b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338148"
---
# <a name="vml-backdepth-attribute"></a><span data-ttu-id="c5f2b-103">Атрибут глубины в формате VML</span><span class="sxs-lookup"><span data-stu-id="c5f2b-103">VML BackDepth Attribute</span></span>

<span data-ttu-id="c5f2b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c5f2b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c5f2b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="c5f2b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c5f2b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="c5f2b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c5f2b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c5f2b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c5f2b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c5f2b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c5f2b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c5f2b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c5f2b-110">Определяет величину обратной придания.</span><span class="sxs-lookup"><span data-stu-id="c5f2b-110">Defines the amount of backward extrusion.</span></span> <span data-ttu-id="c5f2b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="c5f2b-111">Read/write.</span></span> <span data-ttu-id="c5f2b-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="c5f2b-112">**VgNumber**.</span></span>

<span data-ttu-id="c5f2b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c5f2b-113">**Applies To**</span></span>

[<span data-ttu-id="c5f2b-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="c5f2b-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="c5f2b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="c5f2b-115">**Tag Syntax**</span></span>

<span data-ttu-id="c5f2b-116"><o: *элемент* Depth = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="c5f2b-116"><o: *element* backdepth=" *expression* "></span></span>

<span data-ttu-id="c5f2b-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="c5f2b-117">**Script Syntax**</span></span>

<span data-ttu-id="c5f2b-118">*element* . undepth = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="c5f2b-118">*element* .backdepth="*expression*"</span></span>

<span data-ttu-id="c5f2b-119">*выражение* = *элемент*. Глубина</span><span class="sxs-lookup"><span data-stu-id="c5f2b-119">*expression*=*element*.backdepth</span></span>

<span data-ttu-id="c5f2b-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c5f2b-120">**Remarks**</span></span>

<span data-ttu-id="c5f2b-121">Значение "назад" — это объем объема, который отображается позади фигуры.</span><span class="sxs-lookup"><span data-stu-id="c5f2b-121">Backward extrusion is the amount of extrusion that appears to be behind the shape.</span></span> <span data-ttu-id="c5f2b-122">Единицы по умолчанию находятся в точках, а значение по умолчанию — 36pt.</span><span class="sxs-lookup"><span data-stu-id="c5f2b-122">The default units are in points and the default value is 36pt.</span></span>

<span data-ttu-id="c5f2b-123">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="c5f2b-123">*Microsoft Office Extensions Attribute*</span></span>

 

 