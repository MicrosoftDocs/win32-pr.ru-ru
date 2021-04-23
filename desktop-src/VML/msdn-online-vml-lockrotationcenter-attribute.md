---
title: Атрибут Локкротатионцентер VML
description: Атрибут Локкротатионцентер VML
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672383"
---
# <a name="vml-lockrotationcenter-attribute"></a><span data-ttu-id="a9f6d-103">Атрибут Локкротатионцентер VML</span><span class="sxs-lookup"><span data-stu-id="a9f6d-103">VML LockRotationCenter Attribute</span></span>

<span data-ttu-id="a9f6d-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a9f6d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a9f6d-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="a9f6d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a9f6d-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="a9f6d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a9f6d-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a9f6d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a9f6d-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a9f6d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a9f6d-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a9f6d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a9f6d-110">Определяет, задается ли поворот вытянутого объекта атрибутом [ротатионангле](msdn-online-vml-rotationangle-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a9f6d-110">Determines whether the rotation of the extruded object is specified by the [RotationAngle](msdn-online-vml-rotationangle-attribute.md) attribute.</span></span> <span data-ttu-id="a9f6d-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="a9f6d-111">Read/write.</span></span> <span data-ttu-id="a9f6d-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="a9f6d-112">**VgTriState**.</span></span>

<span data-ttu-id="a9f6d-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="a9f6d-113">**Applies To**</span></span>

[<span data-ttu-id="a9f6d-114">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="a9f6d-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="a9f6d-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="a9f6d-115">**Tag Syntax**</span></span>

<span data-ttu-id="a9f6d-116"><o: *element* локкротатионцентер = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="a9f6d-116"><o: *element* lockrotationcenter=" *expression* "></span></span>

<span data-ttu-id="a9f6d-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="a9f6d-117">**Script Syntax**</span></span>

<span data-ttu-id="a9f6d-118">*element* . локкротатионцентер = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="a9f6d-118">*element* .lockrotationcenter="*expression*"</span></span>

<span data-ttu-id="a9f6d-119">*выражение* = *element*. локкротатионцентер</span><span class="sxs-lookup"><span data-stu-id="a9f6d-119">*expression*=*element*.lockrotationcenter</span></span>

<span data-ttu-id="a9f6d-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="a9f6d-120">**Remarks**</span></span>

<span data-ttu-id="a9f6d-121">Если **значение равно false**, поворот определяется атрибутом [Orientation](msdn-online-vml-orientation-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a9f6d-121">If **False**, the rotation is specified by the [Orientation](msdn-online-vml-orientation-attribute.md) attribute.</span></span> <span data-ttu-id="a9f6d-122">Значение по умолчанию равно **True**.</span><span class="sxs-lookup"><span data-stu-id="a9f6d-122">The default is **True**.</span></span>

<span data-ttu-id="a9f6d-123">Обратите внимание на следующее.</span><span class="sxs-lookup"><span data-stu-id="a9f6d-123">Note that:</span></span>


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



<span data-ttu-id="a9f6d-124">тот же самый:</span><span class="sxs-lookup"><span data-stu-id="a9f6d-124">is the same as:</span></span>


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



<span data-ttu-id="a9f6d-125">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="a9f6d-125">*Microsoft Office Extensions Attribute*</span></span>

 

 