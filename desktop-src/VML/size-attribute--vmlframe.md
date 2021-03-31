---
title: Атрибут size (Вмлфраме)
description: Атрибут size (Вмлфраме)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070068"
---
# <a name="size-attribute-vmlframe"></a><span data-ttu-id="c2851-103">Атрибут size (Вмлфраме)</span><span class="sxs-lookup"><span data-stu-id="c2851-103">Size Attribute (VMLFrame)</span></span>

<span data-ttu-id="c2851-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c2851-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c2851-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="c2851-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c2851-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="c2851-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c2851-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c2851-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c2851-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c2851-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c2851-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c2851-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c2851-110">Определяет размер области обрезки рамки.</span><span class="sxs-lookup"><span data-stu-id="c2851-110">Defines the size of the clipping region of the frame.</span></span> <span data-ttu-id="c2851-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="c2851-111">Read/write.</span></span> <span data-ttu-id="c2851-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="c2851-112">**VgVector2D**.</span></span>

<span data-ttu-id="c2851-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c2851-113">**Applies To**</span></span>

[<span data-ttu-id="c2851-114">вмлфраме</span><span class="sxs-lookup"><span data-stu-id="c2851-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="c2851-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="c2851-115">**Tag Syntax**</span></span>

<span data-ttu-id="c2851-116"><v: size *элемента* = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="c2851-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="c2851-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="c2851-117">**Script Syntax**</span></span>

<span data-ttu-id="c2851-118">*element* . size = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="c2851-118">*element* .size="*expression*"</span></span>

<span data-ttu-id="c2851-119">*выражение* = *элемент*. размер</span><span class="sxs-lookup"><span data-stu-id="c2851-119">*expression*=*element*.size</span></span>

<span data-ttu-id="c2851-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c2851-120">**Remarks**</span></span>

<span data-ttu-id="c2851-121">Значение по умолчанию — 0, 0.</span><span class="sxs-lookup"><span data-stu-id="c2851-121">The default value is 0,0.</span></span> <span data-ttu-id="c2851-122">Обратите внимание, что **size** работает, только если функция [Clip](msdn-online-vml-clip-attribute.md) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="c2851-122">Note that **Size** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="c2851-123">В этом атрибуте размер определяется как ширина и высота рамки.</span><span class="sxs-lookup"><span data-stu-id="c2851-123">In this attribute, the size is defined as the width and height of the frame.</span></span>

<span data-ttu-id="c2851-124">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="c2851-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="c2851-125">**Пример**</span><span class="sxs-lookup"><span data-stu-id="c2851-125">**Example**</span></span>

<span data-ttu-id="c2851-126">Размер области отсечения будет 50Pt, 50Pt.</span><span class="sxs-lookup"><span data-stu-id="c2851-126">The size of the clipping region will be 50pt, 50pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 