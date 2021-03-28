---
description: Чтобы создать путь и выбрать его в контроллере домена, сначала необходимо определить точки, которые его описывают.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Создание пути
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263663"
---
# <a name="path-creation"></a><span data-ttu-id="ad4da-103">Создание пути</span><span class="sxs-lookup"><span data-stu-id="ad4da-103">Path Creation</span></span>

<span data-ttu-id="ad4da-104">Чтобы создать путь и выбрать его в контроллере домена, сначала необходимо определить точки, которые его описывают.</span><span class="sxs-lookup"><span data-stu-id="ad4da-104">To create a path and select it into a DC, it is first necessary to define the points that describe it.</span></span> <span data-ttu-id="ad4da-105">Это делается путем вызова функции [**бегинпас**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) , указания соответствующих функций рисования, а затем путем вызова функции [**ендпас**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) .</span><span class="sxs-lookup"><span data-stu-id="ad4da-105">This is done by calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function, specifying the appropriate drawing functions, and then by calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="ad4da-106">Это сочетание функций (**бегинпас**, Drawing functions и **ендпас**) образует *квадратную скобку пути*.</span><span class="sxs-lookup"><span data-stu-id="ad4da-106">This combination of functions (**BeginPath**, drawing functions, and **EndPath**) constitute a *path bracket*.</span></span> <span data-ttu-id="ad4da-107">Ниже приведен список функций рисования, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="ad4da-107">The following is the list of drawing functions that can be used.</span></span>

-   [<span data-ttu-id="ad4da-108">**англеарк**</span><span class="sxs-lookup"><span data-stu-id="ad4da-108">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [<span data-ttu-id="ad4da-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="ad4da-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [<span data-ttu-id="ad4da-110">**аркто**</span><span class="sxs-lookup"><span data-stu-id="ad4da-110">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [<span data-ttu-id="ad4da-111">**Хордовая диаграмма**</span><span class="sxs-lookup"><span data-stu-id="ad4da-111">**Chord**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [<span data-ttu-id="ad4da-112">**клосефигуре**</span><span class="sxs-lookup"><span data-stu-id="ad4da-112">**CloseFigure**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [<span data-ttu-id="ad4da-113">**Эллипс**</span><span class="sxs-lookup"><span data-stu-id="ad4da-113">**Ellipse**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [<span data-ttu-id="ad4da-114">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="ad4da-114">**ExtTextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [<span data-ttu-id="ad4da-115">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="ad4da-115">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [<span data-ttu-id="ad4da-116">**моветоекс**</span><span class="sxs-lookup"><span data-stu-id="ad4da-116">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [<span data-ttu-id="ad4da-117">**Круговая**</span><span class="sxs-lookup"><span data-stu-id="ad4da-117">**Pie**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [<span data-ttu-id="ad4da-118">**PolyBezierSegment**</span><span class="sxs-lookup"><span data-stu-id="ad4da-118">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [<span data-ttu-id="ad4da-119">**полибезиерто**</span><span class="sxs-lookup"><span data-stu-id="ad4da-119">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [<span data-ttu-id="ad4da-120">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="ad4da-120">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [<span data-ttu-id="ad4da-121">**Многоугольник**</span><span class="sxs-lookup"><span data-stu-id="ad4da-121">**Polygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [<span data-ttu-id="ad4da-122">**Линию**</span><span class="sxs-lookup"><span data-stu-id="ad4da-122">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [<span data-ttu-id="ad4da-123">**Для в. lineTo**</span><span class="sxs-lookup"><span data-stu-id="ad4da-123">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [<span data-ttu-id="ad4da-124">**Многоугольник**</span><span class="sxs-lookup"><span data-stu-id="ad4da-124">**PolyPolygon**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [<span data-ttu-id="ad4da-125">**Ломаная линия**</span><span class="sxs-lookup"><span data-stu-id="ad4da-125">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [<span data-ttu-id="ad4da-126">**Углами**</span><span class="sxs-lookup"><span data-stu-id="ad4da-126">**Rectangle**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [<span data-ttu-id="ad4da-127">**раундрект**</span><span class="sxs-lookup"><span data-stu-id="ad4da-127">**RoundRect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [<span data-ttu-id="ad4da-128">**TextOut**</span><span class="sxs-lookup"><span data-stu-id="ad4da-128">**TextOut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

<span data-ttu-id="ad4da-129">Когда приложение вызывает [**ендпас**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), система выбирает связанный путь в УКАЗАНном контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="ad4da-129">When an application calls [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), the system selects the associated path into the specified DC.</span></span> <span data-ttu-id="ad4da-130">(Если в контроллере домена ранее был выбран другой путь, система удалит этот путь без сохранения.) После того как система выберет путь к контроллеру домена, приложение может использовать путь одним из следующих способов.</span><span class="sxs-lookup"><span data-stu-id="ad4da-130">(If another path had previously been selected into the DC, the system deletes that path without saving it.) After the system selects the path into the DC, an application can operate on the path in one of the following ways:</span></span>

-   <span data-ttu-id="ad4da-131">Рисование контура контура (с помощью текущего пера).</span><span class="sxs-lookup"><span data-stu-id="ad4da-131">Draw the outline of the path (using the current pen).</span></span>
-   <span data-ttu-id="ad4da-132">Заполните внутреннюю часть контура (используя текущую кисть).</span><span class="sxs-lookup"><span data-stu-id="ad4da-132">Paint the interior of the path (using the current brush).</span></span>
-   <span data-ttu-id="ad4da-133">Нарисуйте контур и заливку внутренней части контура.</span><span class="sxs-lookup"><span data-stu-id="ad4da-133">Draw the outline and fill the interior of the path.</span></span>
-   <span data-ttu-id="ad4da-134">Измените путь (преобразуя кривые в сегменты линии).</span><span class="sxs-lookup"><span data-stu-id="ad4da-134">Modify the path (converting curves to line segments).</span></span>
-   <span data-ttu-id="ad4da-135">Преобразуйте путь в путь обрезки.</span><span class="sxs-lookup"><span data-stu-id="ad4da-135">Convert the path into a clip path.</span></span>
-   <span data-ttu-id="ad4da-136">Преобразуйте путь в регион.</span><span class="sxs-lookup"><span data-stu-id="ad4da-136">Convert the path into a region.</span></span>
-   <span data-ttu-id="ad4da-137">Сведение пути путем преобразования каждой кривой в контуре в ряд сегментов линии.</span><span class="sxs-lookup"><span data-stu-id="ad4da-137">Flatten the path by converting each curve in the path into a series of line segments.</span></span>
-   <span data-ttu-id="ad4da-138">Получение координат линий и кривых, образующих контур.</span><span class="sxs-lookup"><span data-stu-id="ad4da-138">Retrieve the coordinates of the lines and curves that compose a path.</span></span>

 

 



