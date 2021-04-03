---
title: Атрибут Скевамт VML
description: Атрибут Скевамт VML
ms.assetid: ea685ea7-0853-4bcf-8ff2-39b714091429
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f75e469492ccc15b0ef3a03beffed05a5b2b1031
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987545"
---
# <a name="vml-skewamt-attribute"></a><span data-ttu-id="b1ae7-103">Атрибут Скевамт VML</span><span class="sxs-lookup"><span data-stu-id="b1ae7-103">VML SkewAmt Attribute</span></span>

<span data-ttu-id="b1ae7-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b1ae7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b1ae7-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b1ae7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b1ae7-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b1ae7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b1ae7-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b1ae7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b1ae7-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b1ae7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b1ae7-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b1ae7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b1ae7-110">Определяет величину наклона для объема.</span><span class="sxs-lookup"><span data-stu-id="b1ae7-110">Defines the amount of skew of an extrusion.</span></span> <span data-ttu-id="b1ae7-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b1ae7-111">Read/write.</span></span> <span data-ttu-id="b1ae7-112">**Вгперцент**.</span><span class="sxs-lookup"><span data-stu-id="b1ae7-112">**VgPercent**.</span></span>

<span data-ttu-id="b1ae7-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="b1ae7-113">**Applies To**</span></span>

[<span data-ttu-id="b1ae7-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="b1ae7-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="b1ae7-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="b1ae7-115">**Tag Syntax**</span></span>

<span data-ttu-id="b1ae7-116"><o: *element* скевамт = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="b1ae7-116"><o: *element* skewamt=" *expression* "></span></span>

<span data-ttu-id="b1ae7-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="b1ae7-117">**Script Syntax**</span></span>

<span data-ttu-id="b1ae7-118">*element* . скевамт = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="b1ae7-118">*element* .skewamt="*expression*"</span></span>

<span data-ttu-id="b1ae7-119">*выражение* = *element*. скевамт</span><span class="sxs-lookup"><span data-stu-id="b1ae7-119">*expression*=*element*.skewamt</span></span>

<span data-ttu-id="b1ae7-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b1ae7-120">**Remarks**</span></span>

<span data-ttu-id="b1ae7-121">Применяется к объему, только если значение атрибута [типа](type-attribute--extrusion--vml.md) объемной фигуры — *Parallel*.</span><span class="sxs-lookup"><span data-stu-id="b1ae7-121">Applies to an extrusion only if the extrusion [Type](type-attribute--extrusion--vml.md) attribute value is *parallel*.</span></span> <span data-ttu-id="b1ae7-122">Значение по умолчанию — 50%.</span><span class="sxs-lookup"><span data-stu-id="b1ae7-122">Default value is 50%.</span></span>

<span data-ttu-id="b1ae7-123">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="b1ae7-123">*Microsoft Office Extensions Attribute*</span></span>

 

 