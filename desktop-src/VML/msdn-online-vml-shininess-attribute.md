---
title: Атрибут коэффициента блеска VML
description: Атрибут коэффициента блеска VML
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a116adeb955c0f3449b374947a3f8121bd848e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337596"
---
# <a name="vml-shininess-attribute"></a><span data-ttu-id="ae832-103">Атрибут коэффициента блеска VML</span><span class="sxs-lookup"><span data-stu-id="ae832-103">VML Shininess Attribute</span></span>

<span data-ttu-id="ae832-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ae832-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ae832-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ae832-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ae832-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ae832-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ae832-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ae832-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ae832-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ae832-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ae832-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ae832-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ae832-110">Определяет концентрацию отраженного освещения на поверхности объема.</span><span class="sxs-lookup"><span data-stu-id="ae832-110">Defines the concentration of the reflected light on an extrusion surface.</span></span> <span data-ttu-id="ae832-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ae832-111">Read/write.</span></span> <span data-ttu-id="ae832-112">**Вгнумбер**.</span><span class="sxs-lookup"><span data-stu-id="ae832-112">**VgNumber**.</span></span>

<span data-ttu-id="ae832-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ae832-113">**Applies To**</span></span>

[<span data-ttu-id="ae832-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="ae832-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="ae832-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ae832-115">**Tag Syntax**</span></span>

<span data-ttu-id="ae832-116"><o: *element* коэффициента блеска = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="ae832-116"><o: *element* shininess=" *expression* "></span></span>

<span data-ttu-id="ae832-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ae832-117">**Script Syntax**</span></span>

<span data-ttu-id="ae832-118">*element* . коэффициента блеска = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="ae832-118">*element* .shininess="*expression*"</span></span>

<span data-ttu-id="ae832-119">*выражение* = *element*. коэффициента блеска</span><span class="sxs-lookup"><span data-stu-id="ae832-119">*expression*=*element*.shininess</span></span>

<span data-ttu-id="ae832-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ae832-120">**Remarks**</span></span>

<span data-ttu-id="ae832-121">Высокие значения (8-10) будут приблизительными, что коэффициента блеска зеркального и нижнего значений (2-3) будет приблизительным результатом спекклед.</span><span class="sxs-lookup"><span data-stu-id="ae832-121">High values (8-10) would approximate the shininess of a mirror and low values (2-3) would approximate a speckled effect.</span></span> <span data-ttu-id="ae832-122">Значения 4-7 являются типичными.</span><span class="sxs-lookup"><span data-stu-id="ae832-122">Values of 4-7 are typical.</span></span> <span data-ttu-id="ae832-123">Отражения не отражают другие объекты; отражаются только источники освещения.</span><span class="sxs-lookup"><span data-stu-id="ae832-123">Reflections do not mirror other objects; only pinpoint light sources are reflected.</span></span> <span data-ttu-id="ae832-124">Значение по умолчанию — 5.</span><span class="sxs-lookup"><span data-stu-id="ae832-124">Default value is 5.</span></span>

<span data-ttu-id="ae832-125">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="ae832-125">*Microsoft Office Extensions Attribute*</span></span>

 

 