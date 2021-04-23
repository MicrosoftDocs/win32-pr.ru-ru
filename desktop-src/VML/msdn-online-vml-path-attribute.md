---
title: Атрибут пути VML
description: Атрибут пути VML
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891045"
---
# <a name="vml-path-attribute"></a><span data-ttu-id="582b0-103">Атрибут пути VML</span><span class="sxs-lookup"><span data-stu-id="582b0-103">VML Path Attribute</span></span>

<span data-ttu-id="582b0-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="582b0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="582b0-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="582b0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="582b0-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="582b0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="582b0-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="582b0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="582b0-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="582b0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="582b0-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="582b0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="582b0-110">Задает линию, составляющую края фигуры.</span><span class="sxs-lookup"><span data-stu-id="582b0-110">Specifies the line that makes up the edges of a shape.</span></span> <span data-ttu-id="582b0-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="582b0-111">Read/write.</span></span> <span data-ttu-id="582b0-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="582b0-112">**String**.</span></span>

<span data-ttu-id="582b0-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="582b0-113">**Applies To**</span></span>

[<span data-ttu-id="582b0-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="582b0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="582b0-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="582b0-115">**Tag Syntax**</span></span>

<span data-ttu-id="582b0-116"><v: *элемент* Path = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="582b0-116"><v: *element* path=" *expression* "></span></span>

<span data-ttu-id="582b0-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="582b0-117">**Script Syntax**</span></span>

<span data-ttu-id="582b0-118">*element* . path = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="582b0-118">*element* .path="*expression*"</span></span>

<span data-ttu-id="582b0-119">*выражение* = *элемент*. Path</span><span class="sxs-lookup"><span data-stu-id="582b0-119">*expression*=*element*.path</span></span>

<span data-ttu-id="582b0-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="582b0-120">**Remarks**</span></span>

<span data-ttu-id="582b0-121">Если фигура содержит элемент [path](msdn-online-vml-path-element.md) , команды пути элемента Path имеют приоритет над значением атрибута Shape.</span><span class="sxs-lookup"><span data-stu-id="582b0-121">If a shape contains the [Path](msdn-online-vml-path-element.md) element, the path commands of the Path element take precedence over the shape attribute value.</span></span> <span data-ttu-id="582b0-122">Дополнительные сведения о наборе команд, используемых для путей, см. в разделе элемент **path** .</span><span class="sxs-lookup"><span data-stu-id="582b0-122">See the **Path** element topic for details on the command set used for paths.</span></span>

<span data-ttu-id="582b0-123">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="582b0-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="582b0-124">**Пример**</span><span class="sxs-lookup"><span data-stu-id="582b0-124">**Example**</span></span>

<span data-ttu-id="582b0-125">Замкнутый квадратный путь определяется в строке атрибута path.</span><span class="sxs-lookup"><span data-stu-id="582b0-125">A closed square path is defined in the string of the path attribute.</span></span> <span data-ttu-id="582b0-126">Начальная точка определяется с помощью `m` (используется для команды **MoveTo** ) в 1, 1 и рисуется по строке `l` (буква "L", используемая для команды **lineTo**) от начальной позиции (1, 1) до трех других точек (по порядку): 1 200; 200 200; 200, 1.</span><span class="sxs-lookup"><span data-stu-id="582b0-126">An initial point is defined with `m` (used for the **moveto** command) at 1,1 and a line is drawn with `l` (the letter "L" used for the command **lineto**) from the starting position (1,1) to the other three points (in order): 1,200; 200,200; 200,1.</span></span> <span data-ttu-id="582b0-127">Строка закрывается с помощью `x` (**Close**) и заканчивается `e` (**End**).</span><span class="sxs-lookup"><span data-stu-id="582b0-127">The line is closed with `x` (**close**) and ended with `e` (**end**).</span></span> <span data-ttu-id="582b0-128">Обратите внимание, что координаты задаются в относительном пространстве координат, а реальный размер определяется **шириной** и **высотой**.</span><span class="sxs-lookup"><span data-stu-id="582b0-128">Note that coordinates are given in the relative coordinate space and that the real size is determined by the **width** and **height**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="582b0-129">[Пример атрибута path](/previous-versions/bb264089(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="582b0-129">[Path Attribute Example](/previous-versions/bb264089(v=vs.85)).</span></span> <span data-ttu-id="582b0-130">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="582b0-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 