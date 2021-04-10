---
title: Атрибут Строкеколор VML
description: Атрибут Строкеколор VML
ms.assetid: e7224d77-f788-43c7-aa8e-d5fc318f9d4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d379f41f3d2c1f03349beae8d0420a7c1a26429
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070164"
---
# <a name="vml-strokecolor-attribute"></a><span data-ttu-id="b0fb6-103">Атрибут Строкеколор VML</span><span class="sxs-lookup"><span data-stu-id="b0fb6-103">VML StrokeColor Attribute</span></span>

<span data-ttu-id="b0fb6-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b0fb6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b0fb6-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="b0fb6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b0fb6-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="b0fb6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b0fb6-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b0fb6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b0fb6-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b0fb6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b0fb6-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b0fb6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b0fb6-110">Определяет цвет кисти, которая обозначает контур фигуры.</span><span class="sxs-lookup"><span data-stu-id="b0fb6-110">Defines the brush color that strokes the path of a shape.</span></span> <span data-ttu-id="b0fb6-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="b0fb6-111">Read/write.</span></span> <span data-ttu-id="b0fb6-112">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="b0fb6-112">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span>

<span data-ttu-id="b0fb6-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="b0fb6-113">**Applies To**</span></span>

[<span data-ttu-id="b0fb6-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="b0fb6-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b0fb6-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="b0fb6-115">**Tag Syntax**</span></span>

<span data-ttu-id="b0fb6-116"><v: *element* строкеколор = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="b0fb6-116"><v: *element* strokecolor=" *expression* "></span></span>

<span data-ttu-id="b0fb6-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="b0fb6-117">**Script Syntax**</span></span>

<span data-ttu-id="b0fb6-118">*element* . строкеколор = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="b0fb6-118">*element* .strokecolor="*expression*"</span></span>

<span data-ttu-id="b0fb6-119">*выражение* = *element*. строкеколор</span><span class="sxs-lookup"><span data-stu-id="b0fb6-119">*expression*=*element*.strokecolor</span></span>

<span data-ttu-id="b0fb6-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="b0fb6-120">**Remarks**</span></span>

<span data-ttu-id="b0fb6-121">Значение дублируется из атрибута **Color** элемента [Stroke](msdn-online-vml-stroke-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b0fb6-121">The value is duplicated from the **Color** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="b0fb6-122">*Стандартный атрибут VML*</span><span class="sxs-lookup"><span data-stu-id="b0fb6-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="b0fb6-123">**Пример**</span><span class="sxs-lookup"><span data-stu-id="b0fb6-123">**Example**</span></span>

<span data-ttu-id="b0fb6-124">Цвет штриха прямоугольника — красный.</span><span class="sxs-lookup"><span data-stu-id="b0fb6-124">The color of the stroke of the rectangle is red.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="b0fb6-125">[Пример атрибута строкеколор](/previous-versions/bb264093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0fb6-125">[StrokeColor Attribute Example](/previous-versions/bb264093(v=vs.85)).</span></span> <span data-ttu-id="b0fb6-126">(Требуется Microsoft Internet Explorer 5 или более поздней версии.)</span><span class="sxs-lookup"><span data-stu-id="b0fb6-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 