---
title: Атрибут Ендарров VML
description: Атрибут Ендарров VML
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542d6dbb3b30467c4bcad909f2b49d617f8bd886
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672413"
---
# <a name="vml-endarrow-attribute"></a><span data-ttu-id="76b34-103">Атрибут Ендарров VML</span><span class="sxs-lookup"><span data-stu-id="76b34-103">VML EndArrow Attribute</span></span>

<span data-ttu-id="76b34-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="76b34-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="76b34-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="76b34-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="76b34-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="76b34-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="76b34-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="76b34-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="76b34-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="76b34-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="76b34-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="76b34-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="76b34-110">Определяет наконечник для конца строки.</span><span class="sxs-lookup"><span data-stu-id="76b34-110">Defines an arrowhead for the end of a line.</span></span> <span data-ttu-id="76b34-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="76b34-111">Read/write.</span></span> <span data-ttu-id="76b34-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="76b34-112">**String**.</span></span>

<span data-ttu-id="76b34-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="76b34-113">**Applies To**</span></span>

[<span data-ttu-id="76b34-114">Водок</span><span class="sxs-lookup"><span data-stu-id="76b34-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="76b34-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="76b34-115">**Tag Syntax**</span></span>

<span data-ttu-id="76b34-116"><v: *element* ендарров = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="76b34-116"><v: *element* endarrow=" *expression* "></span></span>

<span data-ttu-id="76b34-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="76b34-117">**Script Syntax**</span></span>

<span data-ttu-id="76b34-118">*element* . ендарров = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="76b34-118">*element* .endarrow="*expression*"</span></span>

<span data-ttu-id="76b34-119">*выражение* = *element*. ендарров</span><span class="sxs-lookup"><span data-stu-id="76b34-119">*expression*=*element*.endarrow</span></span>

<span data-ttu-id="76b34-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="76b34-120">**Remarks**</span></span>

<span data-ttu-id="76b34-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="76b34-121">Values include:</span></span>

-   <span data-ttu-id="76b34-122">Нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76b34-122">None (default)</span></span>
-   <span data-ttu-id="76b34-123">Блокировать</span><span class="sxs-lookup"><span data-stu-id="76b34-123">Block</span></span>
-   <span data-ttu-id="76b34-124">Классический</span><span class="sxs-lookup"><span data-stu-id="76b34-124">Classic</span></span>
-   <span data-ttu-id="76b34-125">Ромб</span><span class="sxs-lookup"><span data-stu-id="76b34-125">Diamond</span></span>
-   <span data-ttu-id="76b34-126">Овал</span><span class="sxs-lookup"><span data-stu-id="76b34-126">Oval</span></span>
-   <span data-ttu-id="76b34-127">Открыть</span><span class="sxs-lookup"><span data-stu-id="76b34-127">Open</span></span>

<span data-ttu-id="76b34-128">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="76b34-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="76b34-129">**Пример**</span><span class="sxs-lookup"><span data-stu-id="76b34-129">**Example**</span></span>

<span data-ttu-id="76b34-130">Линия рисуется с помощью классической стрелки в конце штриха.</span><span class="sxs-lookup"><span data-stu-id="76b34-130">A line is drawn with a classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 