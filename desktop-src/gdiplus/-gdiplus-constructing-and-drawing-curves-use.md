---
description: 'GDI+ поддерживает несколько типов кривых: эллипсы, дуги, фундаментальные сплайны и B&\# 233; кривые Безье.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Построение и рисование кривых
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997522"
---
# <a name="constructing-and-drawing-curves"></a><span data-ttu-id="40b54-103">Построение и рисование кривых</span><span class="sxs-lookup"><span data-stu-id="40b54-103">Constructing and Drawing Curves</span></span>

<span data-ttu-id="40b54-104">GDI+ поддерживает несколько типов кривых: эллипсы, дуги, фундаментальные сплайны и Сплайны Безье.</span><span class="sxs-lookup"><span data-stu-id="40b54-104">GDI+ supports several types of curves: ellipses, arcs, cardinal splines, and Bézier splines.</span></span> <span data-ttu-id="40b54-105">Эллипс определяется его ограничивающим прямоугольником; дуга — это часть эллипса, определяемая начальным углом и углом поворота.</span><span class="sxs-lookup"><span data-stu-id="40b54-105">An ellipse is defined by its bounding rectangle; an arc is a portion of an ellipse defined by a starting angle and a sweep angle.</span></span> <span data-ttu-id="40b54-106">Фундаментальный сплайн определяется массивом точек и параметром натяжения — кривая плавно проходит через каждую точку в массиве, а параметр натяжения влияет на изгиб кривой.</span><span class="sxs-lookup"><span data-stu-id="40b54-106">A cardinal spline is defined by an array of points and a tension parameter — the curve passes smoothly through each point in the array, and the tension parameter influences the way the curve bends.</span></span> <span data-ttu-id="40b54-107">Сплайн Безье определяется двумя конечными точками и двумя контрольными точками — кривая не проходит через контрольные точки, но контрольные точки влияют на направление и изгиб при переходе кривой с одной конечной точки на другую.</span><span class="sxs-lookup"><span data-stu-id="40b54-107">A Bézier spline is defined by two end points and two control points — the curve does not pass through the control points, but the control points influence the direction and bend as the curve goes from one end point to the other.</span></span>

<span data-ttu-id="40b54-108">В следующих разделах подробно рассматриваются фундаментальные сплайны и Сплайны Безье.</span><span class="sxs-lookup"><span data-stu-id="40b54-108">The following topics cover cardinal splines and Bézier splines in more detail:</span></span>

-   [<span data-ttu-id="40b54-109">Рисование фундаментальных сплайнов</span><span class="sxs-lookup"><span data-stu-id="40b54-109">Drawing Cardinal Splines</span></span>](-gdiplus-drawing-cardinal-splines-use.md)
-   [<span data-ttu-id="40b54-110">Рисование сплайнов Безье</span><span class="sxs-lookup"><span data-stu-id="40b54-110">Drawing Bézier Splines</span></span>](-gdiplus-drawing-bezier-splines-use.md)

 

 



