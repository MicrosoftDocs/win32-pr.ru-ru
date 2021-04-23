---
title: Атрибут Ендкап VML
description: Атрибут Ендкап VML
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726d2bba2128ebb1897f306ae608f4bebb48d63f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339185"
---
# <a name="vml-endcap-attribute"></a><span data-ttu-id="b1699-103">Атрибут Ендкап VML</span><span class="sxs-lookup"><span data-stu-id="b1699-103">VML EndCap Attribute</span></span>

<span data-ttu-id="b1699-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b1699-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b1699-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b1699-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b1699-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b1699-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b1699-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b1699-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b1699-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b1699-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b1699-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b1699-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b1699-110">Определяет стиль конца штриха.</span><span class="sxs-lookup"><span data-stu-id="b1699-110">Defines the cap style for the end of a stroke.</span></span> <span data-ttu-id="b1699-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b1699-111">Read/write.</span></span> <span data-ttu-id="b1699-112">**Вглининдкапстиле**.</span><span class="sxs-lookup"><span data-stu-id="b1699-112">**VgLineEndCapStyle**.</span></span>

<span data-ttu-id="b1699-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="b1699-113">**Applies To**</span></span>

[<span data-ttu-id="b1699-114">Водок</span><span class="sxs-lookup"><span data-stu-id="b1699-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="b1699-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="b1699-115">**Tag Syntax**</span></span>

<span data-ttu-id="b1699-116"><v: *element* ендкап = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="b1699-116"><v: *element* endcap=" *expression* "></span></span>

<span data-ttu-id="b1699-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="b1699-117">**Script Syntax**</span></span>

<span data-ttu-id="b1699-118">*element* . ендкап = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="b1699-118">*element* .endcap="*expression*"</span></span>

<span data-ttu-id="b1699-119">*выражение* = *element*. ендкап</span><span class="sxs-lookup"><span data-stu-id="b1699-119">*expression*=*element*.endcap</span></span>

<span data-ttu-id="b1699-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b1699-120">**Remarks**</span></span>

<span data-ttu-id="b1699-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="b1699-121">Values include:</span></span>

-   <span data-ttu-id="b1699-122">Flat (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1699-122">Flat (default)</span></span>
-   <span data-ttu-id="b1699-123">Square</span><span class="sxs-lookup"><span data-stu-id="b1699-123">Square</span></span>
-   <span data-ttu-id="b1699-124">Round</span><span class="sxs-lookup"><span data-stu-id="b1699-124">Round</span></span>

<span data-ttu-id="b1699-125">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="b1699-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="b1699-126">**Пример**</span><span class="sxs-lookup"><span data-stu-id="b1699-126">**Example**</span></span>

<span data-ttu-id="b1699-127">Линия рисуется с плоским ограничением в конце штриха.</span><span class="sxs-lookup"><span data-stu-id="b1699-127">A line is drawn with a flat cap on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 