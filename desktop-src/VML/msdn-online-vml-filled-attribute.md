---
title: Закрашенный атрибут VML
description: Закрашенный атрибут VML
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 232d8b36b6d272c3a1ee8c17f3ddeca023ab4708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488256"
---
# <a name="vml-filled-attribute"></a><span data-ttu-id="85e5d-103">Закрашенный атрибут VML</span><span class="sxs-lookup"><span data-stu-id="85e5d-103">VML Filled Attribute</span></span>

<span data-ttu-id="85e5d-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="85e5d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="85e5d-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="85e5d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="85e5d-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="85e5d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="85e5d-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="85e5d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="85e5d-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="85e5d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="85e5d-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="85e5d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="85e5d-110">Определяет, будет ли заполнен замкнутый контур.</span><span class="sxs-lookup"><span data-stu-id="85e5d-110">Determines whether the closed path will be filled.</span></span> <span data-ttu-id="85e5d-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="85e5d-111">Read/write.</span></span> <span data-ttu-id="85e5d-112">**Вгтристате**.</span><span class="sxs-lookup"><span data-stu-id="85e5d-112">**VgTriState**.</span></span>

<span data-ttu-id="85e5d-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="85e5d-113">**Applies To**</span></span>

[<span data-ttu-id="85e5d-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="85e5d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="85e5d-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="85e5d-115">**Tag Syntax**</span></span>

<span data-ttu-id="85e5d-116"><v: *элемент* заполнен = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="85e5d-116"><v: *element* filled=" *expression* "></span></span>

<span data-ttu-id="85e5d-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="85e5d-117">**Script Syntax**</span></span>

<span data-ttu-id="85e5d-118">*element* . filled = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="85e5d-118">*element* .filled="*expression*"</span></span>

<span data-ttu-id="85e5d-119">*выражение* = *element*. filled</span><span class="sxs-lookup"><span data-stu-id="85e5d-119">*expression*=*element*.filled</span></span>

<span data-ttu-id="85e5d-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="85e5d-120">**Remarks**</span></span>

<span data-ttu-id="85e5d-121">Значение дублируется из атрибута **On** элемента [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="85e5d-121">The value is duplicated from the **On** attribute of the [Fill](msdn-online-vml-fill-element.md) element.</span></span>

<span data-ttu-id="85e5d-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="85e5d-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="85e5d-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="85e5d-123">**Example**</span></span>

<span data-ttu-id="85e5d-124">Контур фигуры заполнен.</span><span class="sxs-lookup"><span data-stu-id="85e5d-124">The shape path is filled.</span></span>


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="85e5d-125">[Пример атрибута с заливкой](/previous-versions/bb229669(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85e5d-125">[Filled Attribute Example](/previous-versions/bb229669(v=vs.85)).</span></span> <span data-ttu-id="85e5d-126">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="85e5d-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 