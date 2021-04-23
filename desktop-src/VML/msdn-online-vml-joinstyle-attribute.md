---
title: Атрибут Жоинстиле VML
description: Атрибут Жоинстиле VML
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d3c815d6165cecd853f394780237ad0b89f0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691574"
---
# <a name="vml-joinstyle-attribute"></a><span data-ttu-id="13fc8-103">Атрибут Жоинстиле VML</span><span class="sxs-lookup"><span data-stu-id="13fc8-103">VML JoinStyle Attribute</span></span>

<span data-ttu-id="13fc8-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="13fc8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="13fc8-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="13fc8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="13fc8-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="13fc8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="13fc8-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="13fc8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="13fc8-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="13fc8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="13fc8-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="13fc8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="13fc8-110">Определяет стиль объединения ломаной линии.</span><span class="sxs-lookup"><span data-stu-id="13fc8-110">Defines the join style of a polyline.</span></span> <span data-ttu-id="13fc8-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="13fc8-111">Read/write.</span></span> <span data-ttu-id="13fc8-112">Строка.</span><span class="sxs-lookup"><span data-stu-id="13fc8-112">String.</span></span>

<span data-ttu-id="13fc8-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="13fc8-113">**Applies To**</span></span>

[<span data-ttu-id="13fc8-114">Водок</span><span class="sxs-lookup"><span data-stu-id="13fc8-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="13fc8-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="13fc8-115">**Tag Syntax**</span></span>

<span data-ttu-id="13fc8-116"><v: *element* жоинстиле = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="13fc8-116"><v: *element* joinstyle=" *expression* "></span></span>

<span data-ttu-id="13fc8-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="13fc8-117">**Script Syntax**</span></span>

<span data-ttu-id="13fc8-118">*element* . жоинстиле = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="13fc8-118">*element* .joinstyle="*expression*"</span></span>

<span data-ttu-id="13fc8-119">*выражение* = *element*. жоинстиле</span><span class="sxs-lookup"><span data-stu-id="13fc8-119">*expression*=*element*.joinstyle</span></span>

<span data-ttu-id="13fc8-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="13fc8-120">**Remarks**</span></span>

<span data-ttu-id="13fc8-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="13fc8-121">Values include:</span></span>

-   <span data-ttu-id="13fc8-122">Round (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13fc8-122">round (default)</span></span>
-   <span data-ttu-id="13fc8-123">рамки</span><span class="sxs-lookup"><span data-stu-id="13fc8-123">bevel</span></span>
-   <span data-ttu-id="13fc8-124">срезу</span><span class="sxs-lookup"><span data-stu-id="13fc8-124">miter</span></span>

<span data-ttu-id="13fc8-125">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="13fc8-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="13fc8-126">**Пример**</span><span class="sxs-lookup"><span data-stu-id="13fc8-126">**Example**</span></span>

<span data-ttu-id="13fc8-127">Соединения в ломаной линии багетны.</span><span class="sxs-lookup"><span data-stu-id="13fc8-127">The joints on the polyline are beveled.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 