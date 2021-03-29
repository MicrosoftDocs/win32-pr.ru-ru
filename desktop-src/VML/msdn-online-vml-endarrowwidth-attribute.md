---
title: Атрибут Ендарроввидс VML
description: Атрибут Ендарроввидс VML
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793765"
---
# <a name="vml-endarrowwidth-attribute"></a><span data-ttu-id="d882b-103">Атрибут Ендарроввидс VML</span><span class="sxs-lookup"><span data-stu-id="d882b-103">VML EndArrowWidth Attribute</span></span>

<span data-ttu-id="d882b-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d882b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d882b-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="d882b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d882b-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="d882b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d882b-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d882b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d882b-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d882b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d882b-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d882b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d882b-110">Определяет ширину стрелки для конца строки.</span><span class="sxs-lookup"><span data-stu-id="d882b-110">Defines an arrowhead width for the end of a line.</span></span> <span data-ttu-id="d882b-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="d882b-111">Read/write.</span></span> <span data-ttu-id="d882b-112">**Вгарровхеадвидс**.</span><span class="sxs-lookup"><span data-stu-id="d882b-112">**VgArrowheadWidth**.</span></span>

<span data-ttu-id="d882b-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="d882b-113">**Applies To**</span></span>

[<span data-ttu-id="d882b-114">Водок</span><span class="sxs-lookup"><span data-stu-id="d882b-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="d882b-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="d882b-115">**Tag Syntax**</span></span>

<span data-ttu-id="d882b-116"><v: *element* ендарроввидс = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="d882b-116"><v: *element* endarrowwidth=" *expression* "></span></span>

<span data-ttu-id="d882b-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="d882b-117">**Script Syntax**</span></span>

<span data-ttu-id="d882b-118">*element* . ендарроввидс = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="d882b-118">*element* .endarrowwidth="*expression*"</span></span>

<span data-ttu-id="d882b-119">*выражение* = *element*. ендарроввидс</span><span class="sxs-lookup"><span data-stu-id="d882b-119">*expression*=*element*.endarrowwidth</span></span>

<span data-ttu-id="d882b-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="d882b-120">**Remarks**</span></span>

<span data-ttu-id="d882b-121">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="d882b-121">Values include:</span></span>

-   <span data-ttu-id="d882b-122">Разрабатываем</span><span class="sxs-lookup"><span data-stu-id="d882b-122">Narrow</span></span>
-   <span data-ttu-id="d882b-123">Среднее (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d882b-123">Medium (default)</span></span>
-   <span data-ttu-id="d882b-124">Широкий</span><span class="sxs-lookup"><span data-stu-id="d882b-124">Wide</span></span>

<span data-ttu-id="d882b-125">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="d882b-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="d882b-126">**Пример**</span><span class="sxs-lookup"><span data-stu-id="d882b-126">**Example**</span></span>

<span data-ttu-id="d882b-127">Линия рисуется с помощью широкой классической стрелки в конце штриха.</span><span class="sxs-lookup"><span data-stu-id="d882b-127">A line is drawn with a wide classic arrowhead on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 