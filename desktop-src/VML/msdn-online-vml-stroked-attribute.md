---
title: Атрибут VML Stroke
description: Атрибут VML Stroke
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134507"
---
# <a name="vml-stroked-attribute"></a><span data-ttu-id="c7e63-103">Атрибут VML Stroke</span><span class="sxs-lookup"><span data-stu-id="c7e63-103">VML Stroked Attribute</span></span>

<span data-ttu-id="c7e63-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c7e63-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c7e63-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="c7e63-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c7e63-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="c7e63-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c7e63-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c7e63-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c7e63-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c7e63-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c7e63-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c7e63-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c7e63-110">Определяет, будет ли контур обводкам.</span><span class="sxs-lookup"><span data-stu-id="c7e63-110">Defines whether the path will be stroked.</span></span> <span data-ttu-id="c7e63-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="c7e63-111">Read/write.</span></span> <span data-ttu-id="c7e63-112">[Вгтристате](msdn-online-vml-vgtristate.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e63-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span></span>

<span data-ttu-id="c7e63-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="c7e63-113">**Applies To**</span></span>

[<span data-ttu-id="c7e63-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="c7e63-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c7e63-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="c7e63-115">**Tag Syntax**</span></span>

<span data-ttu-id="c7e63-116"><v: *element* с обводкой = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="c7e63-116"><v: *element* stroked=" *expression* "></span></span>

<span data-ttu-id="c7e63-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="c7e63-117">**Script Syntax**</span></span>

<span data-ttu-id="c7e63-118">*element* . strokeed = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="c7e63-118">*element* .stroked="*expression*"</span></span>

<span data-ttu-id="c7e63-119">*выражение* = *элемент*. strokeed</span><span class="sxs-lookup"><span data-stu-id="c7e63-119">*expression*=*element*.stroked</span></span>

<span data-ttu-id="c7e63-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="c7e63-120">**Remarks**</span></span>

<span data-ttu-id="c7e63-121">Значение дублируется из атрибута **On** элемента [Stroke](msdn-online-vml-stroke-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e63-121">The value is duplicated from the **On** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="c7e63-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="c7e63-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="c7e63-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="c7e63-123">**Example**</span></span>

<span data-ttu-id="c7e63-124">Контур фигуры является обводкой.</span><span class="sxs-lookup"><span data-stu-id="c7e63-124">The shape path is stroked.</span></span>


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="c7e63-125">[Пример атрибута с обводкой](/previous-versions/bb264094(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7e63-125">[Stroked Attribute Example](/previous-versions/bb264094(v=vs.85)).</span></span> <span data-ttu-id="c7e63-126">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="c7e63-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 