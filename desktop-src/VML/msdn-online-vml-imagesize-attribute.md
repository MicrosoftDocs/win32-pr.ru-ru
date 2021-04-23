---
title: Атрибут ImageSize для VML
description: Атрибут ImageSize для VML
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ae01d3162fdff67f0385736e5f0450b14ed6115
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792216"
---
# <a name="vml-imagesize-attribute"></a><span data-ttu-id="ba189-103">Атрибут ImageSize для VML</span><span class="sxs-lookup"><span data-stu-id="ba189-103">VML ImageSize Attribute</span></span>

<span data-ttu-id="ba189-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ba189-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ba189-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="ba189-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ba189-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="ba189-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ba189-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ba189-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ba189-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ba189-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ba189-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ba189-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ba189-110">Определяет размер изображения для штриха.</span><span class="sxs-lookup"><span data-stu-id="ba189-110">Defines the size of the image for the stroke.</span></span> <span data-ttu-id="ba189-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="ba189-111">Read/write.</span></span> <span data-ttu-id="ba189-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="ba189-112">**VgVector2D**.</span></span>

<span data-ttu-id="ba189-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="ba189-113">**Applies To**</span></span>

[<span data-ttu-id="ba189-114">Водок</span><span class="sxs-lookup"><span data-stu-id="ba189-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="ba189-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="ba189-115">**Tag Syntax**</span></span>

<span data-ttu-id="ba189-116"><v: *element* ImageSize = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="ba189-116"><v: *element* imagesize=" *expression* "></span></span>

<span data-ttu-id="ba189-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="ba189-117">**Script Syntax**</span></span>

<span data-ttu-id="ba189-118">*element* . ImageSize = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="ba189-118">*element* .imagesize="*expression*"</span></span>

<span data-ttu-id="ba189-119">*выражение* = *element*. ImageSize</span><span class="sxs-lookup"><span data-stu-id="ba189-119">*expression*=*element*.imagesize</span></span>

<span data-ttu-id="ba189-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="ba189-120">**Remarks**</span></span>

<span data-ttu-id="ba189-121">Значение по умолчанию — размер образа.</span><span class="sxs-lookup"><span data-stu-id="ba189-121">Default is the size of the image.</span></span>

<span data-ttu-id="ba189-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="ba189-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="ba189-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ba189-123">**Example**</span></span>

<span data-ttu-id="ba189-124">Изображение обводки будет иметь размер 10 на 10 пунктов.</span><span class="sxs-lookup"><span data-stu-id="ba189-124">The stroke image will be a 10-by-10 point size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 