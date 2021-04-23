---
title: Атрибут Врапкурдс VML
description: Атрибут Врапкурдс VML
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792121"
---
# <a name="vml-wrapcoords-attribute"></a><span data-ttu-id="3c85f-103">Атрибут Врапкурдс VML</span><span class="sxs-lookup"><span data-stu-id="3c85f-103">VML WrapCoords Attribute</span></span>

<span data-ttu-id="3c85f-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3c85f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3c85f-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="3c85f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3c85f-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="3c85f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3c85f-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3c85f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3c85f-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3c85f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3c85f-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3c85f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3c85f-110">Определяет ограничивающий многоугольник, который окружает фигуру.</span><span class="sxs-lookup"><span data-stu-id="3c85f-110">Defines the bounding polygon that surrounds a shape.</span></span> <span data-ttu-id="3c85f-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="3c85f-111">Read/write.</span></span> <span data-ttu-id="3c85f-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="3c85f-112">**String**.</span></span>

<span data-ttu-id="3c85f-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="3c85f-113">**Applies To**</span></span>

[<span data-ttu-id="3c85f-114">Фигурная</span><span class="sxs-lookup"><span data-stu-id="3c85f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3c85f-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="3c85f-115">**Tag Syntax**</span></span>

<span data-ttu-id="3c85f-116"><v: *element* о:врапкурдс = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="3c85f-116"><v: *element* o:wrapcoords=" *expression* "></span></span>

<span data-ttu-id="3c85f-117">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="3c85f-117">**Remarks**</span></span>

<span data-ttu-id="3c85f-118">Описывает разделенный запятыми список x и икурдинатес; то есть "x1, y1, x2, Y2, X3, Y3,..." Используется, когда текст тесно заключен вокруг фигуры.</span><span class="sxs-lookup"><span data-stu-id="3c85f-118">Describes a comma-delimited list of x and ycoordinates; that is, "x1,y1,x2,y2,x3,y3,..." This is used when text is tightly wrapped around a shape.</span></span> <span data-ttu-id="3c85f-119">Значение по умолчанию — **null** (пустая строка), пока атрибуту **MSO-Wrap-Mode** не будет присвоено значение « **плотная** » или « **с**».</span><span class="sxs-lookup"><span data-stu-id="3c85f-119">The default is **NULL** (an empty string) until the **MSO-Wrap-Mode** attribute is set to **tight** or **through**.</span></span>

<span data-ttu-id="3c85f-120">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="3c85f-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="3c85f-121">**Пример**</span><span class="sxs-lookup"><span data-stu-id="3c85f-121">**Example**</span></span>

<span data-ttu-id="3c85f-122">Фигура имеет ограничивающий прямоугольник с обтеканием текста 5 единиц, превышающий путь.</span><span class="sxs-lookup"><span data-stu-id="3c85f-122">The shape has a text wrap bounding box that is 5 units larger than the path.</span></span>


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 