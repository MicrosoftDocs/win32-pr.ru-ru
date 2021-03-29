---
title: Атрибут Строкевеигхт VML
description: Атрибут Строкевеигхт VML
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792204"
---
# <a name="vml-strokeweight-attribute"></a><span data-ttu-id="7e7c3-103">Атрибут Строкевеигхт VML</span><span class="sxs-lookup"><span data-stu-id="7e7c3-103">VML StrokeWeight Attribute</span></span>

<span data-ttu-id="7e7c3-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7e7c3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7e7c3-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="7e7c3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7e7c3-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="7e7c3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7e7c3-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7e7c3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7e7c3-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7e7c3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7e7c3-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7e7c3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7e7c3-110">Определяет толщину кисти, которая обозначает контур фигуры.</span><span class="sxs-lookup"><span data-stu-id="7e7c3-110">Defines the brush thickness that strokes the path of a shape.</span></span> <span data-ttu-id="7e7c3-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="7e7c3-111">Read/write.</span></span> <span data-ttu-id="7e7c3-112">**Вгленгс**.</span><span class="sxs-lookup"><span data-stu-id="7e7c3-112">**VGLength**.</span></span>

<span data-ttu-id="7e7c3-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="7e7c3-113">**Applies To**</span></span>

[<span data-ttu-id="7e7c3-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="7e7c3-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="7e7c3-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="7e7c3-115">**Tag Syntax**</span></span>

<span data-ttu-id="7e7c3-116"><v: *element* строкевеигхт = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="7e7c3-116"><v: *element* strokeweight=" *expression* "></span></span>

<span data-ttu-id="7e7c3-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="7e7c3-117">**Script Syntax**</span></span>

<span data-ttu-id="7e7c3-118">*element* . строкевеигхт = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="7e7c3-118">*element* .strokeweight="*expression*"</span></span>

<span data-ttu-id="7e7c3-119">*выражение* = *element*. строкевеигхт</span><span class="sxs-lookup"><span data-stu-id="7e7c3-119">*expression*=*element*.strokeweight</span></span>

<span data-ttu-id="7e7c3-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="7e7c3-120">**Remarks**</span></span>

<span data-ttu-id="7e7c3-121">Значение дублируется из атрибута **веса** элемента **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="7e7c3-121">The value is duplicated from the **Weight** attribute of the **Stroke** element.</span></span> <span data-ttu-id="7e7c3-122">Если указано число, но никакие единицы измерения не добавляются, то по умолчанию единицей измерений является ЕС.</span><span class="sxs-lookup"><span data-stu-id="7e7c3-122">If a number is specified, but no units are added, the default unit of measurement is the Emu.</span></span> <span data-ttu-id="7e7c3-123">Если значение не указано, по умолчанию используется 1 пиксель (1px).</span><span class="sxs-lookup"><span data-stu-id="7e7c3-123">If no value is specified, the default is 1 pixel (1px).</span></span>

<span data-ttu-id="7e7c3-124">Однако для сценариев единицей измерения по умолчанию является точка.</span><span class="sxs-lookup"><span data-stu-id="7e7c3-124">For scripting, however, the default unit of measurement is in points.</span></span>

<span data-ttu-id="7e7c3-125">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="7e7c3-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="7e7c3-126">**См. также:**</span><span class="sxs-lookup"><span data-stu-id="7e7c3-126">**See Also**</span></span>

<span data-ttu-id="7e7c3-127">[Stroke](msdn-online-vml-stroke-element.md), [ивгленгс](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)</span><span class="sxs-lookup"><span data-stu-id="7e7c3-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)</span></span>

<span data-ttu-id="7e7c3-128">**Пример**</span><span class="sxs-lookup"><span data-stu-id="7e7c3-128">**Example**</span></span>

<span data-ttu-id="7e7c3-129">Толщина штриха фигуры равна 1 пункту.</span><span class="sxs-lookup"><span data-stu-id="7e7c3-129">The stroke weight of the shape is 1 point.</span></span>


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="7e7c3-130">[Пример атрибута строкевеигхт](/previous-versions/bb264095(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7e7c3-130">[StrokeWeight Attribute Example](/previous-versions/bb264095(v=vs.85)).</span></span> <span data-ttu-id="7e7c3-131">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="7e7c3-131">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 